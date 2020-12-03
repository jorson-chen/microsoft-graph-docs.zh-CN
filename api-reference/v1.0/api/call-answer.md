---
title: 呼叫：应答
description: 应答传入呼叫。
author: ananmishr
localization_priority: Normal
ms.prod: cloud-communications
doc_type: apiPageType
ms.openlocfilehash: 50e2405f6fd0c093e6dc5f3ebaa48eea969d2990
ms.sourcegitcommit: 958b540f118ef3ce64d4d4e96b29264e2b56d703
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/03/2020
ms.locfileid: "49563917"
---
# <a name="call-answer"></a><span data-ttu-id="db06f-103">呼叫：应答</span><span class="sxs-lookup"><span data-stu-id="db06f-103">call: answer</span></span>

<span data-ttu-id="db06f-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="db06f-104">Namespace: microsoft.graph</span></span>

<span data-ttu-id="db06f-105">使机器人能够应答传入 [呼叫](../resources/call.md)。</span><span class="sxs-lookup"><span data-stu-id="db06f-105">Enable a bot to answer an incoming [call](../resources/call.md).</span></span> <span data-ttu-id="db06f-106">传入呼叫请求可以是来自组呼叫或对等呼叫中参与者的邀请。</span><span class="sxs-lookup"><span data-stu-id="db06f-106">The incoming call request can be an invite from a participant in a group call or a peer-to-peer call.</span></span> <span data-ttu-id="db06f-107">如果收到某个组呼叫邀请，则通知将包含 [chatInfo](../resources/chatinfo.md) 和 [meetingInfo](../resources/meetinginfo.md) 参数。</span><span class="sxs-lookup"><span data-stu-id="db06f-107">If an invite to a group call is received, the notification will contain the [chatInfo](../resources/chatinfo.md) and [meetingInfo](../resources/meetinginfo.md) parameters.</span></span>

<span data-ttu-id="db06f-108">在呼叫超时之前，机器人应应答、 [拒绝](./call-reject.md)或 [重定向](./call-redirect.md) 呼叫。对于常规方案，当前超时值为15秒，而基于策略的录制方案为5秒。</span><span class="sxs-lookup"><span data-stu-id="db06f-108">The bot is expected to answer, [reject](./call-reject.md), or [redirect](./call-redirect.md) the call before the call times out. The current timeout value is 15 seconds for regular scenarios, and 5 seconds for policy-based recording scenarios.</span></span>

## <a name="permissions"></a><span data-ttu-id="db06f-109">权限</span><span class="sxs-lookup"><span data-stu-id="db06f-109">Permissions</span></span>
<span data-ttu-id="db06f-110">您无需任何权限即可应答对等呼叫。</span><span class="sxs-lookup"><span data-stu-id="db06f-110">You do not need any permissions to answer a peer-to-peer call.</span></span> <span data-ttu-id="db06f-111">若要加入组呼叫，您需要以下权限之一。</span><span class="sxs-lookup"><span data-stu-id="db06f-111">You need one of the following permissions to join a group call.</span></span> <span data-ttu-id="db06f-112">若要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="db06f-112">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="db06f-113">权限类型</span><span class="sxs-lookup"><span data-stu-id="db06f-113">Permission type</span></span> | <span data-ttu-id="db06f-114">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="db06f-114">Permissions (from least to most privileged)</span></span>                 |
| :-------------- | :-----------------------------------------------------------|
| <span data-ttu-id="db06f-115">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="db06f-115">Delegated (work or school account)</span></span>     | <span data-ttu-id="db06f-116">不支持</span><span class="sxs-lookup"><span data-stu-id="db06f-116">Not Supported</span></span>                        |
| <span data-ttu-id="db06f-117">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="db06f-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="db06f-118">不支持</span><span class="sxs-lookup"><span data-stu-id="db06f-118">Not Supported</span></span>                        |
| <span data-ttu-id="db06f-119">应用程序</span><span class="sxs-lookup"><span data-stu-id="db06f-119">Application</span></span>     | <span data-ttu-id="db06f-120">JoinGroupCalls 或 JoinGroupCallsasGuest 的所有请求。</span><span class="sxs-lookup"><span data-stu-id="db06f-120">Calls.JoinGroupCalls.All or Calls.JoinGroupCallsasGuest.All</span></span> |

