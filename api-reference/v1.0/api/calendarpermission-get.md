---
title: 获取 calendarPermission
description: 获取 calendarpermission 对象的属性和关系。
localization_priority: Normal
author: sochowdh
ms.prod: outlook
doc_type: apiPageType
ms.openlocfilehash: d319d45ce3ee50f113e711729bc9c0ae71081e6a
ms.sourcegitcommit: 9a6ce4ddf75beead19b7c35a1949cf4d105b9b29
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/11/2020
ms.locfileid: "43229109"
---
# <a name="get-calendarpermission"></a><span data-ttu-id="4d7ba-103">获取 calendarPermission</span><span class="sxs-lookup"><span data-stu-id="4d7ba-103">Get calendarPermission</span></span>

<span data-ttu-id="4d7ba-104">获取已共享的用户或组日历的指定权限对象。</span><span class="sxs-lookup"><span data-stu-id="4d7ba-104">Get the specified permissions object of a user or group calendar that has been shared.</span></span>

## <a name="permissions"></a><span data-ttu-id="4d7ba-105">权限</span><span class="sxs-lookup"><span data-stu-id="4d7ba-105">Permissions</span></span>

<span data-ttu-id="4d7ba-106">根据事件所处日历类型和所请求的权限类型（委派型或应用程序），需要下列某一权限来调用此 API。</span><span class="sxs-lookup"><span data-stu-id="4d7ba-106">Depending on the type of calendar that the event is in and the permission type (delegated or application) requested, one of the following permissions is required to call this API.</span></span> <span data-ttu-id="4d7ba-107">要了解详细信息（包括如何选择权限），请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="4d7ba-107">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="4d7ba-108">日历</span><span class="sxs-lookup"><span data-stu-id="4d7ba-108">Calendar</span></span> | <span data-ttu-id="4d7ba-109">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="4d7ba-109">Delegated (work or school account)</span></span> | <span data-ttu-id="4d7ba-110">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="4d7ba-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4d7ba-111">应用程序</span><span class="sxs-lookup"><span data-stu-id="4d7ba-111">Application</span></span> |
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4d7ba-112">用户日历</span><span class="sxs-lookup"><span data-stu-id="4d7ba-112">user calendar</span></span> | <span data-ttu-id="4d7ba-113">Calendars.Read、Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4d7ba-113">Calendars.Read, Calendars.ReadWrite</span></span> | <span data-ttu-id="4d7ba-114">Calendars.Read、Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4d7ba-114">Calendars.Read, Calendars.ReadWrite</span></span> | <span data-ttu-id="4d7ba-115">Calendars.Read、Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4d7ba-115">Calendars.Read, Calendars.ReadWrite</span></span> |
| <span data-ttu-id="4d7ba-116">组日历</span><span class="sxs-lookup"><span data-stu-id="4d7ba-116">group calendar</span></span> | <span data-ttu-id="4d7ba-117">Group.Read.All、Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4d7ba-117">Group.Read.All, Group.ReadWrite.All</span></span> | <span data-ttu-id="4d7ba-118">不支持。</span><span class="sxs-lookup"><span data-stu-id="4d7ba-118">Not supported.</span></span> | <span data-ttu-id="4d7ba-119">不支持。</span><span class="sxs-lookup"><span data-stu-id="4d7ba-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="4d7ba-120">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="4d7ba-120">HTTP request</span></span>

<span data-ttu-id="4d7ba-121">获取用户的主日历的指定权限：</span><span class="sxs-lookup"><span data-stu-id="4d7ba-121">Get the specified permissions of a user's primary calendar:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id}/calendar/calendarPermissions/{id}
```

<span data-ttu-id="4d7ba-122">获取组日历的指定权限：</span><span class="sxs-lookup"><span data-stu-id="4d7ba-122">Get the specified permissions of a group calendar:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/calendar/calendarPermissions/{id}
```

<span data-ttu-id="4d7ba-123">获取包含标识的事件的用户日历的指定权限：</span><span class="sxs-lookup"><span data-stu-id="4d7ba-123">Get the specified permissions of the user calendar that contains the identified event:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id}/events/{id}/calendar/calendarPermissions/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="4d7ba-124">可选的查询参数</span><span class="sxs-lookup"><span data-stu-id="4d7ba-124">Optional query parameters</span></span>

<span data-ttu-id="4d7ba-125">此方法支持一些 OData 查询参数来帮助自定义响应。</span><span class="sxs-lookup"><span data-stu-id="4d7ba-125">This method supports some of the OData query parameters to help customize the response.</span></span> <span data-ttu-id="4d7ba-126">有关一般信息，请参阅[OData 查询参数](/graph/query-parameters)。</span><span class="sxs-lookup"><span data-stu-id="4d7ba-126">For general information, see [OData query parameters](/graph/query-parameters).</span></span>

## <a name="request-headers"></a><span data-ttu-id="4d7ba-127">请求头</span><span class="sxs-lookup"><span data-stu-id="4d7ba-127">Request headers</span></span>

| <span data-ttu-id="4d7ba-128">名称</span><span class="sxs-lookup"><span data-stu-id="4d7ba-128">Name</span></span>      |<span data-ttu-id="4d7ba-129">说明</span><span class="sxs-lookup"><span data-stu-id="4d7ba-129">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="4d7ba-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="4d7ba-130">Authorization</span></span> | <span data-ttu-id="4d7ba-131">持有者 {token}</span><span class="sxs-lookup"><span data-stu-id="4d7ba-131">Bearer {token}</span></span> |

## <a name="request-body"></a><span data-ttu-id="4d7ba-132">请求正文</span><span class="sxs-lookup"><span data-stu-id="4d7ba-132">Request body</span></span>

<span data-ttu-id="4d7ba-133">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="4d7ba-133">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4d7ba-134">响应</span><span class="sxs-lookup"><span data-stu-id="4d7ba-134">Response</span></span>

<span data-ttu-id="4d7ba-135">如果成功，此方法在响应`200 OK`正文中返回响应代码和请求的[calendarPermission](../resources/calendarpermission.md)对象。</span><span class="sxs-lookup"><span data-stu-id="4d7ba-135">If successful, this method returns a `200 OK` response code and the requested [calendarPermission](../resources/calendarpermission.md) object in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="4d7ba-136">示例</span><span class="sxs-lookup"><span data-stu-id="4d7ba-136">Examples</span></span>

### <a name="request"></a><span data-ttu-id="4d7ba-137">请求</span><span class="sxs-lookup"><span data-stu-id="4d7ba-137">Request</span></span>

<span data-ttu-id="4d7ba-138">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="4d7ba-138">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_calendarpermission"
}-->

```msgraph-interactive
GET https://graph.microsoft.com/v1.0/users/{id}/calendar/calendarPermissions/{id}
```

### <a name="response"></a><span data-ttu-id="4d7ba-139">响应</span><span class="sxs-lookup"><span data-stu-id="4d7ba-139">Response</span></span>

<span data-ttu-id="4d7ba-140">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="4d7ba-140">The following is an example of the response.</span></span>

> <span data-ttu-id="4d7ba-p103">**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。所有属性都将通过实际调用返回。</span><span class="sxs-lookup"><span data-stu-id="4d7ba-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendarPermission"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "emailAddress": {
    "name": "My Organization",
  },
  "isRemovable": true,
  "isInsideOrganization": true,
  "role": "write",
  "allowedRoles": [
    "none",
    "freeBusyRead",
    "limitedRead",
    "read",
    "write"
  ],
  "id": "RGVmYXVsdA=="
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get calendarPermission",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->