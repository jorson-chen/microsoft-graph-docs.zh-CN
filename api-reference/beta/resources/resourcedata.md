---
title: resourceData 资源类型
description: 表示附加到发送到订阅服务器的更改通知的资源数据。
localization_priority: Normal
author: davidmu1
doc_type: resourcePageType
ms.prod: non-product-specific
ms.openlocfilehash: 94af6ae2c8ed1cfa9ec9c66502d48b5eabcb482f
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48087633"
---
# <a name="resourcedata-resource-type"></a>resourceData 资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

表示附加到发送到订阅服务器的更改通知的资源数据。

有关详细信息，请参阅 [使用 Microsoft GRAPH API 获取更改通知](webhooks.md)。

## <a name="methods"></a>方法

无。

## <a name="properties"></a>属性

对于 Outlook 资源， **resourceData** 包含以下字段：

| 属性 | 类型 | 说明 |
|:---------|:-----|:------------|
| @odata.type | string | Microsoft Graph 中描述所表示对象的 OData 实体类型。 |
| @odata.id | string | 对象的 OData 标识符。 |
| @odata.etag | string | 表示对象版本的 HTTP 实体标记。 |
| id | string | 对象的标识符。 |

> **注意：**`id` **ResourceData**中提供的值在生成更改通知时有效。 某些操作（如将邮件移动到另一个文件夹）可能会导致在 `id` 处理更改通知时不再有效。

## <a name="relationships"></a>关系

无。

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.resourceData"
}-->

```json
{
  "id": "1565293727947",
  "@odata.type": "#Microsoft.Graph.ChatMessage",
  "@odata.id": "teams('88cbc8fc-164b-44f0-b6a6-b59b4a1559d3')/channels('19:8d9da062ec7647d4bb1976126e788b47@thread.tacv2')/messages('1565293727947')/replies('1565293727947')"
}
```

<!-- uuid: eb6c98ec-8257-4826-910e-5c603265257f
2020-05-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "change notification resource data resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


