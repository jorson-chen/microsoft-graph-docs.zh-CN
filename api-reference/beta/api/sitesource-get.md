---
title: 获取 siteSource
description: 读取 siteSource 对象的属性和关系。
author: mahage-msft
localization_priority: Normal
ms.prod: compliance
doc_type: apiPageType
ms.openlocfilehash: bebedbfbb6ed340936c7067ecc1a0576f05c182e
ms.sourcegitcommit: f729068e1fbb6b0f34a3d6144b59ec9aafcd8a62
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/08/2020
ms.locfileid: "49597569"
---
# <a name="get-sitesource"></a><span data-ttu-id="ce1cf-103">获取 siteSource</span><span class="sxs-lookup"><span data-stu-id="ce1cf-103">Get siteSource</span></span>

<span data-ttu-id="ce1cf-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="ce1cf-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="ce1cf-105">读取 [siteSource](../resources/sitesource.md) 对象的属性和关系。</span><span class="sxs-lookup"><span data-stu-id="ce1cf-105">Read the properties and relationships of a [siteSource](../resources/sitesource.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="ce1cf-106">权限</span><span class="sxs-lookup"><span data-stu-id="ce1cf-106">Permissions</span></span>

<span data-ttu-id="ce1cf-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="ce1cf-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ce1cf-109">权限类型</span><span class="sxs-lookup"><span data-stu-id="ce1cf-109">Permission type</span></span>|<span data-ttu-id="ce1cf-110">权限（从最高特权到最低特权）</span><span class="sxs-lookup"><span data-stu-id="ce1cf-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ce1cf-111">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="ce1cf-111">Delegated (work or school account)</span></span>|<span data-ttu-id="ce1cf-112">User.Read</span><span class="sxs-lookup"><span data-stu-id="ce1cf-112">User.Read</span></span>|
|<span data-ttu-id="ce1cf-113">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="ce1cf-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ce1cf-114">不支持。</span><span class="sxs-lookup"><span data-stu-id="ce1cf-114">Not supported.</span></span>|
|<span data-ttu-id="ce1cf-115">应用程序</span><span class="sxs-lookup"><span data-stu-id="ce1cf-115">Application</span></span>|<span data-ttu-id="ce1cf-116">不支持。</span><span class="sxs-lookup"><span data-stu-id="ce1cf-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ce1cf-117">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="ce1cf-117">HTTP request</span></span>

<!-- {
  "blockType": "ignored"
}
-->

``` http
GET /compliance/ediscovery/cases/{ediscoveryCaseId}/custodians/{custodianId}/siteSources/{siteSourceId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="ce1cf-118">可选的查询参数</span><span class="sxs-lookup"><span data-stu-id="ce1cf-118">Optional query parameters</span></span>

<span data-ttu-id="ce1cf-119">此方法支持一些 OData 查询参数来帮助自定义响应。</span><span class="sxs-lookup"><span data-stu-id="ce1cf-119">This method supports some of the OData query parameters to help customize the response.</span></span> <span data-ttu-id="ce1cf-120">若要了解一般信息，请参阅 [OData 查询参数](/graph/query-parameters)。</span><span class="sxs-lookup"><span data-stu-id="ce1cf-120">For general information, see [OData query parameters](/graph/query-parameters).</span></span>

## <a name="request-headers"></a><span data-ttu-id="ce1cf-121">请求标头</span><span class="sxs-lookup"><span data-stu-id="ce1cf-121">Request headers</span></span>

|<span data-ttu-id="ce1cf-122">名称</span><span class="sxs-lookup"><span data-stu-id="ce1cf-122">Name</span></span>|<span data-ttu-id="ce1cf-123">说明</span><span class="sxs-lookup"><span data-stu-id="ce1cf-123">Description</span></span>|
|:---|:---|
|<span data-ttu-id="ce1cf-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="ce1cf-124">Authorization</span></span>|<span data-ttu-id="ce1cf-p103">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="ce1cf-p103">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="ce1cf-127">请求正文</span><span class="sxs-lookup"><span data-stu-id="ce1cf-127">Request body</span></span>

<span data-ttu-id="ce1cf-128">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="ce1cf-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ce1cf-129">响应</span><span class="sxs-lookup"><span data-stu-id="ce1cf-129">Response</span></span>

<span data-ttu-id="ce1cf-130">如果成功，此方法 `200 OK` 在响应正文中返回响应代码和 [siteSource](../resources/sitesource.md) 对象。</span><span class="sxs-lookup"><span data-stu-id="ce1cf-130">If successful, this method returns a `200 OK` response code and a [siteSource](../resources/sitesource.md) object in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="ce1cf-131">示例</span><span class="sxs-lookup"><span data-stu-id="ce1cf-131">Examples</span></span>

### <a name="request"></a><span data-ttu-id="ce1cf-132">请求</span><span class="sxs-lookup"><span data-stu-id="ce1cf-132">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_sitesource"
}
-->

``` http
GET https://graph.microsoft.com/beta/compliance/ediscovery/cases/4c8f8f70-7785-4bd4-b296-c98376a2c5e1/custodians/2192ca408ea2410eba3bec8ae873be6b/siteSources/38304445-3741-3333-4233-344238454333
```

### <a name="response"></a><span data-ttu-id="ce1cf-133">响应</span><span class="sxs-lookup"><span data-stu-id="ce1cf-133">Response</span></span>

<span data-ttu-id="ce1cf-134">**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。</span><span class="sxs-lookup"><span data-stu-id="ce1cf-134">**Note:** The response object shown here might be shortened for readability.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.siteSource"
}
-->

``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#compliance/ediscovery/cases('4c8f8f70-7785-4bd4-b296-c98376a2c5e1')/custodians('2192ca408ea2410eba3bec8ae873be6b')/siteSources",
    "displayName": "Human resources site",
    "createdDateTime": "2020-10-27T15:14:11.0048392Z",
    "id": "38304445-3741-3333-4233-344238454333",
    "createdBy": {
        "user": {
            "id": "c1db6f13-332a-4d84-b111-914383ff9fc9",
            "displayName": null
        }
    }
}
```