> <span data-ttu-id="db06f-121">**注意：** 对于使用应用程序托管媒体的呼叫，您还需要 AccessMedia 权限。</span><span class="sxs-lookup"><span data-stu-id="db06f-121">**Note:** For a call that uses application-hosted media, you also need the Calls.AccessMedia.All permission.</span></span> <span data-ttu-id="db06f-122">您必须至少具有以下权限之一，才能确保 `source` 传入呼叫通知中的解密： AccessMedia、Calls.Initiate。All，Calls.InitiateGroupCall、JoinGroupCall、JoinGroupCallAsGuest、all。</span><span class="sxs-lookup"><span data-stu-id="db06f-122">You must have at least one of the following permissions to ensure that the `source` in the incoming call notification is decrypted: Calls.AccessMedia.All, Calls.Initiate.All, Calls.InitiateGroupCall.All, Calls.JoinGroupCall.All, Calls.JoinGroupCallAsGuest.All.</span></span> <span data-ttu-id="db06f-123">`source`是传入呼叫通知中的呼叫者信息。</span><span class="sxs-lookup"><span data-stu-id="db06f-123">The `source` is the caller info in the incoming call notification.</span></span> <span data-ttu-id="db06f-124">如果至少缺少其中一个权限，则 `source` 将保持加密。</span><span class="sxs-lookup"><span data-stu-id="db06f-124">Without at least one of these permissions, the `source` will remain encrypted.</span></span>

## <a name="http-request"></a><span data-ttu-id="db06f-125">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="db06f-125">HTTP request</span></span>
<!-- {"blockType": "ignored" } -->
```http
POST /communications/calls/{id}/answer
```

