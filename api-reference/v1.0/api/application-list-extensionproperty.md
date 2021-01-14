---
title: 列出 extensionProperties
description: 检索 extensionproperty 对象的列表。
localization_priority: Normal
author: sureshja
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: 814c465dc0479dbe70dd23c7177a6b0bdbd0e0f2
ms.sourcegitcommit: a9731e19589dcb5c0c6fe2e24b008c86573ef803
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/13/2021
ms.locfileid: "49844681"
---
# <a name="list-extensionproperties"></a><span data-ttu-id="df044-103">列出 extensionProperties</span><span class="sxs-lookup"><span data-stu-id="df044-103">List extensionProperties</span></span>

<span data-ttu-id="df044-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="df044-104">Namespace: microsoft.graph</span></span>

<span data-ttu-id="df044-105">检索应用程序上的 [extensionProperty](../resources/extensionproperty.md) 对象列表。</span><span class="sxs-lookup"><span data-stu-id="df044-105">Retrieve the list of [extensionProperty](../resources/extensionproperty.md) objects on an application.</span></span>

## <a name="permissions"></a><span data-ttu-id="df044-106">Permissions</span><span class="sxs-lookup"><span data-stu-id="df044-106">Permissions</span></span>

<span data-ttu-id="df044-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="df044-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="df044-109">权限类型</span><span class="sxs-lookup"><span data-stu-id="df044-109">Permission type</span></span>      | <span data-ttu-id="df044-110">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="df044-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="df044-111">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="df044-111">Delegated (work or school account)</span></span> | <span data-ttu-id="df044-112">Application.Read.All、Application.ReadWrite.All、Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="df044-112">Application.Read.All, Application.ReadWrite.All, Directory.Read.All</span></span> |
|<span data-ttu-id="df044-113">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="df044-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="df044-114">Application.Read.All， Application.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="df044-114">Application.Read.All, Application.ReadWrite.All</span></span> |
|<span data-ttu-id="df044-115">应用程序</span><span class="sxs-lookup"><span data-stu-id="df044-115">Application</span></span> | <span data-ttu-id="df044-116">Application.Read.All、Application.ReadWrite.All、Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="df044-116">Application.Read.All, Application.ReadWrite.All, Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="df044-117">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="df044-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /applications/{id}/extensionProperties
```

## <a name="optional-query-parameters"></a><span data-ttu-id="df044-118">可选的查询参数</span><span class="sxs-lookup"><span data-stu-id="df044-118">Optional query parameters</span></span>

<span data-ttu-id="df044-119">此方法支持一些 OData 查询参数来帮助自定义响应。</span><span class="sxs-lookup"><span data-stu-id="df044-119">This method supports some of the OData query parameters to help customize the response.</span></span> <span data-ttu-id="df044-120">若要了解一般信息，请参阅 [OData 查询参数](/graph/query-parameters)。</span><span class="sxs-lookup"><span data-stu-id="df044-120">For general information, see [OData query parameters](/graph/query-parameters).</span></span>

## <a name="request-headers"></a><span data-ttu-id="df044-121">请求标头</span><span class="sxs-lookup"><span data-stu-id="df044-121">Request headers</span></span>

| <span data-ttu-id="df044-122">名称</span><span class="sxs-lookup"><span data-stu-id="df044-122">Name</span></span>       | <span data-ttu-id="df044-123">说明</span><span class="sxs-lookup"><span data-stu-id="df044-123">Description</span></span>|
|:-----------|:----------|
| <span data-ttu-id="df044-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="df044-124">Authorization</span></span>  | <span data-ttu-id="df044-p103">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="df044-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="df044-127">请求正文</span><span class="sxs-lookup"><span data-stu-id="df044-127">Request body</span></span>

<span data-ttu-id="df044-128">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="df044-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="df044-129">响应</span><span class="sxs-lookup"><span data-stu-id="df044-129">Response</span></span>

<span data-ttu-id="df044-130">如果成功，此方法在响应正文中返回响应 `200 OK` 代码和 [extensionProperty](../resources/extensionproperty.md) 对象集合。</span><span class="sxs-lookup"><span data-stu-id="df044-130">If successful, this method returns a `200 OK` response code and a collection of [extensionProperty](../resources/extensionproperty.md) objects in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="df044-131">示例</span><span class="sxs-lookup"><span data-stu-id="df044-131">Examples</span></span>

### <a name="request"></a><span data-ttu-id="df044-132">请求</span><span class="sxs-lookup"><span data-stu-id="df044-132">Request</span></span>

<span data-ttu-id="df044-133">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="df044-133">The following is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="df044-134">HTTP</span><span class="sxs-lookup"><span data-stu-id="df044-134">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_extensionproperties"
}-->

```msgraph-interactive
GET https://graph.microsoft.com/v1.0/applications/{id}/extensionProperties
```
# <a name="c"></a>[<span data-ttu-id="df044-135">C#</span><span class="sxs-lookup"><span data-stu-id="df044-135">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-extensionproperties-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="df044-136">JavaScript</span><span class="sxs-lookup"><span data-stu-id="df044-136">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-extensionproperties-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="df044-137">Objective-C</span><span class="sxs-lookup"><span data-stu-id="df044-137">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-extensionproperties-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[<span data-ttu-id="df044-138">Java</span><span class="sxs-lookup"><span data-stu-id="df044-138">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/get-extensionproperties-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


### <a name="response"></a><span data-ttu-id="df044-139">响应</span><span class="sxs-lookup"><span data-stu-id="df044-139">Response</span></span>

<span data-ttu-id="df044-140">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="df044-140">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.extensionProperty",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
        {
            "id": "a2c459db-f5dc-4328-ae9b-118e88d04d19",
            "deletedDateTime": null,
            "appDisplayName": "Display name",
            "name": "extension_b3efaf8f68a44275abcff28ef86b2ee3_extensionName",
            "dataType": "String",
            "isSyncedFromOnPremises": false,
            "targetObjects": [
                "Application"
            ]
        }
    ]
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List extensionProperties",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

