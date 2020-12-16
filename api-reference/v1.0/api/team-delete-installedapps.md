---
title: 从团队中删除应用
description: 从指定团队卸载应用。
author: clearab
localization_priority: Normal
ms.prod: microsoft-teams
doc_type: apiPageType
ms.openlocfilehash: 6d51730971ad26bb7f5de5479d4c95aaa874fd00
ms.sourcegitcommit: 75428fc7535662f34e965c6b69fef3a53fdaf1cb
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/16/2020
ms.locfileid: "49690647"
---
# <a name="remove-app-from-team"></a><span data-ttu-id="8bff3-103">从团队中删除应用</span><span class="sxs-lookup"><span data-stu-id="8bff3-103">Remove app from team</span></span>

<span data-ttu-id="8bff3-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="8bff3-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="8bff3-105">从指定的 [团队](../resources/teamsappinstallation.md) 卸载 [应用](../resources/team.md)。</span><span class="sxs-lookup"><span data-stu-id="8bff3-105">Uninstalls an [app](../resources/teamsappinstallation.md) from the specified [team](../resources/team.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="8bff3-106">权限</span><span class="sxs-lookup"><span data-stu-id="8bff3-106">Permissions</span></span>

<span data-ttu-id="8bff3-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="8bff3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8bff3-109">权限类型</span><span class="sxs-lookup"><span data-stu-id="8bff3-109">Permission type</span></span>      | <span data-ttu-id="8bff3-110">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="8bff3-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8bff3-111">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="8bff3-111">Delegated (work or school account)</span></span> | <span data-ttu-id="8bff3-112">TeamsAppInstallation.ReadWriteForTeam、Group.ReadWrite.All、Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8bff3-112">TeamsAppInstallation.ReadWriteForTeam, Group.ReadWrite.All, Directory.ReadWrite.All</span></span> |
|<span data-ttu-id="8bff3-113">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="8bff3-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8bff3-114">不支持。</span><span class="sxs-lookup"><span data-stu-id="8bff3-114">Not supported.</span></span>    |
|<span data-ttu-id="8bff3-115">Application</span><span class="sxs-lookup"><span data-stu-id="8bff3-115">Application</span></span> | <span data-ttu-id="8bff3-116">TeamsAppInstallation.ReadWriteForTeam.All、Group.ReadWrite.All、Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8bff3-116">TeamsAppInstallation.ReadWriteForTeam.All, Group.ReadWrite.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="8bff3-117">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="8bff3-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /teams/{team-id}/installedApps/{app-installation-id}
```

## <a name="request-headers"></a><span data-ttu-id="8bff3-118">请求标头</span><span class="sxs-lookup"><span data-stu-id="8bff3-118">Request headers</span></span>

| <span data-ttu-id="8bff3-119">标头</span><span class="sxs-lookup"><span data-stu-id="8bff3-119">Header</span></span>       | <span data-ttu-id="8bff3-120">值</span><span class="sxs-lookup"><span data-stu-id="8bff3-120">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="8bff3-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="8bff3-121">Authorization</span></span>  | <span data-ttu-id="8bff3-p102">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="8bff3-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="8bff3-124">请求正文</span><span class="sxs-lookup"><span data-stu-id="8bff3-124">Request body</span></span>

<span data-ttu-id="8bff3-125">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="8bff3-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8bff3-126">响应</span><span class="sxs-lookup"><span data-stu-id="8bff3-126">Response</span></span>

<span data-ttu-id="8bff3-p103">如果成功，此方法返回 `204 No Content` 响应代码。它不在响应正文中返回任何内容。</span><span class="sxs-lookup"><span data-stu-id="8bff3-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8bff3-129">示例</span><span class="sxs-lookup"><span data-stu-id="8bff3-129">Example</span></span>

### <a name="request"></a><span data-ttu-id="8bff3-130">请求</span><span class="sxs-lookup"><span data-stu-id="8bff3-130">Request</span></span>

<span data-ttu-id="8bff3-131">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="8bff3-131">The following is an example of the request.</span></span>


# <a name="http"></a>[<span data-ttu-id="8bff3-132">HTTP</span><span class="sxs-lookup"><span data-stu-id="8bff3-132">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "uninstall_teamsapp_in_team"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/teams/6903fa93-605b-43ef-920e-77c4729f8258/installedApps/NjkwM2ZhOTMtNjA1Yi00M2VmLTkyMGUtNzdjNDcyOWY4MjU4IyMwMDAwMTAxNi1kZTA1LTQ5MmUtOTEwNi00ODI4ZmM4YTg2ODc=
```
# <a name="c"></a>[<span data-ttu-id="8bff3-133">C#</span><span class="sxs-lookup"><span data-stu-id="8bff3-133">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/uninstall-teamsapp-in-team-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="8bff3-134">JavaScript</span><span class="sxs-lookup"><span data-stu-id="8bff3-134">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/uninstall-teamsapp-in-team-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="8bff3-135">Objective-C</span><span class="sxs-lookup"><span data-stu-id="8bff3-135">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/uninstall-teamsapp-in-team-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[<span data-ttu-id="8bff3-136">Java</span><span class="sxs-lookup"><span data-stu-id="8bff3-136">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/uninstall-teamsapp-in-team-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


### <a name="response"></a><span data-ttu-id="8bff3-137">响应</span><span class="sxs-lookup"><span data-stu-id="8bff3-137">Response</span></span>

<span data-ttu-id="8bff3-138">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="8bff3-138">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "name": "uninstall_teamsapp_in_team",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Remove app from team",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