## <a name="request-headers"></a><span data-ttu-id="db06f-126">请求标头</span><span class="sxs-lookup"><span data-stu-id="db06f-126">Request headers</span></span>
| <span data-ttu-id="db06f-127">名称</span><span class="sxs-lookup"><span data-stu-id="db06f-127">Name</span></span>          | <span data-ttu-id="db06f-128">说明</span><span class="sxs-lookup"><span data-stu-id="db06f-128">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="db06f-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="db06f-129">Authorization</span></span> | <span data-ttu-id="db06f-p104">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="db06f-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="db06f-132">Content-type</span><span class="sxs-lookup"><span data-stu-id="db06f-132">Content-type</span></span>  | <span data-ttu-id="db06f-p105">application/json. Required.</span><span class="sxs-lookup"><span data-stu-id="db06f-p105">application/json. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="db06f-135">请求正文</span><span class="sxs-lookup"><span data-stu-id="db06f-135">Request body</span></span>
<span data-ttu-id="db06f-136">在请求正文中，提供具有以下参数的 JSON 对象。</span><span class="sxs-lookup"><span data-stu-id="db06f-136">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="db06f-137">参数</span><span class="sxs-lookup"><span data-stu-id="db06f-137">Parameter</span></span>        | <span data-ttu-id="db06f-138">类型</span><span class="sxs-lookup"><span data-stu-id="db06f-138">Type</span></span>                                     |<span data-ttu-id="db06f-139">说明</span><span class="sxs-lookup"><span data-stu-id="db06f-139">Description</span></span>                                                                                                                                    |
|:-----------------|:-----------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
|<span data-ttu-id="db06f-140">callbackUri</span><span class="sxs-lookup"><span data-stu-id="db06f-140">callbackUri</span></span>       |<span data-ttu-id="db06f-141">String</span><span class="sxs-lookup"><span data-stu-id="db06f-141">String</span></span>                                    |<span data-ttu-id="db06f-142">允许 bot 为当前呼叫提供特定的回调 URI，以接收后续通知。</span><span class="sxs-lookup"><span data-stu-id="db06f-142">Allows bots to provide a specific callback URI for the current call to receive later notifications.</span></span> <span data-ttu-id="db06f-143">如果尚未设置此属性，则将改为使用 bot 的全局回调 URI。</span><span class="sxs-lookup"><span data-stu-id="db06f-143">If this property has not been set, the bot's global callback URI will be used instead.</span></span> <span data-ttu-id="db06f-144">这必须是 `https` 。</span><span class="sxs-lookup"><span data-stu-id="db06f-144">This must be `https`.</span></span>    |
|<span data-ttu-id="db06f-145">acceptedModalities</span><span class="sxs-lookup"><span data-stu-id="db06f-145">acceptedModalities</span></span>|<span data-ttu-id="db06f-146">字符串集合</span><span class="sxs-lookup"><span data-stu-id="db06f-146">String collection</span></span>                         |<span data-ttu-id="db06f-147">接受形式的列表。</span><span class="sxs-lookup"><span data-stu-id="db06f-147">The list of accept modalities.</span></span> <span data-ttu-id="db06f-148">可取值为：`audio`、`video`、`videoBasedScreenSharing`。</span><span class="sxs-lookup"><span data-stu-id="db06f-148">Possible values are: `audio`, `video`, `videoBasedScreenSharing`.</span></span> <span data-ttu-id="db06f-149">应答呼叫的必选。</span><span class="sxs-lookup"><span data-stu-id="db06f-149">Required for answering a call.</span></span> |
|<span data-ttu-id="db06f-150">mediaConfig</span><span class="sxs-lookup"><span data-stu-id="db06f-150">mediaConfig</span></span>       | <span data-ttu-id="db06f-151">[appHostedMediaConfig](../resources/apphostedmediaconfig.md) 或 [serviceHostedMediaConfig](../resources/servicehostedmediaconfig.md)</span><span class="sxs-lookup"><span data-stu-id="db06f-151">[appHostedMediaConfig](../resources/apphostedmediaconfig.md) or [serviceHostedMediaConfig](../resources/servicehostedmediaconfig.md)</span></span> |<span data-ttu-id="db06f-152">媒体配置。</span><span class="sxs-lookup"><span data-stu-id="db06f-152">The media configuration.</span></span> <span data-ttu-id="db06f-153"> (必需的) </span><span class="sxs-lookup"><span data-stu-id="db06f-153">(Required)</span></span>                                                                                                            |

## <a name="response"></a><span data-ttu-id="db06f-154">响应</span><span class="sxs-lookup"><span data-stu-id="db06f-154">Response</span></span>
<span data-ttu-id="db06f-155">此方法返回 `202 Accepted` 响应代码。</span><span class="sxs-lookup"><span data-stu-id="db06f-155">This method returns a `202 Accepted` response code.</span></span>

## <a name="examples"></a><span data-ttu-id="db06f-156">示例</span><span class="sxs-lookup"><span data-stu-id="db06f-156">Examples</span></span>
<span data-ttu-id="db06f-157">以下示例演示如何调用此 API。</span><span class="sxs-lookup"><span data-stu-id="db06f-157">The following example shows how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="db06f-158">请求</span><span class="sxs-lookup"><span data-stu-id="db06f-158">Request</span></span>
<span data-ttu-id="db06f-159">下面为请求示例。</span><span class="sxs-lookup"><span data-stu-id="db06f-159">The following example shows the request.</span></span>


# <a name="http"></a>[<span data-ttu-id="db06f-160">HTTP</span><span class="sxs-lookup"><span data-stu-id="db06f-160">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "call-answer"
}-->
```http
POST https://graph.microsoft.com/v1.0/communications/calls/{id}/answer
Content-Type: application/json
Content-Length: 211

{
  "callbackUri": "callbackUri-value",
  "mediaConfig": {
    "@odata.type": "#microsoft.graph.appHostedMediaConfig",
    "blob": "<Media Session Configuration Blob>"
  },
  "acceptedModalities": [
    "audio"
  ]
}
```
<span data-ttu-id="db06f-161">此 blob 是从媒体 SDK 生成的媒体会话的序列化配置。</span><span class="sxs-lookup"><span data-stu-id="db06f-161">This blob is the serialized configuration for media sessions which is generated from the media SDK.</span></span>

