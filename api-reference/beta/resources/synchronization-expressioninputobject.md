---
title: expressionInputObject 资源类型
description: 表示在 synchronizationSchema parseExpression 操作执行表达式评估时用作输入测试数据的对象。
localization_priority: Normal
doc_type: resourcePageType
author: ArvindHarinder1
ms.prod: microsoft-identity-platform
ms.openlocfilehash: e9727f50b05eb8cdb5319883dd0058a91d9383cc
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "47968351"
---
# <a name="expressioninputobject-resource-type"></a>expressionInputObject 资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

表示在 [parseExpression](../api/synchronization-synchronizationschema-parseexpression.md) 操作执行表达式评估时用作输入测试数据的对象。

## <a name="properties"></a>属性
| 属性     | 类型   |说明|
|:---------------|:--------|:----------|
|定义|[objectDefinition](synchronization-objectdefinition.md)|Test 对象的定义。|
|properties|[stringKeyObjectValuePair](synchronization-stringkeyobjectvaluepair.md) 集合|Test 对象的属性值。|

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.expressionInputObject"
}-->

```json
{
  "definition": {"@odata.type": "microsoft.graph.objectDefinition"},
  "properties": [{"@odata.type": "microsoft.graph.stringKeyObjectValuePair"}]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "expressionInputObject resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


