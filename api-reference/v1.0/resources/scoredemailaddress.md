---
title: scoredEmailAddress 资源类型
description: 表示经过评分的电子邮件地址。
localization_priority: Normal
author: AAmatino
ms.prod: ''
doc_type: resourcePageType
ms.openlocfilehash: 11efd8331cf8fca844b912703fa927b627624611
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "47984136"
---
# <a name="scoredemailaddress-resource-type"></a>scoredEmailAddress 资源类型

命名空间：microsoft.graph

表示经过评分的电子邮件地址。


## <a name="properties"></a>属性
| 属性     | 类型   |说明|
|:---------------|:--------|:----------|
|address|string|电子邮件地址。|
|relevanceScore|double|电子邮件地址的相关性评分。相关性评分用作排序关键字，与其他返回的结果相关。相关性评分值越高，对应结果的相关性越高。相关性由用户的通信和协作模式及业务关系决定。 |

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.scoredEmailAddress"
}-->

```json
{
  "address": "string",
  "relevanceScore": 1024.0
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "scoredEmailAddress resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

