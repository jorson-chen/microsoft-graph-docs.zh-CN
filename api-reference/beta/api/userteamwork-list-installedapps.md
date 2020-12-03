---
title: 列出为用户安装的应用
description: 检索在指定用户的个人范围内安装的应用列表。
author: clearab
doc_type: apiPageType
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 41367caeeca0b323a774d21c63d4431bf21e1201
ms.sourcegitcommit: 958b540f118ef3ce64d4d4e96b29264e2b56d703
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/03/2020
ms.locfileid: "49564155"
---
# <a name="list-apps-installed-for-user"></a><span data-ttu-id="2d40c-103">列出为用户安装的应用</span><span class="sxs-lookup"><span data-stu-id="2d40c-103">List apps installed for user</span></span>

<span data-ttu-id="2d40c-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="2d40c-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="2d40c-105">检索在指定[用户](../resources/user.md)的个人作用域中安装的[应用程序](../resources/teamsappinstallation.md)的列表。</span><span class="sxs-lookup"><span data-stu-id="2d40c-105">Retrieve the list of [apps](../resources/teamsappinstallation.md) installed in the personal scope of the specified [user](../resources/user.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="2d40c-106">权限</span><span class="sxs-lookup"><span data-stu-id="2d40c-106">Permissions</span></span>

<span data-ttu-id="2d40c-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="2d40c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2d40c-109">权限类型</span><span class="sxs-lookup"><span data-stu-id="2d40c-109">Permission type</span></span>      | <span data-ttu-id="2d40c-110">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="2d40c-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2d40c-111">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="2d40c-111">Delegated (work or school account)</span></span> | <span data-ttu-id="2d40c-112">TeamsAppInstallation、ReadForUser、ReadWriteForUser</span><span class="sxs-lookup"><span data-stu-id="2d40c-112">TeamsAppInstallation.ReadForUser, TeamsAppInstallation.ReadWriteForUser</span></span> |
|<span data-ttu-id="2d40c-113">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="2d40c-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2d40c-114">不支持。</span><span class="sxs-lookup"><span data-stu-id="2d40c-114">Not supported.</span></span>    |
|<span data-ttu-id="2d40c-115">应用程序</span><span class="sxs-lookup"><span data-stu-id="2d40c-115">Application</span></span> | <span data-ttu-id="2d40c-116">TeamsAppInstallation、ReadForUser、TeamsAppInstallation</span><span class="sxs-lookup"><span data-stu-id="2d40c-116">TeamsAppInstallation.ReadForUser.All, TeamsAppInstallation.ReadWriteForUser.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="2d40c-117">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="2d40c-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /users/{id}/teamwork/installedApps
```

## <a name="optional-query-parameters"></a><span data-ttu-id="2d40c-118">可选的查询参数</span><span class="sxs-lookup"><span data-stu-id="2d40c-118">Optional query parameters</span></span>

<span data-ttu-id="2d40c-119">此方法支持 $filter、$select 和 $expand [OData 查询参数](/graph/query-parameters)来帮助自定义响应。</span><span class="sxs-lookup"><span data-stu-id="2d40c-119">This method supports the $filter, $select, and $expand [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="2d40c-120">请求标头</span><span class="sxs-lookup"><span data-stu-id="2d40c-120">Request headers</span></span>

| <span data-ttu-id="2d40c-121">标头</span><span class="sxs-lookup"><span data-stu-id="2d40c-121">Header</span></span>       | <span data-ttu-id="2d40c-122">值</span><span class="sxs-lookup"><span data-stu-id="2d40c-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="2d40c-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="2d40c-123">Authorization</span></span>  | <span data-ttu-id="2d40c-p102">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="2d40c-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="2d40c-126">请求正文</span><span class="sxs-lookup"><span data-stu-id="2d40c-126">Request body</span></span>

<span data-ttu-id="2d40c-127">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="2d40c-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2d40c-128">响应</span><span class="sxs-lookup"><span data-stu-id="2d40c-128">Response</span></span>

<span data-ttu-id="2d40c-129">如果成功，此方法 `200 OK` 在响应正文中返回响应代码和 [teamsAppInstallation](../resources/teamsappinstallation.md) 对象集合。</span><span class="sxs-lookup"><span data-stu-id="2d40c-129">If successful, this method returns a `200 OK` response code and a collection of [teamsAppInstallation](../resources/teamsappinstallation.md) objects in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="2d40c-130">示例</span><span class="sxs-lookup"><span data-stu-id="2d40c-130">Examples</span></span>

### <a name="example-1-list-apps-installed-for-the-specified-user"></a><span data-ttu-id="2d40c-131">示例1：列出为指定用户安装的应用程序</span><span class="sxs-lookup"><span data-stu-id="2d40c-131">Example 1: List apps installed for the specified user</span></span>

#### <a name="request"></a><span data-ttu-id="2d40c-132">请求</span><span class="sxs-lookup"><span data-stu-id="2d40c-132">Request</span></span>

<span data-ttu-id="2d40c-133">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="2d40c-133">The following is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="2d40c-134">HTTP</span><span class="sxs-lookup"><span data-stu-id="2d40c-134">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "user_list_teamsApps"
}-->
```msgraph-interactive
GET https://graph.microsoft.com/beta/users/{id}/teamwork/installedApps
```
# <a name="c"></a>[<span data-ttu-id="2d40c-135">C#</span><span class="sxs-lookup"><span data-stu-id="2d40c-135">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/user-list-teamsapps-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="2d40c-136">JavaScript</span><span class="sxs-lookup"><span data-stu-id="2d40c-136">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/user-list-teamsapps-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="2d40c-137">Objective-C</span><span class="sxs-lookup"><span data-stu-id="2d40c-137">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/user-list-teamsapps-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[<span data-ttu-id="2d40c-138">Java</span><span class="sxs-lookup"><span data-stu-id="2d40c-138">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/user-list-teamsapps-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


#### <a name="response"></a><span data-ttu-id="2d40c-139">响应</span><span class="sxs-lookup"><span data-stu-id="2d40c-139">Response</span></span>

<span data-ttu-id="2d40c-140">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="2d40c-140">The following is an example of the response.</span></span>
><span data-ttu-id="2d40c-p103">**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。所有属性都将通过实际调用返回。</span><span class="sxs-lookup"><span data-stu-id="2d40c-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "name": "user_list_teamsApps",
  "truncated": true,
  "@odata.type": "microsoft.graph.teamsAppInstallation",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "id": "id-value"
    }
  ]
}
```
### <a name="example-2-get-the-names-and-other-details-of-apps-installed-for-the-user"></a><span data-ttu-id="2d40c-143">示例2：获取为用户安装的应用程序的名称和其他详细信息</span><span class="sxs-lookup"><span data-stu-id="2d40c-143">Example 2: Get the names and other details of apps installed for the user</span></span>

#### <a name="request"></a><span data-ttu-id="2d40c-144">请求</span><span class="sxs-lookup"><span data-stu-id="2d40c-144">Request</span></span>

<span data-ttu-id="2d40c-145">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="2d40c-145">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "user_list_teamsApps_details"
}-->
```http
GET https://graph.microsoft.com/beta/users/{id}/teamwork/installedApps?$expand=teamsAppDefinition
```

