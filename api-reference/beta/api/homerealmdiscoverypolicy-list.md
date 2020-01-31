---
title: 列出 homeRealmDiscoveryPolicies
description: 获取 homeRealmDiscoveryPolicy 对象的列表。
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: 34fc65cecaaef50be3eccf129f3a9e86fa0f4694
ms.sourcegitcommit: 0536ab327c8b8bf215b726e0d4c25e8f6e8996f9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/18/2020
ms.locfileid: "41234172"
---
# <a name="list-homerealmdiscoverypolicies"></a><span data-ttu-id="93362-103">列出 homeRealmDiscoveryPolicies</span><span class="sxs-lookup"><span data-stu-id="93362-103">List homeRealmDiscoveryPolicies</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="93362-104">获取[homeRealmDiscoveryPolicy](../resources/homerealmdiscoverypolicy.md)对象的列表。</span><span class="sxs-lookup"><span data-stu-id="93362-104">Get a list of [homeRealmDiscoveryPolicy](../resources/homerealmdiscoverypolicy.md) objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="93362-105">Permissions</span><span class="sxs-lookup"><span data-stu-id="93362-105">Permissions</span></span>

<span data-ttu-id="93362-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="93362-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="93362-108">权限类型</span><span class="sxs-lookup"><span data-stu-id="93362-108">Permission type</span></span>                        | <span data-ttu-id="93362-109">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="93362-109">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="93362-110">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="93362-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="93362-111">Policy.Read.All</span><span class="sxs-lookup"><span data-stu-id="93362-111">Policy.Read.All</span></span> |
| <span data-ttu-id="93362-112">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="93362-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="93362-113">不支持。</span><span class="sxs-lookup"><span data-stu-id="93362-113">Not supported.</span></span> |
| <span data-ttu-id="93362-114">应用程序</span><span class="sxs-lookup"><span data-stu-id="93362-114">Application</span></span>                            | <span data-ttu-id="93362-115">Policy.Read.All</span><span class="sxs-lookup"><span data-stu-id="93362-115">Policy.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="93362-116">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="93362-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET policies/homeRealmDiscoveryPolicies
```

## <a name="optional-query-parameters"></a><span data-ttu-id="93362-117">可选的查询参数</span><span class="sxs-lookup"><span data-stu-id="93362-117">Optional query parameters</span></span>

<span data-ttu-id="93362-118">`$expand`此方法支持`$filter`、 `$select`和`$top` OData 查询参数来帮助自定义响应。</span><span class="sxs-lookup"><span data-stu-id="93362-118">This method supports the `$expand`, `$filter`, `$select` and `$top` OData query parameters to help customize the response.</span></span> <span data-ttu-id="93362-119">有关一般信息，请参阅[OData 查询参数](/graph/query-parameters)。</span><span class="sxs-lookup"><span data-stu-id="93362-119">For general information, see [OData query parameters](/graph/query-parameters).</span></span> <span data-ttu-id="93362-120">使用`$expand`时，请确保您的应用程序请求读取扩展的对象的权限。</span><span class="sxs-lookup"><span data-stu-id="93362-120">When using `$expand` make sure your app requests permissions to read the expanded objects.</span></span>

## <a name="request-headers"></a><span data-ttu-id="93362-121">请求头</span><span class="sxs-lookup"><span data-stu-id="93362-121">Request headers</span></span>

| <span data-ttu-id="93362-122">名称</span><span class="sxs-lookup"><span data-stu-id="93362-122">Name</span></span>      |<span data-ttu-id="93362-123">说明</span><span class="sxs-lookup"><span data-stu-id="93362-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="93362-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="93362-124">Authorization</span></span> | <span data-ttu-id="93362-125">持有者 {token}</span><span class="sxs-lookup"><span data-stu-id="93362-125">Bearer {token}</span></span> |

## <a name="request-body"></a><span data-ttu-id="93362-126">请求正文</span><span class="sxs-lookup"><span data-stu-id="93362-126">Request body</span></span>

<span data-ttu-id="93362-127">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="93362-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="93362-128">响应</span><span class="sxs-lookup"><span data-stu-id="93362-128">Response</span></span>

<span data-ttu-id="93362-129">如果成功，此方法在响应`200 OK`正文中返回响应代码和[homeRealmDiscoveryPolicy](../resources/homerealmdiscoverypolicy.md)对象集合。</span><span class="sxs-lookup"><span data-stu-id="93362-129">If successful, this method returns a `200 OK` response code and a collection of [homeRealmDiscoveryPolicy](../resources/homerealmdiscoverypolicy.md) objects in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="93362-130">示例</span><span class="sxs-lookup"><span data-stu-id="93362-130">Examples</span></span>

### <a name="request"></a><span data-ttu-id="93362-131">请求</span><span class="sxs-lookup"><span data-stu-id="93362-131">Request</span></span>

<span data-ttu-id="93362-132">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="93362-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_homerealmdiscoverypolicies"
}-->

```http
GET https://graph.microsoft.com/beta/policies/homeRealmDiscoveryPolicies
```

### <a name="response"></a><span data-ttu-id="93362-133">响应</span><span class="sxs-lookup"><span data-stu-id="93362-133">Response</span></span>

<span data-ttu-id="93362-134">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="93362-134">The following is an example of the response.</span></span>

> <span data-ttu-id="93362-p103">**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。所有属性都将通过实际调用返回。</span><span class="sxs-lookup"><span data-stu-id="93362-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.homeRealmDiscoveryPolicy",
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
  "description": "List homeRealmDiscoveryPolicies",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->