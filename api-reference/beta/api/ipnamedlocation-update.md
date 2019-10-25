---
title: 更新 ipnamedlocation
description: 更新 ipNamedLocation 对象的属性。
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: e9b1dfbe84124c6f6049260732bf254e98682870
ms.sourcegitcommit: d189830649794365464e37539e02239f883011da
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/24/2019
ms.locfileid: "37653718"
---
# <a name="update-ipnamedlocation"></a><span data-ttu-id="58776-103">更新 ipNamedlocation</span><span class="sxs-lookup"><span data-stu-id="58776-103">Update ipNamedlocation</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="58776-104">更新[ipNamedLocation](../resources/ipNamedLocation.md)对象的属性。</span><span class="sxs-lookup"><span data-stu-id="58776-104">Update the properties of an [ipNamedLocation](../resources/ipNamedLocation.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="58776-105">权限</span><span class="sxs-lookup"><span data-stu-id="58776-105">Permissions</span></span>

<span data-ttu-id="58776-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="58776-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="58776-108">权限类型</span><span class="sxs-lookup"><span data-stu-id="58776-108">Permission type</span></span>                        | <span data-ttu-id="58776-109">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="58776-109">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="58776-110">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="58776-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="58776-111">ConditionalAccess 和 Directory.accessasuser.all 的所有</span><span class="sxs-lookup"><span data-stu-id="58776-111">Policy.ReadWrite.ConditionalAccess and Directory.AccessAsUser.All</span></span> |
| <span data-ttu-id="58776-112">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="58776-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="58776-113">不支持。</span><span class="sxs-lookup"><span data-stu-id="58776-113">Not supported.</span></span> |
| <span data-ttu-id="58776-114">应用程序</span><span class="sxs-lookup"><span data-stu-id="58776-114">Application</span></span>                            | <span data-ttu-id="58776-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="58776-115">Not supported.</span></span> |

