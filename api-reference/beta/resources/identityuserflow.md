---
title: UserFlow 资源类型
description: 标识用户流是内置身份验证旅程
localization_priority: Normal
author: Nickgmicrosoft
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 0d76d7a2ab3516717d01f0371b84531e211181fd
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48016631"
---
# <a name="userflow-resource-type"></a>UserFlow 资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

用户流使您能够定义预定义的可配置策略，用于登录、注册、组合注册和登录、密码重置和配置文件更新。

## <a name="methods"></a>方法

| 方法       | 返回类型 | Description |
|:-------------|:------------|:------------|
| [List](../api/identityuserflow-list.md) | [UserFlow](identityuserflow.md) 集合 | 列出 UserFlows。 |
| [创建](../api/identityuserflow-post-userflows.md) | [UserFlow](identityuserflow.md) | 创建 UserFlow 对象。 |
| [获取](../api/identityuserflow-get.md) | [UserFlow](identityuserflow.md) | 读取 UserFlow 对象的属性和关系。 |
| [删除](../api/identityuserflow-delete.md) | 无 | 删除 UserFlow 对象。 |

## <a name="properties"></a>属性

| 属性     | 类型        | 说明 |
|:-------------|:------------|:------------|
|id|String| 只读。|
|userFlowType|string| 可取值为：`signUp`、`signIn`、`signUpOrSignIn`、`passwordReset`、`profileUpdate`、`resourceOwner` 或 `unknownFutureValue`。|
|userFlowTypeVersion|单一| 这是用户流类型的版本。 每个用户流类型都可以有不同的可能版本，如1、1.1 或2。  |

## <a name="relationships"></a>关系

无

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.UserFlow",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "id": "String (identifier)",
  "userFlowType": "string",
  "userFlowTypeVersion": "Single"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "UserFlow resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


