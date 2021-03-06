---
title: 列出 accessReviewInstanceDecisionItem 等待审批
description: 检索 accessReviewInstanceDecisionItem 对象等待调用用户批准。
localization_priority: Normal
author: isabelleatmsft
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: 22c47613ef2017ee226d55cac08df68d718686bd
ms.sourcegitcommit: 479b366f3265b666fdc024b0f90b8d29764bb4b2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/26/2021
ms.locfileid: "49981086"
---
# <a name="list-accessreviewinstancedecisionitems-pending-approval"></a>列出 accessReviewInstanceDecisionItems 等待审批

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

检索 [特定 accessReviewInstanceDecisionItem](../resources/accessreviewinstance.md) 对象的 [accessReviewInstance](../resources/accessreviewscheduledefinition.md) 等待调用用户批准。 返回零个或多个 accessReviewInstanceDecisionItem 对象的列表，包括所有嵌套属性。

>[!NOTE]
>如果返回了许多 **accessReviewInstanceDecisionItems，** 为了提高效率并避免超时，请通过同时在请求中同时包含页面大小最多为 100 的 $top 查询参数和 $skip=0 查询参数，在页面中检索 结果集。 当结果集跨多个页面时，Microsoft Graph 在响应中返回包含指向下一页结果的 URL 的 @odata.nextLink 属性的页面。 如果该属性存在，请在每个响应中继续使用 @odata.nextLink URL 提出其他请求，直到返回所有结果，如在应用中分页 Microsoft Graph 数据中所述。
>
>如果未提供查询参数且结果超过 100 个，Microsoft Graph 将按每页 100 个结果自动对结果分页。

## <a name="permissions"></a>Permissions
要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。

|权限类型                        | 权限（从最低特权到最高特权）              |
|:--------------------------------------|:---------------------------------------------------------|
|委派（工作或学校帐户）     | AccessReview.Read.All、AccessReview.ReadWrite.All  |
|委派（个人 Microsoft 帐户）|不支持。|

登录用户还将仅在该决策实例的 accessReviewScheduleDefinition 中查看为其分配审阅者的决策。

## <a name="http-request"></a>HTTP 请求
<!-- { "blockType": "ignored" } -->
```http
GET /me/pendingAccessReviewInstances/{instance-id}/decisions
```
## <a name="request-headers"></a>请求标头
无。

## <a name="request-body"></a>请求正文
不提供请求正文。

## <a name="response"></a>响应
如果成功，此方法在响应正文中返回响应代码 `200 OK` 和 [accessReviewInstanceDecisionItem](../resources/accessreviewinstance.md) 对象数组。

## <a name="examples"></a>示例
### <a name="request"></a>请求
以下示例显示了一个请求，请求检索有关访问评审实例的所有决策，等待呼叫用户批准。


# <a name="http"></a>[HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "list_accessReviewInstanceDecisionItem_pendingapproval"
}-->
```msgraph-interactive
GET https://graph.microsoft.com/beta/me/pendingAccessReviewInstances/70a68410-67f3-4d4c-b946-6989e050be19/decisions?$top=100&$skip=0
```
# <a name="c"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/list-accessreviewinstancedecisionitem-pendingapproval-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/list-accessreviewinstancedecisionitem-pendingapproval-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/list-accessreviewinstancedecisionitem-pendingapproval-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/list-accessreviewinstancedecisionitem-pendingapproval-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


---


### <a name="response"></a>响应
>**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。所有属性都将通过实际调用返回。
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.accessReviewInstanceDecisionItem",
  "isCollection": "true"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.count": 2,
    "value": [
        {
            "id": "654b34e7-b48f-4772-a2d4-08f1d0dd014c",
            "accessReviewId": "70a68410-67f3-4d4c-b946-6989e050be19",
            "reviewedDateTime": null,
            "decision": "NotReviewed",
            "justification": "",
            "appliedDateTime": null,
            "applyResult": "New",
            "recommendation": "Approve",
            "reviewedBy": {
                "id": "00000000-0000-0000-0000-000000000000",
                "displayName": "",
                "userPrincipalName": ""
            },
            "appliedBy": {
                "id": "00000000-0000-0000-0000-000000000000",
                "displayName": "",
                "userPrincipalName": ""
            },
            "target": {
                "@odata.type": "#microsoft.graph.accessReviewInstanceDecisionItemUserTarget",
                "userId": "7eae986b-d425-48b2-adf2-3c777f6256f3",
                "userDisplayName": "Adele Vance",
                "userPrincipalName": "AdeleV@contoso.com"
            }
        },
        {
            "id": "0311dba4-c60c-412e-ac77-14e1da23daf1",
            "accessReviewId": "70a68410-67f3-4d4c-b946-6989e050be19",
            "reviewedDateTime": null,
            "decision": "NotReviewed",
            "justification": "",
            "appliedDateTime": null,
            "applyResult": "New",
            "recommendation": "Approve",
            "reviewedBy": {
                "id": "00000000-0000-0000-0000-000000000000",
                "displayName": "",
                "userPrincipalName": ""
            },
            "appliedBy": {
                "id": "00000000-0000-0000-0000-000000000000",
                "displayName": "",
                "userPrincipalName": ""
            },
            "target": {
                "@odata.type": "#microsoft.graph.accessReviewInstanceDecisionItemUserTarget",
                "userId": "957f1027-c0ee-460d-9269-b8828e59e0fe",
                "userDisplayName": "MOD Administrator",
                "userPrincipalName": "admin@contoso.com"
            }
        }
    ]
}
```

## <a name="see-also"></a>另请参阅

- [获取 accessReviewScheduleDefinition](accessreviewscheduledefinition-get.md)
- [获取 accessReviewInstance](accessreviewinstance-get.md)


<!--
{
  "type": "#page.annotation",
  "description": "List accessReviewInstanceDecisionItem pendingApproval",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
