---
title: win32LobAppRestartBehavior 枚举类型
description: 指示重新启动操作的类型。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: enumPageType
ms.openlocfilehash: 6747b9b0b3f46e5c2fcf913725d915232a1559ed
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2019
ms.locfileid: "37538544"
---
# <a name="win32lobapprestartbehavior-enum-type"></a><span data-ttu-id="99848-103">win32LobAppRestartBehavior 枚举类型</span><span class="sxs-lookup"><span data-stu-id="99848-103">win32LobAppRestartBehavior enum type</span></span>

> <span data-ttu-id="99848-104">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="99848-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="99848-105">**注意：** 适用于 Intune 的 Microsoft Graph API 需要租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="99848-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="99848-106">指示重新启动操作的类型。</span><span class="sxs-lookup"><span data-stu-id="99848-106">Indicates the type of restart action.</span></span>

## <a name="members"></a><span data-ttu-id="99848-107">成员</span><span class="sxs-lookup"><span data-stu-id="99848-107">Members</span></span>
|<span data-ttu-id="99848-108">成员</span><span class="sxs-lookup"><span data-stu-id="99848-108">Member</span></span>|<span data-ttu-id="99848-109">值</span><span class="sxs-lookup"><span data-stu-id="99848-109">Value</span></span>|<span data-ttu-id="99848-110">说明</span><span class="sxs-lookup"><span data-stu-id="99848-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="99848-111">basedOnReturnCode</span><span class="sxs-lookup"><span data-stu-id="99848-111">basedOnReturnCode</span></span>|<span data-ttu-id="99848-112">0</span><span class="sxs-lookup"><span data-stu-id="99848-112">0</span></span>|<span data-ttu-id="99848-113">如果操作返回重新启动代码，则在运行应用程序安装后，Intune 将重新启动设备。</span><span class="sxs-lookup"><span data-stu-id="99848-113">Intune will restart the device after running the app installation if the operation returns a reboot code.</span></span>|
|<span data-ttu-id="99848-114">允许</span><span class="sxs-lookup"><span data-stu-id="99848-114">allow</span></span>|<span data-ttu-id="99848-115">1</span><span class="sxs-lookup"><span data-stu-id="99848-115">1</span></span>|<span data-ttu-id="99848-116">Intune 不会对由应用安装引起的重新启动代码执行任何特定操作。</span><span class="sxs-lookup"><span data-stu-id="99848-116">Intune will not take any specific action on reboot codes resulting from app installations.</span></span> <span data-ttu-id="99848-117">Intune 不会尝试取消对 MSI 应用的重新启动。</span><span class="sxs-lookup"><span data-stu-id="99848-117">Intune will not attempt to suppress restarts for MSI apps.</span></span>|
|<span data-ttu-id="99848-118">强制</span><span class="sxs-lookup"><span data-stu-id="99848-118">suppress</span></span>|<span data-ttu-id="99848-119">双面</span><span class="sxs-lookup"><span data-stu-id="99848-119">2</span></span>|<span data-ttu-id="99848-120">Intune 将尝试取消对 MSI 应用的重新启动。</span><span class="sxs-lookup"><span data-stu-id="99848-120">Intune will attempt to suppress restarts for MSI apps.</span></span>|
|<span data-ttu-id="99848-121">有效</span><span class="sxs-lookup"><span data-stu-id="99848-121">force</span></span>|<span data-ttu-id="99848-122">第三章</span><span class="sxs-lookup"><span data-stu-id="99848-122">3</span></span>|<span data-ttu-id="99848-123">Intune 将强制在应用程序安装操作完成后立即重新启动设备。</span><span class="sxs-lookup"><span data-stu-id="99848-123">Intune will force the device to restart immediately after the app installation operation.</span></span>|