# <a name="c"></a>[<span data-ttu-id="db06f-162">C#</span><span class="sxs-lookup"><span data-stu-id="db06f-162">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/call-answer-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="db06f-163">JavaScript</span><span class="sxs-lookup"><span data-stu-id="db06f-163">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/call-answer-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="db06f-164">Objective-C</span><span class="sxs-lookup"><span data-stu-id="db06f-164">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/call-answer-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[<span data-ttu-id="db06f-165">Java</span><span class="sxs-lookup"><span data-stu-id="db06f-165">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/call-answer-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a><span data-ttu-id="db06f-166">响应</span><span class="sxs-lookup"><span data-stu-id="db06f-166">Response</span></span>
<span data-ttu-id="db06f-167">下面是一个响应示例。</span><span class="sxs-lookup"><span data-stu-id="db06f-167">Here is an example of the response.</span></span> 

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->
```http
HTTP/1.1 202 Accepted
```

### <a name="example-1-answer-a-peer-to-peer-voip-call-with-service-hosted-media"></a><span data-ttu-id="db06f-168">示例1：使用服务托管媒体应答对等 VoIP 呼叫</span><span class="sxs-lookup"><span data-stu-id="db06f-168">Example 1: Answer a Peer-to-Peer VoIP call with service hosted media</span></span>

##### <a name="notification---incoming"></a><span data-ttu-id="db06f-169">通知传入</span><span class="sxs-lookup"><span data-stu-id="db06f-169">Notification - incoming</span></span>

```http
POST https://bot.contoso.com/api/calls
Content-Type: application/json
```

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.commsNotifications"
}-->
```json
{
  "@odata.type": "#microsoft.graph.commsNotifications",
  "value": [
    {
      "@odata.type": "#microsoft.graph.commsNotification",
      "changeType": "created",
      "resourceUrl": "/communications/calls/57DAB8B1894C409AB240BD8BEAE78896",
      "resourceData": {
        "@odata.type": "#microsoft.graph.call",
        "@odata.id": "/communications/calls/57DAB8B1894C409AB240BD8BEAE78896",
        "@odata.etag": "W/\"5445\"",
        "state": "incoming",
        "direction": "incoming",
        "source": {
          "identity": {
            "user": {
              "displayName": "Test User",
              "id": "8A34A46B-3D17-4ADC-8DCE-DC4E7D572698"
            }
          },
          "region": "westus",
          "languageId": "en-US"
        },
        "targets": [
          {
            "identity": {
              "application": {
                "displayName": "Test BOT",
                "id": "8A34A46B-3D17-4ADC-8DCE-DC4E7D572698"
              }
            }
          }
        ],
        "requestedModalities": [ "audio" ]
      }
    }
  ]
}
```

##### <a name="request"></a><span data-ttu-id="db06f-170">请求</span><span class="sxs-lookup"><span data-stu-id="db06f-170">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "call-answer-service-hosted-media"
}-->
```http
POST /communications/calls/57DAB8B1894C409AB240BD8BEAE78896/answer
Content-Type: application/json

{
  "callbackUri": "https://bot.contoso.com/api/calls",
  "acceptedModalities": [ "audio" ],
  "mediaConfig": {
    "@odata.type": "#microsoft.graph.serviceHostedMediaConfig",
    "preFetchMedia": [
      {
        "uri": "https://cdn.contoso.com/beep.wav",
        "resourceId": "1D6DE2D4-CD51-4309-8DAA-70768651088E"
      },
      {
        "uri": "https://cdn.contoso.com/cool.wav",
        "resourceId": "1D6DE2D4-CD51-4309-8DAA-70768651088F"
      }
    ]
  }
}
```

##### <a name="response"></a><span data-ttu-id="db06f-171">响应</span><span class="sxs-lookup"><span data-stu-id="db06f-171">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->
```http
HTTP/1.1 202 Accepted
```

##### <a name="notification---establishing"></a><span data-ttu-id="db06f-172">通知-建立</span><span class="sxs-lookup"><span data-stu-id="db06f-172">Notification - establishing</span></span>

