---
title: Microsoft Graph 中 Excel API 的最佳实践
description: 列出 Microsoft Graph 中 Excel API 的最佳实践和示例
author: grangeryy
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: c7e72c4c6480c75d3080d32c2984e6d0f594c409
ms.sourcegitcommit: a1675c7b8dfc7d7c3c7923d06cda2b0127f9c3e6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/05/2021
ms.locfileid: "49754066"
---
# <a name="best-practices-for-working-with-the-excel-api-in-microsoft-graph"></a><span data-ttu-id="e798e-103">在 Microsoft Graph 中处理 Excel API 的最佳实践</span><span class="sxs-lookup"><span data-stu-id="e798e-103">Best practices for working with the Excel API in Microsoft Graph</span></span>

<span data-ttu-id="e798e-104">本文提供有关在 Microsoft Graph 中使用 Excel API 的建议。</span><span class="sxs-lookup"><span data-stu-id="e798e-104">This article provides recommendations for working with the Excel APIs in Microsoft Graph.</span></span>

## <a name="manage-sessions-in-the-most-efficient-way"></a><span data-ttu-id="e798e-105">以最有效的方式管理会话</span><span class="sxs-lookup"><span data-stu-id="e798e-105">Manage sessions in the most efficient way</span></span>

<span data-ttu-id="e798e-106">如果在一定时间内进行多个呼叫，我们建议您创建一个会话，并传递每个请求的会话 ID。</span><span class="sxs-lookup"><span data-stu-id="e798e-106">If you have more than one call to make within a certain period of time, we recommend that you create a session and pass the session ID with each request.</span></span> <span data-ttu-id="e798e-107">若要表示 API 中的会话，请使用 `workbook-session-id: {session-id}` 标头。</span><span class="sxs-lookup"><span data-stu-id="e798e-107">To represent the session in the API, use the `workbook-session-id: {session-id}` header.</span></span> <span data-ttu-id="e798e-108">通过执行此操作，您可以以最有效的方式使用 Excel API。</span><span class="sxs-lookup"><span data-stu-id="e798e-108">By doing so, you can use the Excel APIs in the most efficient way.</span></span>

<span data-ttu-id="e798e-109">以下示例演示如何向表中添加新编号，然后使用这种方法在工作簿中查找一条记录。</span><span class="sxs-lookup"><span data-stu-id="e798e-109">The following example shows you how to add a new number to a table and then find one record in a workbook using this approach.</span></span>

### <a name="step-1-create-a-session"></a><span data-ttu-id="e798e-110">步骤 1：创建会话</span><span class="sxs-lookup"><span data-stu-id="e798e-110">Step 1: Create a session</span></span>

#### <a name="request"></a><span data-ttu-id="e798e-111">请求</span><span class="sxs-lookup"><span data-stu-id="e798e-111">Request</span></span>

```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/createSession
Content-type: application/json
Content-length: 52

{
  "persistChanges": true
}
```
#### <a name="response"></a><span data-ttu-id="e798e-112">响应</span><span class="sxs-lookup"><span data-stu-id="e798e-112">Response</span></span>

<span data-ttu-id="e798e-113">下面是一个成功响应。</span><span class="sxs-lookup"><span data-stu-id="e798e-113">The following is a successful response.</span></span>

```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 52

{
  "id": "id-value",
  "persistChanges": true
}
```

### <a name="step-2-add-a-new-row-to-the-table"></a><span data-ttu-id="e798e-114">步骤 2：向表中添加新行</span><span class="sxs-lookup"><span data-stu-id="e798e-114">Step 2: Add a new row to the table</span></span>

#### <a name="request"></a><span data-ttu-id="e798e-115">请求</span><span class="sxs-lookup"><span data-stu-id="e798e-115">Request</span></span>

```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/Table1/rows/add
Content-type: application/json
workbook-session-id: {session-id}

{
  "values": [[“east”, “pear”, 4]]
}
```

#### <a name="response"></a><span data-ttu-id="e798e-116">响应</span><span class="sxs-lookup"><span data-stu-id="e798e-116">Response</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 42