>[!NOTE]
><span data-ttu-id="58776-116">此 API 需要多个权限。</span><span class="sxs-lookup"><span data-stu-id="58776-116">This API requires multiple permissions.</span></span> <span data-ttu-id="58776-117">有关详细信息，请参阅[已知问题](/graph/known-issues#conditional-access-policies-and-named-locations)。</span><span class="sxs-lookup"><span data-stu-id="58776-117">For details, see [Known issues](/graph/known-issues#conditional-access-policies-and-named-locations).</span></span>

## <a name="http-request"></a><span data-ttu-id="58776-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="58776-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PATCH /conditionalAccess/namedLocations/{id}
```

## <a name="request-headers"></a><span data-ttu-id="58776-119">请求标头</span><span class="sxs-lookup"><span data-stu-id="58776-119">Request headers</span></span>

| <span data-ttu-id="58776-120">名称</span><span class="sxs-lookup"><span data-stu-id="58776-120">Name</span></span>       | <span data-ttu-id="58776-121">说明</span><span class="sxs-lookup"><span data-stu-id="58776-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="58776-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="58776-122">Authorization</span></span> | <span data-ttu-id="58776-p103">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="58776-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="58776-125">Content-type</span><span class="sxs-lookup"><span data-stu-id="58776-125">Content-type</span></span> | <span data-ttu-id="58776-p104">application/json. Required.</span><span class="sxs-lookup"><span data-stu-id="58776-p104">application/json. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="58776-128">请求正文</span><span class="sxs-lookup"><span data-stu-id="58776-128">Request body</span></span>

<span data-ttu-id="58776-129">在请求正文中，提供应更新的相关字段的值。</span><span class="sxs-lookup"><span data-stu-id="58776-129">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="58776-130">请求正文中不包括的现有属性将保留其以前的值，或根据对其他属性值的更改重新计算。</span><span class="sxs-lookup"><span data-stu-id="58776-130">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="58776-131">为了获得最佳性能，请勿加入尚未更改的现有值。</span><span class="sxs-lookup"><span data-stu-id="58776-131">For best performance, don't include existing values that haven't changed.</span></span>

| <span data-ttu-id="58776-132">属性</span><span class="sxs-lookup"><span data-stu-id="58776-132">Property</span></span>     | <span data-ttu-id="58776-133">类型</span><span class="sxs-lookup"><span data-stu-id="58776-133">Type</span></span>        | <span data-ttu-id="58776-134">说明</span><span class="sxs-lookup"><span data-stu-id="58776-134">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="58776-135">displayName</span><span class="sxs-lookup"><span data-stu-id="58776-135">displayName</span></span>|<span data-ttu-id="58776-136">String</span><span class="sxs-lookup"><span data-stu-id="58776-136">String</span></span>|<span data-ttu-id="58776-137">位置的人可读名称。</span><span class="sxs-lookup"><span data-stu-id="58776-137">Human-readable name of the location.</span></span>|
|<span data-ttu-id="58776-138">ipRanges</span><span class="sxs-lookup"><span data-stu-id="58776-138">ipRanges</span></span>|<span data-ttu-id="58776-139">[ipRange](../resources/iprange.md) 集合</span><span class="sxs-lookup"><span data-stu-id="58776-139">[ipRange](../resources/iprange.md) collection</span></span>|<span data-ttu-id="58776-140">来自 IETF RFC5962 的 IPv4 CIDR 格式（1.2.3.4/32）或任何允许的 IPv6 格式的 IP 地址范围列表。</span><span class="sxs-lookup"><span data-stu-id="58776-140">List of IP address ranges in IPv4 CIDR format (1.2.3.4/32) or any allowable IPv6 format from IETF RFC5962.</span></span>|
|<span data-ttu-id="58776-141">isTrusted</span><span class="sxs-lookup"><span data-stu-id="58776-141">isTrusted</span></span>|<span data-ttu-id="58776-142">Boolean</span><span class="sxs-lookup"><span data-stu-id="58776-142">Boolean</span></span>|<span data-ttu-id="58776-143">如果此位置`true`是明确信任的，则该值为。</span><span class="sxs-lookup"><span data-stu-id="58776-143">The value is `true` if this location is explicitly trusted.</span></span>|

## <a name="response"></a><span data-ttu-id="58776-144">响应</span><span class="sxs-lookup"><span data-stu-id="58776-144">Response</span></span>

<span data-ttu-id="58776-p106">如果成功，此方法返回 `204 No Content` 响应代码。它不在响应正文中返回任何内容。</span><span class="sxs-lookup"><span data-stu-id="58776-p106">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="58776-147">示例</span><span class="sxs-lookup"><span data-stu-id="58776-147">Examples</span></span>

### <a name="request"></a><span data-ttu-id="58776-148">请求</span><span class="sxs-lookup"><span data-stu-id="58776-148">Request</span></span>

<span data-ttu-id="58776-149">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="58776-149">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_ipnamedlocation"
}-->

```http
PATCH https://graph.microsoft.com/beta/conditionalAccess/namedLocations/0854951d-5fc0-4eb1-b392-9b2c9d7949c2
Content-type: application/json

{
    "@odata.type": "#microsoft.graph.ipNamedLocation",
    "displayName": "Untrusted named location with only IPv4 address",
    "isTrusted": false,
    "ipRanges": [
        {
            "@odata.type": "#microsoft.graph.iPv4CidrRange",
            "cidrAddress": "6.5.4.3/18"
        }

    ]
}
```

### <a name="response"></a><span data-ttu-id="58776-150">响应</span><span class="sxs-lookup"><span data-stu-id="58776-150">Response</span></span>

<span data-ttu-id="58776-151">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="58776-151">The following is an example of the response.</span></span>

> <span data-ttu-id="58776-p107">**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。所有属性都将通过实际调用返回。</span><span class="sxs-lookup"><span data-stu-id="58776-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.ipNamedLocation"
} -->

```http
HTTP/1.1 204 No Content
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update ipnamedlocation",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->