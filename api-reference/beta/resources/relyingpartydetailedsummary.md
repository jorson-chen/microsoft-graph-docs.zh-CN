---
title: relyingPartyDetailedSummary 资源类型
description: 表示 AD FS 中的信赖方。
localization_priority: Normal
author: besiler
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: a3a6fd0ad84ce8e41902cd7c0e82a314fb1aa3ca
ms.sourcegitcommit: 9f88b7e41a4a4a4d5f52bd995ce07c6f702bd5d6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/01/2020
ms.locfileid: "49524713"
---
# <a name="relyingpartydetailedsummary-resource-type"></a>relyingPartyDetailedSummary 资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

表示配置了 Active Directory 联合身份验证服务 (AD FS) 的信赖方、其聚合的使用情况，以及是否可以将信赖方配置迁移到 Azure Active Directory。

## <a name="methods"></a>方法

| 方法       | 返回类型 | Description |
|:-------------|:------------|:------------|
| [List](../api/relyingpartydetailedsummary-list.md) | [relyingPartyDetailedSummary](relyingpartydetailedsummary.md) | 检索 **relyingPartyDetailedSummary** 对象的列表。 |


## <a name="properties"></a>属性

| 属性     | 类型        | 说明 |
|:-------------|:------------|:------------|
|id|String| 只读。 在 API 级别生成的唯一标识符。| 
|relyingPartyId|String|此标识符用于将信赖方标识为此联合身份验证服务。 向信赖方颁发声明时使用它。|
|服务 Id|String|唯一标识 Active Directory 林。|
|migrationStatus|string| 指示是否可以将应用程序移动到 Azure AD 或需要更多调查。 可取值为：`ready`、`needsReview`、`additionalStepsRequired`。|
|migrationValidationDetails|[keyValuePair](keyvaluepair.md) 集合|指定对应用程序配置详细信息进行的所有验证检查，以评估应用程序是否已准备好迁移到 Azure AD。 可能的名称为：、、、、、、、、、、、、、、、 `AdditionalWSFedEndpointCheckResult`  `AllowedAuthenticationClassReferencesCheckResult` `AlwaysRequireAuthenticationCheckResult`   `AutoUpdateEnabledCheckResult` `ClaimsProviderNameCheckResult` `EncryptClaimsCheckResult`  `EncryptedNameIdRequiredCheckResult` `MonitoringEnabledCheckResult` `NotBeforeSkewCheckResult`  `RequestMFAFromClaimsProvidersCheckResult` `SignedSamlRequestsRequiredCheckResult` `AdditionalAuthenticationRulesCheckResult` `TokenLifetimeCheckResult`  `DelegationAuthorizationRulesCheckResult` `IssuanceAuthorizationRulesCheckResult` `IssuanceTransformRulesCheckResult` 。 可能的结果值为 `0` 、 `1` 或 `2` 。 `0` 验证检查通过后，验证检查 `1` 失败，并且在 `2` 验证检查为警告时。 |
|relyingPartyName|String|Internet 上的应用程序或其他实体的名称，该实体使用标识提供程序对要登录的用户进行身份验证。|
|failedSignInCount|Int64| 在指定时间段内，在 Active Directory 联合身份验证服务上登录失败的次数。 |
|replyUrls|String 集合|指定信赖方预期接收令牌的位置。|
|signInSuccessRate|双精度|在指定时间段内，Active Directory 联合身份验证服务上) 成功/ (登录失败次数的次数。|
|successfulSignInCount|Int64|在 Active Directory 联合身份验证服务上成功登录的次数。|
|totalSignInCount|Int64|在指定时间段内，在 Active Directory 联合身份验证服务上成功的 + 失败登录登录失败的次数。|
|uniqueUserCount|Int64|已登录到应用程序的唯一用户数。|

## <a name="relationships"></a>关系

无。

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.relyingPartyDetailedSummary",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "failedSignInCount": 10,
  "id": "String (identifier)",
  "migrationStatus": "ready | needsReview | additionalStepsRequired",
  "migrationValidationDetails": [{"@odata.type": "microsoft.graph.keyValuePair"}],
  "relyingPartyId": "String",
  "relyingPartyName": "String",
  "replyUrls": ["String"],
  "serviceId": "String (identifier)",
  "signInSuccessRate": 90.0,
  "successfulSignInCount": 90,
  "totalSignInCount": 100,
  "uniqueUserCount": 10
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "relyingPartyDetailedSummary resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