```http
POST https://bot.contoso.com/api/calls
Content-Type: application/json
```

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.commsNotifications"
}-->
```json
{
  "@odata.type": "#microsoft.graph.commsNotifications",
  "value": [
    {
      "@odata.type": "#microsoft.graph.commsNotification",
      "changeType": "updated",
      "resourceUrl": "/communications/calls/57DAB8B1894C409AB240BD8BEAE78896",
      "resourceData": {
        "@odata.type": "#microsoft.graph.call",
        "@odata.id": "/communications/calls/57DAB8B1894C409AB240BD8BEAE78896",
        "@odata.etag": "W/\"5445\"",
        "state": "establishing"
      }
    }
  ]
}
```

##### <a name="notification---established"></a><span data-ttu-id="db06f-173">已建立通知</span><span class="sxs-lookup"><span data-stu-id="db06f-173">Notification - established</span></span>

```http
POST https://bot.contoso.com/api/calls
Content-Type: application/json
```

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.commsNotifications"
}-->
```json
{
  "@odata.type": "#microsoft.graph.commsNotifications",
  "value": [
    {
      "@odata.type": "#microsoft.graph.commsNotification",
      "changeType": "updated",
      "resourceUrl": "/communications/calls/57DAB8B1894C409AB240BD8BEAE78896",
      "resourceData": {
        "@odata.type": "#microsoft.graph.call",
        "@odata.id": "/communications/calls/57DAB8B1894C409AB240BD8BEAE78896",
        "@odata.etag": "W/\"5445\"",
        "state": "established"
      }
    }
  ]
}
```

### <a name="example-2-answer-voip-call-with-application-hosted-media"></a><span data-ttu-id="db06f-174">示例2：使用应用程序托管媒体应答 VOIP 呼叫</span><span class="sxs-lookup"><span data-stu-id="db06f-174">Example 2: Answer VOIP call with application hosted media</span></span>

##### <a name="notification---incoming"></a><span data-ttu-id="db06f-175">通知传入</span><span class="sxs-lookup"><span data-stu-id="db06f-175">Notification - incoming</span></span>

```http
POST https://bot.contoso.com/api/calls
Content-Type: application/json
```

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.commsNotifications"
}-->
```json
{
  "@odata.type": "#microsoft.graph.commsNotifications",
  "value": [
    {
      "@odata.type": "#microsoft.graph.commsNotification",
      "changeType": "created",
      "resourceUrl": "/communications/calls/57DAB8B1894C409AB240BD8BEAE78896",
      "resourceData": {
        "@odata.type": "#microsoft.graph.call",
        "@odata.id": "/communications/calls/57DAB8B1894C409AB240BD8BEAE78896",
        "@odata.etag": "W/\"5445\"",
        "state": "incoming",
        "direction": "incoming",
        "source": {
          "@odata.type": "#microsoft.graph.participantInfo",
          "identity": {
            "user": {
              "displayName": "Test User",
              "id": "8A34A46B-3D17-4ADC-8DCE-DC4E7D572698"
            }
          },
          "region": "westus",
          "languageId": "en-US"
        },
        "targets": [
          {
            "@odata.type": "#microsoft.graph.invitationParticipantInfo",
            "identity": {
              "application": {
                "displayName": "Test BOT",
                "id": "8A34A46B-3D17-4ADC-8DCE-DC4E7D572698"
              }
            }
          }
        ],
        "requestedModalities": [ "audio" ]
      }
    }
  ]
}
```

##### <a name="request"></a><span data-ttu-id="db06f-176">请求</span><span class="sxs-lookup"><span data-stu-id="db06f-176">Request</span></span>


