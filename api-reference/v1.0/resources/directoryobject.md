---
title: directoryObject 资源类型
description: 表示 Azure Active Directory 对象。**directoryObject** 类型是其他许多目录实体类型的基类型。
localization_priority: Priority
author: keylimesoda
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 3fafb936712c1416a228b281c5eb8a760db49f82
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48091787"
---
# <a name="directoryobject-resource-type"></a>directoryObject 资源类型

命名空间：microsoft.graph

表示 Azure Active Directory 对象。**directoryObject** 类型是其他许多目录实体类型的基类型。

## <a name="methods"></a>方法

| 方法       | 返回类型  |说明|
|:---------------|:--------|:----------|
|[获取 directoryObject](../api/directoryobject-get.md) | [directoryObject](directoryobject.md) |读取 directory 对象的属性。|
|[删除 directoryObject](../api/directoryobject-delete.md) | 无 |删除 directory 对象。 |
|[checkMemberGroups](../api/directoryobject-checkmembergroups.md)|String collection|检查组列表中的成员身份。检查是可传递的。|
|[获取可用扩展属性](../api/directoryobject-getavailableextensionproperties.md)|[extensionProperty](../resources/extensionproperty.md) 集合|获取已在目录中注册的目录扩展属性的所有或筛选列表。|
|[getMemberGroups](../api/directoryobject-getmembergroups.md)|String collection|返回 user、group 或 directory 对象所属的所有组。检查是可传递的。|
|[getMemberObjects](../api/directoryobject-getmemberobjects.md)|String collection| 返回 user、group 或 directory 对象所属的所有组和目录角色。检查是可传递的。 |
|[getByIds](../api/directoryobject-getbyids.md) | [directoryObject](directoryobject.md) 集合 | 基于提供的 ID 集获取目录对象集。 |
|[validateProperties](../api/directoryobject-validateproperties.md)|Json| 验证 Microsoft 365 组的显示名称或邮件昵称是否符合命名策略。 |

## <a name="properties"></a>属性

| 属性   | 类型 |说明|
|:---------------|:--------|:----------|
|id|String|对象的全局唯一标识符。 例如，12345678-9abc-def0-1234-56789abcde。 **id** 属性的值通常（但不总是）用 GUID 表示；将它视为不透明标识符，不要总将它视为 GUID。 键。 不可为 null。 只读。|

## <a name="relationships"></a>关系

无


## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!--{
  "blockType": "resource",
  "openType": true,
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.directoryObject",
  "@odata.annotations": [
    {
      "capabilities": {
        "skippable": false,
        "countable": false,
        "expandable": false,
        "filterable": false,
        "referenceable": false,
        "selectable": false
      }
    }
  ]
}-->

```json
{
  "id": "string (identifier)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryObject resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

