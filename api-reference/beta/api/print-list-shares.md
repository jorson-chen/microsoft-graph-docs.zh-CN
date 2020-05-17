---
title: 获取共享
description: 检索打印机共享的列表。
author: braedenp-msft
localization_priority: Normal
ms.prod: universal-print
doc_type: apiPageType
ms.openlocfilehash: 5e3e58c34481022ca23507b20af71c8ff0de4388
ms.sourcegitcommit: d4114bac58628527611e83e436132c6581a19c52
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/13/2020
ms.locfileid: "44216964"
---
# <a name="list-shares"></a><span data-ttu-id="0d115-103">列出共享</span><span class="sxs-lookup"><span data-stu-id="0d115-103">List shares</span></span>

<span data-ttu-id="0d115-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="0d115-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="0d115-105">检索**printerShares**的列表。</span><span class="sxs-lookup"><span data-stu-id="0d115-105">Retrieve a list of **printerShares**.</span></span>

## <a name="permissions"></a><span data-ttu-id="0d115-106">权限</span><span class="sxs-lookup"><span data-stu-id="0d115-106">Permissions</span></span>
<span data-ttu-id="0d115-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="0d115-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

<span data-ttu-id="0d115-109">除了以下权限之外，用户的租户还必须具有活动的通用打印订阅。</span><span class="sxs-lookup"><span data-stu-id="0d115-109">In addition to the following permissions, the user's tenant must have an active Universal Print subscription.</span></span>

|<span data-ttu-id="0d115-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="0d115-110">Permission type</span></span> | <span data-ttu-id="0d115-111">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="0d115-111">Permissions (from least to most privileged)</span></span> |
|:---------------|:--------------------------------------------|
|<span data-ttu-id="0d115-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="0d115-112">Delegated (work or school account)</span></span>| <span data-ttu-id="0d115-113">已阅读的用户。所有</span><span class="sxs-lookup"><span data-stu-id="0d115-113">Users.Read.All</span></span> |
|<span data-ttu-id="0d115-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="0d115-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0d115-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="0d115-115">Not Supported.</span></span>|
|<span data-ttu-id="0d115-116">Application</span><span class="sxs-lookup"><span data-stu-id="0d115-116">Application</span></span>|<span data-ttu-id="0d115-117">不支持。</span><span class="sxs-lookup"><span data-stu-id="0d115-117">Not Supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0d115-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="0d115-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /print/shares
```

## <a name="optional-query-parameters"></a><span data-ttu-id="0d115-119">可选的查询参数</span><span class="sxs-lookup"><span data-stu-id="0d115-119">Optional query parameters</span></span>
<span data-ttu-id="0d115-120">此方法支持一些 OData 查询参数来帮助自定义响应。</span><span class="sxs-lookup"><span data-stu-id="0d115-120">This method supports some of the OData query parameters to help customize the response.</span></span> <span data-ttu-id="0d115-121">有关一般信息，请参阅[OData 查询参数](/graph/query-parameters)。</span><span class="sxs-lookup"><span data-stu-id="0d115-121">For general information, see [OData query parameters](/graph/query-parameters).</span></span>

### <a name="exceptions"></a><span data-ttu-id="0d115-122">异常</span><span class="sxs-lookup"><span data-stu-id="0d115-122">Exceptions</span></span>
<span data-ttu-id="0d115-123">某些运算符不受支持： `$count` 、 `$orderby` 、 `$search` 。</span><span class="sxs-lookup"><span data-stu-id="0d115-123">Some operators are not supported: `$count`, `$orderby`, `$search`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="0d115-124">请求标头</span><span class="sxs-lookup"><span data-stu-id="0d115-124">Request headers</span></span>
| <span data-ttu-id="0d115-125">名称</span><span class="sxs-lookup"><span data-stu-id="0d115-125">Name</span></span>      |<span data-ttu-id="0d115-126">说明</span><span class="sxs-lookup"><span data-stu-id="0d115-126">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="0d115-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="0d115-127">Authorization</span></span> | <span data-ttu-id="0d115-p103">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="0d115-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="0d115-130">请求正文</span><span class="sxs-lookup"><span data-stu-id="0d115-130">Request body</span></span>
<span data-ttu-id="0d115-131">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="0d115-131">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="0d115-132">响应</span><span class="sxs-lookup"><span data-stu-id="0d115-132">Response</span></span>
<span data-ttu-id="0d115-133">如果成功，此方法 `200 OK` 在响应正文中返回响应代码和[printerShare](../resources/printershare.md)对象集合。</span><span class="sxs-lookup"><span data-stu-id="0d115-133">If successful, this method returns a `200 OK` response code and a collection of [printerShare](../resources/printershare.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="0d115-134">示例</span><span class="sxs-lookup"><span data-stu-id="0d115-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="0d115-135">请求</span><span class="sxs-lookup"><span data-stu-id="0d115-135">Request</span></span>
<span data-ttu-id="0d115-136">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="0d115-136">The following is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="0d115-137">HTTP</span><span class="sxs-lookup"><span data-stu-id="0d115-137">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_shares"
}-->
```msgraph-interactive
GET https://graph.microsoft.com/beta/print/shares
```
# <a name="c"></a>[<span data-ttu-id="0d115-138">C#</span><span class="sxs-lookup"><span data-stu-id="0d115-138">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-shares-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="0d115-139">JavaScript</span><span class="sxs-lookup"><span data-stu-id="0d115-139">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-shares-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="0d115-140">Objective-C</span><span class="sxs-lookup"><span data-stu-id="0d115-140">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-shares-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

##### <a name="response"></a><span data-ttu-id="0d115-141">响应</span><span class="sxs-lookup"><span data-stu-id="0d115-141">Response</span></span>
<span data-ttu-id="0d115-142">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="0d115-142">The following is an example of the response.</span></span>
><span data-ttu-id="0d115-p104">**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。所有属性都将通过实际调用返回。</span><span class="sxs-lookup"><span data-stu-id="0d115-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.printerShare",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 269

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#print/shares",
  "value": [
    {
      "id": "016b5565-3bbf-4067-b9ff-4d68167eb1a6",
      "name": "PrinterShareName",
      "createdDateTime": "2020-02-04T00:00:00.0000000Z"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List shares",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->