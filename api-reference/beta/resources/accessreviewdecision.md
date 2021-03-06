---
title: accessReviewDecision 资源类型
description: AccessReviewDecision 表示特定实体的访问的 Azure AD 访问审核决策。
localization_priority: Normal
author: markwahl-msft
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: f22411e15b7c886847c366537a5f3a77f8283b7a
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48024579"
---
# <a name="accessreviewdecision-resource-type"></a>accessReviewDecision 资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

在 Azure AD [access 评论](accessreviews-root.md) 功能中， `accessReviewDecision` 表示特定实体的访问的 azure ad 访问审核决策。  在访问评审或定期访问审核实例中， `accessReviewDecision` 每个审阅的用户都有一个。  例如，如果一个组有两个来宾，一个非来宾作为成员，并且对该组执行来宾的访问审核，则会有两个访问审核决策对象。  如果审阅者更改了他们的决定，或另一个审阅者将其覆盖，则 `accessReviewDecision` 会更新。


## <a name="methods"></a>方法

无。  此类对象将在 access 评审初始化时自动创建，并且无法删除。  可以使用 [决策](../api/accessreview-listdecisions.md) 和 [mydecisions](../api/accessreview-listmydecisions.md) 关系从访问审核中检索它们。

## <a name="properties"></a>属性

此表阐释了此类型对象的基本属性。 

| 属性                        | 类型                         | 说明                                                                                            |
| :------------------------------ | :-----------------------     | :----------------------------------------------------------------------------------------------------- |
| `id`                            |`String`                      | 访问评审中决策的 id。                                                                                     |
| `accessReviewId`                |`String`                      | 功能生成的访问评审的 id。                                                                                       |
| `reviewedBy`                    |[userIdentity](useridentity.md)| 审阅者的标识。 如果将建议用作审阅，则 userPrincipalName 为空。                                                                                      |
| `reviewedDate`                  |`DateTimeOffset`              | 提供此访问权限最近一次审阅的日期和时间。                                                                         |
| `reviewResult`                  |`String`                      | 评审的结果、、 `NotReviewed` `Deny` `DontKnow` 或 `Approve` 。                                                                                    |
| `justification`                 |`String`                      | 审阅者的业务理由（如果提供）。                                                                         |
| `appliedBy`                     |[userIdentity](useridentity.md)| 当评审完成时，如果手动应用了结果，则为应用决策的用户的用户标识。 如果已自动应用审阅，则 userPrincipalName 为空。                                                          |
| `appliedDateTime`               |`DateTimeOffset`              | 应用评审决策的日期和时间。                                                          |
| `applyResult`                   |`String`                      | 应用决策、、、或的结果 `NotApplied` `Success` `Failed` `NotFound` `NotSupported` 。                      |
| `accessRecommendation`          |`String`                      | 向审阅者、或之一显示的功能生成的建议 `Approve` `Deny` `NotAvailable` 。 |


此外，还可能会出现其他属性，具体取决于拥有所决定的访问权限的对象的对象类型。  例如，如果访问审核决策是特定用户的组成员身份或应用程序访问权限，则可以通过以下属性来标识可能要删除其访问权限的用户：

| 属性                        | 类型                         | 说明                                                                                            |
| :------------------------------ | :-----------------------     | :----------------------------------------------------------------------------------------------------- |
| `userId`                            |`String`                      | 已查看其访问权限的用户的 id。                                                                                    |
| `userDisplayName`                            |`String`                      | 已查看其访问权限的用户的显示名称。                                                                                     |
| `userPrincipalName`                            |`String`                      | 已查看其访问权限的用户的用户主体名称。                                                                                     |



## <a name="relationships"></a>关系

无。  通过使用[accessReview](accessreview.md)对象的[决策](../api/accessreview-listdecisions.md)和[mydecisions](../api/accessreview-listmydecisions.md)关系，可以从访问审核中检索此类型的对象。

## <a name="see-also"></a>另请参阅

| 方法           | 返回类型    |说明|
|:---------------|:--------|:----------|
|[列出 accessReview 决策](../api/accessreview-listdecisions.md) |      [accessReviewDecision](accessreviewdecision.md) 集合| 获取 accessReview 的决策。|
|[列出我的 accessReview 决策](../api/accessreview-listmydecisions.md) |     [accessReviewDecision](accessreviewdecision.md) 集合| 作为审阅者，请 accessReview 的决策。|

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.accessReviewDecision"
}-->

```json
{
"id": "string (identifier)",
"accessReviewId": "string (identifier)",
"reviewedBy": "microsoft.graph.userIdentity",
"reviewedDate": "string (timestamp)",
"reviewResult": "string",
"justification": "string",
"appliedBy": "microsoft.graph.userIdentity",
"appliedDateTime": "string (timestamp)",
"applyResult": "string",
"accessRecommendation": "string",
"userId": "string",
"userDisplayName": "string",
"userPrincipalName": "string"
}

```

<!--
{
  "type": "#page.annotation",
  "description": "accessReviewDecision resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


