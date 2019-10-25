---
title: 获取 ipNamedLocation
description: 检索 ipnamedlocation 对象的属性和关系。
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: b9aeb1bd07c465e73f55cf95fef71a80c8f5bb8f
ms.sourcegitcommit: d189830649794365464e37539e02239f883011da
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/24/2019
ms.locfileid: "37653711"
---
# <a name="get-ipnamedlocation"></a><span data-ttu-id="ffaa6-103">获取 ipNamedLocation</span><span class="sxs-lookup"><span data-stu-id="ffaa6-103">Get ipNamedLocation</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="ffaa6-104">检索[ipNamedLocation](../resources/ipNamedLocation.md)对象的属性和关系。</span><span class="sxs-lookup"><span data-stu-id="ffaa6-104">Retrieve the properties and relationships of an [ipNamedLocation](../resources/ipNamedLocation.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="ffaa6-105">权限</span><span class="sxs-lookup"><span data-stu-id="ffaa6-105">Permissions</span></span>

<span data-ttu-id="ffaa6-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="ffaa6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="ffaa6-108">权限类型</span><span class="sxs-lookup"><span data-stu-id="ffaa6-108">Permission type</span></span>                        | <span data-ttu-id="ffaa6-109">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="ffaa6-109">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="ffaa6-110">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="ffaa6-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="ffaa6-111">Policy.Read.All</span><span class="sxs-lookup"><span data-stu-id="ffaa6-111">Policy.Read.All</span></span> |
| <span data-ttu-id="ffaa6-112">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="ffaa6-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ffaa6-113">不支持。</span><span class="sxs-lookup"><span data-stu-id="ffaa6-113">Not supported.</span></span> |
| <span data-ttu-id="ffaa6-114">应用程序</span><span class="sxs-lookup"><span data-stu-id="ffaa6-114">Application</span></span>                            | <span data-ttu-id="ffaa6-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="ffaa6-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="ffaa6-116">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="ffaa6-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /conditionalAccess/namedLocations/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="ffaa6-117">可选的查询参数</span><span class="sxs-lookup"><span data-stu-id="ffaa6-117">Optional query parameters</span></span>

<span data-ttu-id="ffaa6-118">此方法支持`select` OData 查询参数来帮助自定义响应。</span><span class="sxs-lookup"><span data-stu-id="ffaa6-118">This method supports the `select` OData query parameter to help customize the response.</span></span> <span data-ttu-id="ffaa6-119">有关一般信息，请参阅[OData 查询参数](/graph/query-parameters)。</span><span class="sxs-lookup"><span data-stu-id="ffaa6-119">For general information, see [OData query parameters](/graph/query-parameters).</span></span>

## <a name="request-headers"></a><span data-ttu-id="ffaa6-120">请求头</span><span class="sxs-lookup"><span data-stu-id="ffaa6-120">Request headers</span></span>

| <span data-ttu-id="ffaa6-121">名称</span><span class="sxs-lookup"><span data-stu-id="ffaa6-121">Name</span></span>      |<span data-ttu-id="ffaa6-122">说明</span><span class="sxs-lookup"><span data-stu-id="ffaa6-122">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="ffaa6-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="ffaa6-123">Authorization</span></span> | <span data-ttu-id="ffaa6-p103">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="ffaa6-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ffaa6-126">请求正文</span><span class="sxs-lookup"><span data-stu-id="ffaa6-126">Request body</span></span>

<span data-ttu-id="ffaa6-127">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="ffaa6-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ffaa6-128">响应</span><span class="sxs-lookup"><span data-stu-id="ffaa6-128">Response</span></span>

<span data-ttu-id="ffaa6-129">如果成功，此方法在响应`200 OK`正文中返回响应代码和请求的[ipNamedLocation](../resources/ipnamedlocation.md)对象。</span><span class="sxs-lookup"><span data-stu-id="ffaa6-129">If successful, this method returns a `200 OK` response code and the requested [ipNamedLocation](../resources/ipnamedlocation.md) object in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="ffaa6-130">示例</span><span class="sxs-lookup"><span data-stu-id="ffaa6-130">Examples</span></span>

### <a name="request"></a><span data-ttu-id="ffaa6-131">请求</span><span class="sxs-lookup"><span data-stu-id="ffaa6-131">Request</span></span>

<span data-ttu-id="ffaa6-132">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="ffaa6-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_ipnamedlocation"
}-->

```http
GET https://graph.microsoft.com/beta/conditionalAccess/namedLocations/0854951d-5fc0-4eb1-b392-9b2c9d7949c2
```

### <a name="response"></a><span data-ttu-id="ffaa6-133">响应</span><span class="sxs-lookup"><span data-stu-id="ffaa6-133">Response</span></span>

<span data-ttu-id="ffaa6-134">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="ffaa6-134">The following is an example of the response.</span></span>

> <span data-ttu-id="ffaa6-p104">**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。所有属性都将通过实际调用返回。</span><span class="sxs-lookup"><span data-stu-id="ffaa6-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.ipNamedLocation"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#namedLocations/$entity",
    "@odata.type": "#microsoft.graph.ipNamedLocation",
    "id": "0854951d-5fc0-4eb1-b392-9b2c9d7949c2",
    "displayName": "Untrusted IP named location",
    "modifiedDateTime": "2019-09-04T01:11:34.9387578Z",
    "createdDateTime": "2019-09-04T01:11:34.9387578Z",
    "isTrusted": false,
    "ipRanges": [
        {
            "@odata.type": "#microsoft.graph.iPv4CidrRange",
            "cidrAddress": "12.34.221.11/22"
        },
        {
            "@odata.type": "#microsoft.graph.iPv6CidrRange",
            "cidrAddress": "2001:0:9d38:90d6:0:0:0:0/63"
        }
    ]
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get ipNamedLocation",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->