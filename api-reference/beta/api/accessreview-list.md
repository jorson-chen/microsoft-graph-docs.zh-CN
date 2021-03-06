---
title: 列出 accessReviews
description: 检索 businessFlowTemplate 的 accessReview 对象。
localization_priority: Normal
author: markwahl-msft
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: c76dc3a245e003838290f3d233941e6535347b72
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2020
ms.locfileid: "48951639"
---
# <a name="list-accessreviews"></a>列出 accessReviews

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

检索特定[businessFlowTemplate](../resources/businessflowtemplate.md)的[accessReview](../resources/accessreview.md)对象。 返回零个或多个 **accessReview** 对象的列表，对于使用该业务流模板创建的每个一次性和定期访问评审。  请注意，业务流模板 Id 区分大小写。

>[!NOTE]
> 如果与筛选器匹配的任何访问评审是定期访问审核，则将返回一个 **accessReview** 对象，以将每个定期系列作为一个整体来表示，以及任何当前的过去和下一个即将开始的实例。 例如，如果对组 A 的来宾成员进行每月定期访问审核，则为组 B 的来宾成员进行季度定期访问审核，并对组 C 中的来宾成员进行一次性访问审核，每个重复启动时刚刚启动，并且呼叫者使用对组的来宾成员审阅的业务流模板来查询访问审阅，将返回三个对象，其中包含三个系列，以及当前访问评审实例的三个对象，以及下一个即将发生的实例的可能三个对象。 若要检索定期访问审核实例或为特定月份或季度计划的访问评审实例，调用方可以随后导航到定期 **accessReview** 对象的 **实例** 关系。 指向当前或过去的定期访问审核实例的 **accessReview** 对象的 **实例** 关系。

如果许多访问评审与筛选器匹配，则要提高效率并避免超时，请在页面中检索结果集，方法是将 `$top` 查询参数包含页面大小（例如，100）和 `$skip=0` 请求中的查询参数。 即使您不预计请求将跨多个页面，也可以包含这些参数。 当结果集跨多个页面时，Microsoft Graph 将返回该页面，其中 `@odata.nextLink` 包含响应中包含指向下一页结果的 URL 的属性。 如果该属性存在，请继续使用每次响应中的 `@odata.nextLink` URL 来创建额外请求，直至返回所有结果，如[在应用中对 Microsoft Graph 数据进行分页](/graph/paging.md)一文中所述。

此 API 返回的 **accessReview** 对象将不包含嵌套的结构属性（如 **设置** 或关系）。  若要检索访问审核设置或关系，请使用 [Get accessReview](accessreview-get.md) API。


## <a name="permissions"></a>权限
要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。

|权限类型                        | 权限（从最低特权到最高特权）              |
|:--------------------------------------|:---------------------------------------------------------|
|委派（工作或学校帐户）     | AccessReview、AccessReview、成员身份、AccessReview。所有  |
|委派（个人 Microsoft 帐户） | 不支持。 |
|应用程序                            | AccessReview、AccessReview、成员身份 |

 登录用户还必须位于允许他们阅读访问审核的目录角色中。

## <a name="http-request"></a>HTTP 请求
<!-- { "blockType": "ignored" } -->
```http
GET /accessReviews?$filter=businessFlowTemplateId eq {businessFlowTemplate-id}&$top={pagesize}&$skip=0
```
## <a name="request-headers"></a>请求标头
| 名称         | 类型        | 说明 |
|:-------------|:------------|:------------|
| Authorization | string | 持有者 \{token\}。必需。 |

## <a name="request-body"></a>请求正文
请勿提供请求正文。

## <a name="response"></a>响应
如果成功，此方法 `200 OK` 在响应正文中返回响应代码和 [accessReview](../resources/accessreview.md) 对象的数组。

## <a name="examples"></a>示例
##### <a name="request"></a>请求
下面的示例演示检索业务流模板 "6e4f3d20-c5c3-407f-9695-8460952bcc68" 的所有一次性和定期访问评审的请求。

# <a name="http"></a>[HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_accessReviews"
}-->
```msgraph-interactive
GET https://graph.microsoft.com/beta/accessReviews?$filter=businessFlowTemplateId+eq+'6e4f3d20-c5c3-407f-9695-8460952bcc68'&$top=100&$skip=0
```
# <a name="c"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-accessreviews-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-accessreviews-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-accessreviews-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/get-accessreviews-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---



---


##### <a name="response"></a>响应
>**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。所有属性都将通过实际调用返回。
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.accessReview",
  "isCollection": "true"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value":[
       {
         "id": "2b83cc42-09db-46f6-8c6e-16fec466a82d",
         "displayName": "review",
         "startDateTime": "2017-11-14T01:14:54.89Z",
         "endDateTime": "2017-12-14T01:14:54.89Z",
         "status": "InProgress",
         "businessFlowTemplateId": "6e4f3d20-c5c3-407f-9695-8460952bcc68",
         "reviewerType": "self",
         "description": "",
         "reviewedEntity":{"id":"3b4f7e74-eb82-4120-9ff5-ba429c1ea6df","displayName":"Salesforce"}
       }
    ]
}
```

## <a name="see-also"></a>另请参阅

- [获取 accessReview](accessreview-get.md)


<!--
{
  "type": "#page.annotation",
  "description": "Get accessReviews",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->


