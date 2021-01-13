---
title: 获取 userFlowApiConnectorConfiguration
description: 获取 b2cIdentityUserFlow 的 userFlowApiConnectorConfiguration 属性。
author: nickgmicrosoft
localization_priority: Normal
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: b065c20f7b6e4c9f70abd42dd09347f75d1b8dae
ms.sourcegitcommit: a9731e19589dcb5c0c6fe2e24b008c86573ef803
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/13/2021
ms.locfileid: "49843961"
---
# <a name="get-userflowapiconnectorconfiguration"></a><span data-ttu-id="f0def-103">获取 userFlowApiConnectorConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0def-103">Get userFlowApiConnectorConfiguration</span></span>

<span data-ttu-id="f0def-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="f0def-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="f0def-105">获取[b2cIdentityUserFlow](../resources/userFlowApiConnectorConfiguration.md)中的[apiConnectorConfiguration](../resources/userflowapiconnectorconfiguration.md)属性，以详细说明为用户流启用的 API 连接器。</span><span class="sxs-lookup"><span data-stu-id="f0def-105">Get the [apiConnectorConfiguration](../resources/userflowapiconnectorconfiguration.md) property in a [b2cIdentityUserFlow](../resources/userFlowApiConnectorConfiguration.md) to detail the API connectors enabled for the user flow.</span></span>

## <a name="permissions"></a><span data-ttu-id="f0def-106">Permissions</span><span class="sxs-lookup"><span data-stu-id="f0def-106">Permissions</span></span>

<span data-ttu-id="f0def-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="f0def-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f0def-109">权限类型</span><span class="sxs-lookup"><span data-stu-id="f0def-109">Permission type</span></span>      | <span data-ttu-id="f0def-110">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="f0def-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f0def-111">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="f0def-111">Delegated (work or school account)</span></span>|<span data-ttu-id="f0def-112">IdentityUserFlow.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f0def-112">IdentityUserFlow.ReadWrite.All</span></span>|
|<span data-ttu-id="f0def-113">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="f0def-113">Delegated (personal Microsoft account)</span></span>| <span data-ttu-id="f0def-114">不支持。</span><span class="sxs-lookup"><span data-stu-id="f0def-114">Not supported.</span></span>|
|<span data-ttu-id="f0def-115">应用程序</span><span class="sxs-lookup"><span data-stu-id="f0def-115">Application</span></span>|<span data-ttu-id="f0def-116">IdentityUserFlow.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f0def-116">IdentityUserFlow.ReadWrite.All</span></span>|

<span data-ttu-id="f0def-117">工作或学校帐户需要属于以下角色之一：</span><span class="sxs-lookup"><span data-stu-id="f0def-117">The work or school account needs to belong to one of the following roles:</span></span>

* <span data-ttu-id="f0def-118">全局管理员</span><span class="sxs-lookup"><span data-stu-id="f0def-118">Global administrator</span></span>
* <span data-ttu-id="f0def-119">外部标识用户流管理员</span><span class="sxs-lookup"><span data-stu-id="f0def-119">External Identity User Flow administrator</span></span>

## <a name="http-request"></a><span data-ttu-id="f0def-120">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="f0def-120">HTTP request</span></span>

<!-- {
  "blockType": "ignored"
}
-->

``` http
GET identity/b2cUserFlows/{id}/apiConnectorConfiguration
```

## <a name="optional-query-parameters"></a><span data-ttu-id="f0def-121">可选的查询参数</span><span class="sxs-lookup"><span data-stu-id="f0def-121">Optional query parameters</span></span>

<span data-ttu-id="f0def-122">此方法支持 `$expand` OData 查询参数来帮助自定义响应。</span><span class="sxs-lookup"><span data-stu-id="f0def-122">This method supports the `$expand` OData query parameter to help customize the response.</span></span> <span data-ttu-id="f0def-123">例如，若要检索和步骤的 API `postFederationSignup` 连接器 `postAttributeCollection` ，请添加 `$expand=postFederationSignup,postAttributeCollection` 。</span><span class="sxs-lookup"><span data-stu-id="f0def-123">For example, to retrieve the API connector for the `postFederationSignup` and `postAttributeCollection` steps, add `$expand=postFederationSignup,postAttributeCollection`.</span></span> <span data-ttu-id="f0def-124">若要了解一般信息，请参阅 [OData 查询参数](/graph/query-parameters)。</span><span class="sxs-lookup"><span data-stu-id="f0def-124">For general information, see [OData query parameters](/graph/query-parameters).</span></span>

