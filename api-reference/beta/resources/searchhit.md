---
title: searchHit 资源类型
description: 在此处提供说明
localization_priority: Normal
author: nmoreau
ms.prod: search
doc_type: resourcePageType
ms.openlocfilehash: 2ce5671933589f6066698df3e082390207474b49
ms.sourcegitcommit: 62507617292d5ad8598e83a8a253c986d9bac787
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/02/2019
ms.locfileid: "37939864"
---
# <a name="searchhit-resource-type"></a>searchHit 资源类型

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

表示搜索结果列表中的单个结果。

## <a name="properties"></a>属性

| 属性     | 类型        | 描述 |
|:-------------|:------------|:------------|
|_id|字符串|项的内部标识符。|
|_score|Int32|结果的分数或顺序。|
|_sortField|字符串|使用的排序顺序。 它可以是 DateTime 或相关性。|
|_summary|字符串|结果的摘要（如果摘要可用）。|
|_source|[实体](entity.md)|搜索结果的基础图形表示形式。|

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.searchHit",
  "baseType": null
}-->

```json
{
  "_id": "String",
  "_score": 1024,
  "_sortField": "String",
  "_summary": "String",
  "_source": { "@odata.type": "microsoft.graph.entity" }
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "searchHit resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->