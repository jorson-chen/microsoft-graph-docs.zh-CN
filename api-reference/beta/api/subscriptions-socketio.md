---
author: learafa
ms.author: learafa
title: 获取 websocket 终结点
description: 不支持在生产应用程序中使用这些 API。
localization_priority: Normal
ms.prod: sharepoint
doc_type: apiPageType
ms.openlocfilehash: 067fc455a0a122761c45ac1078712ea04b68845c
ms.sourcegitcommit: d6386c5d4bb8917132c3f6c4de945487939b7fb7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "43109186"
---
# <a name="get-websocket-endpoint"></a><span data-ttu-id="ea2b6-103">获取 websocket 终结点</span><span class="sxs-lookup"><span data-stu-id="ea2b6-103">Get websocket endpoint</span></span>

<span data-ttu-id="ea2b6-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="ea2b6-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]
<span data-ttu-id="ea2b6-105">不支持在生产应用程序中使用这些 API。</span><span class="sxs-lookup"><span data-stu-id="ea2b6-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ea2b6-106">允许您使用[socket.io][]接收[驱动器][]和[列表][]的近实时更改通知。</span><span class="sxs-lookup"><span data-stu-id="ea2b6-106">Allows you to receive near-real-time change notifications for a [drive][] and [list][] using [socket.io][].</span></span>
<span data-ttu-id="ea2b6-107">Socket.io 是适用于 JavaScript 的热门通知库，可利用 Websocket。</span><span class="sxs-lookup"><span data-stu-id="ea2b6-107">Socket.io is a popular notifications library for JavaScript that utilizes WebSockets.</span></span> <span data-ttu-id="ea2b6-108">若要了解详细信息，请参阅[socket.io](https://socket.io)。</span><span class="sxs-lookup"><span data-stu-id="ea2b6-108">To learn more, see [socket.io](https://socket.io).</span></span>

[drive]: ../resources/drive.md
[list]: ../resources/list.md
[socket.io]: https://socket.io/

## <a name="permissions"></a><span data-ttu-id="ea2b6-112">权限</span><span class="sxs-lookup"><span data-stu-id="ea2b6-112">Permissions</span></span>

<span data-ttu-id="ea2b6-p102">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="ea2b6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="ea2b6-115">权限类型</span><span class="sxs-lookup"><span data-stu-id="ea2b6-115">Permission type</span></span>                        | <span data-ttu-id="ea2b6-116">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="ea2b6-116">Permissions (from least to most privileged)</span></span>
|:---------------------------------------|:-------------------------------------------
| <span data-ttu-id="ea2b6-117">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="ea2b6-117">Delegated (work or school account)</span></span>     | <span data-ttu-id="ea2b6-118">文件. 读取、文件读写、全部、读写全部。</span><span class="sxs-lookup"><span data-stu-id="ea2b6-118">Files.Read, Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>
| <span data-ttu-id="ea2b6-119">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="ea2b6-119">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ea2b6-120">Read，文件. ReadWrite，全部文件。</span><span class="sxs-lookup"><span data-stu-id="ea2b6-120">Files.Read, Files.ReadWrite, Files.ReadWrite.All</span></span>
| <span data-ttu-id="ea2b6-121">应用程序</span><span class="sxs-lookup"><span data-stu-id="ea2b6-121">Application</span></span>                            | <span data-ttu-id="ea2b6-122">不支持。</span><span class="sxs-lookup"><span data-stu-id="ea2b6-122">Not supported.</span></span>

## <a name="http-request"></a><span data-ttu-id="ea2b6-123">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="ea2b6-123">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /me/drive/root/subscriptions/socketIo
GET /drives/{driveId}/root/subscriptions/socketIo
GET /lists/{list-id}/subscriptions/socketIo
GET /groups/{groupId}/drive/root/subscriptions/socketIo
GET /sites/{siteId}/lists/{listId}/drive/root/subscriptions/socketIo
```

## <a name="example"></a><span data-ttu-id="ea2b6-124">示例</span><span class="sxs-lookup"><span data-stu-id="ea2b6-124">Example</span></span>

### <a name="request"></a><span data-ttu-id="ea2b6-125">请求</span><span class="sxs-lookup"><span data-stu-id="ea2b6-125">Request</span></span>


# <a name="http"></a>[<span data-ttu-id="ea2b6-126">HTTP</span><span class="sxs-lookup"><span data-stu-id="ea2b6-126">HTTP</span></span>](#tab/http)
<!-- { "blockType": "request", "name": "drive_root_subscriptions_socketIo" } -->
```msgraph-interactive
GET /me/drive/root/subscriptions/socketIo
```
# <a name="c"></a>[<span data-ttu-id="ea2b6-127">C#</span><span class="sxs-lookup"><span data-stu-id="ea2b6-127">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/drive-root-subscriptions-socketio-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="ea2b6-128">JavaScript</span><span class="sxs-lookup"><span data-stu-id="ea2b6-128">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/drive-root-subscriptions-socketio-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="ea2b6-129">Objective-C</span><span class="sxs-lookup"><span data-stu-id="ea2b6-129">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/drive-root-subscriptions-socketio-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


### <a name="response"></a><span data-ttu-id="ea2b6-130">响应</span><span class="sxs-lookup"><span data-stu-id="ea2b6-130">Response</span></span>

<span data-ttu-id="ea2b6-131">如果成功，此方法在响应`200 OK`正文中返回响应代码和[订阅](../resources/subscription.md)对象。</span><span class="sxs-lookup"><span data-stu-id="ea2b6-131">If successful, this method returns a `200 OK` response code and a [subscription](../resources/subscription.md) object in the response body.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.subscription"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "id": "opaqueId-fj3hd7yf283jfk193726nvc2w3i2diemdu8",
  "notificationUrl": "https://f3hb0mpua.svc.ms/zbaehwg/callback?snthgk=1ff3-2345672zz831837523"
}
```

<span data-ttu-id="ea2b6-132">`notificationUrl`返回的是 socket.io 终结点 URL。</span><span class="sxs-lookup"><span data-stu-id="ea2b6-132">The `notificationUrl` returned is a socket.io endpoint URL.</span></span>
<span data-ttu-id="ea2b6-133">若要将它与 socket.io 客户端一起使用，请拆分`/callback?`令牌上的字符串。</span><span class="sxs-lookup"><span data-stu-id="ea2b6-133">To use it with a socket.io client, split the string on the `/callback?` token.</span></span>
<span data-ttu-id="ea2b6-134">之前`/callback?`的字符串部分是 socket.io 终结点 URL，后面的字符串部分是必须向库提供的不透明查询字符串。</span><span class="sxs-lookup"><span data-stu-id="ea2b6-134">The part of the string before `/callback?` is the socket.io endpoint URL and the part of the string after is an opaque query string that must be given to the libary.</span></span>

<span data-ttu-id="ea2b6-135">下面的示例演示如何在 JavaScript 中`notificationUrl`将 with socket.io。</span><span class="sxs-lookup"><span data-stu-id="ea2b6-135">The following example shows how to use the `notificationUrl` with socket.io in JavaScript.</span></span>

```javascript
// this is the notificationUrl returned from this API
var notificationUrl = "https://f3hb0mpua.svc.ms/zbaehwg/callback?snthgk=1ff3-2345672zz831837523";

// after the split, split[0] will be everything leading up to '/callback?' and split[1] will be everything after.
var split = notificationUrl.split("/callback?");

// 'io' comes from the socket.io client library
var socket = io(split[0], { query: split[1] });

// these examples log to the console.
// your app would provide its own callbacks
socket.on("connect", ()=>console.log("Connected!"));
socket.on("notification", (data)=>console.log("Notification!", data));
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79 
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Example",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->