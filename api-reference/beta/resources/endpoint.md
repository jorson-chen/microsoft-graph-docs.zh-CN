---
title: 终结点资源类型
description: 终结点表示与实体关联的资源的 URL。
localization_priority: Normal
doc_type: resourcePageType
ms.prod: ''
author: yyuank
ms.openlocfilehash: 47bef2bfa14fb8a00fd1ca2356d7f880ff3207d6
ms.sourcegitcommit: 6ec748ef00d025ee216274a608291be3c1257777
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/27/2021
ms.locfileid: "50013595"
---
# <a name="endpoint-resource-type"></a>终结点资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

终结点表示与实体关联的资源的 URL。  例如，当创建一个新的 Microsoft 365 组时，其他资源也会作为 Microsoft 365 组的一部分创建。 其中包括用于对话的组邮箱和文档和文件的组 OneDrive 文件夹等内容。 现在，可以使用组资源类型的终结点导航来阅读有关这些 Microsoft 365 组资源（包括其关联的资源 URL）的更多信息。 这允许应用程序了解这些资源，甚至可以在其自己的体验中嵌入资源 URL 体验。

## <a name="methods"></a>方法

| 方法           | 返回类型    |说明|
|:---------------|:--------|:----------|
|[List endpoints](../api/group-list-endpoints.md) |[Endpoint](endpoint.md) 集合| 获取 endpoint 对象集合。 |
|[Get endpoint](../api/endpoint-get.md) | [终结点](endpoint.md) |读取 endpoint 对象的属性和关系。|

## <a name="properties"></a>属性
| 属性     | 类型   |说明|
|:---------------|:--------|:----------|
| 功能     | String  | 描述与此资源关联的功能。  (例如消息、对话等) 不可为空。 只读。 |
| id             | String  | 终结点的唯一标识符;键。 不可为 null。 只读。|
| providerId     | String  | 发布基础服务的应用程序 ID。 不可为 null。 只读。|
| providerName   | String  | 发布基础服务的名称。 只读。|
| providerResourceId|String| 对于 Microsoft 365 组，这设置为资源资源的已知名称 (例如 Yammer.FeedURL 等) 。 不可为 null。 只读。|
| uri            | String  | 已发布资源的 URL。 不可为 null。 只读。|

## <a name="relationships"></a>关系

无。


## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.endpoint"
}-->

```json
{
  "capability": "String",
  "id": "String (identifier)",
  "providerId": "String",
  "providerName": "String",
  "providerResourceId": "String",
  "uri": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Endpoint resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


