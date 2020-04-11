---
title: 更新 activitybasedtimeoutpolicy
description: 更新 activityBasedTimeoutPolicy 对象的属性。
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: c3043d7248002492b0a8b81a080e75b079461b33
ms.sourcegitcommit: 9a6ce4ddf75beead19b7c35a1949cf4d105b9b29
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/11/2020
ms.locfileid: "43229115"
---
# <a name="update-activitybasedtimeoutpolicy"></a><span data-ttu-id="22734-103">更新 activitybasedtimeoutpolicy</span><span class="sxs-lookup"><span data-stu-id="22734-103">Update activitybasedtimeoutpolicy</span></span>

<span data-ttu-id="22734-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="22734-104">Namespace: microsoft.graph</span></span>



<span data-ttu-id="22734-105">更新[activityBasedTimeoutPolicy](../resources/activitybasedtimeoutpolicy.md)对象的属性。</span><span class="sxs-lookup"><span data-stu-id="22734-105">Update the properties of an [activityBasedTimeoutPolicy](../resources/activitybasedtimeoutpolicy.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="22734-106">权限</span><span class="sxs-lookup"><span data-stu-id="22734-106">Permissions</span></span>

<span data-ttu-id="22734-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="22734-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="22734-109">权限类型</span><span class="sxs-lookup"><span data-stu-id="22734-109">Permission type</span></span>                        | <span data-ttu-id="22734-110">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="22734-110">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="22734-111">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="22734-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="22734-112">Policy.ReadWrite.ApplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="22734-112">Policy.ReadWrite.ApplicationConfiguration</span></span> |
| <span data-ttu-id="22734-113">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="22734-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="22734-114">不支持。</span><span class="sxs-lookup"><span data-stu-id="22734-114">Not supported.</span></span> |
| <span data-ttu-id="22734-115">Application</span><span class="sxs-lookup"><span data-stu-id="22734-115">Application</span></span>                            | <span data-ttu-id="22734-116">Policy.ReadWrite.ApplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="22734-116">Policy.ReadWrite.ApplicationConfiguration</span></span> |

## <a name="http-request"></a><span data-ttu-id="22734-117">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="22734-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PATCH /policies/activityBasedTimeoutPolicies/{id}
```

## <a name="request-headers"></a><span data-ttu-id="22734-118">请求标头</span><span class="sxs-lookup"><span data-stu-id="22734-118">Request headers</span></span>

| <span data-ttu-id="22734-119">名称</span><span class="sxs-lookup"><span data-stu-id="22734-119">Name</span></span>       | <span data-ttu-id="22734-120">说明</span><span class="sxs-lookup"><span data-stu-id="22734-120">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="22734-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="22734-121">Authorization</span></span> | <span data-ttu-id="22734-p102">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="22734-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="22734-124">Content-type</span><span class="sxs-lookup"><span data-stu-id="22734-124">Content-type</span></span> | <span data-ttu-id="22734-p103">application/json. Required.</span><span class="sxs-lookup"><span data-stu-id="22734-p103">application/json. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="22734-127">请求正文</span><span class="sxs-lookup"><span data-stu-id="22734-127">Request body</span></span>

<span data-ttu-id="22734-128">在请求正文中，提供应更新的相关字段的值。</span><span class="sxs-lookup"><span data-stu-id="22734-128">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="22734-129">请求正文中不包括的现有属性将保留其以前的值，或根据对其他属性值的更改重新计算。</span><span class="sxs-lookup"><span data-stu-id="22734-129">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="22734-130">为了获得最佳性能，请勿加入尚未更改的现有值。</span><span class="sxs-lookup"><span data-stu-id="22734-130">For best performance, don't include existing values that haven't changed.</span></span>

| <span data-ttu-id="22734-131">属性</span><span class="sxs-lookup"><span data-stu-id="22734-131">Property</span></span>     | <span data-ttu-id="22734-132">类型</span><span class="sxs-lookup"><span data-stu-id="22734-132">Type</span></span>        | <span data-ttu-id="22734-133">说明</span><span class="sxs-lookup"><span data-stu-id="22734-133">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="22734-134">定义</span><span class="sxs-lookup"><span data-stu-id="22734-134">definition</span></span>|<span data-ttu-id="22734-135">String 集合</span><span class="sxs-lookup"><span data-stu-id="22734-135">String collection</span></span>| <span data-ttu-id="22734-136">一个包含 JSON 字符串的字符串集合，该字符串定义此策略的规则和设置。</span><span class="sxs-lookup"><span data-stu-id="22734-136">A string collection containing a JSON string that defines the rules and settings for this policy.</span></span>  <span data-ttu-id="22734-137">必需。</span><span class="sxs-lookup"><span data-stu-id="22734-137">Required.</span></span>|
|<span data-ttu-id="22734-138">description</span><span class="sxs-lookup"><span data-stu-id="22734-138">description</span></span>|<span data-ttu-id="22734-139">String</span><span class="sxs-lookup"><span data-stu-id="22734-139">String</span></span>| <span data-ttu-id="22734-140">此策略的说明。</span><span class="sxs-lookup"><span data-stu-id="22734-140">Description for this policy.</span></span>|
|<span data-ttu-id="22734-141">displayName</span><span class="sxs-lookup"><span data-stu-id="22734-141">displayName</span></span>|<span data-ttu-id="22734-142">String</span><span class="sxs-lookup"><span data-stu-id="22734-142">String</span></span>| <span data-ttu-id="22734-143">此策略的显示名称。</span><span class="sxs-lookup"><span data-stu-id="22734-143">Display name for this policy.</span></span> <span data-ttu-id="22734-144">必需。</span><span class="sxs-lookup"><span data-stu-id="22734-144">Required.</span></span>|
|<span data-ttu-id="22734-145">isOrganizationDefault</span><span class="sxs-lookup"><span data-stu-id="22734-145">isOrganizationDefault</span></span>|<span data-ttu-id="22734-146">布尔</span><span class="sxs-lookup"><span data-stu-id="22734-146">Boolean</span></span>|<span data-ttu-id="22734-147">如果设置为 true，则激活此策略。</span><span class="sxs-lookup"><span data-stu-id="22734-147">If set to true, activates this policy.</span></span> <span data-ttu-id="22734-148">对于同一策略类型，可以有多个策略，但只有一个策略可以作为组织默认激活。</span><span class="sxs-lookup"><span data-stu-id="22734-148">There can be many policies for the same policy type, but only one can be activated as the organization default.</span></span> <span data-ttu-id="22734-149">可选，默认值为 false。</span><span class="sxs-lookup"><span data-stu-id="22734-149">Optional, default value is false.</span></span>|

## <a name="response"></a><span data-ttu-id="22734-150">响应</span><span class="sxs-lookup"><span data-stu-id="22734-150">Response</span></span>

<span data-ttu-id="22734-p108">如果成功，此方法返回 `204 No Content` 响应代码。它不在响应正文中返回任何内容。</span><span class="sxs-lookup"><span data-stu-id="22734-p108">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="22734-153">示例</span><span class="sxs-lookup"><span data-stu-id="22734-153">Example</span></span>

### <a name="request"></a><span data-ttu-id="22734-154">请求</span><span class="sxs-lookup"><span data-stu-id="22734-154">Request</span></span>

<span data-ttu-id="22734-155">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="22734-155">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "update_activitybasedtimeoutpolicy"
}-->

```http
PATCH https://graph.microsoft.com/v1.0/policies/activityBasedTimeoutPolicies/{id}
Content-type: application/json

{
  "definition": [
    "definition-value"
  ],
  "displayName": "displayName-value",
  "isOrganizationDefault": true,
  "type": "type-value"
}
```

### <a name="response"></a><span data-ttu-id="22734-156">响应</span><span class="sxs-lookup"><span data-stu-id="22734-156">Response</span></span>

<span data-ttu-id="22734-157">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="22734-157">The following is an example of the response.</span></span>

> <span data-ttu-id="22734-p109">**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。所有属性都将通过实际调用返回。</span><span class="sxs-lookup"><span data-stu-id="22734-p109">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.activityBasedTimeoutPolicy"
} -->

```http
HTTP/1.1 204 No Content
Content-type: application/json

{
  "definition": [
    "definition-value"
  ],
  "displayName": "displayName-value",
  "isOrganizationDefault": true,
  "id": "id-value"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update activitybasedtimeoutpolicy",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->