# <a name="http"></a>[<span data-ttu-id="db06f-177">HTTP</span><span class="sxs-lookup"><span data-stu-id="db06f-177">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "call-answer-app-hosted-media"
}-->
```http
POST /communications/calls/57DAB8B1894C409AB240BD8BEAE78896/answer
Content-Type: application/json

{
  "callbackUri": "https://bot.contoso.com/api/calls",
  "acceptedModalities": [ "audio" ],
  "mediaConfig": {
    "@odata.type": "#microsoft.graph.appHostedMediaConfig",
    "blob": "<Media Session Configuration Blob>"
  }
}
```
# <a name="c"></a>[<span data-ttu-id="db06f-178">C#</span><span class="sxs-lookup"><span data-stu-id="db06f-178">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/call-answer-app-hosted-media-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="db06f-179">JavaScript</span><span class="sxs-lookup"><span data-stu-id="db06f-179">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/call-answer-app-hosted-media-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="db06f-180">Objective-C</span><span class="sxs-lookup"><span data-stu-id="db06f-180">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/call-answer-app-hosted-media-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[<span data-ttu-id="db06f-181">Java</span><span class="sxs-lookup"><span data-stu-id="db06f-181">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/call-answer-app-hosted-media-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a><span data-ttu-id="db06f-182">响应</span><span class="sxs-lookup"><span data-stu-id="db06f-182">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->
```http
HTTP/1.1 202 Accepted
```

##### <a name="notification---establishing"></a><span data-ttu-id="db06f-183">通知-建立</span><span class="sxs-lookup"><span data-stu-id="db06f-183">Notification - establishing</span></span>

```http
POST https://bot.contoso.com/api/calls
Content-Type: application/json
```

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.commsNotifications"
}-->
```json
{
  "@odata.type": "#microsoft.graph.commsNotifications",
  "value": [
    {
      "@odata.type": "#microsoft.graph.commsNotification",
      "changeType": "updated",
      "resourceUrl": "/communications/calls/57DAB8B1894C409AB240BD8BEAE78896",
      "resourceData": {
        "@odata.type": "#microsoft.graph.call",
        "@odata.id": "/communications/calls/57DAB8B1894C409AB240BD8BEAE78896",
        "@odata.etag": "W/\"5445\"",
        "state": "establishing"
      }
    }
  ]
}
```

##### <a name="notification---established"></a><span data-ttu-id="db06f-184">已建立通知</span><span class="sxs-lookup"><span data-stu-id="db06f-184">Notification - established</span></span>

```http
POST https://bot.contoso.com/api/calls
Content-Type: application/json
```

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.commsNotifications"
}-->
```json
{
  "@odata.type": "#microsoft.graph.commsNotifications",
  "value": [
    {
      "@odata.type": "#microsoft.graph.commsNotification",
      "changeType": "updated",
      "resourceUrl": "/communications/calls/57DAB8B1894C409AB240BD8BEAE78896",
      "resourceData": {
        "@odata.type": "#microsoft.graph.call",
        "@odata.id": "/communications/calls/57DAB8B1894C409AB240BD8BEAE78896",
        "@odata.etag": "W/\"5445\"",
        "state": "established"
      }
    }
  ]
}
```

### <a name="example-3-answer-a-policy-based-recording-call"></a><span data-ttu-id="db06f-185">示例3：应答基于策略的录制呼叫</span><span class="sxs-lookup"><span data-stu-id="db06f-185">Example 3: Answer a policy-based recording call</span></span>

<span data-ttu-id="db06f-186">在 [基于策略的录制方案](/microsoftteams/teams-recording-policy)下，在 "策略" 下的参与者加入呼叫之前，传入呼叫通知将发送到与该策略关联的 bot。</span><span class="sxs-lookup"><span data-stu-id="db06f-186">Under the [Policy-based recording scenario](/microsoftteams/teams-recording-policy), before a participant under policy joins a call, an incoming call notification will be sent to the bot associated with the policy.</span></span>
<span data-ttu-id="db06f-187">可以在 **botData** 属性下找到联接信息。</span><span class="sxs-lookup"><span data-stu-id="db06f-187">The join information can be found under the **botData** property.</span></span> <span data-ttu-id="db06f-188">然后，bot 可以选择应答呼叫并相应地 [更新录制状态](call-updaterecordingstatus.md) 。</span><span class="sxs-lookup"><span data-stu-id="db06f-188">The bot can then choose to answer the call and [update the recording status](call-updaterecordingstatus.md) accordingly.</span></span>

