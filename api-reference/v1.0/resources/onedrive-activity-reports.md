---
title: OneDrive 活动报表
description: OneDrive 活动报表可用于获取每个有权使用 OneDrive 的用户的活动，具体是以用户与 OneDrive 文件的交互为依据。 此类报表也有助于了解以共享文件数为依据的协作级别。
localization_priority: Normal
ms.prod: reports
author: sarahwxy
doc_type: conceptualPageType
ms.openlocfilehash: 5a40e194b7ac315639842432ca279ce309248ed8
ms.sourcegitcommit: 479b366f3265b666fdc024b0f90b8d29764bb4b2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/26/2021
ms.locfileid: "49980981"
---
# <a name="onedrive-activity-reports"></a><span data-ttu-id="36a3e-104">OneDrive 活动报表</span><span class="sxs-lookup"><span data-stu-id="36a3e-104">OneDrive activity reports</span></span>

<span data-ttu-id="36a3e-105">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="36a3e-105">Namespace: microsoft.graph</span></span>

<span data-ttu-id="36a3e-106">OneDrive 活动报表可用于获取每个有权使用 OneDrive 的用户的活动，具体是以用户与 OneDrive 文件的交互为依据。</span><span class="sxs-lookup"><span data-stu-id="36a3e-106">Use the OneDrive activity reports to get the activity of every user licensed to use OneDrive by looking at their interaction with files on OneDrive.</span></span> <span data-ttu-id="36a3e-107">此类报表也有助于了解以共享文件数为依据的协作级别。</span><span class="sxs-lookup"><span data-stu-id="36a3e-107">These reports can help you to understand the level of collaboration going on by showing the number of files shared.</span></span>

> <span data-ttu-id="36a3e-108">**注意：** 有关不同报表视图和名称的详细信息，请参阅 [Microsoft 365 报表 - OneDrive for Business 活动](https://support.office.com/client/OneDrive-for-Business-user-activity-8bbe4bf8-221b-46d6-99a5-2fb3c8ef9353)。</span><span class="sxs-lookup"><span data-stu-id="36a3e-108">**Note:** For details about different report views and names, see [Microsoft 365 reports - OneDrive for Business activity](https://support.office.com/client/OneDrive-for-Business-user-activity-8bbe4bf8-221b-46d6-99a5-2fb3c8ef9353).</span></span>

## <a name="reports"></a><span data-ttu-id="36a3e-109">报告</span><span class="sxs-lookup"><span data-stu-id="36a3e-109">Reports</span></span>

| <span data-ttu-id="36a3e-110">函数</span><span class="sxs-lookup"><span data-stu-id="36a3e-110">Function</span></span>                                 | <span data-ttu-id="36a3e-111">返回类型</span><span class="sxs-lookup"><span data-stu-id="36a3e-111">Return Type</span></span> | <span data-ttu-id="36a3e-112">说明</span><span class="sxs-lookup"><span data-stu-id="36a3e-112">Description</span></span>                              |
| :--------------------------------------- | :---------- | :--------------------------------------- |
| [<span data-ttu-id="36a3e-113">获取用户详细信息</span><span class="sxs-lookup"><span data-stu-id="36a3e-113">Get user detail</span></span>](../api/reportroot-getonedriveactivityuserdetail.md) | <span data-ttu-id="36a3e-114">Stream</span><span class="sxs-lookup"><span data-stu-id="36a3e-114">Stream</span></span>      | <span data-ttu-id="36a3e-115">获取用户执行的 OneDrive 活动的详细信息。</span><span class="sxs-lookup"><span data-stu-id="36a3e-115">Get details about OneDrive activity by user.</span></span> |
| [<span data-ttu-id="36a3e-116">获取用户计数</span><span class="sxs-lookup"><span data-stu-id="36a3e-116">Get user counts</span></span>](../api/reportroot-getonedriveactivityusercounts.md) | <span data-ttu-id="36a3e-117">Stream</span><span class="sxs-lookup"><span data-stu-id="36a3e-117">Stream</span></span>      | <span data-ttu-id="36a3e-118">获取 OneDrive 活跃用户数趋势。</span><span class="sxs-lookup"><span data-stu-id="36a3e-118">Get the trend in the number of active OneDrive users.</span></span> |
| [<span data-ttu-id="36a3e-119">获取文件数</span><span class="sxs-lookup"><span data-stu-id="36a3e-119">Get file counts</span></span>](../api/reportroot-getonedriveactivityfilecounts.md) | <span data-ttu-id="36a3e-120">Stream</span><span class="sxs-lookup"><span data-stu-id="36a3e-120">Stream</span></span>      | <span data-ttu-id="36a3e-121">获取对任意 OneDrive 帐户执行文件交互的唯一许可用户数。</span><span class="sxs-lookup"><span data-stu-id="36a3e-121">Get the number of unique, licensed users that performed file interactions against any OneDrive account.</span></span> |


