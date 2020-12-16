---
title: Planner 任务和计划 API 概述
description: Planner 提供了一种简单而又直观的方法，可用于团队组织他们的工作。 客户可以使用 Planner 来创建计划、组织和分配任务、共享进度以及协作处理内容。  Planner 提供了多个交互式体验，包括任务板、图表页和日程安排视图，以及在整个 Microsoft 365 中的集成。
author: TarkanSevilmis
localization_priority: Priority
ms.prod: planner
ms.openlocfilehash: 076660fe1aa03dc79937166ac2549a9a4cb6a85d
ms.sourcegitcommit: 7153a13f4e95c7d9fed3f2c10a3d075ff87b368d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/26/2020
ms.locfileid: "44895606"
---
# <a name="planner-tasks-and-plans-api-overview"></a><span data-ttu-id="61ae2-105">Planner 任务和计划 API 概述</span><span class="sxs-lookup"><span data-stu-id="61ae2-105">Planner tasks and plans API overview</span></span>
<span data-ttu-id="61ae2-106">Planner 提供了一种简单而又直观的方法，可用于团队组织他们的工作。</span><span class="sxs-lookup"><span data-stu-id="61ae2-106">Planner provides a simple and visual way for teams to organize their work.</span></span> <span data-ttu-id="61ae2-107">客户可以使用 Planner 来创建计划、组织和分配任务、共享进度以及协作处理内容。</span><span class="sxs-lookup"><span data-stu-id="61ae2-107">Customers can use Planner to create plans, organize and assign tasks, share progress, and collaborate on content.</span></span>  <span data-ttu-id="61ae2-108">Planner 提供了多个交互式体验，包括任务板、图表页和日程安排视图，以及在整个 Microsoft 365 中的集成。</span><span class="sxs-lookup"><span data-stu-id="61ae2-108">Planner provides several interactive experiences including a task board, a charts page, and a schedule view, as well as integrations throughout Microsoft 365.</span></span>

<span data-ttu-id="61ae2-109">**Microsoft 365 Planner 任务板**</span><span class="sxs-lookup"><span data-stu-id="61ae2-109">**Microsoft 365 Planner task board**</span></span>

<span data-ttu-id="61ae2-110">![Microsoft 365 Planner 任务板屏幕截图](images/plannerboard.png "Planner 版块图像")</span><span class="sxs-lookup"><span data-stu-id="61ae2-110">![Screenshot of a Microsoft 365 Planner task board](images/plannerboard.png "Image of Planner board")</span></span>


## <a name="why-integrate-with-planner-tasks"></a><span data-ttu-id="61ae2-111">为什么与 Planner 任务集成？</span><span class="sxs-lookup"><span data-stu-id="61ae2-111">Why integrate with Planner tasks?</span></span>
<span data-ttu-id="61ae2-112">Planner 为 Microsoft 365 中的协作体验提供了任务跟踪功能。</span><span class="sxs-lookup"><span data-stu-id="61ae2-112">Planner provides task tracking capabilities for collaboration experiences in Microsoft 365.</span></span> <span data-ttu-id="61ae2-113">如果你的应用场景需要为一个团队或一组最终用户跟踪任务并组织工作，那么，Planner 就是正确的服务。</span><span class="sxs-lookup"><span data-stu-id="61ae2-113">If your scenarios require tracking tasks and organizing work for a team or group of end users, Planner is the right service for you.</span></span> <span data-ttu-id="61ae2-114">Planner 集成可有助于你覆盖数百万在 Microsoft 365 上进行协作的用户。</span><span class="sxs-lookup"><span data-stu-id="61ae2-114">Planner integration can help you reach the millions of users collaborating on Microsoft 365.</span></span> 

### <a name="organize-your-teams-work"></a><span data-ttu-id="61ae2-115">组织团队的工作</span><span class="sxs-lookup"><span data-stu-id="61ae2-115">Organize your team’s work</span></span>
<span data-ttu-id="61ae2-116">Planner 提供了一个共享的空间，可以在其中构建团队、[创建任务](/graph/api/planner-post-tasks?view=graph-rest-1.0)，并将这些任务分配给团队中的其他人。</span><span class="sxs-lookup"><span data-stu-id="61ae2-116">Planner provides a shared space where you can build a team, [create tasks](/graph/api/planner-post-tasks?view=graph-rest-1.0), and assign them to others on the team.</span></span> <span data-ttu-id="61ae2-117">Planner 可让每个人轻松了解谁在做什么工作以及各项工作是否正常。你可以使用其他信息（如截止日期、进度和说明）来更新任务，然后使用可自定义的存储桶和类别标签对任务做进一步的组织。</span><span class="sxs-lookup"><span data-stu-id="61ae2-117">Planner makes it easy for everyone to know who’s doing what and if things are on track. You can update tasks with additional information like due dates, progress, and descriptions, and then further organize tasks with customizable buckets and category labels.</span></span>   

