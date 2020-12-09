---
title: 为用户安装应用
description: 在指定用户的个人范围内安装应用。
author: clearab
doc_type: apiPageType
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 37591c37f09b07baa88a47f707e0a910a0a7de40
ms.sourcegitcommit: 59e79cf2693cbb550da3e61eb4f68d9e0f57faf6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/09/2020
ms.locfileid: "49607577"
---
# <a name="install-app-for-user"></a><span data-ttu-id="a1ee5-103">为用户安装应用</span><span class="sxs-lookup"><span data-stu-id="a1ee5-103">Install app for user</span></span>

<span data-ttu-id="a1ee5-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="a1ee5-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="a1ee5-105">在指定[用户](../resources/user.md)的个人作用域中安装[应用程序](../resources/teamsapp.md)。</span><span class="sxs-lookup"><span data-stu-id="a1ee5-105">Install an [app](../resources/teamsapp.md) in the personal scope of the specified [user](../resources/user.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="a1ee5-106">权限</span><span class="sxs-lookup"><span data-stu-id="a1ee5-106">Permissions</span></span>

<span data-ttu-id="a1ee5-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="a1ee5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a1ee5-109">权限类型</span><span class="sxs-lookup"><span data-stu-id="a1ee5-109">Permission type</span></span>      | <span data-ttu-id="a1ee5-110">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="a1ee5-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a1ee5-111">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="a1ee5-111">Delegated (work or school account)</span></span> | <span data-ttu-id="a1ee5-112">TeamsAppInstallation、ReadWriteSelfForUser、ReadWriteForUser</span><span class="sxs-lookup"><span data-stu-id="a1ee5-112">TeamsAppInstallation.ReadWriteSelfForUser, TeamsAppInstallation.ReadWriteForUser</span></span> |
|<span data-ttu-id="a1ee5-113">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="a1ee5-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a1ee5-114">不支持。</span><span class="sxs-lookup"><span data-stu-id="a1ee5-114">Not supported.</span></span>    |
|<span data-ttu-id="a1ee5-115">应用程序</span><span class="sxs-lookup"><span data-stu-id="a1ee5-115">Application</span></span> | <span data-ttu-id="a1ee5-116">TeamsAppInstallation、ReadWriteSelfForUser、TeamsAppInstallation</span><span class="sxs-lookup"><span data-stu-id="a1ee5-116">TeamsAppInstallation.ReadWriteSelfForUser.All, TeamsAppInstallation.ReadWriteForUser.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="a1ee5-117">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="a1ee5-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{user-id}/teamwork/installedApps
```

## <a name="request-headers"></a><span data-ttu-id="a1ee5-118">请求标头</span><span class="sxs-lookup"><span data-stu-id="a1ee5-118">Request headers</span></span>

| <span data-ttu-id="a1ee5-119">标头</span><span class="sxs-lookup"><span data-stu-id="a1ee5-119">Header</span></span>       | <span data-ttu-id="a1ee5-120">值</span><span class="sxs-lookup"><span data-stu-id="a1ee5-120">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="a1ee5-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="a1ee5-121">Authorization</span></span>  | <span data-ttu-id="a1ee5-p102">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="a1ee5-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="a1ee5-124">请求正文</span><span class="sxs-lookup"><span data-stu-id="a1ee5-124">Request body</span></span>

<span data-ttu-id="a1ee5-125">请求正文应包含要添加的现有目录应用程序的 ID。</span><span class="sxs-lookup"><span data-stu-id="a1ee5-125">The request body should contain the ID of the existing catalog app to be added.</span></span>

| <span data-ttu-id="a1ee5-126">属性</span><span class="sxs-lookup"><span data-stu-id="a1ee5-126">Property</span></span>   | <span data-ttu-id="a1ee5-127">类型</span><span class="sxs-lookup"><span data-stu-id="a1ee5-127">Type</span></span> |<span data-ttu-id="a1ee5-128">Description</span><span class="sxs-lookup"><span data-stu-id="a1ee5-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a1ee5-129">teamsApp</span><span class="sxs-lookup"><span data-stu-id="a1ee5-129">teamsApp</span></span>|<span data-ttu-id="a1ee5-130">String</span><span class="sxs-lookup"><span data-stu-id="a1ee5-130">String</span></span>|<span data-ttu-id="a1ee5-131">要添加的应用程序的 ID。</span><span class="sxs-lookup"><span data-stu-id="a1ee5-131">The ID of the app to add.</span></span>|

## <a name="response"></a><span data-ttu-id="a1ee5-132">响应</span><span class="sxs-lookup"><span data-stu-id="a1ee5-132">Response</span></span>

<span data-ttu-id="a1ee5-p103">如果成功，此方法返回 `201 Created` 响应代码。它不在响应正文中返回任何内容。</span><span class="sxs-lookup"><span data-stu-id="a1ee5-p103">If successful, this method returns a `201 Created` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a1ee5-135">示例</span><span class="sxs-lookup"><span data-stu-id="a1ee5-135">Example</span></span>

### <a name="request"></a><span data-ttu-id="a1ee5-136">请求</span><span class="sxs-lookup"><span data-stu-id="a1ee5-136">Request</span></span>

<span data-ttu-id="a1ee5-137">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="a1ee5-137">The following is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="a1ee5-138">HTTP</span><span class="sxs-lookup"><span data-stu-id="a1ee5-138">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "user_add_teamsApp"
}-->
```http
POST https://graph.microsoft.com/beta/users/5b649834-7412-4cce-9e69-176e95a394f5/teamwork/installedApps
Content-type: application/json

{
   "teamsApp@odata.bind":"https://graph.microsoft.com/beta/appCatalogs/teamsApps/12345678-9abc-def0-123456789a"
}
```
# <a name="c"></a>[<span data-ttu-id="a1ee5-139">C#</span><span class="sxs-lookup"><span data-stu-id="a1ee5-139">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/user-add-teamsapp-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="a1ee5-140">JavaScript</span><span class="sxs-lookup"><span data-stu-id="a1ee5-140">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/user-add-teamsapp-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="a1ee5-141">Objective-C</span><span class="sxs-lookup"><span data-stu-id="a1ee5-141">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/user-add-teamsapp-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[<span data-ttu-id="a1ee5-142">Java</span><span class="sxs-lookup"><span data-stu-id="a1ee5-142">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/user-add-teamsapp-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


### <a name="response"></a><span data-ttu-id="a1ee5-143">响应</span><span class="sxs-lookup"><span data-stu-id="a1ee5-143">Response</span></span>

<span data-ttu-id="a1ee5-144">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="a1ee5-144">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true
} -->

```http
HTTP/1.1 201 Created
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "User add teamsAppInstallations",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


