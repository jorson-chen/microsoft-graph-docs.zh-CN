---
title: userCredentialUsageDetails 资源类型
description: 表示给定租户的自助服务密码重置用法。
localization_priority: Normal
author: besiler
ms.prod: reports
doc_type: resourcePageType
ms.openlocfilehash: 6ac0e1b8b73b019636e460772975da7a4f0505a1
ms.sourcegitcommit: 9f88b7e41a4a4a4d5f52bd995ce07c6f702bd5d6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/01/2020
ms.locfileid: "49524237"
---
# <a name="usercredentialusagedetails-resource-type"></a>userCredentialUsageDetails 资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

表示给定租户的自助服务密码重置用法。 详细信息包括用户信息、重置状态和失败原因。

## <a name="methods"></a>方法

| 方法       | 返回类型 | 说明 |
|:-------------|:------------|:------------|
| [列出 userCredentialUsageDetails](../api/reportroot-list-usercredentialusagedetails.md) | userCredentialUsageDetails | 读取 userCredentialUsageDetails 对象的属性和关系。 |

## <a name="properties"></a>属性

| 属性     | 类型        | 说明 |
|:-------------|:------------|:------------|
| authMethod | string | 表示用户使用的身份验证方法。 可能的值为： `email` 、、、、 `mobileSMS` `mobileCall` `officePhone` `securityQuestion` (仅用于自助密码重置) 、、 `appNotification` `appCode` 和 `alternateMobileCall` (仅在注册) 中受支持。 |
| eventDateTime | DateTimeOffset | 时间戳类型表示采用 ISO 8601 格式的日期和时间信息，始终采用 UTC 时区。 例如，2014 年 1 月 1 日午夜 UTC 如下所示：`'2014-01-01T00:00:00Z'`。 |
| failureReason | String | 提供相应重置或注册工作流的失败原因。 |
| 功能 | string | 可能的值为： `registration` 和 `reset` 。 |
| id | String | 只读。 活动的唯一标识符。 只读。|
| isSuccess | 布尔值 | 指示工作流是成功还是失败。 |
| userDisplayName | String | 执行重置或注册工作流的用户的用户名。 |
| userPrincipalName | String | 执行重置或注册工作流的用户的用户主体名称。 |

## <a name="relationships"></a>关系

无。

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.userCredentialUsageDetails",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "id" : "String",
  "feature":"string",
  "userPrincipalName":"String",
  "userDisplayName": "String",
  "isSuccess" : true,
  "authMethod": "string",
  "failureReason": "String",
  "eventDateTime" : "DateTimeOffset"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "userCredentialUsageDetails resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

