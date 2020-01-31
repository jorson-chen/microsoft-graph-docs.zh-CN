---
title: 列表已分配 tokenLifetimePolicies
description: 列出分配给应用程序或 servicePrincipal 的 tokenLifetimePolicies。
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: 4ffd3395b362a1ecee61005a7663b09793e50f63
ms.sourcegitcommit: 0536ab327c8b8bf215b726e0d4c25e8f6e8996f9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/18/2020
ms.locfileid: "41234140"
---
# <a name="list-assigned-tokenlifetimepolicy"></a><span data-ttu-id="0219c-103">列表已分配 tokenLifetimePolicy</span><span class="sxs-lookup"><span data-stu-id="0219c-103">List assigned tokenLifetimePolicy</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="0219c-104">列出分配给[应用程序](../resources/application.md)或[servicePrincipal](../resources/servicePrincipal.md)的[tokenLifetimePolicy](../resources/tokenlifetimepolicy.md)对象。。</span><span class="sxs-lookup"><span data-stu-id="0219c-104">List the [tokenLifetimePolicy](../resources/tokenlifetimepolicy.md) objects that are assigned to an [application](../resources/application.md) or [servicePrincipal](../resources/servicePrincipal.md)..</span></span>

## <a name="permissions"></a><span data-ttu-id="0219c-105">Permissions</span><span class="sxs-lookup"><span data-stu-id="0219c-105">Permissions</span></span>

<span data-ttu-id="0219c-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="0219c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="0219c-108">权限类型</span><span class="sxs-lookup"><span data-stu-id="0219c-108">Permission type</span></span>                        | <span data-ttu-id="0219c-109">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="0219c-109">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="0219c-110">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="0219c-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="0219c-111">Policy. All 和 Application。所有读写。</span><span class="sxs-lookup"><span data-stu-id="0219c-111">Policy.Read.All and Application.ReadWrite.All</span></span> |
| <span data-ttu-id="0219c-112">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="0219c-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0219c-113">不支持。</span><span class="sxs-lookup"><span data-stu-id="0219c-113">Not supported.</span></span> |
| <span data-ttu-id="0219c-114">应用程序</span><span class="sxs-lookup"><span data-stu-id="0219c-114">Application</span></span>                            | <span data-ttu-id="0219c-115">Policy. All 和 Application.readwrite.ownedby，all 和应用程序的 Read. all</span><span class="sxs-lookup"><span data-stu-id="0219c-115">Policy.Read.All and Application.ReadWrite.OwnedBy, Policy.Read.All and Application.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="0219c-116">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="0219c-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /applications/{id}/tokenLifetimePolicies
GET /servicePrincipals/{id}/tokenLifetimePolicies
```

## <a name="request-headers"></a><span data-ttu-id="0219c-117">请求标头</span><span class="sxs-lookup"><span data-stu-id="0219c-117">Request headers</span></span>

| <span data-ttu-id="0219c-118">名称</span><span class="sxs-lookup"><span data-stu-id="0219c-118">Name</span></span>          | <span data-ttu-id="0219c-119">说明</span><span class="sxs-lookup"><span data-stu-id="0219c-119">Description</span></span>   |
|:--------------|:--------------|
| <span data-ttu-id="0219c-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="0219c-120">Authorization</span></span> | <span data-ttu-id="0219c-121">持有者 {token}</span><span class="sxs-lookup"><span data-stu-id="0219c-121">Bearer {token}</span></span> |

## <a name="request-body"></a><span data-ttu-id="0219c-122">请求正文</span><span class="sxs-lookup"><span data-stu-id="0219c-122">Request body</span></span>

<span data-ttu-id="0219c-123">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="0219c-123">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0219c-124">响应</span><span class="sxs-lookup"><span data-stu-id="0219c-124">Response</span></span>

<span data-ttu-id="0219c-125">如果成功，此方法在响应`200 OK`正文中返回响应代码和[tokenLifetimePolicy](../resources/tokenLifetimePolicy.md)对象集合。</span><span class="sxs-lookup"><span data-stu-id="0219c-125">If successful, this method returns a `200 OK` response code and a collection of [tokenLifetimePolicy](../resources/tokenLifetimePolicy.md) objects in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="0219c-126">示例</span><span class="sxs-lookup"><span data-stu-id="0219c-126">Examples</span></span>

### <a name="request"></a><span data-ttu-id="0219c-127">请求</span><span class="sxs-lookup"><span data-stu-id="0219c-127">Request</span></span>

<span data-ttu-id="0219c-128">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="0219c-128">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "list_tokenlifetimepolicies_on_application"
}-->

```http
GET https://graph.microsoft.com/beta/applications/{id}/tokenLifetimePolicies
```

### <a name="response"></a><span data-ttu-id="0219c-129">响应</span><span class="sxs-lookup"><span data-stu-id="0219c-129">Response</span></span>

<span data-ttu-id="0219c-130">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="0219c-130">The following is an example of the response.</span></span>

> <span data-ttu-id="0219c-p102">**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。所有属性都将通过实际调用返回。</span><span class="sxs-lookup"><span data-stu-id="0219c-p102">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.tokenLifetimePolicy",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "definition": [
        "definition-value"
      ],
      "displayName": "displayName-value",
      "isOrganizationDefault": true,
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List assigned tokenLifetimePolicy",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->