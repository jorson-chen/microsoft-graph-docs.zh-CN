---
title: 获取订阅
description: 检索订阅的属性和关系。
localization_priority: Normal
author: davidmu1
doc_type: apiPageType
ms.prod: ''
ms.openlocfilehash: 75e492fbba5e61810f9edb309dedffe6c14f4450
ms.sourcegitcommit: f729068e1fbb6b0f34a3d6144b59ec9aafcd8a62
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/08/2020
ms.locfileid: "49597436"
---
# <a name="get-subscription"></a><span data-ttu-id="13dd2-103">获取订阅</span><span class="sxs-lookup"><span data-stu-id="13dd2-103">Get subscription</span></span>

<span data-ttu-id="13dd2-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="13dd2-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="13dd2-105">检索订阅的属性和关系。</span><span class="sxs-lookup"><span data-stu-id="13dd2-105">Retrieve the properties and relationships of a subscription.</span></span>

## <a name="permissions"></a><span data-ttu-id="13dd2-106">权限</span><span class="sxs-lookup"><span data-stu-id="13dd2-106">Permissions</span></span>

<span data-ttu-id="13dd2-107">根据请求的资源和权限类型（委托或应用程序），下表中指定的权限为调用此 API 所需的最小权限。</span><span class="sxs-lookup"><span data-stu-id="13dd2-107">Depending on the resource and the permission type (delegated or application) requested, the permission specified in the following table is the least privileged required to call this API.</span></span> <span data-ttu-id="13dd2-108">若要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="13dd2-108">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="13dd2-109">支持的资源</span><span class="sxs-lookup"><span data-stu-id="13dd2-109">Supported resource</span></span> | <span data-ttu-id="13dd2-110">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="13dd2-110">Delegated (work or school account)</span></span> | <span data-ttu-id="13dd2-111">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="13dd2-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="13dd2-112">应用程序</span><span class="sxs-lookup"><span data-stu-id="13dd2-112">Application</span></span> |
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="13dd2-113">callRecord</span><span class="sxs-lookup"><span data-stu-id="13dd2-113">callRecord</span></span>](../resources/callrecords-callrecord.md) | <span data-ttu-id="13dd2-114">不支持</span><span class="sxs-lookup"><span data-stu-id="13dd2-114">Not supported</span></span> | <span data-ttu-id="13dd2-115">不支持</span><span class="sxs-lookup"><span data-stu-id="13dd2-115">Not supported</span></span> | <span data-ttu-id="13dd2-116">CallRecords.Read.All</span><span class="sxs-lookup"><span data-stu-id="13dd2-116">CallRecords.Read.All</span></span>  |
|<span data-ttu-id="13dd2-117">[chatMessage](../resources/chatmessage.md) (/teams/{id}/channels/{id}/messages)</span><span class="sxs-lookup"><span data-stu-id="13dd2-117">[chatMessage](../resources/chatmessage.md) (/teams/{id}/channels/{id}/messages)</span></span> | <span data-ttu-id="13dd2-118">ChannelMessage.Read.All、Group.Read.All、Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="13dd2-118">ChannelMessage.Read.All, Group.Read.All, Group.ReadWrite.All</span></span> | <span data-ttu-id="13dd2-119">不支持</span><span class="sxs-lookup"><span data-stu-id="13dd2-119">Not supported</span></span> | <span data-ttu-id="13dd2-120">ChannelMessage \*、ChannelMessage \*。</span><span class="sxs-lookup"><span data-stu-id="13dd2-120">ChannelMessage.Read.Group\*, ChannelMessage.Read.All</span></span>  |
|<span data-ttu-id="13dd2-121">[chatMessage](../resources/chatmessage.md)（/teams/getAllMessages -- 组织中所有频道消息）</span><span class="sxs-lookup"><span data-stu-id="13dd2-121">[chatMessage](../resources/chatmessage.md) (/teams/getAllMessages -- all channel messages in organization)</span></span> | <span data-ttu-id="13dd2-122">不支持</span><span class="sxs-lookup"><span data-stu-id="13dd2-122">Not supported</span></span> | <span data-ttu-id="13dd2-123">不支持</span><span class="sxs-lookup"><span data-stu-id="13dd2-123">Not supported</span></span> | <span data-ttu-id="13dd2-124">ChannelMessage.Read.All</span><span class="sxs-lookup"><span data-stu-id="13dd2-124">ChannelMessage.Read.All</span></span>  |
|<span data-ttu-id="13dd2-125">[chatMessage](../resources/chatmessage.md) (/chats/{id}/messages)</span><span class="sxs-lookup"><span data-stu-id="13dd2-125">[chatMessage](../resources/chatmessage.md) (/chats/{id}/messages)</span></span> | <span data-ttu-id="13dd2-126">Chat.Read、Chat.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="13dd2-126">Chat.Read, Chat.ReadWrite</span></span> | <span data-ttu-id="13dd2-127">不支持</span><span class="sxs-lookup"><span data-stu-id="13dd2-127">Not supported</span></span> | <span data-ttu-id="13dd2-128">Chat.Read.All</span><span class="sxs-lookup"><span data-stu-id="13dd2-128">Chat.Read.All</span></span>  |
|<span data-ttu-id="13dd2-129">[chatMessage](../resources/chatmessage.md)（/chats/getAllMessages -- 组织中所有聊天消息）</span><span class="sxs-lookup"><span data-stu-id="13dd2-129">[chatMessage](../resources/chatmessage.md) (/chats/getAllMessages -- all chat messages in organization)</span></span> | <span data-ttu-id="13dd2-130">不支持</span><span class="sxs-lookup"><span data-stu-id="13dd2-130">Not supported</span></span> | <span data-ttu-id="13dd2-131">不支持</span><span class="sxs-lookup"><span data-stu-id="13dd2-131">Not supported</span></span> | <span data-ttu-id="13dd2-132">Chat.Read.All</span><span class="sxs-lookup"><span data-stu-id="13dd2-132">Chat.Read.All</span></span>  |
|[<span data-ttu-id="13dd2-133">contact</span><span class="sxs-lookup"><span data-stu-id="13dd2-133">contact</span></span>](../resources/contact.md) | <span data-ttu-id="13dd2-134">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="13dd2-134">Contacts.Read</span></span> | <span data-ttu-id="13dd2-135">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="13dd2-135">Contacts.Read</span></span> | <span data-ttu-id="13dd2-136">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="13dd2-136">Contacts.Read</span></span> |
|<span data-ttu-id="13dd2-137">[driveItem](../resources/driveitem.md)（用户的个人 OneDrive）</span><span class="sxs-lookup"><span data-stu-id="13dd2-137">[driveItem](../resources/driveitem.md) (user's personal OneDrive)</span></span> | <span data-ttu-id="13dd2-138">不支持</span><span class="sxs-lookup"><span data-stu-id="13dd2-138">Not supported</span></span> | <span data-ttu-id="13dd2-139">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="13dd2-139">Files.ReadWrite</span></span> | <span data-ttu-id="13dd2-140">不支持</span><span class="sxs-lookup"><span data-stu-id="13dd2-140">Not supported</span></span> |
|<span data-ttu-id="13dd2-141">[driveItem](../resources/driveitem.md) (OneDrive for Business)</span><span class="sxs-lookup"><span data-stu-id="13dd2-141">[driveItem](../resources/driveitem.md) (OneDrive for Business)</span></span> | <span data-ttu-id="13dd2-142">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="13dd2-142">Files.ReadWrite.All</span></span> | <span data-ttu-id="13dd2-143">不支持</span><span class="sxs-lookup"><span data-stu-id="13dd2-143">Not supported</span></span> | <span data-ttu-id="13dd2-144">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="13dd2-144">Files.ReadWrite.All</span></span> |
|[<span data-ttu-id="13dd2-145">事件</span><span class="sxs-lookup"><span data-stu-id="13dd2-145">event</span></span>](../resources/event.md) | <span data-ttu-id="13dd2-146">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="13dd2-146">Calendars.Read</span></span> | <span data-ttu-id="13dd2-147">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="13dd2-147">Calendars.Read</span></span> | <span data-ttu-id="13dd2-148">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="13dd2-148">Calendars.Read</span></span> |
|[<span data-ttu-id="13dd2-149">组</span><span class="sxs-lookup"><span data-stu-id="13dd2-149">group</span></span>](../resources/group.md) | <span data-ttu-id="13dd2-150">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="13dd2-150">Group.Read.All</span></span> | <span data-ttu-id="13dd2-151">不支持</span><span class="sxs-lookup"><span data-stu-id="13dd2-151">Not supported</span></span> | <span data-ttu-id="13dd2-152">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="13dd2-152">Group.Read.All</span></span> |
|[<span data-ttu-id="13dd2-153">组对话</span><span class="sxs-lookup"><span data-stu-id="13dd2-153">group conversation</span></span>](../resources/conversation.md) | <span data-ttu-id="13dd2-154">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="13dd2-154">Group.Read.All</span></span> | <span data-ttu-id="13dd2-155">不支持</span><span class="sxs-lookup"><span data-stu-id="13dd2-155">Not supported</span></span> | <span data-ttu-id="13dd2-156">不支持</span><span class="sxs-lookup"><span data-stu-id="13dd2-156">Not supported</span></span> |
|[<span data-ttu-id="13dd2-157">列表</span><span class="sxs-lookup"><span data-stu-id="13dd2-157">list</span></span>](../resources/list.md) | <span data-ttu-id="13dd2-158">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="13dd2-158">Sites.ReadWrite.All</span></span> | <span data-ttu-id="13dd2-159">不支持</span><span class="sxs-lookup"><span data-stu-id="13dd2-159">Not supported</span></span> | <span data-ttu-id="13dd2-160">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="13dd2-160">Sites.ReadWrite.All</span></span> |
|[<span data-ttu-id="13dd2-161">邮件</span><span class="sxs-lookup"><span data-stu-id="13dd2-161">message</span></span>](../resources/message.md) | <span data-ttu-id="13dd2-162">Mail.ReadBasic、Mail.Read</span><span class="sxs-lookup"><span data-stu-id="13dd2-162">Mail.ReadBasic, Mail.Read</span></span> | <span data-ttu-id="13dd2-163">Mail.ReadBasic、Mail.Read</span><span class="sxs-lookup"><span data-stu-id="13dd2-163">Mail.ReadBasic, Mail.Read</span></span> | <span data-ttu-id="13dd2-164">Mail.ReadBasic、Mail.Read</span><span class="sxs-lookup"><span data-stu-id="13dd2-164">Mail.ReadBasic, Mail.Read</span></span> |
|[<span data-ttu-id="13dd2-165">状态</span><span class="sxs-lookup"><span data-stu-id="13dd2-165">presence</span></span>](../resources/presence.md) | <span data-ttu-id="13dd2-166">Presence.Read.All</span><span class="sxs-lookup"><span data-stu-id="13dd2-166">Presence.Read.All</span></span> | <span data-ttu-id="13dd2-167">不支持</span><span class="sxs-lookup"><span data-stu-id="13dd2-167">Not supported</span></span> | <span data-ttu-id="13dd2-168">不支持</span><span class="sxs-lookup"><span data-stu-id="13dd2-168">Not supported</span></span> |
|[<span data-ttu-id="13dd2-169">printTaskDefinition</span><span class="sxs-lookup"><span data-stu-id="13dd2-169">printTaskDefinition</span></span>](../resources/printtaskdefinition.md) | <span data-ttu-id="13dd2-170">不支持</span><span class="sxs-lookup"><span data-stu-id="13dd2-170">Not supported</span></span> | <span data-ttu-id="13dd2-171">不支持</span><span class="sxs-lookup"><span data-stu-id="13dd2-171">Not supported</span></span> | <span data-ttu-id="13dd2-172">PrintTaskDefinition.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="13dd2-172">PrintTaskDefinition.ReadWrite.All</span></span> |
|<span data-ttu-id="13dd2-173">安全[警报](../resources/alert.md)</span><span class="sxs-lookup"><span data-stu-id="13dd2-173">[security alert](../resources/alert.md)</span></span> | <span data-ttu-id="13dd2-174">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="13dd2-174">SecurityEvents.ReadWrite.All</span></span> | <span data-ttu-id="13dd2-175">不支持</span><span class="sxs-lookup"><span data-stu-id="13dd2-175">Not supported</span></span> | <span data-ttu-id="13dd2-176">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="13dd2-176">SecurityEvents.ReadWrite.All</span></span> |
|[<span data-ttu-id="13dd2-177">todoTask</span><span class="sxs-lookup"><span data-stu-id="13dd2-177">todoTask</span></span>](../resources/todotask.md) | <span data-ttu-id="13dd2-178">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="13dd2-178">Tasks.ReadWrite</span></span> | <span data-ttu-id="13dd2-179">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="13dd2-179">Tasks.ReadWrite</span></span> | <span data-ttu-id="13dd2-180">不支持</span><span class="sxs-lookup"><span data-stu-id="13dd2-180">Not supported</span></span> |
|[<span data-ttu-id="13dd2-181">用户</span><span class="sxs-lookup"><span data-stu-id="13dd2-181">user</span></span>](../resources/user.md) | <span data-ttu-id="13dd2-182">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="13dd2-182">User.Read.All</span></span> | <span data-ttu-id="13dd2-183">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="13dd2-183">User.Read.All</span></span> | <span data-ttu-id="13dd2-184">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="13dd2-184">User.Read.All</span></span> |

> <span data-ttu-id="13dd2-185">**注意**：标有 \* 的权限用于 [特定于资源的同意]( https://aka.ms/teams-rsc)。</span><span class="sxs-lookup"><span data-stu-id="13dd2-185">**Note**: Permissions marked with \* use [resource-specific consent]( https://aka.ms/teams-rsc).</span></span>

### <a name="chatmessage"></a><span data-ttu-id="13dd2-186">chatMessage</span><span class="sxs-lookup"><span data-stu-id="13dd2-186">chatMessage</span></span>

<span data-ttu-id="13dd2-187">具有委派权限的 **了 chatmessage** 订阅不支持资源数据 (**includeResourceData** 必须 `false`) ，并且不需要 [加密](/graph/webhooks-with-resource-data)。</span><span class="sxs-lookup"><span data-stu-id="13dd2-187">**chatMessage** subscriptions with delegated permissions do not support resource data (**includeResourceData** must be `false`), and do not require [encryption](/graph/webhooks-with-resource-data).</span></span>

<span data-ttu-id="13dd2-188">具有应用程序权限的 **chatMessage** 订阅包含资源数据，并且需要进行 [加密](/graph/webhooks-with-resource-data)。</span><span class="sxs-lookup"><span data-stu-id="13dd2-188">**chatMessage** subscriptions with application permissions include resource data, and require [encryption](/graph/webhooks-with-resource-data).</span></span> <span data-ttu-id="13dd2-189">如果未指定 [encryptionCertificate](../resources/subscription.md)，则订阅创建将失败。</span><span class="sxs-lookup"><span data-stu-id="13dd2-189">Subscription creation will fail if [encryptionCertificate](../resources/subscription.md) is not specified.</span></span> <span data-ttu-id="13dd2-190">创建 **chatMessage** 订阅前，必须请求访问权限。</span><span class="sxs-lookup"><span data-stu-id="13dd2-190">Before creating a **chatMessage** subscription, you must request access.</span></span> <span data-ttu-id="13dd2-191">有关详细信息，请参阅 [Microsoft Teams 中的受保护 API](/graph/teams-protected-apis)。</span><span class="sxs-lookup"><span data-stu-id="13dd2-191">For details, see [Protected APIs in Microsoft Teams](/graph/teams-protected-apis).</span></span> 

> <span data-ttu-id="13dd2-192">**注意：** `/teams/getAllMessages` 和 `/chats/getAllMessages` 可供拥有 [所需许可证](https://aka.ms/teams-changenotification-licenses)的用户使用。</span><span class="sxs-lookup"><span data-stu-id="13dd2-192">**Note:** `/teams/getAllMessages` and `/chats/getAllMessages` are available to users that have the [required licenses](https://aka.ms/teams-changenotification-licenses).</span></span>

### <a name="driveitem"></a><span data-ttu-id="13dd2-193">driveItem</span><span class="sxs-lookup"><span data-stu-id="13dd2-193">driveItem</span></span>

<span data-ttu-id="13dd2-194">其他限制适用于 OneDrive 项目的订阅。</span><span class="sxs-lookup"><span data-stu-id="13dd2-194">Additional limitations apply for subscriptions on OneDrive items.</span></span> <span data-ttu-id="13dd2-195">这些限制适用于订阅的创建和管理（获取、更新和删除）。</span><span class="sxs-lookup"><span data-stu-id="13dd2-195">The limitations apply to creating as well as managing (getting, updating, and deleting) subscriptions.</span></span>

<span data-ttu-id="13dd2-196">在个人 OneDrive 上，可订阅根文件夹或该驱动器中的任何子文件夹。</span><span class="sxs-lookup"><span data-stu-id="13dd2-196">On a personal OneDrive, you can subscribe to the root folder or any subfolder in that drive.</span></span> <span data-ttu-id="13dd2-197">在 OneDrive for Business 上，只可以订阅根文件夹。</span><span class="sxs-lookup"><span data-stu-id="13dd2-197">On OneDrive for Business, you can subscribe to only the root folder.</span></span> <span data-ttu-id="13dd2-198">对订阅的文件夹或者其层次结构中的任何文件、文件夹或其他 **driveItem** 实例所做更改属于请求的更改类型时，发送更改通知。</span><span class="sxs-lookup"><span data-stu-id="13dd2-198">Change notifications are sent for the requested types of changes on the subscribed folder, or any file, folder, or other **driveItem** instances in its hierarchy.</span></span> <span data-ttu-id="13dd2-199">无法订阅不是文件夹的“**驱动器**”或“**driveItem**”实例，例如单个文件。</span><span class="sxs-lookup"><span data-stu-id="13dd2-199">You cannot subscribe to **drive** or **driveItem** instances that are not folders, such as individual files.</span></span>

### <a name="contact-event-and-message"></a><span data-ttu-id="13dd2-200">联系人、事件和消息</span><span class="sxs-lookup"><span data-stu-id="13dd2-200">contact, event, and message</span></span>

<span data-ttu-id="13dd2-201">其他限制适用于 Outlook 项目的订阅。</span><span class="sxs-lookup"><span data-stu-id="13dd2-201">Additional limitations apply for subscriptions on Outlook items.</span></span> <span data-ttu-id="13dd2-202">这些限制适用于订阅的创建和管理（获取、更新和删除）。</span><span class="sxs-lookup"><span data-stu-id="13dd2-202">The limitations apply to creating as well as managing (getting, updating, and deleting) subscriptions.</span></span>

- <span data-ttu-id="13dd2-203">委托的权限仅支持订阅已登录用户的邮箱内文件夹中的项。</span><span class="sxs-lookup"><span data-stu-id="13dd2-203">Delegated permission supports subscribing to items in folders in only the signed-in user's mailbox.</span></span> <span data-ttu-id="13dd2-204">例如，不能使用委托的权限 Calendars.Read 来订阅另一个用户邮箱中的事件。</span><span class="sxs-lookup"><span data-stu-id="13dd2-204">For example, you cannot use the delegated permission Calendars.Read to subscribe to events in another user’s mailbox.</span></span>
- <span data-ttu-id="13dd2-205">订阅 _共享或委托_ 文件夹中 Outlook 联系人、事件或邮件的更改通知：</span><span class="sxs-lookup"><span data-stu-id="13dd2-205">To subscribe to change notifications of Outlook contacts, events, or messages in _shared or delegated_ folders:</span></span>

  - <span data-ttu-id="13dd2-206">使用相应的应用程序权限订阅租户内 _任何_ 用户的文件夹或邮箱中项目的更改。</span><span class="sxs-lookup"><span data-stu-id="13dd2-206">Use the corresponding application permission to subscribe to changes of items in a folder or mailbox of _any_ user in the tenant.</span></span>
  - <span data-ttu-id="13dd2-207">切勿使用 Outlook 共享权限（Contacts.Read.Shared、Calendars.Read.Shared、Mail.Read.Shared 及其相应的读写权限），因为它们 **不** 支持订阅对共享或委托文件夹中的项的更改通知。</span><span class="sxs-lookup"><span data-stu-id="13dd2-207">Do not use the Outlook sharing permissions (Contacts.Read.Shared, Calendars.Read.Shared, Mail.Read.Shared, and their read/write counterparts), as they do **not** support subscribing to change notifications on items in shared or delegated folders.</span></span>

### <a name="presence"></a><span data-ttu-id="13dd2-208">状态</span><span class="sxs-lookup"><span data-stu-id="13dd2-208">presence</span></span>

<span data-ttu-id="13dd2-209">**状态** 订阅需要 [加密](/graph/webhooks-with-resource-data)。</span><span class="sxs-lookup"><span data-stu-id="13dd2-209">**presence** subscriptions require [encryption](/graph/webhooks-with-resource-data).</span></span> <span data-ttu-id="13dd2-210">如果未指定 [encryptionCertificate](../resources/subscription.md)，则订阅创建将失败。</span><span class="sxs-lookup"><span data-stu-id="13dd2-210">Subscription creation will fail if [encryptionCertificate](../resources/subscription.md) is not specified.</span></span>

## <a name="http-request"></a><span data-ttu-id="13dd2-211">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="13dd2-211">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /subscriptions/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="13dd2-212">可选的查询参数</span><span class="sxs-lookup"><span data-stu-id="13dd2-212">Optional query parameters</span></span>

<span data-ttu-id="13dd2-213">此方法支持 [OData 查询参数](https://developer.microsoft.com/graph/docs/concepts/query_parameters) 来帮助自定义响应。</span><span class="sxs-lookup"><span data-stu-id="13dd2-213">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="13dd2-214">请求标头</span><span class="sxs-lookup"><span data-stu-id="13dd2-214">Request headers</span></span>

| <span data-ttu-id="13dd2-215">名称</span><span class="sxs-lookup"><span data-stu-id="13dd2-215">Name</span></span>       | <span data-ttu-id="13dd2-216">类型</span><span class="sxs-lookup"><span data-stu-id="13dd2-216">Type</span></span> | <span data-ttu-id="13dd2-217">说明</span><span class="sxs-lookup"><span data-stu-id="13dd2-217">Description</span></span>|
|:-----------|:-----|:-----------|
| <span data-ttu-id="13dd2-218">Authorization</span><span class="sxs-lookup"><span data-stu-id="13dd2-218">Authorization</span></span>  | <span data-ttu-id="13dd2-219">string</span><span class="sxs-lookup"><span data-stu-id="13dd2-219">string</span></span>  | <span data-ttu-id="13dd2-p108">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="13dd2-p108">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="13dd2-222">请求正文</span><span class="sxs-lookup"><span data-stu-id="13dd2-222">Request body</span></span>

<span data-ttu-id="13dd2-223">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="13dd2-223">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="13dd2-224">响应</span><span class="sxs-lookup"><span data-stu-id="13dd2-224">Response</span></span>

<span data-ttu-id="13dd2-225">如果成功，此方法在响应正文中返回 `200 OK` 响应代码和 [subscription](../resources/subscription.md) 对象。</span><span class="sxs-lookup"><span data-stu-id="13dd2-225">If successful, this method returns a `200 OK` response code and [subscription](../resources/subscription.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="13dd2-226">示例</span><span class="sxs-lookup"><span data-stu-id="13dd2-226">Example</span></span>

##### <a name="request"></a><span data-ttu-id="13dd2-227">请求</span><span class="sxs-lookup"><span data-stu-id="13dd2-227">Request</span></span>

<span data-ttu-id="13dd2-228">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="13dd2-228">Here is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="13dd2-229">HTTP</span><span class="sxs-lookup"><span data-stu-id="13dd2-229">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_subscription"
}-->

```msgraph-interactive
GET https://graph.microsoft.com/beta/subscriptions/{id}
```
# <a name="c"></a>[<span data-ttu-id="13dd2-230">C#</span><span class="sxs-lookup"><span data-stu-id="13dd2-230">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-subscription-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="13dd2-231">JavaScript</span><span class="sxs-lookup"><span data-stu-id="13dd2-231">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-subscription-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="13dd2-232">Objective-C</span><span class="sxs-lookup"><span data-stu-id="13dd2-232">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-subscription-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[<span data-ttu-id="13dd2-233">Java</span><span class="sxs-lookup"><span data-stu-id="13dd2-233">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/get-subscription-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a><span data-ttu-id="13dd2-234">响应</span><span class="sxs-lookup"><span data-stu-id="13dd2-234">Response</span></span>

<span data-ttu-id="13dd2-235">下面是一个响应示例。</span><span class="sxs-lookup"><span data-stu-id="13dd2-235">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.subscription"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 252

{
  "id":"7f105c7d-2dc5-4530-97cd-4e7ae6534c07",
  "resource":"me/messages",
  "applicationId" : "string",
  "changeType":"created,updated",
  "clientState":"secretClientValue",
  "notificationUrl":"https://webhook.azurewebsites.net/api/send/myNotifyClient",
  "lifecycleNotificationUrl":"https://webhook.azurewebsites.net/api/send/lifecycleNotifications",
  "expirationDateTime":"2016-11-20T18:23:45.9356913Z",
  "creatorId": "string",
  "latestSupportedTlsVersion": "v1_2",
  "encryptionCertificate": "",
  "encryptionCertificateId": "",
  "includeResourceData": false
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Get subscription",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->


