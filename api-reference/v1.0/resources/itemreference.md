---
author: JeremyKelley
ms.date: 09/10/2017
title: ItemReference
localization_priority: Normal
description: ItemReference 资源提供通过 API 寻址 DriveItem 所需的必要信息。
ms.prod: sharepoint
doc_type: resourcePageType
ms.openlocfilehash: dd24f0d1fc0a5f5db576f5eea89b8205ff55b2b7
ms.sourcegitcommit: 0d4377b0153bc339ab7b3b1a6ee4d52848b622d4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/18/2020
ms.locfileid: "49714254"
---
# <a name="itemreference-resource-type"></a>ItemReference 资源类型

命名空间：microsoft.graph

**ItemReference** 资源提供了通过 API 查找 [DriveItem](driveitem.md) 的必要信息。

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "path", "shareId", "sharepointIds" ],
  "@odata.type": "microsoft.graph.itemReference"
}-->

```json
{
  "driveId": "string",
  "driveType": "personal | business | documentLibrary",
  "id": "string",
  "name": "string",
  "path": "string",
  "shareId": "string",
  "sharepointIds": { "@odata.type": "microsoft.graph.sharepointIds" },
  "siteId": "string"
}
```

## <a name="properties"></a>属性

| 属性      | 类型              | 说明
|:--------------|:------------------|:-----------------------------------------
| driveId       | String            | 包含项的驱动器实例的唯一标识符。只读。
| driveType     | String            | 标识驱动器的类型。 请参阅 [drive][] 资源查看其值。
| id            | String            | 项在驱动器中的唯一标识符。只读。
| name          | String            | 所引用的项的名称。只读。
| 路径          | String            | 可用于导航到该项的路径。只读。
| shareId       | String            | 可通过 [Shares][] API 访问的共享资源的唯一标识符。
| sharepointIds | [sharepointIds][] | 返回对 SharePoint REST 兼容性有用的标识符。只读。
| siteId        | String            | 对于 OneDrive for Business 和 SharePoint，此属性表示包含 driveItem 资源的父文档库的网站的 ID。 该值与该网站资源的 ID [属性][] 相同。 它是一 [个不透明的字符串，由网站的三个](/graph/api/resources/site#id-property) 标识符组成。 <br>对于 OneDrive，不填充此属性。

[drive]: ../resources/drive.md
[sharepointIds]: ../resources/sharepointids.md
[Shares]: ../api/shares-get.md
[网站]: ../resources/site.md

## <a name="remarks"></a>注解

为了从 **itemReference** 资源中找到 **driveItem**，请构建以下格式的 URL：

```http
GET https://graph.microsoft.com/v1.0/drives/{driveId}/items/{id}
```

**path** 值是相对于目标驱动器的 API 路径，例如：`/drive/root:/Documents/myfile.docx`。

要检索人工可读路径中的痕迹，可以放心地忽略路径字符串中的第一个 `:` 之前的所有内容。

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ItemReference returns a pointer to another item.",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/itemreference.md:
      Found potential enums in resource example that weren't defined in a table:(personal,business,documentLibrary) are in resource, but () are in table"
  ],
  "tocPath": "Resources/ItemReference"
} -->

