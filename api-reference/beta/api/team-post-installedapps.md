---
title: 向团队添加应用
description: 将应用程序安装到指定的团队。
author: clearab
localization_priority: Normal
ms.prod: microsoft-teams
doc_type: apiPageType
ms.openlocfilehash: 8fde83a82e1c46b8b37cfedea2a202b8d339ea2d
ms.sourcegitcommit: 59e79cf2693cbb550da3e61eb4f68d9e0f57faf6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/09/2020
ms.locfileid: "49607565"
---
# <a name="add-app-to-team"></a><span data-ttu-id="45916-103">向团队添加应用</span><span class="sxs-lookup"><span data-stu-id="45916-103">Add app to team</span></span>

<span data-ttu-id="45916-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="45916-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="45916-105">将 [应用程序](../resources/teamsapp.md) 安装到指定的 [团队](../resources/team.md)。</span><span class="sxs-lookup"><span data-stu-id="45916-105">Install an [app](../resources/teamsapp.md) to the specified [team](../resources/team.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="45916-106">权限</span><span class="sxs-lookup"><span data-stu-id="45916-106">Permissions</span></span>

<span data-ttu-id="45916-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="45916-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="45916-109">权限类型</span><span class="sxs-lookup"><span data-stu-id="45916-109">Permission type</span></span>      | <span data-ttu-id="45916-110">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="45916-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="45916-111">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="45916-111">Delegated (work or school account)</span></span> | <span data-ttu-id="45916-112">TeamsAppInstallation，ReadWriteForTeam，all，All，All</span><span class="sxs-lookup"><span data-stu-id="45916-112">TeamsAppInstallation.ReadWriteForTeam, Group.ReadWrite.All, Directory.ReadWrite.All</span></span> |
|<span data-ttu-id="45916-113">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="45916-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="45916-114">不支持。</span><span class="sxs-lookup"><span data-stu-id="45916-114">Not supported.</span></span>    |
|<span data-ttu-id="45916-115">应用程序</span><span class="sxs-lookup"><span data-stu-id="45916-115">Application</span></span> | <span data-ttu-id="45916-116">TeamsAppInstallation、ReadWriteForTeam、all、ReadWrite。所有</span><span class="sxs-lookup"><span data-stu-id="45916-116">TeamsAppInstallation.ReadWriteForTeam.All, Group.ReadWrite.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="45916-117">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="45916-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{team-id}/installedApps
```

## <a name="request-headers"></a><span data-ttu-id="45916-118">请求标头</span><span class="sxs-lookup"><span data-stu-id="45916-118">Request headers</span></span>

| <span data-ttu-id="45916-119">标头</span><span class="sxs-lookup"><span data-stu-id="45916-119">Header</span></span>       | <span data-ttu-id="45916-120">值</span><span class="sxs-lookup"><span data-stu-id="45916-120">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="45916-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="45916-121">Authorization</span></span>  | <span data-ttu-id="45916-p102">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="45916-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="45916-124">请求正文</span><span class="sxs-lookup"><span data-stu-id="45916-124">Request body</span></span>

| <span data-ttu-id="45916-125">属性</span><span class="sxs-lookup"><span data-stu-id="45916-125">Property</span></span>   | <span data-ttu-id="45916-126">类型</span><span class="sxs-lookup"><span data-stu-id="45916-126">Type</span></span> |<span data-ttu-id="45916-127">Description</span><span class="sxs-lookup"><span data-stu-id="45916-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="45916-128">teamsApp</span><span class="sxs-lookup"><span data-stu-id="45916-128">teamsApp</span></span>|<span data-ttu-id="45916-129">String</span><span class="sxs-lookup"><span data-stu-id="45916-129">String</span></span>|<span data-ttu-id="45916-130">要添加的应用程序的 id。</span><span class="sxs-lookup"><span data-stu-id="45916-130">The id of the app to add.</span></span>|

## <a name="response"></a><span data-ttu-id="45916-131">响应</span><span class="sxs-lookup"><span data-stu-id="45916-131">Response</span></span>

<span data-ttu-id="45916-p103">如果成功，此方法返回 `200 OK` 响应代码。它不在响应正文中返回任何内容。</span><span class="sxs-lookup"><span data-stu-id="45916-p103">If successful, this method returns a `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="45916-134">示例</span><span class="sxs-lookup"><span data-stu-id="45916-134">Example</span></span>

### <a name="request"></a><span data-ttu-id="45916-135">请求</span><span class="sxs-lookup"><span data-stu-id="45916-135">Request</span></span>

<span data-ttu-id="45916-136">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="45916-136">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "add_app_in_team"
}-->
```http
POST /teams/87654321-0abc-zqf0-321456789q/installedApps
Content-type: application/json

{
   "teamsApp@odata.bind":"https://graph.microsoft.com/beta/appCatalogs/teamsApps/12345678-9abc-def0-123456789a"
}
```

### <a name="response"></a><span data-ttu-id="45916-137">响应</span><span class="sxs-lookup"><span data-stu-id="45916-137">Response</span></span>

<span data-ttu-id="45916-138">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="45916-138">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Add teamsApp",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