{
  "index": 6,
  "values": [[“east”, “pear”, 4]]
}
```

### <a name="step-3-look-up-a-value-in-the-updated-table"></a><span data-ttu-id="e798e-117">步骤 3：在更新的表中查找值</span><span class="sxs-lookup"><span data-stu-id="e798e-117">Step 3: Look up a value in the updated table</span></span>

#### <a name="request"></a><span data-ttu-id="e798e-118">请求</span><span class="sxs-lookup"><span data-stu-id="e798e-118">Request</span></span>

```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/functions/vlookup
Content-type: application/json
workbook-session-id: {session-id}

{
    "lookupValue":"pear",
    "tableArray":{"Address":"Sheet1!B2:C7"},
    "colIndexNum":2,
    "rangeLookup":false
}
```

#### <a name="response"></a><span data-ttu-id="e798e-119">响应</span><span class="sxs-lookup"><span data-stu-id="e798e-119">Response</span></span>

```http
HTTP code: 200 OK
content-type: application/json

{
    "value": 5
}
```

### <a name="step-4-close-the-session-after-all-the-requests-are-completed"></a><span data-ttu-id="e798e-120">步骤 4：完成所有请求后关闭会话</span><span class="sxs-lookup"><span data-stu-id="e798e-120">Step 4: Close the session after all the requests are completed</span></span>

#### <a name="request"></a><span data-ttu-id="e798e-121">请求</span><span class="sxs-lookup"><span data-stu-id="e798e-121">Request</span></span>

```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/closeSession
Content-type: application/json
workbook-session-id: {session-id}
Content-length: 0

{
}
```

#### <a name="response"></a><span data-ttu-id="e798e-122">响应</span><span class="sxs-lookup"><span data-stu-id="e798e-122">Response</span></span>

```http
HTTP/1.1 204 No Content
```

<span data-ttu-id="e798e-123">有关详细信息，请参阅"创建[会话"和](/graph/api/workbook-createsession?view=graph-rest-1.0)"[关闭会话"。](/graph/api/workbook-closesession?view=graph-rest-1.0)</span><span class="sxs-lookup"><span data-stu-id="e798e-123">For more details, see [Create session](/graph/api/workbook-createsession?view=graph-rest-1.0) and [Close session](/graph/api/workbook-closesession?view=graph-rest-1.0).</span></span>

## <a name="working-with-apis-that-take-a-long-time-to-complete"></a><span data-ttu-id="e798e-124">使用需要很长时间才能完成的 API</span><span class="sxs-lookup"><span data-stu-id="e798e-124">Working with APIs that take a long time to complete</span></span>

<span data-ttu-id="e798e-125">您可能会注意到，某些操作需要不确定的时间才能完成;例如，打开一个大型工作簿。</span><span class="sxs-lookup"><span data-stu-id="e798e-125">You might notice that some operations take an indeterminate amount time to complete; for example, opening a large workbook.</span></span> <span data-ttu-id="e798e-126">在等待这些请求的响应时，很容易命中超时。</span><span class="sxs-lookup"><span data-stu-id="e798e-126">It is easy to hit timeout while waiting for the response to these requests.</span></span> <span data-ttu-id="e798e-127">为了解决此问题，我们提供长时间运行的操作模式。</span><span class="sxs-lookup"><span data-stu-id="e798e-127">To resolve this issue, we provide the long-running operation pattern.</span></span> <span data-ttu-id="e798e-128">使用此模式时，无需担心请求的超时。</span><span class="sxs-lookup"><span data-stu-id="e798e-128">When you use this pattern, you don't need to worry about the timeout for the request.</span></span>

<span data-ttu-id="e798e-129">目前，Microsoft Graph 中的会话创建 Excel API 已启用长时间运行的操作模式。</span><span class="sxs-lookup"><span data-stu-id="e798e-129">Currently, the session creation Excel API in Microsoft Graph has the long-running operation pattern enabled.</span></span> <span data-ttu-id="e798e-130">此模式涉及以下步骤：</span><span class="sxs-lookup"><span data-stu-id="e798e-130">This pattern involves the following steps:</span></span>

1. <span data-ttu-id="e798e-131">向请求添加一个标头，以指示创建会话时这是 `Prefer: respond-async` 一个长时间运行的操作。</span><span class="sxs-lookup"><span data-stu-id="e798e-131">Add a `Prefer: respond-async` header to the request to indicate that it is a long-running operation when you crate a session.</span></span>
2. <span data-ttu-id="e798e-132">长时间运行的操作将返回响应以及 `202 Accepted` 位置标头，以检索操作状态。</span><span class="sxs-lookup"><span data-stu-id="e798e-132">A long-running operation will return a `202 Accepted` response along with a Location header to retrieve the operation status.</span></span> <span data-ttu-id="e798e-133">如果会话创建在几秒钟后完成，它将返回常规创建会话响应，而不是使用长时间运行的操作模式。</span><span class="sxs-lookup"><span data-stu-id="e798e-133">If the session creation completes in several seconds, it will return a regular create session response instead of using the long-running operation pattern.</span></span>
3. <span data-ttu-id="e798e-134">通过 `202 Accepted` 响应，您可以在指定位置检索操作状态。</span><span class="sxs-lookup"><span data-stu-id="e798e-134">With the `202 Accepted` response, you can retrieve the operation status at the specified location.</span></span> <span data-ttu-id="e798e-135">操作状态值包括 `notStarted` 、 `running` 和 `succeeded` `failed` 。</span><span class="sxs-lookup"><span data-stu-id="e798e-135">Operation status values include `notStarted`, `running`, `succeeded`, and `failed`.</span></span>
4. <span data-ttu-id="e798e-136">操作完成后，可以通过成功响应中的指定 URL 获取会话创建结果。</span><span class="sxs-lookup"><span data-stu-id="e798e-136">After the operation completes, you can get the session creation result through the specified URL in the succeeded response.</span></span>

<span data-ttu-id="e798e-137">以下示例使用长时间运行的操作模式创建会话。</span><span class="sxs-lookup"><span data-stu-id="e798e-137">The following example creates a session using the long-running operation pattern.</span></span>

### <a name="initial-request-to-create-session"></a><span data-ttu-id="e798e-138">创建会话的初始请求</span><span class="sxs-lookup"><span data-stu-id="e798e-138">Initial request to create session</span></span>

#### <a name="request"></a><span data-ttu-id="e798e-139">请求</span><span class="sxs-lookup"><span data-stu-id="e798e-139">Request</span></span>

```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{drive-item-id}/workbook/worksheets({id})/createSession
Prefer: respond-async
Content-type: application/json
{
    "persistChanges": true
}
```

#### <a name="response"></a><span data-ttu-id="e798e-140">响应</span><span class="sxs-lookup"><span data-stu-id="e798e-140">Response</span></span>
<span data-ttu-id="e798e-141">长时间运行的操作模式将返回 `202 Accepted` 类似于以下内容的响应。</span><span class="sxs-lookup"><span data-stu-id="e798e-141">The long-running operation pattern will return a `202 Accepted` response similar to the following.</span></span>

```http
HTTP/1.1 202 Accepted
Location: https://graph.microsoft.com/v1.0/me/drive/items/{drive-item-id}/workbook/operations/{operation-id}
Content-type: application/json

