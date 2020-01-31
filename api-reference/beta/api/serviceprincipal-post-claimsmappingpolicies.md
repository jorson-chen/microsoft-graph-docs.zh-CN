---
title: 分配 claimsMappingPolicy
description: 将 claimsMappingPolicy 分配给服务主体。
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: ce7a1af7b058aa25fbeaad3df21fb8f4ed735046
ms.sourcegitcommit: 0536ab327c8b8bf215b726e0d4c25e8f6e8996f9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/18/2020
ms.locfileid: "41234175"
---
# <a name="assign-claimsmappingpolicy"></a><span data-ttu-id="87c3f-103">分配 claimsMappingPolicy</span><span class="sxs-lookup"><span data-stu-id="87c3f-103">Assign claimsMappingPolicy</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="87c3f-104">将[claimsMappingPolicy](../resources/claimsmappingpolicy.md)分配给[servicePrincipal](../resources/servicePrincipal.md)。</span><span class="sxs-lookup"><span data-stu-id="87c3f-104">Assign a [claimsMappingPolicy](../resources/claimsmappingpolicy.md) to a [servicePrincipal](../resources/servicePrincipal.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="87c3f-105">Permissions</span><span class="sxs-lookup"><span data-stu-id="87c3f-105">Permissions</span></span>

<span data-ttu-id="87c3f-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="87c3f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="87c3f-108">权限类型</span><span class="sxs-lookup"><span data-stu-id="87c3f-108">Permission type</span></span>                        | <span data-ttu-id="87c3f-109">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="87c3f-109">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="87c3f-110">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="87c3f-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="87c3f-111">Policy. All 和 Application。所有读写。</span><span class="sxs-lookup"><span data-stu-id="87c3f-111">Policy.Read.All and Application.ReadWrite.All</span></span> |
| <span data-ttu-id="87c3f-112">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="87c3f-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="87c3f-113">不支持。</span><span class="sxs-lookup"><span data-stu-id="87c3f-113">Not supported.</span></span> |
| <span data-ttu-id="87c3f-114">应用程序</span><span class="sxs-lookup"><span data-stu-id="87c3f-114">Application</span></span>                            | <span data-ttu-id="87c3f-115">Policy. All 和 Application.readwrite.ownedby，all 和应用程序的 Read. all</span><span class="sxs-lookup"><span data-stu-id="87c3f-115">Policy.Read.All and Application.ReadWrite.OwnedBy, Policy.Read.All and Application.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="87c3f-116">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="87c3f-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /servicePrincipals/{id}/claimsMappingPolicies/$ref
```

## <a name="request-headers"></a><span data-ttu-id="87c3f-117">请求标头</span><span class="sxs-lookup"><span data-stu-id="87c3f-117">Request headers</span></span>

| <span data-ttu-id="87c3f-118">名称</span><span class="sxs-lookup"><span data-stu-id="87c3f-118">Name</span></span>          | <span data-ttu-id="87c3f-119">说明</span><span class="sxs-lookup"><span data-stu-id="87c3f-119">Description</span></span>   |
|:--------------|:--------------|
| <span data-ttu-id="87c3f-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="87c3f-120">Authorization</span></span> | <span data-ttu-id="87c3f-121">持有者 {token}</span><span class="sxs-lookup"><span data-stu-id="87c3f-121">Bearer {token}</span></span> |
| <span data-ttu-id="87c3f-122">Content-Type</span><span class="sxs-lookup"><span data-stu-id="87c3f-122">Content-Type</span></span> | <span data-ttu-id="87c3f-123">application/json</span><span class="sxs-lookup"><span data-stu-id="87c3f-123">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="87c3f-124">请求正文</span><span class="sxs-lookup"><span data-stu-id="87c3f-124">Request body</span></span>

<span data-ttu-id="87c3f-125">在请求正文中，提供应分配给服务主体的[claimsMappingPolicy](../resources/claimsmappingpolicy.md)对象的`@odata.id`标识符（使用属性）。</span><span class="sxs-lookup"><span data-stu-id="87c3f-125">In the request body, supply the identifier of the [claimsMappingPolicy](../resources/claimsmappingpolicy.md) object (using an `@odata.id` property) that should be assigned to the service principal.</span></span>

## <a name="response"></a><span data-ttu-id="87c3f-126">响应</span><span class="sxs-lookup"><span data-stu-id="87c3f-126">Response</span></span>

<span data-ttu-id="87c3f-p102">如果成功，此方法返回 `204 No Content` 响应代码。它不在响应正文中返回任何内容。</span><span class="sxs-lookup"><span data-stu-id="87c3f-p102">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="87c3f-129">示例</span><span class="sxs-lookup"><span data-stu-id="87c3f-129">Examples</span></span>

### <a name="request"></a><span data-ttu-id="87c3f-130">请求</span><span class="sxs-lookup"><span data-stu-id="87c3f-130">Request</span></span>

<span data-ttu-id="87c3f-131">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="87c3f-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_claimsmappingpolicy_from_serviceprincipal"
}-->

```http
POST https://graph.microsoft.com/beta/servicePrincipals/{id}/claimsMappingPolicies
Content-Type: application/json

{
  "@odata.id":"https://graph.microsoft.com/beta/policies/claimsMappingPolicies/cd3d9b57-0aee-4f25-8ee3-ac74ef5986a9"
}
```

### <a name="response"></a><span data-ttu-id="87c3f-132">响应</span><span class="sxs-lookup"><span data-stu-id="87c3f-132">Response</span></span>

<span data-ttu-id="87c3f-133">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="87c3f-133">The following is an example of the response.</span></span>

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
  "description": "Assign claimsMappingPolicy",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->