---
title: stringKeyObjectValuePair 资源类型
description: 表示键值对，其中键是字符串，值是任意的 JSON 对象。 这是一种 OData 开放类型，它应具有一个名为 `value` 的属性，它是一个有效的 JSON 对象。
localization_priority: Normal
doc_type: resourcePageType
author: ArvindHarinder1
ms.prod: microsoft-identity-platform
ms.openlocfilehash: d2b7c32a0048e3aafa3c0c56ff91f1ae51542914
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48026150"
---
# <a name="stringkeyobjectvaluepair-resource-type"></a>stringKeyObjectValuePair 资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

表示键值对，其中键是字符串，值是任意的 JSON 对象。 这是一种 OData 开放类型，它应具有一个名为 `value` 的属性，它是一个有效的 JSON 对象。

## <a name="properties"></a>属性
| 属性     | 类型   |说明|
|:---------------|:--------|:----------|
|Key|String|键。|
|值|Json|任意 JSON 对象。|

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.stringKeyObjectValuePair"
}-->

```json
{
  "key": "String",
  "value": {
    "@odata.type": "microsoft.graph.Json"
  }
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "stringKeyObjectValuePair resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


