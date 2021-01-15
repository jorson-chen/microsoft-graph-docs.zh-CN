---
title: 从团队删除成员
description: 从团队删除 conversationMember。
author: nkramer
localization_priority: Priority
ms.prod: microsoft-teams
doc_type: apiPageType
ms.openlocfilehash: efe094094ee8777d1590a86bbbc6bbb9bfb6abd9
ms.sourcegitcommit: eacd2a6e46c19dd3cd8519592b1668fabe14d85d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "49872238"
---
# <a name="remove-member-from-team"></a><span data-ttu-id="c31fe-103">从团队删除成员</span><span class="sxs-lookup"><span data-stu-id="c31fe-103">Remove member from team</span></span>
<span data-ttu-id="c31fe-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="c31fe-104">Namespace: microsoft.graph</span></span>

<span data-ttu-id="c31fe-105">从[团队](../resources/team.md)删除一个 [conversationMember](../resources/conversationmember.md)。</span><span class="sxs-lookup"><span data-stu-id="c31fe-105">Remove a [conversationMember](../resources/conversationmember.md) from a [team](../resources/team.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="c31fe-106">权限</span><span class="sxs-lookup"><span data-stu-id="c31fe-106">Permissions</span></span>
<span data-ttu-id="c31fe-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="c31fe-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c31fe-109">权限类型</span><span class="sxs-lookup"><span data-stu-id="c31fe-109">Permission type</span></span>|<span data-ttu-id="c31fe-110">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="c31fe-110">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c31fe-111">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="c31fe-111">Delegated (work or school account)</span></span>| <span data-ttu-id="c31fe-112">TeamMember.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c31fe-112">TeamMember.ReadWrite.All</span></span> |
|<span data-ttu-id="c31fe-113">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="c31fe-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c31fe-114">不支持。</span><span class="sxs-lookup"><span data-stu-id="c31fe-114">Not supported.</span></span>    |
|<span data-ttu-id="c31fe-115">应用程序</span><span class="sxs-lookup"><span data-stu-id="c31fe-115">Application</span></span>| <span data-ttu-id="c31fe-116">TeamMember.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c31fe-116">TeamMember.ReadWrite.All</span></span> |


## <a name="http-request"></a><span data-ttu-id="c31fe-117">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="c31fe-117">HTTP request</span></span>

<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /teams/{team-id}/members/{membership-id}
```

## <a name="request-headers"></a><span data-ttu-id="c31fe-118">请求标头</span><span class="sxs-lookup"><span data-stu-id="c31fe-118">Request headers</span></span>
|<span data-ttu-id="c31fe-119">名称</span><span class="sxs-lookup"><span data-stu-id="c31fe-119">Name</span></span>|<span data-ttu-id="c31fe-120">说明</span><span class="sxs-lookup"><span data-stu-id="c31fe-120">Description</span></span>|
|:---|:---|
|<span data-ttu-id="c31fe-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="c31fe-121">Authorization</span></span>|<span data-ttu-id="c31fe-p102">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="c31fe-p102">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="c31fe-124">请求正文</span><span class="sxs-lookup"><span data-stu-id="c31fe-124">Request body</span></span>
<span data-ttu-id="c31fe-125">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="c31fe-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c31fe-126">响应</span><span class="sxs-lookup"><span data-stu-id="c31fe-126">Response</span></span>

<span data-ttu-id="c31fe-127">如果成功，此方法返回 `204 No Content` 响应代码。</span><span class="sxs-lookup"><span data-stu-id="c31fe-127">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="examples"></a><span data-ttu-id="c31fe-128">示例</span><span class="sxs-lookup"><span data-stu-id="c31fe-128">Examples</span></span>

### <a name="request"></a><span data-ttu-id="c31fe-129">请求</span><span class="sxs-lookup"><span data-stu-id="c31fe-129">Request</span></span>

# <a name="http"></a>[<span data-ttu-id="c31fe-130">HTTP</span><span class="sxs-lookup"><span data-stu-id="c31fe-130">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "delete_members_from_team"
}
-->
``` http
DELETE https://graph.microsoft.com/v1.0/teams/ee0f5ae2-8bc6-4ae5-8466-7daeebbfa062/members/ZWUwZjVhZTItOGJjNi00YWU1LTg0NjYtN2RhZWViYmZhMDYyIyM3Mzc2MWYwNi0yYWM5LTQ2OWMtOWYxMC0yNzlhOGNjMjY3Zjk=
```
# <a name="c"></a>[<span data-ttu-id="c31fe-131">C#</span><span class="sxs-lookup"><span data-stu-id="c31fe-131">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/delete-members-from-team-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="c31fe-132">JavaScript</span><span class="sxs-lookup"><span data-stu-id="c31fe-132">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/delete-members-from-team-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="c31fe-133">Objective-C</span><span class="sxs-lookup"><span data-stu-id="c31fe-133">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/delete-members-from-team-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[<span data-ttu-id="c31fe-134">Java</span><span class="sxs-lookup"><span data-stu-id="c31fe-134">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/delete-members-from-team-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

### <a name="response"></a><span data-ttu-id="c31fe-135">响应</span><span class="sxs-lookup"><span data-stu-id="c31fe-135">Response</span></span>
<span data-ttu-id="c31fe-136">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="c31fe-136">The following is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 204 No Content
```

## <a name="see-also"></a><span data-ttu-id="c31fe-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c31fe-137">See also</span></span>

- [<span data-ttu-id="c31fe-138">从频道中删除成员</span><span class="sxs-lookup"><span data-stu-id="c31fe-138">Remove member from channel</span></span>](channel-delete-members.md)
