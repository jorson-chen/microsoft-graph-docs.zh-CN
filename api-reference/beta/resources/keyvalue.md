---
title: 键值资源类型
description: 提供有关登录请求的其他相关信息
localization_priority: Normal
author: besiler
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 78dd4f6ede6e918bb1caaae3761ef258b4e0a427
ms.sourcegitcommit: 9f88b7e41a4a4a4d5f52bd995ce07c6f702bd5d6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/01/2020
ms.locfileid: "49524699"
---
# <a name="keyvalue-resource-type"></a>键值资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

提供其他身份验证处理信息，如服务器名称和登录和域的提示的存在。

## <a name="properties"></a>属性

| 属性     | 类型        | 说明 |
|:-------------|:------------|:------------|
|Key|String|包含与值相关联的字段的名称。 当登录请求中包含登录或域提示时，相应的字段作为键值对包含。 可能的键： `Login hint present` 、 `Domain hint present` 。|
|value|String|包含指定键的相应值。 `true`如果登录请求中包含登录提示，则值为; 否则为 false `false` 。 值是在 `true` 登录请求中包含域提示; 否则，值为 `false` 。|

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.keyValue",
  "baseType": null
}-->

```json
{
  "key": "String",
  "value": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "keyValue resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