### <a name="collaborate-across-microsoft-365"></a><span data-ttu-id="61ae2-118">在整个 Microsoft 365 内协作</span><span class="sxs-lookup"><span data-stu-id="61ae2-118">Collaborate across Microsoft 365</span></span>
<span data-ttu-id="61ae2-119">Planner 可集成到整个 Microsoft 365 内的协作体验中。</span><span class="sxs-lookup"><span data-stu-id="61ae2-119">Planner integrates into collaboration experiences across Microsoft 365.</span></span> <span data-ttu-id="61ae2-120">除了 Planner Web 客户端和移动客户端，用户还可从 SharePoint 和 Microsoft Teams 中查看和更新 Planner 计划和任务。</span><span class="sxs-lookup"><span data-stu-id="61ae2-120">In addition to Planner web and mobile clients, users can view and update Planner plans and tasks from within SharePoint and Microsoft Teams.</span></span>  

<span data-ttu-id="61ae2-121">Microsoft Graph 和 Microsoft 365 组服务还支持 Planner 本身。</span><span class="sxs-lookup"><span data-stu-id="61ae2-121">Planner itself is also powered by the Microsoft Graph and the Microsoft 365 group service.</span></span> <span data-ttu-id="61ae2-122">上传并附加到 Planner 任务的文件将存储在 SharePoint 中。</span><span class="sxs-lookup"><span data-stu-id="61ae2-122">Files that you upload and attach to Planner tasks are stored in SharePoint.</span></span> <span data-ttu-id="61ae2-123">Planner 注释基于 Outlook 组对话。</span><span class="sxs-lookup"><span data-stu-id="61ae2-123">Planner comments are based on Outlook group conversations.</span></span>

<!-- Add image
Note: Put an image here showing the relationship between Planner and other things
-->

### <a name="automate-the-creation-of-plans-and-tasks"></a><span data-ttu-id="61ae2-124">自动创建计划和任务</span><span class="sxs-lookup"><span data-stu-id="61ae2-124">Automate the creation of plans and tasks</span></span>
<span data-ttu-id="61ae2-125">是否正在处理重复的流程或项目类型？</span><span class="sxs-lookup"><span data-stu-id="61ae2-125">Are you working on repeated process or project type?</span></span> <span data-ttu-id="61ae2-126">Planner API 可用于自动创建计划和任务列表。</span><span class="sxs-lookup"><span data-stu-id="61ae2-126">You can use the Planner API to automate the creation of a plan and a list of tasks.</span></span>  
 
## <a name="top-planner-api-tasks"></a><span data-ttu-id="61ae2-127">首要 Planner API 任务</span><span class="sxs-lookup"><span data-stu-id="61ae2-127">Top Planner API tasks</span></span>

