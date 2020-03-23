---
title: 列出 monthlyPrintUsageSummariesByUser
description: 检索按用户分组的按月打印使用情况摘要列表。
author: braedenp-msft
localization_priority: Normal
ms.prod: universal-print
doc_type: apiPageType
ms.openlocfilehash: 0d9246a6206e37600578cc836fe7f476c06e486b
ms.sourcegitcommit: 7baf4847486885edf08ead533c76503cd31a98a4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/21/2020
ms.locfileid: "42895648"
---
# <a name="list-monthlyprintusagesummariesbyuser"></a><span data-ttu-id="8202c-103">列出 monthlyPrintUsageSummariesByUser</span><span class="sxs-lookup"><span data-stu-id="8202c-103">List monthlyPrintUsageSummariesByUser</span></span>

<span data-ttu-id="8202c-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="8202c-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="8202c-105">检索按用户分组的按月打印使用情况摘要列表。</span><span class="sxs-lookup"><span data-stu-id="8202c-105">Retrieve a list of monthly print usage summaries, grouped by user.</span></span>

## <a name="permissions"></a><span data-ttu-id="8202c-106">权限</span><span class="sxs-lookup"><span data-stu-id="8202c-106">Permissions</span></span>
<span data-ttu-id="8202c-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="8202c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

<span data-ttu-id="8202c-109">除了以下权限之外，用户的租户还必须具有活动的通用打印订阅。</span><span class="sxs-lookup"><span data-stu-id="8202c-109">In addition to the following permissions, the user's tenant must have an active Universal Print subscription.</span></span>

|<span data-ttu-id="8202c-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="8202c-110">Permission type</span></span> | <span data-ttu-id="8202c-111">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="8202c-111">Permissions (from least to most privileged)</span></span> |
|:---------------|:--------------------------------------------|
|<span data-ttu-id="8202c-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="8202c-112">Delegated (work or school account)</span></span>| <span data-ttu-id="8202c-113">已阅读的用户。所有</span><span class="sxs-lookup"><span data-stu-id="8202c-113">Users.Read.All</span></span> |
|<span data-ttu-id="8202c-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="8202c-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8202c-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="8202c-115">Not Supported.</span></span>|
|<span data-ttu-id="8202c-116">应用程序</span><span class="sxs-lookup"><span data-stu-id="8202c-116">Application</span></span>|<span data-ttu-id="8202c-117">不支持。</span><span class="sxs-lookup"><span data-stu-id="8202c-117">Not Supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8202c-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="8202c-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /reports/monthlyPrintUsageSummariesByUser
GET /print/reports/monthlyPrintUsageSummariesByUser
```

## <a name="optional-query-parameters"></a><span data-ttu-id="8202c-119">可选的查询参数</span><span class="sxs-lookup"><span data-stu-id="8202c-119">Optional query parameters</span></span>
<span data-ttu-id="8202c-120">此方法支持一些 OData 查询参数来帮助自定义响应。</span><span class="sxs-lookup"><span data-stu-id="8202c-120">This method supports some of the OData query parameters to help customize the response.</span></span> <span data-ttu-id="8202c-121">有关一般信息，请参阅[OData 查询参数](/graph/query-parameters)。</span><span class="sxs-lookup"><span data-stu-id="8202c-121">For general information, see [OData query parameters](/graph/query-parameters).</span></span>

## <a name="request-headers"></a><span data-ttu-id="8202c-122">请求标头</span><span class="sxs-lookup"><span data-stu-id="8202c-122">Request headers</span></span>
| <span data-ttu-id="8202c-123">名称</span><span class="sxs-lookup"><span data-stu-id="8202c-123">Name</span></span>      |<span data-ttu-id="8202c-124">说明</span><span class="sxs-lookup"><span data-stu-id="8202c-124">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="8202c-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="8202c-125">Authorization</span></span> | <span data-ttu-id="8202c-p103">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="8202c-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="8202c-128">请求正文</span><span class="sxs-lookup"><span data-stu-id="8202c-128">Request body</span></span>
<span data-ttu-id="8202c-129">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="8202c-129">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="8202c-130">响应</span><span class="sxs-lookup"><span data-stu-id="8202c-130">Response</span></span>
<span data-ttu-id="8202c-131">如果成功，此方法在响应`200 OK`正文中返回响应代码和[printUsageSummaryByUser](../resources/printusagesummarybyuser.md)对象集合。</span><span class="sxs-lookup"><span data-stu-id="8202c-131">If successful, this method returns a `200 OK` response code and a collection of [printUsageSummaryByUser](../resources/printusagesummarybyuser.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="8202c-132">示例</span><span class="sxs-lookup"><span data-stu-id="8202c-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="8202c-133">请求</span><span class="sxs-lookup"><span data-stu-id="8202c-133">Request</span></span>
<span data-ttu-id="8202c-134">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="8202c-134">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_endpoints"
}-->
```http
GET https://graph.microsoft.com/beta/print/reports/monthlyPrintUsageSummariesByUser
```
##### <a name="response"></a><span data-ttu-id="8202c-135">响应</span><span class="sxs-lookup"><span data-stu-id="8202c-135">Response</span></span>
<span data-ttu-id="8202c-136">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="8202c-136">The following is an example of the response.</span></span>
><span data-ttu-id="8202c-p104">**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。所有属性都将通过实际调用返回。</span><span class="sxs-lookup"><span data-stu-id="8202c-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.printUsageSummaryByUser",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 268

{
  "value": [
    {
      "id": "016b5565-3bbf-4067-b9ff-4d68167eb1a6",
      "userPrincipalName": "username@microsoft.com",
      "usageDate": "2020-02-04T00:00:00.0000000Z",
      "completedBlackAndWhiteJobCount": 42,
      "completedColorJobCount": 0,
      "incompleteJobCount": 6
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List monthlyPrintUsageSummariesByUser",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->