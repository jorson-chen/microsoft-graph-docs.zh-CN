---
author: JeremyKelley
description: 表示用于将大型文件上载到 OneDrive、OneDrive for Business 或 SharePoint 文档库，或作为 Outlook 事件和邮件对象的文件附件的迭代过程的信息。
title: uploadSession 资源类型
localization_priority: Normal
doc_type: resourcePageType
ms.prod: non-product-specific
ms.openlocfilehash: 64c907559337a1e6c5f40e046726c747751aaf03
ms.sourcegitcommit: 3b9eb50b790d952c7f350433ef7531d5e6d4b963
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/22/2020
ms.locfileid: "48723719"
---
# <a name="uploadsession-resource-type"></a>uploadSession 资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

表示用于将大文件上载到的迭代过程的信息：

- OneDrive
- OneDrive for Business
- SharePoint 文档库
- Outlook [事件](event.md) 和 [邮件](message.md) 项目作为附件
- 通用打印 [printDocument](printdocument.md) 项目

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "uploadUrl", "nextExpectedRanges" ],
  "@odata.type": "microsoft.graph.uploadSession",
  "baseType": null
}-->

```json
{
  "uploadUrl": "String",
  "expirationDateTime": "String (timestamp)",
  "nextExpectedRanges": ["String"]
}
```

## <a name="properties"></a>属性


| 属性       | 类型              |说明
|:-------------------|:------------------|:------------------------------------
| expirationDateTime | DateTimeOffset    | 以 UTC 表示的上载会话过期的日期和时间。在此过期时间之前必须上载完整的文件文件。
| nextExpectedRanges | String collection | 将文件上载到文档库时，这是文件的服务器缺少的字节范围的集合。 这些区域的索引为零，格式为 "{start}-{end}" (例如，"0-26" 表示文件) 的前27个字节。 将文件作为 Outlook 附件（而不是区域集合）上载时，此属性始终指示单个值 "{start}"，即文件中应开始下一次上载的位置。
| uploadUrl          | String            | 接受文件字节范围的 PUT 请求的 URL 端点。

## <a name="see-also"></a>另请参阅

- [将大型文件作为附件附加到 Outlook 邮件和事件 ](/graph/outlook-large-attachments)
- [通过上传会话上传大文件](../api/driveitem-createuploadsession.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "UploadSession is used to provide information about large file uploads.",
  "section": "documentation",
  "tocPath": "Resources/UploadSession",
  "suppressions": []
}
-->