{
}
```

<span data-ttu-id="e798e-142">在某些情况下，如果创建在几秒钟内成功，它不会进入长时间运行的操作模式;相反，它将作为常规创建会话返回，并且成功的请求将返回 `201 Created` 响应。</span><span class="sxs-lookup"><span data-stu-id="e798e-142">In some cases, if the creation succeeds within seconds, it won't enter the long-running operation pattern; instead, it returns as a regular create session and the successful request will return a `201 Created` response.</span></span>

```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 52

{
  "id": "id-value",
  "persistChanges": true
}
```

<span data-ttu-id="e798e-143">以下示例显示请求失败时的响应。</span><span class="sxs-lookup"><span data-stu-id="e798e-143">The following example shows the response when the request fails.</span></span>

><span data-ttu-id="e798e-144">**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。</span><span class="sxs-lookup"><span data-stu-id="e798e-144">**Note:** The response object shown here might be shortened for readability.</span></span>

```http
HTTP/1.1 500 Internal Server Error
Content-type: application/json

{
  "error":{
    "code": "internalServerError",
    "message": "An internal server error occurred while processing the request.",
    "innerError": {
      "code": "internalServerErrorUncategorized",
      "message": "An unspecified error has occurred.",
      "innerError": {
        "code": "GenericFileOpenError",
        "message": "The workbook cannot be opened."
      }
    }
  }
}
```

### <a name="poll-status-of-the-long-running-create-session"></a><span data-ttu-id="e798e-145">长时间运行的创建会话的轮询状态</span><span class="sxs-lookup"><span data-stu-id="e798e-145">Poll status of the long-running create session</span></span>


<span data-ttu-id="e798e-146">使用长时间运行的操作模式，可以通过以下请求获取指定位置的创建状态。</span><span class="sxs-lookup"><span data-stu-id="e798e-146">With the long-running operation pattern, you can get the creation status at specified location by using the following request.</span></span> <span data-ttu-id="e798e-147">建议的轮询状态的间隔约为 30 秒。</span><span class="sxs-lookup"><span data-stu-id="e798e-147">The suggested interval to poll status is around 30 seconds.</span></span> <span data-ttu-id="e798e-148">最大间隔不应超过 4 分钟。</span><span class="sxs-lookup"><span data-stu-id="e798e-148">The maximum interval should be no more than 4 minutes.</span></span>

#### <a name="request"></a><span data-ttu-id="e798e-149">请求</span><span class="sxs-lookup"><span data-stu-id="e798e-149">Request</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{drive-item-id}/workbook/operations/{operation-id}
{
}
```

