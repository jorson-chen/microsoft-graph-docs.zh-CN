---
title: anonymousIpRiskEvent 资源类型
description: Azure Active Directory 标识保护检测到的一个风险事件，其中的帐户登录尝试来自看似匿名的 IP 地址。 有关风险事件的完整信息，请参阅 Azure AD Identity Protection 文档。
localization_priority: Normal
doc_type: resourcePageType
ms.prod: ''
author: cloudhandler
ms.openlocfilehash: bcbe25270f4752e7660ab4ce0c8b9d7d636c22e6
ms.sourcegitcommit: 7ceec757fd82ef3fd80aa3089ef46d3807aa3aa2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2020
ms.locfileid: "48405615"
---
# <a name="anonymousipriskevent-resource-type-deprecated"></a>anonymousIpRiskEvent 资源类型 (弃用) 

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

>[!CAUTION]
>**IdentityRiskEvents** API 已弃用，并将停止返回2020年1月10日的数据。 有关详细信息，请参阅 [弃用的 IDENTITYRISKEVENTS API](https://developer.microsoft.com/office/blogs/deprecatation-of-the-identityriskevents-api/)。

[Azure Active Directory 标识保护](/azure/active-directory/identity-protection/overview-identity-protection)检测到的一个风险事件，其中的帐户登录尝试来自看似匿名的 IP 地址。 有关风险事件的完整信息，请参阅 [AZURE AD Identity Protection 文档](/azure/active-directory/identity-protection/overview-identity-protection)。


## <a name="methods"></a>方法

| 方法           | 返回类型    |说明|
|:---------------|:--------|:----------|
|[获取 anonymousIpRiskEvent](../api/anonymousipriskevent-get.md) | [anonymousIpRiskEvent](anonymousipriskevent.md) |读取 anonymousIpRiskEvent 对象的属性和关系。|

## <a name="properties"></a>属性
| 属性     | 类型   |说明|
|:---------------|:--------|:----------|
|closedDateTime|dateTimeOffset| 风险事件关闭的日期和时间|
|createdDateTime|dateTimeOffset| 风险事件的创建日期和时间。 此值始终大于或等于风险事件本身的日期时间。 这是查询风险事件时用作筛选器的正确属性。|
|id|string| 只读|
|ipAddress|string| 登录的 IP 地址|
|location|string| 连接到登录 IP 地址的位置|
|riskEventDateTime|dateTimeOffset| 风险事件发生的日期和时间|
|riskEventStatus|string| 可取值为：`active`、`remediated`、`dismissedAsFixed`、`dismissedAsFalsePositive`、`dismissedAsIgnore`、`loginBlocked`、`closedMfaAuto`、`closedMultipleReasons`。|
|riskLevel|string| 可取值为：`low`、`medium`、`high`。|
|riskEventType|string| 风险的类型|
|userDisplayName|string| 具有风险的用户的名称|
|userId|string| 用户面临风险的 id|
|userPrincipalName|string| 用户面临风险的用户主体名称|

## <a name="relationships"></a>关系
| 关系 | 类型   |说明|
|:---------------|:--------|:----------|
|impactedUser|[用户](user.md)| 只读。可为空。|

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
   "baseType":"microsoft.graph.locatedRiskEvent",
  "@odata.type": "microsoft.graph.anonymousIpRiskEvent"
}-->

```json
{
  "closedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "ipAddress": "string",
  "location": "string",
  "riskEventDateTime": "String (timestamp)",
  "riskEventStatus": "string",
  "riskLevel": "string",
  "riskType": "string",
  "userDisplayName": "string",
  "userId": "string",
  "userPrincipalName": "string",
  "riskEventType": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "anonymousIpRiskEvent resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->