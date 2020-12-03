---
title: 使用活动源 REST API
description: '您可以使用 Microsoft Graph 中的活动源 API，在设备和平台之间恢复用户的活动。 活动源 API 请求通过委派权限和用户活动权限（可用于个人或工作和学校帐户）代表用户执行。 '
localization_priority: Normal
ms.prod: project-rome
doc_type: conceptualPageType
author: ailae
ms.openlocfilehash: 4ed2b55c06710b17be984e2c9be71ba8496d5991
ms.sourcegitcommit: 9f88b7e41a4a4a4d5f52bd995ce07c6f702bd5d6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/01/2020
ms.locfileid: "49523362"
---
# <a name="use-the-activity-feed-rest-api"></a><span data-ttu-id="b1b6c-104">使用活动源 REST API</span><span class="sxs-lookup"><span data-stu-id="b1b6c-104">Use the activity feed REST API</span></span>

<span data-ttu-id="b1b6c-105">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="b1b6c-105">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]


<span data-ttu-id="b1b6c-106">您可以使用 Microsoft Graph 中的活动源 API，在设备和平台之间恢复用户的活动。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-106">You can use the activity feed API in Microsoft Graph to resume a user's activity across devices and platforms.</span></span> <span data-ttu-id="b1b6c-107">活动源 API 请求通过 [委派权限](/graph/permissions-reference#delegated-permissions-application-permissions-and-effective-permissions) 和 [用户活动权限](/graph/permissions-reference)（可用于个人或工作和学校帐户）代表用户执行。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-107">Activity feed API requests are performed on behalf of a user via [delegated permissions](/graph/permissions-reference#delegated-permissions-application-permissions-and-effective-permissions) and the [user activity permission](/graph/permissions-reference), which can be used with either personal or work and school accounts.</span></span>

<span data-ttu-id="b1b6c-108">用户活动由 [活动](/graph/api/resources/projectrome-activity) 资源表示，并在由 "收藏"/"活动" 表示的基于时间的订阅源中进行组织。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-108">User activities are represented by the [activity](/graph/api/resources/projectrome-activity) resource and are organized in a time-based feed represented by the collection me/activities.</span></span>
<!-- Add missing content.
Each activity represents a unique...
-->
## <a name="what-makes-a-great-user-activity"></a><span data-ttu-id="b1b6c-109">什么使用户成为出色的活动？</span><span class="sxs-lookup"><span data-stu-id="b1b6c-109">What makes a great user activity?</span></span>

<span data-ttu-id="b1b6c-110">用户活动不只是启动应用程序，它们都是应用程序中的特定内容的深层链接。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-110">User activities don’t just launch apps — they are deep links into specific content within your app.</span></span> <span data-ttu-id="b1b6c-111">您创建的用户活动不仅可以在您自己的应用程序中使用，还会显示在 Cortana 和 Windows 时间线中—驱动更多的应用程序 reengagement，使用户可以更轻松地在多个设备上继续使用您的应用程序。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-111">The user activities you create can not only be used in your own app, but will also appear in Cortana and Windows Timeline — driving more app reengagement and making it easier for your users to continue using your app across multiple devices.</span></span>

### <a name="what-should-become-an-activity"></a><span data-ttu-id="b1b6c-112">什么应该成为活动？</span><span class="sxs-lookup"><span data-stu-id="b1b6c-112">What should become an activity?</span></span>

<span data-ttu-id="b1b6c-113">由于每个应用程序都不同，因此，每个应用程序开发人员都可以了解将应用程序中的操作映射到用户活动的最佳方式。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-113">Because every app is different, it's up to each app developer to understand the best way to map actions within your application to user activities.</span></span> <span data-ttu-id="b1b6c-114">例如，游戏可能会为每个市场活动创建一个活动，文档创作应用程序可能会为每个唯一文档创建一个活动，并且业务线应用程序可能会为每个工作流创建一个活动。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-114">For example, games might create an activity for each campaign, document authoring apps might create an activity for each unique document, and line-of-business apps might create an activity for each workflow.</span></span>

<span data-ttu-id="b1b6c-115">在您的应用程序中定义活动时，请应用以下准则：</span><span class="sxs-lookup"><span data-stu-id="b1b6c-115">Apply the following guidelines as you define activities in your app:</span></span>

<span data-ttu-id="b1b6c-116">操作 **：** 记录一组相关用户操作的单个活动。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-116">**DO:** Record a single activity for a group of related user actions.</span></span>
<span data-ttu-id="b1b6c-117">如果您的应用程序用于一系列相关的内容，则记录整个参与会话的单个活动可能很有意义。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-117">If your application is used for a sequence of related content, it probably makes sense to record a single activity for the entire engagement session.</span></span>

<span data-ttu-id="b1b6c-118">*播放列表方案：* 这一点尤其适用于音乐播放列表或电视节目-可以更新单个用户活动以显示进度。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-118">*Playlist scenarios:* This is especially relevant for music playlists or TV shows — a single user activity can be updated to show your progress.</span></span> <span data-ttu-id="b1b6c-119">在这种情况下，您将有一个用户活动，其中多个 [历史项目](/graph/api/resources/projectrome-historyitem) 表示一段时间内多天或几周的服务。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-119">In this case, you will have a single user activity with multiple [history items](/graph/api/resources/projectrome-historyitem) representing periods of engagement across multiple days or weeks.</span></span>

<span data-ttu-id="b1b6c-120">操作 **：** 将用户数据存储到云。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-120">**DO:** Store user data to the cloud.</span></span>
<span data-ttu-id="b1b6c-121">如果要支持跨设备活动，则需要确保将 reengage 此活动所需的内容存储到云位置。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-121">If you want to support cross-device activities, you need to make sure the content required to reengage this activity is stored to a cloud location.</span></span> <span data-ttu-id="b1b6c-122">例如，如果您在每次用户编辑文档时发布活动，则应将文档存储在云中，而不是在用户的设备上本地存储，以便启用跨设备 reengagement。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-122">For example, if you publish an activity each time a user edits a document, the document should be stored in the cloud as opposed to locally on the user's device in order to enable cross-device reengagement.</span></span>

<span data-ttu-id="b1b6c-123">**请勿执行以下操作：** 为用户无需在将来恢复的操作创建用户活动。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-123">**DO NOT:** Create a user activity for actions that users do not need to resume in the future.</span></span>
<span data-ttu-id="b1b6c-124">如果您的应用程序用于完成简单的一次性操作，这些操作不会保留状态以供将来跟踪，则您可能不需要编写用户活动。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-124">If your application is used to complete simple, one-time operations that do not persist status for you to track in the future, you probably do not need to write a user activity.</span></span>

<span data-ttu-id="b1b6c-125">若要清楚，即使用户活动出现在 Windows 日程表中，也不会将其设计为版本控制工具—选择基于文档的活动应始终显示该文档的最新版本 (包括其他用户所做的更改。 ) </span><span class="sxs-lookup"><span data-stu-id="b1b6c-125">To be clear, even though user activities appear in Windows Timeline, this is not designed as a versioning tool — choosing a document-based activity should always show the latest version of that document (including changes that were made by another user.)</span></span>

<span data-ttu-id="b1b6c-126">**请勿执行以下操作：** 为 *其他用户* 完成的操作创建用户活动。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-126">**DO NOT:** Create a user activity for actions completed by *other users*.</span></span>
<span data-ttu-id="b1b6c-127">如果某人向用户发送邮件，或在您的应用程序中 @mentions 用户，则不应编写新活动。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-127">If someone sends the user a message, or @mentions the user within your app, you should not write a new activity.</span></span> <span data-ttu-id="b1b6c-128">通过呈现通知，可以更好地提供这些交互。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-128">These interactions are better served by surfacing notifications.</span></span>

<span data-ttu-id="b1b6c-129">*协作方案：* 如果有多个用户在同一个活动 (（如 Word 文档) ）上工作，则在您上次编辑文档后，其他用户对该文档所做的更改将会发生。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-129">*Collaboration scenarios:* If multiple people are working on the same activity (such as a Word document), there will be cases when another user has made changes to the document after you last edited it.</span></span> <span data-ttu-id="b1b6c-130">在这种情况下，应用程序开发人员可能需要更新活动中的可视元素，以反映对文档所做的更改。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-130">In this case, app developers might want to update the visual elements in the activity to reflect changes made to the document.</span></span> <span data-ttu-id="b1b6c-131">若要执行此操作，应用程序可能会更新现有活动，而不会创建新的历史记录项。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-131">To do this, the app might update the existing activity without creating a new history item.</span></span>

><span data-ttu-id="b1b6c-132">**注意：** 如果要为 web 应用程序发布活动，请务必同时 `activationURL` `fallbackURL` 为每个活动包含和。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-132">**Note:** If you're publishing activities for a web application, it's important to include both an `activationURL` and a `fallbackURL` for each of your activities.</span></span> <span data-ttu-id="b1b6c-133">这些活动将从 Microsoft 体验（如 Windows 日程表）按预期方式将用户重新启动到应用中。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-133">The activities will launch the user back into your app as expected from Microsoft experiences like Windows Timeline.</span></span>

## <a name="app-interaction-patterns-and-user-activities"></a><span data-ttu-id="b1b6c-134">应用交互模式和用户活动</span><span class="sxs-lookup"><span data-stu-id="b1b6c-134">App interaction patterns and user activities</span></span>
<span data-ttu-id="b1b6c-135">您创建的用户活动将根据您的应用程序的交互模式而变化。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-135">The user activities that you create will vary based on the interaction pattern of your app.</span></span> <span data-ttu-id="b1b6c-136">虽然每个应用程序不同，但大多数都属于以下交互模式之一：</span><span class="sxs-lookup"><span data-stu-id="b1b6c-136">While every app is different, most will fall into one of the following interaction patterns:</span></span>

* <span data-ttu-id="b1b6c-137">**基于文档的应用程序** -为每个文档创建一个活动，其中包含一个或多个历史记录，并反映使用时间段。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-137">**Document-based apps** — Create one activity per document with one or more history records reflecting periods of use.</span></span> <span data-ttu-id="b1b6c-138">对文档进行更改时，更新活动卡非常重要。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-138">It is important to update your activity card as changes are made to the document.</span></span>
* <span data-ttu-id="b1b6c-139">**Media 回放应用** —根据内容（如播放列表、程序或独立内容）的逻辑分组创建一个活动。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-139">**Media playback apps** — Create one activity per logical grouping of content such as a playlist, program, or standalone content.</span></span>
* <span data-ttu-id="b1b6c-140">**游戏** —为每个已保存的游戏或世界创建一个活动。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-140">**Games** — Create one activity for each saved game or world.</span></span> <span data-ttu-id="b1b6c-141">如果你的游戏仅支持一系列级别，则可以在一段时间内编写相同的活动，尽管你可能需要更新卡片以显示你的最新进度或成就。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-141">If your game supports only a single sequence of levels, you can write the same activity over time, although you might want to update your card to show your latest progress or achievements.</span></span>
* <span data-ttu-id="b1b6c-142">**实用程序应用** 程序-如果用户要恢复的应用程序中没有任何内容，则不应发布活动。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-142">**Utility apps** — If there is nothing within your app that users would want to resume, you should not publish activities.</span></span> <span data-ttu-id="b1b6c-143">一个很棒的示例是简单的单一用途应用（如计算器）。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-143">A good example is a simple single-purpose app like calculator.</span></span>
* <span data-ttu-id="b1b6c-144">**业务线应用程序** —用于管理简单任务或工作流的许多应用程序都存在。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-144">**Line-of-business apps** — Many apps exist for managing simple tasks or workflows.</span></span> <span data-ttu-id="b1b6c-145">为通过您的应用程序访问的每个单独的工作流创建一个活动。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-145">Create one activity for each separate workflow accessed through your app.</span></span> <span data-ttu-id="b1b6c-146">例如，每个零用金报销单都是一个单独的活动，因为您可能想要单击该活动以查看该活动是否已获得批准。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-146">For example, each expense report would be a separate activity, because you might want to click that activity to see if it was approved.</span></span>

<span data-ttu-id="b1b6c-147">*一些复杂的应用程序包含多个交互模式。您可能需要针对应用程序处理的不同应用场景遵循不同的用户活动创建模式。*</span><span class="sxs-lookup"><span data-stu-id="b1b6c-147">*Some complex apps include multiple interaction patterns. You might want to follow different user activity creation patterns for different scenarios handled by your app.*</span></span>

<!-- Add content or remove H2.
## Common use cases
-->

## <a name="next-steps"></a><span data-ttu-id="b1b6c-148">后续步骤</span><span class="sxs-lookup"><span data-stu-id="b1b6c-148">Next steps</span></span>

- <span data-ttu-id="b1b6c-149">查看 [活动资源](/graph/api/resources/projectrome-activity) 并定义您的应用程序活动，以帮助用户恢复重要任务。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-149">See the [activity resource](/graph/api/resources/projectrome-activity) and define your app's activities to help users resume important tasks.</span></span>
- <span data-ttu-id="b1b6c-150">浏览 [自适应卡示例](https://adaptivecards.io/samples/) 示例，以获取活动 **pop** 的创意。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-150">Explore the [adaptive card samples](https://adaptivecards.io/samples/) samples for ideas to make your activities **pop**.</span></span>
- <span data-ttu-id="b1b6c-151">尝试在 [Graph 浏览器](https://developer.microsoft.com/graph/graph-explorer)中调用 API。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-151">Try the API in the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer).</span></span>

<span data-ttu-id="b1b6c-152">**是否要查找更多创意？**</span><span class="sxs-lookup"><span data-stu-id="b1b6c-152">**Looking for more ideas?**</span></span>

- <span data-ttu-id="b1b6c-153">了解 [Microsoft 在使用活动时的体验](https://channel9.msdn.com/events/Build/2017/B8108)。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-153">See [how Microsoft experiences are using activities](https://channel9.msdn.com/events/Build/2017/B8108).</span></span>
- <span data-ttu-id="b1b6c-154">了解 [活动源 API 并获取我离开的位置](https://channel9.msdn.com/Events/Windows/Windows-Developer-Day-Fall-Creators-Update/WinDev011)。</span><span class="sxs-lookup"><span data-stu-id="b1b6c-154">Learn about [the activity feed API and pick up where I left off](https://channel9.msdn.com/Events/Windows/Windows-Developer-Day-Fall-Creators-Update/WinDev011).</span></span>
