---
title: governanceRuleSetting 资源类型
description: 表示角色设置所组成的规则。
localization_priority: Normal
doc_type: resourcePageType
ms.prod: ''
author: shauliu
ms.openlocfilehash: b2a4b70eb7d8af5dde6e3741c3473683ca7e0586
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48081634"
---
# <a name="governancerulesetting-resource-type"></a>governanceRuleSetting 资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

表示角色设置所组成的规则。


## <a name="properties"></a>属性
|属性      | 类型         |说明|
|:-------------|:-------------|:----------|
|ruleIdentifier|字符串        |规则的 id。 例如 ``ExpirationRule`` 和 ``MfaRule`` 。|
|setting       |String        |规则的设置。 此值是一个 JSON 字符串，其格式为 Parameter_Name： Parameter_Value 的一对列表。 例如，`{"permanentAssignment":false,"maximumGrantPeriodInMinutes":129600}`|

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.governanceRuleSetting"
}-->


```json
{
  "ruleIdentifier": "String",
  "setting": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "governanceRuleSetting",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