#### <a name="response"></a><span data-ttu-id="2d40c-146">响应</span><span class="sxs-lookup"><span data-stu-id="2d40c-146">Response</span></span>

<span data-ttu-id="2d40c-147">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="2d40c-147">The following is an example of the response.</span></span>

><span data-ttu-id="2d40c-p104">**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。所有属性都将通过实际调用返回。</span><span class="sxs-lookup"><span data-stu-id="2d40c-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "name": "user_list_teamsApps_details",
  "truncated": true,
  "@odata.type": "microsoft.graph.teamsAppInstallation",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
        {
            "id": "NjRiOWM3NDYtYjE1NS00MDQyLThkNDctOTQxYmQzODE2ODFiIyMwZDgyMGVjZC1kZWYyLTQyOTctYWRhZC03ODA1NmNkZTdjNzg=",
            "teamsAppDefinition": {
                "id": "MGQ4MjBlY2QtZGVmMi00Mjk3LWFkYWQtNzgwNTZjZGU3Yzc4IyMxLjAuMA==",
                "teamsAppId": "0d820ecd-def2-4297-adad-78056cde7c78",
                "displayName": "OneNote",
                "version": "1.0.0"
            }
        },
        {
            "id": "NjRiOWM3NDYtYjE1NS00MDQyLThkNDctOTQxYmQzODE2ODFiIyMwZmQ5MjVhMC0zNTdmLTRkMjUtODQ1Ni1iMzAyMmFhYTQxYTk=",
            "teamsAppDefinition": {
                "id": "MGZkOTI1YTAtMzU3Zi00ZDI1LTg0NTYtYjMwMjJhYWE0MWE5IyMxLjc=",
                "teamsAppId": "0fd925a0-357f-4d25-8456-b3022aaa41a9",
                "displayName": "SurveyMonkey",
                "version": "1.7"
            }
        },
        {
            "id": "NjRiOWM3NDYtYjE1NS00MDQyLThkNDctOTQxYmQzODE2ODFiIyMyYTUyNzcwMy0xZjZmLTQ1NTktYTMzMi1kOGE3ZDI4OGNkODg=",
            "teamsAppDefinition": {
                "id": "MmE1Mjc3MDMtMWY2Zi00NTU5LWEzMzItZDhhN2QyODhjZDg4IyMxLjA=",
                "teamsAppId": "2a527703-1f6f-4559-a332-d8a7d288cd88",
                "displayName": "SharePoint",
                "version": "1.0"
            }
        }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "User list teamsAppInstallations",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


