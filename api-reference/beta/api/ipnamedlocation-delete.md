---
title: 删除 ipNamedLocation
description: 删除 ipNamedLocation 对象。
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: 34938db8172533bf23774b159f73aaf331d7ea0c
ms.sourcegitcommit: d189830649794365464e37539e02239f883011da
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/24/2019
ms.locfileid: "37653704"
---
# <a name="delete-ipnamedlocation"></a><span data-ttu-id="4b714-103">删除 ipNamedLocation</span><span class="sxs-lookup"><span data-stu-id="4b714-103">Delete ipNamedLocation</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="4b714-104">删除[ipNamedLocation](../resources/ipNamedLocation.md)对象。</span><span class="sxs-lookup"><span data-stu-id="4b714-104">Delete an [ipNamedLocation](../resources/ipNamedLocation.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="4b714-105">权限</span><span class="sxs-lookup"><span data-stu-id="4b714-105">Permissions</span></span>

<span data-ttu-id="4b714-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="4b714-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="4b714-108">权限类型</span><span class="sxs-lookup"><span data-stu-id="4b714-108">Permission type</span></span>                        | <span data-ttu-id="4b714-109">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="4b714-109">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="4b714-110">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="4b714-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="4b714-111">ConditionalAccess 和 Directory.accessasuser.all 的所有</span><span class="sxs-lookup"><span data-stu-id="4b714-111">Policy.ReadWrite.ConditionalAccess and Directory.AccessAsUser.All</span></span> |
| <span data-ttu-id="4b714-112">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="4b714-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4b714-113">不支持。</span><span class="sxs-lookup"><span data-stu-id="4b714-113">Not supported.</span></span> |
| <span data-ttu-id="4b714-114">应用程序</span><span class="sxs-lookup"><span data-stu-id="4b714-114">Application</span></span>                            | <span data-ttu-id="4b714-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="4b714-115">Not supported.</span></span> |

>[!NOTE]
><span data-ttu-id="4b714-116">此 API 需要多个权限。</span><span class="sxs-lookup"><span data-stu-id="4b714-116">This API requires multiple permissions.</span></span> <span data-ttu-id="4b714-117">有关详细信息，请参阅[已知问题](/graph/known-issues#conditional-access-policies-and-named-locations)。</span><span class="sxs-lookup"><span data-stu-id="4b714-117">For details, see [Known issues](/graph/known-issues#conditional-access-policies-and-named-locations).</span></span>

## <a name="http-request"></a><span data-ttu-id="4b714-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="4b714-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /conditionalAccess/namedLocations/{id}
```

## <a name="request-headers"></a><span data-ttu-id="4b714-119">请求标头</span><span class="sxs-lookup"><span data-stu-id="4b714-119">Request headers</span></span>

| <span data-ttu-id="4b714-120">名称</span><span class="sxs-lookup"><span data-stu-id="4b714-120">Name</span></span>          | <span data-ttu-id="4b714-121">说明</span><span class="sxs-lookup"><span data-stu-id="4b714-121">Description</span></span>   |
|:--------------|:--------------|
| <span data-ttu-id="4b714-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="4b714-122">Authorization</span></span> | <span data-ttu-id="4b714-p103">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="4b714-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4b714-125">请求正文</span><span class="sxs-lookup"><span data-stu-id="4b714-125">Request body</span></span>

<span data-ttu-id="4b714-126">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="4b714-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4b714-127">响应</span><span class="sxs-lookup"><span data-stu-id="4b714-127">Response</span></span>

<span data-ttu-id="4b714-p104">如果成功，此方法返回 `204 No Content` 响应代码。它不在响应正文中返回任何内容。</span><span class="sxs-lookup"><span data-stu-id="4b714-p104">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="4b714-130">示例</span><span class="sxs-lookup"><span data-stu-id="4b714-130">Examples</span></span>

### <a name="request"></a><span data-ttu-id="4b714-131">请求</span><span class="sxs-lookup"><span data-stu-id="4b714-131">Request</span></span>

<span data-ttu-id="4b714-132">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="4b714-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_ipnamedlocation"
}-->

```http
DELETE https://graph.microsoft.com/beta/conditionalAccess/namedLocations/0854951d-5fc0-4eb1-b392-9b2c9d7949c2
```

### <a name="response"></a><span data-ttu-id="4b714-133">响应</span><span class="sxs-lookup"><span data-stu-id="4b714-133">Response</span></span>

<span data-ttu-id="4b714-134">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="4b714-134">The following is an example of the response.</span></span>

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
  "description": "Delete ipNamedLocation",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->