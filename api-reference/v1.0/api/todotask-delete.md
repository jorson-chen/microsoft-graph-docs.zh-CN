---
title: 删除 todoTask
description: 删除 todoTask 对象。
author: avijityadav
localization_priority: Normal
ms.prod: outlook
doc_type: apiPageType
ms.openlocfilehash: a991d641f807898fa644361a55d350b162c884ff
ms.sourcegitcommit: eacd2a6e46c19dd3cd8519592b1668fabe14d85d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "49873820"
---
# <a name="delete-todotask"></a><span data-ttu-id="23bc1-103">删除 todoTask</span><span class="sxs-lookup"><span data-stu-id="23bc1-103">Delete todoTask</span></span>
<span data-ttu-id="23bc1-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="23bc1-104">Namespace: microsoft.graph</span></span>

<span data-ttu-id="23bc1-105">删除 [todoTask](../resources/todotask.md) 对象。</span><span class="sxs-lookup"><span data-stu-id="23bc1-105">Deletes a [todoTask](../resources/todotask.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="23bc1-106">权限</span><span class="sxs-lookup"><span data-stu-id="23bc1-106">Permissions</span></span>
<span data-ttu-id="23bc1-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="23bc1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="23bc1-109">权限类型</span><span class="sxs-lookup"><span data-stu-id="23bc1-109">Permission type</span></span>|<span data-ttu-id="23bc1-110">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="23bc1-110">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="23bc1-111">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="23bc1-111">Delegated (work or school account)</span></span>|<span data-ttu-id="23bc1-112">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="23bc1-112">Tasks.ReadWrite</span></span>|
|<span data-ttu-id="23bc1-113">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="23bc1-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="23bc1-114">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="23bc1-114">Tasks.ReadWrite</span></span>|
|<span data-ttu-id="23bc1-115">应用</span><span class="sxs-lookup"><span data-stu-id="23bc1-115">Application</span></span>|<span data-ttu-id="23bc1-116">不支持</span><span class="sxs-lookup"><span data-stu-id="23bc1-116">Not supported</span></span>|

## <a name="http-request"></a><span data-ttu-id="23bc1-117">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="23bc1-117">HTTP request</span></span>

<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /me/todo/lists/{todoTaskListId}/tasks/{taskId}
DELETE /users/{id|userPrincipalName}/todo/lists/{todoTaskListId}/tasks/{taskId}
```

## <a name="request-headers"></a><span data-ttu-id="23bc1-118">请求标头</span><span class="sxs-lookup"><span data-stu-id="23bc1-118">Request headers</span></span>
|<span data-ttu-id="23bc1-119">名称</span><span class="sxs-lookup"><span data-stu-id="23bc1-119">Name</span></span>|<span data-ttu-id="23bc1-120">说明</span><span class="sxs-lookup"><span data-stu-id="23bc1-120">Description</span></span>|
|:---|:---|
|<span data-ttu-id="23bc1-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="23bc1-121">Authorization</span></span>|<span data-ttu-id="23bc1-p102">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="23bc1-p102">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="23bc1-124">请求正文</span><span class="sxs-lookup"><span data-stu-id="23bc1-124">Request body</span></span>
<span data-ttu-id="23bc1-125">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="23bc1-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="23bc1-126">响应</span><span class="sxs-lookup"><span data-stu-id="23bc1-126">Response</span></span>

<span data-ttu-id="23bc1-127">如果成功，此方法返回 `204 No Content` 响应代码。</span><span class="sxs-lookup"><span data-stu-id="23bc1-127">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="examples"></a><span data-ttu-id="23bc1-128">示例</span><span class="sxs-lookup"><span data-stu-id="23bc1-128">Examples</span></span>

### <a name="request"></a><span data-ttu-id="23bc1-129">请求</span><span class="sxs-lookup"><span data-stu-id="23bc1-129">Request</span></span>


# <a name="http"></a>[<span data-ttu-id="23bc1-130">HTTP</span><span class="sxs-lookup"><span data-stu-id="23bc1-130">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "sampleKeys": ["AAMkADA1MTHgwAAA=", "721a35e2-35e2-721a-e235-1a72e2351a72"],
  "name": "delete_todotask"
}
-->
``` http
DELETE https://graph.microsoft.com/v1.0/me/todo/lists/AAMkADA1MTHgwAAA=/tasks/721a35e2-35e2-721a-e235-1a72e2351a72
```
# <a name="c"></a>[<span data-ttu-id="23bc1-131">C#</span><span class="sxs-lookup"><span data-stu-id="23bc1-131">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/delete-todotask-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="23bc1-132">JavaScript</span><span class="sxs-lookup"><span data-stu-id="23bc1-132">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/delete-todotask-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="23bc1-133">Objective-C</span><span class="sxs-lookup"><span data-stu-id="23bc1-133">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/delete-todotask-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[<span data-ttu-id="23bc1-134">Java</span><span class="sxs-lookup"><span data-stu-id="23bc1-134">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/delete-todotask-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---



### <a name="response"></a><span data-ttu-id="23bc1-135">响应</span><span class="sxs-lookup"><span data-stu-id="23bc1-135">Response</span></span>
<span data-ttu-id="23bc1-136">**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。</span><span class="sxs-lookup"><span data-stu-id="23bc1-136">**Note:** The response object shown here might be shortened for readability.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 204 No Content
```