#### <a name="response"></a><span data-ttu-id="e798e-150">响应</span><span class="sxs-lookup"><span data-stu-id="e798e-150">Response</span></span>

<span data-ttu-id="e798e-151">下面是操作状态为时的响应 `running` 。</span><span class="sxs-lookup"><span data-stu-id="e798e-151">The following is the response when the operation has a status of `running`.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "id": {operation-id},
    "status": "running"
}
```

<span data-ttu-id="e798e-152">下面是操作状态为时的响应 `succeeded` 。</span><span class="sxs-lookup"><span data-stu-id="e798e-152">The following is the response when the operation status is `succeeded`.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "id": {operation-id},
    "status": "succeeded",
    "resourceLocation": "https://graph.microsoft.com/v1.0/me/drive/items/{drive-item-id}/workbook/sessionInfoResource(key='{key}')
}
```

<span data-ttu-id="e798e-153">下面是操作状态为时的响应 `failed` 。</span><span class="sxs-lookup"><span data-stu-id="e798e-153">The following is the response when the operation status is `failed`.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "id": {operation-id},
  "status": "failed",
  "error":{
    "code": "internalServerError",
    "message": "An internal server error occurred while processing the request.",
    "innerError": {
      "code": ""internalServerErrorUncategorized",
      "message": "An unspecified error has occurred.",
      "innerError": {
        "code": "GenericFileOpenError",
        "message": "The workbook cannot be opened."
      }
    }
  }
}
```

<span data-ttu-id="e798e-154">有关错误的更多详细信息，请参阅错误 [代码](workbook-error-codes.md#error-code)。</span><span class="sxs-lookup"><span data-stu-id="e798e-154">For more details about errors, see [Error codes](workbook-error-codes.md#error-code).</span></span>

### <a name="acquire-session-information"></a><span data-ttu-id="e798e-155">获取会话信息</span><span class="sxs-lookup"><span data-stu-id="e798e-155">Acquire session information</span></span>

#### <a name="request"></a><span data-ttu-id="e798e-156">请求</span><span class="sxs-lookup"><span data-stu-id="e798e-156">Request</span></span>

<span data-ttu-id="e798e-157">如果状态为 ，则可以通过类似于以下内容的请求获取创建的 `succeeded` `resourceLocation` 会话信息。</span><span class="sxs-lookup"><span data-stu-id="e798e-157">With a status of `succeeded`, you can get the created session information through `resourceLocation` with a request similar to the following.</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{drive-item-id}/workbook/sessionInfoResource(key='{key}')
{
}
```

#### <a name="response"></a><span data-ttu-id="e798e-158">响应</span><span class="sxs-lookup"><span data-stu-id="e798e-158">Response</span></span>
<span data-ttu-id="e798e-159">以下是答复。</span><span class="sxs-lookup"><span data-stu-id="e798e-159">The following is the response.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "id": "id-value",
    "persistChanges": true
}
```

><span data-ttu-id="e798e-160">**注意：** 获取会话信息取决于初始请求。</span><span class="sxs-lookup"><span data-stu-id="e798e-160">**Note:** Acquire session information depends on the initial request.</span></span> <span data-ttu-id="e798e-161">如果初始请求未返回响应正文，则无需获取结果。</span><span class="sxs-lookup"><span data-stu-id="e798e-161">You don't need to acquire the result if the initial request doesn't return a response body.</span></span>