<span data-ttu-id="db06f-189">下面的示例展示了 bot 在这种情况下将收到的传入呼叫通知。</span><span class="sxs-lookup"><span data-stu-id="db06f-189">Here is an example of the incoming call notification that a bot would recieve in this case.</span></span>

```json
{
   "@odata.type":"#microsoft.graph.commsNotifications",
   "value":[
      {
         "@odata.type":"#microsoft.graph.commsNotification",
         "changeType":"created",
         "resource":"/app/calls/e71f0300-9c1f-4d99-b5f4-2722e877d497",
         "resourceUrl":"/communications/calls/e71f0300-9c1f-4d99-b5f4-2722e877d497",
         "resourceData":{
            "@odata.type":"#microsoft.graph.call",
            "state":"incoming",
            "direction":"incoming",
            "source":{
               "@odata.type":"#microsoft.graph.participantInfo",
               "id":"90fad2ce-8989-41a1-8a66-f6636e629a2a",
               "identity":{
                  "@odata.type":"#microsoft.graph.identitySet",
                  "user":{
                     "@odata.type":"#microsoft.graph.identity",
                     "id":"8A34A46B-3D17-4ADC-8DCE-DC4E7D572698",
                     "identityProvider":"AAD"
                  }
               },
               "endpointType":"default",
               "region":"amer"
            },
            "targets":[
               {
                  "@odata.type":"#microsoft.graph.invitationParticipantInfo",
                  "identity":{
                     "@odata.type":"#microsoft.graph.identitySet",
                     "applicationInstance":{
                        "@odata.type":"#microsoft.graph.identity",
                        "id":"832899f8-2ea1-4604-8413-27bd2892079f",
                        "identityProvider":"AAD"
                     }
                  },
                  "endpointType":"default",
                  "id":"4520a1a5-5394-5a41-aa12-9ee6fa18cfc8",
                  "region":null,
                  "languageId":null
               }
            ],
            "meetingInfo":{
               "@odata.type":"#microsoft.graph.tokenMeetingInfo",
               "token":"join token"
            },
            "tenantId":"932899f8-2ea1-4604-8413-27bd2892079f",
            "myParticipantId":"1520a1a5-5394-4a41-aa72-9ee6fa18cfc8",
            "callChainId":"05f2f70f-3a9c-47c1-80a9-cc79e91d8cec",
            "incomingContext":{
               "@odata.type":"#microsoft.graph.incomingContext",
               "sourceParticipantId":"30fad2ce-8989-41a1-8a66-f6636e629a2a",
               "observedParticipantId":"30fad2ce-8989-41a1-8a66-f6636e629a2a"
            },
            "id":"e71f0300-9c1f-4d99-b5f4-2722e877d497",
            "applicationMetadata":{
               "botData":{
                  "mediaHostedRegion":"USEA",
                  "user":{
                     "participationMethod":"callee",
                     "clientLocation":"US"
                  },
                  "otherSideUser":{
                     "id":"971f0300-9c1f-4d99-b5f4-2722e877d490",
                     "participantId":"3520a1a5-5394-4a41-aa72-9ee6fa18cfc8",
                     "tenantId":"1540a1a5-2394-4a41-aa72-9ee6fa18cfc8",
                     "onBehalfOf":{
                        "id":"871f0300-9c1f-4d99-b5f4-2722e877d490"
                     },
                     "participationMethod":"caller",
                     "clientLocation":"EUNO"
                  },
                  "inviteReasons":[
                     "PolicyBasedRecording"
                  ],
                  "policyIdentifier":"Test Policy",
                  "pairedRecorders":[
                     {
                        "id":"471f0300-5c1f-4d99-b5f4-2722e877d490",
                        "participantId":"371f0300-2c1f-4d99-b5f4-2722e877d490"
                     }
                  ],
                  "otherRecorders":[
                     {
                        "id":"671f0300-9c1f-4d99-b5f4-2722e877d490",
                        "participantId":"a71f0300-ec1f-4d99-b5f4-2722e877d490"
                     }
                  ]
               }
            }
         }
      }
   ]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "call: answer",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