## <a name="request-headers"></a><span data-ttu-id="f0def-125">请求标头</span><span class="sxs-lookup"><span data-stu-id="f0def-125">Request headers</span></span>

|<span data-ttu-id="f0def-126">名称</span><span class="sxs-lookup"><span data-stu-id="f0def-126">Name</span></span>|<span data-ttu-id="f0def-127">说明</span><span class="sxs-lookup"><span data-stu-id="f0def-127">Description</span></span>|
|:---|:---|
|<span data-ttu-id="f0def-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="f0def-128">Authorization</span></span>|<span data-ttu-id="f0def-p103">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="f0def-p103">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="f0def-131">请求正文</span><span class="sxs-lookup"><span data-stu-id="f0def-131">Request body</span></span>

<span data-ttu-id="f0def-132">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="f0def-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f0def-133">响应</span><span class="sxs-lookup"><span data-stu-id="f0def-133">Response</span></span>

<span data-ttu-id="f0def-134">如果成功，此方法返回响应 `200 OK` 代码和 [apiConnectorConfiguration](../resources/userflowapiconnectorconfiguration.md) 对象。</span><span class="sxs-lookup"><span data-stu-id="f0def-134">If successful, this method returns a `200 OK` response code and an [apiConnectorConfiguration](../resources/userflowapiconnectorconfiguration.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="f0def-135">示例</span><span class="sxs-lookup"><span data-stu-id="f0def-135">Examples</span></span>

### <a name="request"></a><span data-ttu-id="f0def-136">请求</span><span class="sxs-lookup"><span data-stu-id="f0def-136">Request</span></span>

<span data-ttu-id="f0def-137">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="f0def-137">The following is an example of the request.</span></span>


# <a name="http"></a>[<span data-ttu-id="f0def-138">HTTP</span><span class="sxs-lookup"><span data-stu-id="f0def-138">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_b2cuserflows-apiconnectorconfiguration"
}
-->

``` http
GET https://graph.microsoft.com/beta/identity/b2cUserFlows/B2C_1_testuserflow/apiConnectorConfiguration?$expand=postFederationSignup,postAttributeCollection
```
# <a name="c"></a>[<span data-ttu-id="f0def-139">C#</span><span class="sxs-lookup"><span data-stu-id="f0def-139">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-b2cuserflows-apiconnectorconfiguration-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="f0def-140">JavaScript</span><span class="sxs-lookup"><span data-stu-id="f0def-140">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-b2cuserflows-apiconnectorconfiguration-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="f0def-141">Objective-C</span><span class="sxs-lookup"><span data-stu-id="f0def-141">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-b2cuserflows-apiconnectorconfiguration-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[<span data-ttu-id="f0def-142">Java</span><span class="sxs-lookup"><span data-stu-id="f0def-142">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/get-b2cuserflows-apiconnectorconfiguration-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


### <a name="response"></a><span data-ttu-id="f0def-143">响应</span><span class="sxs-lookup"><span data-stu-id="f0def-143">Response</span></span>

<span data-ttu-id="f0def-144">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="f0def-144">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.userFlowApiConnectorConfiguration"
}
-->

``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#identity/b2cUserFlows('B2C_1_testuserflow')/apiConnectorConfiguration(postFederationSignup(),postAttributeCollection())",
    "postFederationSignup@odata.context": "https://graph.microsoft.com/beta/$metadata#identity/b2cUserFlows('B2C_1_testuserflow')/apiConnectorConfiguration/microsoft.graph.userFlowApiConnectorConfiguration/postFederationSignup/$entity",
    "postFederationSignup": {
        "id": "<guid1>",
        "displayName": "Test API Connector 1",
        "targetUrl": "https://someapi.com/api/endpoint",
        "authenticationConfiguration": {
            "@odata.type": "#microsoft.graph.basicAuthentication",
            "username": "<USERNAME>",
            "password": "******"
        }
    },
    "postAttributeCollection@odata.context": "https://graph.microsoft.com/beta/$metadata#identity/b2cUserFlows('B2C_1_testuserflow')/apiConnectorConfiguration/microsoft.graph.userFlowApiConnectorConfiguration/microsoft.graph.userFlowApiConnectorConfiguration/postAttributeCollection/$entity",
    "postAttributeCollection": {
        "id": "<guid2>",
        "displayName": "Test API Connector 2",
        "targetUrl": "https://someotherapi.com/api/endpoint",
        "authenticationConfiguration": {
            "@odata.type": "#microsoft.graph.basicAuthentication",
            "username": "<USERNAME2>",
            "password": "******"
        }
    }
}
```
