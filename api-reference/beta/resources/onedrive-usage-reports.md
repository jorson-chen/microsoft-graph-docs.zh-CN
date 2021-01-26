---
title: OneDrive 使用情况报表
description: 你可以从 OneDrive 获取值的高级别视图，了解组织中所有 OneDrive 帐户使用的文件总数和存储。 然后，可以向下钻取活跃 OneDrive 帐户的趋势、用户已交互的文件数以及使用的存储空间。 它还提供每个 OneDrive 帐户的详细信息。
localization_priority: Normal
ms.prod: reports
author: sarahwxy
doc_type: conceptualPageType
ms.openlocfilehash: e1c6128fab80fb0b7a0ec1391f4022bb625b2442
ms.sourcegitcommit: 479b366f3265b666fdc024b0f90b8d29764bb4b2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/26/2021
ms.locfileid: "49983207"
---
# <a name="onedrive-usage-reports"></a><span data-ttu-id="b855b-105">OneDrive 使用情况报表</span><span class="sxs-lookup"><span data-stu-id="b855b-105">OneDrive usage reports</span></span>

<span data-ttu-id="b855b-106">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="b855b-106">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="b855b-107">你可以从 OneDrive 获取值的高级别视图，了解组织中所有 OneDrive 帐户使用的文件总数和存储。</span><span class="sxs-lookup"><span data-stu-id="b855b-107">You can get a high-level view of the value you are getting from OneDrive in terms of the total number of files and storage used across all the OneDrive accounts in your organization.</span></span> <span data-ttu-id="b855b-108">然后，可以向下钻取活跃 OneDrive 帐户的趋势、用户已交互的文件数以及使用的存储空间。</span><span class="sxs-lookup"><span data-stu-id="b855b-108">You can then drill down to understand the trends of active OneDrive accounts, how many files users have interacted with, and how much storage is used.</span></span> <span data-ttu-id="b855b-109">它还提供每个 OneDrive 帐户的详细信息。</span><span class="sxs-lookup"><span data-stu-id="b855b-109">It also gives you the per OneDrive account details.</span></span>

> <span data-ttu-id="b855b-110">**注意：** 有关不同报表视图和名称的详细信息，请参阅 [Microsoft 365 报表 - OneDrive for Business 使用情况](https://support.office.com/client/OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680)。</span><span class="sxs-lookup"><span data-stu-id="b855b-110">**Note:** For details about different report views and names, see [Microsoft 365 reports - OneDrive for Business usage](https://support.office.com/client/OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680).</span></span>

## <a name="reports"></a><span data-ttu-id="b855b-111">报告</span><span class="sxs-lookup"><span data-stu-id="b855b-111">Reports</span></span>

| <span data-ttu-id="b855b-112">函数</span><span class="sxs-lookup"><span data-stu-id="b855b-112">Function</span></span>                                 | <span data-ttu-id="b855b-113">CSV 返回类型</span><span class="sxs-lookup"><span data-stu-id="b855b-113">CSV return type</span></span> | <span data-ttu-id="b855b-114">JSON 返回类型</span><span class="sxs-lookup"><span data-stu-id="b855b-114">JSON return type</span></span>                         | <span data-ttu-id="b855b-115">说明</span><span class="sxs-lookup"><span data-stu-id="b855b-115">Description</span></span>                              |
| :--------------------------------------- | :-------------- | ---------------------------------------- | ---------------------------------------- |
| [<span data-ttu-id="b855b-116">获取帐户详细信息</span><span class="sxs-lookup"><span data-stu-id="b855b-116">Get account detail</span></span>](../api/reportroot-getonedriveusageaccountdetail.md) | <span data-ttu-id="b855b-117">Stream</span><span class="sxs-lookup"><span data-stu-id="b855b-117">Stream</span></span>          | [<span data-ttu-id="b855b-118">oneDriveUsageAccountDetail</span><span class="sxs-lookup"><span data-stu-id="b855b-118">oneDriveUsageAccountDetail</span></span>](../resources/onedriveusageaccountdetail.md) | <span data-ttu-id="b855b-119">获取帐户的 OneDrive 使用情况的详细信息。</span><span class="sxs-lookup"><span data-stu-id="b855b-119">Get details about OneDrive usage by account.</span></span> |
| [<span data-ttu-id="b855b-120">获取帐户数</span><span class="sxs-lookup"><span data-stu-id="b855b-120">Get account counts</span></span>](../api/reportroot-getonedriveusageaccountcounts.md) | <span data-ttu-id="b855b-121">Stream</span><span class="sxs-lookup"><span data-stu-id="b855b-121">Stream</span></span>          | [<span data-ttu-id="b855b-122">oneDriveUsageAccountCounts</span><span class="sxs-lookup"><span data-stu-id="b855b-122">oneDriveUsageAccountCounts</span></span>](../resources/onedriveusageaccountcounts.md) | <span data-ttu-id="b855b-123">获取 OneDrive for Business 活跃网站数趋势。</span><span class="sxs-lookup"><span data-stu-id="b855b-123">Get the trend in the number of active OneDrive for Business sites.</span></span> <span data-ttu-id="b855b-124">用户在其中查看、修改、上传、下载、共享或同步文件的任何网站都被视为活跃网站。</span><span class="sxs-lookup"><span data-stu-id="b855b-124">Any site on which users viewed, modified, uploaded, downloaded, shared, or synced files is considered an active site.</span></span> |
| [<span data-ttu-id="b855b-125">获取文件数</span><span class="sxs-lookup"><span data-stu-id="b855b-125">Get file counts</span></span>](../api/reportroot-getonedriveusagefilecounts.md) | <span data-ttu-id="b855b-126">Stream</span><span class="sxs-lookup"><span data-stu-id="b855b-126">Stream</span></span>          | [<span data-ttu-id="b855b-127">oneDriveUsageFileCounts</span><span class="sxs-lookup"><span data-stu-id="b855b-127">oneDriveUsageFileCounts</span></span>](../resources/onedriveusagefilecounts.md) | <span data-ttu-id="b855b-128">获取跨所有网站的文件总数和活跃文件数。</span><span class="sxs-lookup"><span data-stu-id="b855b-128">Get the total number of files across all sites and how many are active files.</span></span> <span data-ttu-id="b855b-129">如果文件在指定时间段内被保存、同步、修改或共享，则视为活跃文件。</span><span class="sxs-lookup"><span data-stu-id="b855b-129">A file is considered active if it has been saved, synced, modified, or shared within the specified time period.</span></span> |
| [<span data-ttu-id="b855b-130">获取存储</span><span class="sxs-lookup"><span data-stu-id="b855b-130">Get storage</span></span>](../api/reportroot-getonedriveusagestorage.md) | <span data-ttu-id="b855b-131">Stream</span><span class="sxs-lookup"><span data-stu-id="b855b-131">Stream</span></span>          | [<span data-ttu-id="b855b-132">siteUsageStorage</span><span class="sxs-lookup"><span data-stu-id="b855b-132">siteUsageStorage</span></span>](../resources/siteusagestorage.md) | <span data-ttu-id="b855b-133">获取 OneDrive for Business 使用的存储空间趋势。</span><span class="sxs-lookup"><span data-stu-id="b855b-133">Get the trend on the amount of storage you are using in OneDrive for Business.</span></span> |


