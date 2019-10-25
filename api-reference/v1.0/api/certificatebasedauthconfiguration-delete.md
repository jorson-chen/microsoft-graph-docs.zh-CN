---
title: 删除 certificateBasedAuthConfiguration
description: 删除 certificateBasedAuthConfiguration。
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: 113823fcb19014255b8334fb88f6a9f897eace8b
ms.sourcegitcommit: c9b9ff2c862f8d96d282a7bdf641cdb9c53a4600
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/22/2019
ms.locfileid: "37632558"
---
# <a name="delete-certificatebasedauthconfiguration"></a><span data-ttu-id="01d13-103">删除 certificateBasedAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="01d13-103">Delete certificateBasedAuthConfiguration</span></span>

<span data-ttu-id="01d13-104">删除[certificateBasedAuthConfiguration](../resources/certificateBasedAuthConfiguration.md)对象。</span><span class="sxs-lookup"><span data-stu-id="01d13-104">Delete a [certificateBasedAuthConfiguration](../resources/certificateBasedAuthConfiguration.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="01d13-105">权限</span><span class="sxs-lookup"><span data-stu-id="01d13-105">Permissions</span></span>

<span data-ttu-id="01d13-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="01d13-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="01d13-108">权限类型</span><span class="sxs-lookup"><span data-stu-id="01d13-108">Permission type</span></span>                        | <span data-ttu-id="01d13-109">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="01d13-109">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="01d13-110">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="01d13-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="01d13-111">Organization.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="01d13-111">Organization.ReadWrite.All</span></span> |
| <span data-ttu-id="01d13-112">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="01d13-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="01d13-113">不支持。</span><span class="sxs-lookup"><span data-stu-id="01d13-113">Not supported.</span></span> |
| <span data-ttu-id="01d13-114">应用程序</span><span class="sxs-lookup"><span data-stu-id="01d13-114">Application</span></span>    | <span data-ttu-id="01d13-115">Organization.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="01d13-115">Organization.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="01d13-116">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="01d13-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /organization/{id}/certificateBasedAuthConfiguration/{id}
```

## <a name="request-headers"></a><span data-ttu-id="01d13-117">请求标头</span><span class="sxs-lookup"><span data-stu-id="01d13-117">Request headers</span></span>

| <span data-ttu-id="01d13-118">名称</span><span class="sxs-lookup"><span data-stu-id="01d13-118">Name</span></span>          | <span data-ttu-id="01d13-119">说明</span><span class="sxs-lookup"><span data-stu-id="01d13-119">Description</span></span>   |
|:--------------|:--------------|
| <span data-ttu-id="01d13-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="01d13-120">Authorization</span></span> | <span data-ttu-id="01d13-p102">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="01d13-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="01d13-123">请求正文</span><span class="sxs-lookup"><span data-stu-id="01d13-123">Request body</span></span>

<span data-ttu-id="01d13-124">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="01d13-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="01d13-125">响应</span><span class="sxs-lookup"><span data-stu-id="01d13-125">Response</span></span>

<span data-ttu-id="01d13-p103">如果成功，此方法返回 `204 No Content` 响应代码。它不在响应正文中返回任何内容。</span><span class="sxs-lookup"><span data-stu-id="01d13-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="01d13-128">示例</span><span class="sxs-lookup"><span data-stu-id="01d13-128">Examples</span></span>

### <a name="request"></a><span data-ttu-id="01d13-129">请求</span><span class="sxs-lookup"><span data-stu-id="01d13-129">Request</span></span>

<span data-ttu-id="01d13-130">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="01d13-130">The following is an example of the request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="01d13-131">HTTP</span><span class="sxs-lookup"><span data-stu-id="01d13-131">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "delete_certificatebasedauthconfiguration"
}-->

```http
DELETE https://graph.microsoft.com/v1.0/organization/{id}/certificateBasedAuthConfiguration/{id}
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="01d13-132">C#</span><span class="sxs-lookup"><span data-stu-id="01d13-132">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/delete-certificatebasedauthconfiguration-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="01d13-133">JavaScript</span><span class="sxs-lookup"><span data-stu-id="01d13-133">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/delete-certificatebasedauthconfiguration-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="01d13-134">Objective-C</span><span class="sxs-lookup"><span data-stu-id="01d13-134">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/delete-certificatebasedauthconfiguration-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="01d13-135">Java</span><span class="sxs-lookup"><span data-stu-id="01d13-135">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/delete-certificatebasedauthconfiguration-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


### <a name="response"></a><span data-ttu-id="01d13-136">响应</span><span class="sxs-lookup"><span data-stu-id="01d13-136">Response</span></span>

<span data-ttu-id="01d13-137">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="01d13-137">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true
} -->

```http
HTTP/1.1 204 No Content
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete certificateBasedAuthConfiguration",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->