|<span data-ttu-id="61ae2-128">操作</span><span class="sxs-lookup"><span data-stu-id="61ae2-128">Operation</span></span>|<span data-ttu-id="61ae2-129">URL</span><span class="sxs-lookup"><span data-stu-id="61ae2-129">URL</span></span>|
|:--------|:--|
|<span data-ttu-id="61ae2-130">查看组的所有[计划](/graph/api/resources/plannerplan?view=graph-rest-beta)</span><span class="sxs-lookup"><span data-stu-id="61ae2-130">See all the [plans](/graph/api/resources/plannerplan?view=graph-rest-beta) for a group</span></span>|<span data-ttu-id="61ae2-131">GET [https://graph.microsoft.com/v1.0/groups/{id}/planner/plans](https://developer.microsoft.com/graph/graph-explorer?request=groups/{id}/planner/plans&version=v1.0)</span><span class="sxs-lookup"><span data-stu-id="61ae2-131">GET [https://graph.microsoft.com/v1.0/groups/{id}/planner/plans](https://developer.microsoft.com/graph/graph-explorer?request=groups/{id}/planner/plans&version=v1.0)</span></span>|
|<span data-ttu-id="61ae2-132">查看计划中的[任务](/graph/api/resources/plannertask?view=graph-rest-beta)</span><span class="sxs-lookup"><span data-stu-id="61ae2-132">See [tasks](/graph/api/resources/plannertask?view=graph-rest-beta) in a plan</span></span>|<span data-ttu-id="61ae2-133">GET [https://graph.microsoft.com/v1.0/planner/plans/{id}/tasks](https://developer.microsoft.com/graph/graph-explorer?request=planner/plans/{id}/tasks&version=v1.0)</span><span class="sxs-lookup"><span data-stu-id="61ae2-133">GET [https://graph.microsoft.com/v1.0/planner/plans/{id}/tasks](https://developer.microsoft.com/graph/graph-explorer?request=planner/plans/{id}/tasks&version=v1.0)</span></span>|
|<span data-ttu-id="61ae2-134">查看不同计划中分配给我的所有[我的任务](/graph/api/planneruser-list-tasks?view=graph-rest-beta)</span><span class="sxs-lookup"><span data-stu-id="61ae2-134">See all [my tasks](/graph/api/planneruser-list-tasks?view=graph-rest-beta) assigned to me across plans</span></span>|<span data-ttu-id="61ae2-135">GET [https://graph.microsoft.com/v1.0/me/planner/tasks/](https://developer.microsoft.com/graph/graph-explorer?request=me/planner/tasks/&version=v1.0)</span><span class="sxs-lookup"><span data-stu-id="61ae2-135">GET [https://graph.microsoft.com/v1.0/me/planner/tasks/](https://developer.microsoft.com/graph/graph-explorer?request=me/planner/tasks/&version=v1.0)</span></span>|
|[<span data-ttu-id="61ae2-136">新建任务</span><span class="sxs-lookup"><span data-stu-id="61ae2-136">Create a new task</span></span>](/graph/api/planner-post-tasks?view=graph-rest-1.0)|<span data-ttu-id="61ae2-137">POST [https://graph.microsoft.com/v1.0/planner/tasks](https://developer.microsoft.com/graph/graph-explorer?request=groups/{id}/planner/plans&version=v1.0)</span><span class="sxs-lookup"><span data-stu-id="61ae2-137">POST [https://graph.microsoft.com/v1.0/planner/tasks](https://developer.microsoft.com/graph/graph-explorer?request=groups/{id}/planner/plans&version=v1.0)</span></span>|
|[<span data-ttu-id="61ae2-138">更新任务</span><span class="sxs-lookup"><span data-stu-id="61ae2-138">Update a task</span></span>](/graph/api/plannertask-update?view=graph-rest-1.0)|<span data-ttu-id="61ae2-139">PATCH [https://graph.microsoft.com/v1.0/planner/tasks/{task-id}](https://developer.microsoft.com/graph/graph-explorer?request=groups/{id}/planner/plans&version=v1.0)</span><span class="sxs-lookup"><span data-stu-id="61ae2-139">PATCH [https://graph.microsoft.com/v1.0/planner/tasks/{task-id}](https://developer.microsoft.com/graph/graph-explorer?request=groups/{id}/planner/plans&version=v1.0)</span></span>|
|[<span data-ttu-id="61ae2-140">删除任务</span><span class="sxs-lookup"><span data-stu-id="61ae2-140">Delete a task</span></span>](/graph/api/plannertask-delete?view=graph-rest-1.0)|<span data-ttu-id="61ae2-141">删除 [https://graph.microsoft.com/v1.0/planner/tasks/{id}](https://developer.microsoft.com/graph/graph-explorer?request=groups/{id}/planner/plans&version=v1.0)</span><span class="sxs-lookup"><span data-stu-id="61ae2-141">DELETE [https://graph.microsoft.com/v1.0/planner/tasks/{id}](https://developer.microsoft.com/graph/graph-explorer?request=groups/{id}/planner/plans&version=v1.0)</span></span>|

## <a name="api-reference"></a><span data-ttu-id="61ae2-142">API 参考</span><span class="sxs-lookup"><span data-stu-id="61ae2-142">API reference</span></span>
<span data-ttu-id="61ae2-143">在查找此服务的 API 参考？</span><span class="sxs-lookup"><span data-stu-id="61ae2-143">Looking for the API reference for this service?</span></span>

- [<span data-ttu-id="61ae2-144">Microsoft Graph v1.0 中的 Planner API</span><span class="sxs-lookup"><span data-stu-id="61ae2-144">Planner API in Microsoft Graph v1.0</span></span>](/graph/api/resources/planner-overview?view=graph-rest-1.0)
- [<span data-ttu-id="61ae2-145">Microsoft Graph beta 中的 Planner API</span><span class="sxs-lookup"><span data-stu-id="61ae2-145">Planner API in Microsoft Graph beta</span></span>](/graph/api/resources/planner-overview?view=graph-rest-beta)


## <a name="next-steps"></a><span data-ttu-id="61ae2-146">后续步骤</span><span class="sxs-lookup"><span data-stu-id="61ae2-146">Next steps</span></span>

- [<span data-ttu-id="61ae2-147">使用 Planner API</span><span class="sxs-lookup"><span data-stu-id="61ae2-147">Use the Planner API</span></span>](/graph/api/resources/planner-overview?view=graph-rest-1.0)
- [<span data-ttu-id="61ae2-148">使用计划</span><span class="sxs-lookup"><span data-stu-id="61ae2-148">Work with plans</span></span>](/graph/api/resources/planner-overview?view=graph-rest-1.0#plans)
- [<span data-ttu-id="61ae2-149">使用任务</span><span class="sxs-lookup"><span data-stu-id="61ae2-149">Work with tasks</span></span>](/graph/api/resources/planner-overview?view=graph-rest-1.0#tasks)
