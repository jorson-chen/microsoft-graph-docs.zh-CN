---
title: 获取团队
description: 检索指定团队的属性和关系。
author: nkramer
localization_priority: Priority
ms.prod: microsoft-teams
doc_type: apiPageType
ms.openlocfilehash: c83c99e1519f952ee8fb80c5a179cefc9abb458e
ms.sourcegitcommit: d1e72c8d36aad78732133f9ecefaf66c433b8530
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2020
ms.locfileid: "48848659"
---
# <a name="get-team"></a><span data-ttu-id="851c7-103">获取团队</span><span class="sxs-lookup"><span data-stu-id="851c7-103">Get team</span></span>

<span data-ttu-id="851c7-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="851c7-104">Namespace: microsoft.graph</span></span>



<span data-ttu-id="851c7-105">检索指定[团队](../resources/team.md)的属性和关系。</span><span class="sxs-lookup"><span data-stu-id="851c7-105">Retrieve the properties and relationships of the specified [team](../resources/team.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="851c7-106">权限</span><span class="sxs-lookup"><span data-stu-id="851c7-106">Permissions</span></span>
<span data-ttu-id="851c7-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="851c7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="851c7-109">权限类型</span><span class="sxs-lookup"><span data-stu-id="851c7-109">Permission type</span></span>      | <span data-ttu-id="851c7-110">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="851c7-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="851c7-111">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="851c7-111">Delegated (work or school account)</span></span> | <span data-ttu-id="851c7-112">Team.ReadBasic.All, TeamSettings.Read.All, TeamSettings.ReadWrite.All, Group.Read.All, Group.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="851c7-112">Team.ReadBasic.All, TeamSettings.Read.All, TeamSettings.ReadWrite.All, Group.Read.All, Group.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |
|<span data-ttu-id="851c7-113">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="851c7-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="851c7-114">不支持。</span><span class="sxs-lookup"><span data-stu-id="851c7-114">Not supported.</span></span>    |
|<span data-ttu-id="851c7-115">应用程序</span><span class="sxs-lookup"><span data-stu-id="851c7-115">Application</span></span> | <span data-ttu-id="851c7-116">TeamSettings.Read.Group *, TeamSettings.ReadWrite.Group*, Team.ReadBasic.All, TeamSettings.Read.All, TeamSettings.ReadWrite.All, Group.Read.All, Group.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="851c7-116">TeamSettings.Read.Group *, TeamSettings.ReadWrite.Group*, Team.ReadBasic.All, TeamSettings.Read.All, TeamSettings.ReadWrite.All, Group.Read.All, Group.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

> <span data-ttu-id="851c7-117">**注意**：标有 \* 的权限用于 [特定于资源的同意]( https://aka.ms/teams-rsc)。</span><span class="sxs-lookup"><span data-stu-id="851c7-117">**Note**: Permissions marked with \* use [resource-specific consent]( https://aka.ms/teams-rsc).</span></span>

> <span data-ttu-id="851c7-118">**注意**：此 API 支持管理员权限。</span><span class="sxs-lookup"><span data-stu-id="851c7-118">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="851c7-119">全局管理员和 Microsoft Teams 服务管理员可以访问自己不是其中成员的团队。</span><span class="sxs-lookup"><span data-stu-id="851c7-119">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="851c7-120">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="851c7-120">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /teams/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="851c7-121">可选的查询参数</span><span class="sxs-lookup"><span data-stu-id="851c7-121">Optional query parameters</span></span>
<span data-ttu-id="851c7-122">此方法支持 $select 和 $expand [OData 查询参数](/graph/query-parameters)来帮助自定义响应。</span><span class="sxs-lookup"><span data-stu-id="851c7-122">This method supports the $select and $expand [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="851c7-123">请求标头</span><span class="sxs-lookup"><span data-stu-id="851c7-123">Request headers</span></span>
| <span data-ttu-id="851c7-124">标头</span><span class="sxs-lookup"><span data-stu-id="851c7-124">Header</span></span>       | <span data-ttu-id="851c7-125">值</span><span class="sxs-lookup"><span data-stu-id="851c7-125">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="851c7-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="851c7-126">Authorization</span></span>  | <span data-ttu-id="851c7-p103">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="851c7-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="851c7-129">请求正文</span><span class="sxs-lookup"><span data-stu-id="851c7-129">Request body</span></span>
<span data-ttu-id="851c7-130">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="851c7-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="851c7-131">响应</span><span class="sxs-lookup"><span data-stu-id="851c7-131">Response</span></span>

<span data-ttu-id="851c7-132">如果成功，此方法会在响应正文中返回 `200 OK` 响应代码和 [team](../resources/team.md) 对象。</span><span class="sxs-lookup"><span data-stu-id="851c7-132">If successful, this method returns a `200 OK` response code and a [team](../resources/team.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="851c7-133">示例</span><span class="sxs-lookup"><span data-stu-id="851c7-133">Example</span></span>
#### <a name="request"></a><span data-ttu-id="851c7-134">请求</span><span class="sxs-lookup"><span data-stu-id="851c7-134">Request</span></span>
<span data-ttu-id="851c7-135">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="851c7-135">The following is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="851c7-136">HTTP</span><span class="sxs-lookup"><span data-stu-id="851c7-136">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_team"
}-->
```msgraph-interactive
GET https://graph.microsoft.com/v1.0/teams/{id}
```
# <a name="c"></a>[<span data-ttu-id="851c7-137">C#</span><span class="sxs-lookup"><span data-stu-id="851c7-137">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-team-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="851c7-138">JavaScript</span><span class="sxs-lookup"><span data-stu-id="851c7-138">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-team-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="851c7-139">Objective-C</span><span class="sxs-lookup"><span data-stu-id="851c7-139">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-team-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[<span data-ttu-id="851c7-140">Java</span><span class="sxs-lookup"><span data-stu-id="851c7-140">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/get-team-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

#### <a name="response"></a><span data-ttu-id="851c7-141">响应</span><span class="sxs-lookup"><span data-stu-id="851c7-141">Response</span></span>
<span data-ttu-id="851c7-142">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="851c7-142">The following is an example of the response.</span></span> 

><span data-ttu-id="851c7-p104">**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。所有属性都将通过实际调用返回。</span><span class="sxs-lookup"><span data-stu-id="851c7-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.team"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 401

{
  "isArchived": false,
  "discoverySettings": {
    "showInTeamsSearchAndSuggestions": true
  },
  "memberSettings": {
    "allowCreateUpdateChannels": true,
    "allowDeleteChannels": true,
    "allowAddRemoveApps": true,
    "allowCreateUpdateRemoveTabs": true,
    "allowCreateUpdateRemoveConnectors": true
  },
  "guestSettings": {
    "allowCreateUpdateChannels": true,
    "allowDeleteChannels": true
  },
  "messagingSettings": {
    "allowUserEditMessages": true,
    "allowUserDeleteMessages": true,
    "allowOwnerDeleteMessages": true,
    "allowTeamMentions": true,
    "allowChannelMentions": true
  },
  "funSettings": {
    "allowGiphy": true,
    "giphyContentRating": "strict",
    "allowStickersAndMemes": true,
    "allowCustomMemes": true
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get team",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

