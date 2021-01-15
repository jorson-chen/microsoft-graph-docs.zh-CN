---
title: 删除 cloudPcProvisioningPolicy
description: 删除 cloudPcProvisioningPolicy 对象。
author: AshleyYangSZ
localization_priority: Normal
ms.prod: cloud-pc
doc_type: apiPageType
ms.openlocfilehash: b90a8005f7d2f4e48e07cce07ba3ba525c6fd0f2
ms.sourcegitcommit: eacd2a6e46c19dd3cd8519592b1668fabe14d85d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "49872735"
---
# <a name="delete-cloudpcprovisioningpolicy"></a><span data-ttu-id="9cbf4-103">删除 cloudPcProvisioningPolicy</span><span class="sxs-lookup"><span data-stu-id="9cbf4-103">Delete cloudPcProvisioningPolicy</span></span>

<span data-ttu-id="9cbf4-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="9cbf4-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="9cbf4-105">删除 [cloudPcProvisioningPolicy](../resources/cloudpcprovisioningpolicy.md) 对象。</span><span class="sxs-lookup"><span data-stu-id="9cbf4-105">Delete a [cloudPcProvisioningPolicy](../resources/cloudpcprovisioningpolicy.md) object.</span></span> <span data-ttu-id="9cbf4-106">无法删除使用中的策略。</span><span class="sxs-lookup"><span data-stu-id="9cbf4-106">You can’t delete a policy that’s in use.</span></span>

[!INCLUDE [cloudpc-api-preview](../../includes/cloudpc-api-preview.md)]
## <a name="permissions"></a><span data-ttu-id="9cbf4-107">权限</span><span class="sxs-lookup"><span data-stu-id="9cbf4-107">Permissions</span></span>

<span data-ttu-id="9cbf4-p102">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="9cbf4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9cbf4-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="9cbf4-110">Permission type</span></span>|<span data-ttu-id="9cbf4-111">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="9cbf4-111">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9cbf4-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="9cbf4-112">Delegated (work or school account)</span></span>|<span data-ttu-id="9cbf4-113">CloudPC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9cbf4-113">CloudPC.ReadWrite.All</span></span>|
|<span data-ttu-id="9cbf4-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="9cbf4-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9cbf4-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="9cbf4-115">Not supported.</span></span>|
|<span data-ttu-id="9cbf4-116">应用程序</span><span class="sxs-lookup"><span data-stu-id="9cbf4-116">Application</span></span>|<span data-ttu-id="9cbf4-117">不支持。</span><span class="sxs-lookup"><span data-stu-id="9cbf4-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9cbf4-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="9cbf4-118">HTTP request</span></span>

<!-- {
  "blockType": "ignored"
}
-->

``` http
DELETE /deviceManagement/virtualEndpoint/provisioningPolicies/{id}
```

## <a name="request-headers"></a><span data-ttu-id="9cbf4-119">请求标头</span><span class="sxs-lookup"><span data-stu-id="9cbf4-119">Request headers</span></span>

|<span data-ttu-id="9cbf4-120">名称</span><span class="sxs-lookup"><span data-stu-id="9cbf4-120">Name</span></span>|<span data-ttu-id="9cbf4-121">说明</span><span class="sxs-lookup"><span data-stu-id="9cbf4-121">Description</span></span>|
|:---|:---|
|<span data-ttu-id="9cbf4-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="9cbf4-122">Authorization</span></span>|<span data-ttu-id="9cbf4-p103">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="9cbf4-p103">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="9cbf4-125">请求正文</span><span class="sxs-lookup"><span data-stu-id="9cbf4-125">Request body</span></span>

<span data-ttu-id="9cbf4-126">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="9cbf4-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9cbf4-127">响应</span><span class="sxs-lookup"><span data-stu-id="9cbf4-127">Response</span></span>

<span data-ttu-id="9cbf4-128">如果成功，此方法返回 `204 No Content` 响应代码。</span><span class="sxs-lookup"><span data-stu-id="9cbf4-128">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="examples"></a><span data-ttu-id="9cbf4-129">示例</span><span class="sxs-lookup"><span data-stu-id="9cbf4-129">Examples</span></span>

### <a name="request"></a><span data-ttu-id="9cbf4-130">请求</span><span class="sxs-lookup"><span data-stu-id="9cbf4-130">Request</span></span>


# <a name="http"></a>[<span data-ttu-id="9cbf4-131">HTTP</span><span class="sxs-lookup"><span data-stu-id="9cbf4-131">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "delete_provisioningpolicies_from_virtualendpoint"
}
-->

``` http
DELETE https://graph.microsoft.com/beta/deviceManagement/virtualEndpoint/provisioningPolicies/{id}
```
# <a name="c"></a>[<span data-ttu-id="9cbf4-132">C#</span><span class="sxs-lookup"><span data-stu-id="9cbf4-132">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/delete-provisioningpolicies-from-virtualendpoint-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="9cbf4-133">JavaScript</span><span class="sxs-lookup"><span data-stu-id="9cbf4-133">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/delete-provisioningpolicies-from-virtualendpoint-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="9cbf4-134">Objective-C</span><span class="sxs-lookup"><span data-stu-id="9cbf4-134">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/delete-provisioningpolicies-from-virtualendpoint-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[<span data-ttu-id="9cbf4-135">Java</span><span class="sxs-lookup"><span data-stu-id="9cbf4-135">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/delete-provisioningpolicies-from-virtualendpoint-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


### <a name="response"></a><span data-ttu-id="9cbf4-136">响应</span><span class="sxs-lookup"><span data-stu-id="9cbf4-136">Response</span></span>

<span data-ttu-id="9cbf4-137">**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。</span><span class="sxs-lookup"><span data-stu-id="9cbf4-137">**Note:** The response object shown here might be shortened for readability.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
}
-->

``` http
HTTP/1.1 204 No Content
```
