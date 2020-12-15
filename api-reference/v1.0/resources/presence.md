---
title: 状态资源类型
description: 包含有关用户状态的信息，包括其可用性和用户活动。
author: elvinyang-msft
localization_priority: Normal
doc_type: resourcePageType
ms.prod: cloud-communications
ms.openlocfilehash: 1122e14c91a8562757434e4bd36e267ed70790dd
ms.sourcegitcommit: 86d427ac670ebc3fdcf8e06541218bb74d39279d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/15/2020
ms.locfileid: "49675959"
---
# <a name="presence-resource-type"></a><span data-ttu-id="45ebf-103">状态资源类型</span><span class="sxs-lookup"><span data-stu-id="45ebf-103">presence resource type</span></span>

<span data-ttu-id="45ebf-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="45ebf-104">Namespace: microsoft.graph</span></span>

<span data-ttu-id="45ebf-105">包含有关用户状态的信息，包括其可用性和用户活动。</span><span class="sxs-lookup"><span data-stu-id="45ebf-105">Contains information about a user's presence, including their availability and user activity.</span></span>

> <span data-ttu-id="45ebf-106">**注意：** 此资源当前仅受 Microsoft Teams 用户支持。</span><span class="sxs-lookup"><span data-stu-id="45ebf-106">**Note:** This resource is currently only supported for Microsoft Teams users.</span></span>

<span data-ttu-id="45ebf-107">此资源支持订阅 [更改通知](/graph/webhooks)。</span><span class="sxs-lookup"><span data-stu-id="45ebf-107">This resource supports subscribing to [change notifications](/graph/webhooks).</span></span>

## <a name="methods"></a><span data-ttu-id="45ebf-108">方法</span><span class="sxs-lookup"><span data-stu-id="45ebf-108">Methods</span></span>

| <span data-ttu-id="45ebf-109">方法</span><span class="sxs-lookup"><span data-stu-id="45ebf-109">Method</span></span>                                                            | <span data-ttu-id="45ebf-110">返回类型</span><span class="sxs-lookup"><span data-stu-id="45ebf-110">Return Type</span></span>                                       | <span data-ttu-id="45ebf-111">说明</span><span class="sxs-lookup"><span data-stu-id="45ebf-111">Description</span></span>                                  |
|:------------------------------------------------------------------|:--------------------------------------------------|:---------------------------------------------|
| [<span data-ttu-id="45ebf-112">获取状态</span><span class="sxs-lookup"><span data-stu-id="45ebf-112">Get presence</span></span>](../api/presence-get.md)     | [<span data-ttu-id="45ebf-113">状态</span><span class="sxs-lookup"><span data-stu-id="45ebf-113">presence</span></span>](../resources/presence.md)     | <span data-ttu-id="45ebf-114">获取用户状态信息。</span><span class="sxs-lookup"><span data-stu-id="45ebf-114">Get a user's presence information.</span></span>
| [<span data-ttu-id="45ebf-115">获取多个用户状态</span><span class="sxs-lookup"><span data-stu-id="45ebf-115">Get presence of multiple users</span></span>](../api/cloudcommunications-getpresencesbyuserid.md)    |  <span data-ttu-id="45ebf-116">[presence](../resources/presence.md) 集合</span><span class="sxs-lookup"><span data-stu-id="45ebf-116">[presence](../resources/presence.md) collection</span></span>     |  <span data-ttu-id="45ebf-117">获取多个用户状态信息。</span><span class="sxs-lookup"><span data-stu-id="45ebf-117">Get the presence information for multiple users.</span></span>      |


## <a name="properties"></a><span data-ttu-id="45ebf-118">属性</span><span class="sxs-lookup"><span data-stu-id="45ebf-118">Properties</span></span>

| <span data-ttu-id="45ebf-119">关系</span><span class="sxs-lookup"><span data-stu-id="45ebf-119">Relationship</span></span>        | <span data-ttu-id="45ebf-120">类型</span><span class="sxs-lookup"><span data-stu-id="45ebf-120">Type</span></span>                                                 | <span data-ttu-id="45ebf-121">说明</span><span class="sxs-lookup"><span data-stu-id="45ebf-121">Description</span></span>                                                         |
|:--------------------|:-----------------------------------------------------|:--------------------------------------------------------------------|
|<span data-ttu-id="45ebf-122">id</span><span class="sxs-lookup"><span data-stu-id="45ebf-122">id</span></span>    |  <span data-ttu-id="45ebf-123">string</span><span class="sxs-lookup"><span data-stu-id="45ebf-123">string</span></span>     |  <span data-ttu-id="45ebf-124">用户对象 ID</span><span class="sxs-lookup"><span data-stu-id="45ebf-124">The user object id</span></span>   |
|<span data-ttu-id="45ebf-125">availability</span><span class="sxs-lookup"><span data-stu-id="45ebf-125">availability</span></span>    |  <span data-ttu-id="45ebf-126">字符串集合</span><span class="sxs-lookup"><span data-stu-id="45ebf-126">string collection</span></span>   |   <span data-ttu-id="45ebf-127">用户的基本状态信息。</span><span class="sxs-lookup"><span data-stu-id="45ebf-127">The base presence information for a user.</span></span> <span data-ttu-id="45ebf-128">可能的值是 `Available` `AvailableIdle` ， ， ， ， ， `Away` `BeRightBack` `Busy` `BusyIdle` ， ， `DoNotDisturb` `Offline``PresenceUnknown`</span><span class="sxs-lookup"><span data-stu-id="45ebf-128">Possible values are `Available`, `AvailableIdle`,  `Away`, `BeRightBack`, `Busy`, `BusyIdle`, `DoNotDisturb`, `Offline`, `PresenceUnknown`</span></span>  |
|<span data-ttu-id="45ebf-129">activity</span><span class="sxs-lookup"><span data-stu-id="45ebf-129">activity</span></span>    |  <span data-ttu-id="45ebf-130">字符串集合</span><span class="sxs-lookup"><span data-stu-id="45ebf-130">string collection</span></span>      |    <span data-ttu-id="45ebf-131">用户可用性的补充信息。</span><span class="sxs-lookup"><span data-stu-id="45ebf-131">The supplemental information to a user's availability.</span></span> <span data-ttu-id="45ebf-132">可能的值是 `Available` ， ， ， ， ， ， ， ， `Away` `BeRightBack` `Busy` `DoNotDisturb` `InACall` `InAConferenceCall` `Inactive` `InAMeeting` `Offline` ， `OffWork` `OutOfOffice` `PresenceUnknown` `Presenting` `UrgentInterruptionsOnly` ， 。</span><span class="sxs-lookup"><span data-stu-id="45ebf-132">Possible values are `Available`, `Away`, `BeRightBack`, `Busy`, `DoNotDisturb`, `InACall`, `InAConferenceCall`, `Inactive`, `InAMeeting`, `Offline`, `OffWork`, `OutOfOffice`, `PresenceUnknown`, `Presenting`, `UrgentInterruptionsOnly`.</span></span>       |

><span data-ttu-id="45ebf-133">**注意：** 若要详细了解不同的状态，请参阅 [Teams 中的用户状态](/microsoftteams/presence-admins)。</span><span class="sxs-lookup"><span data-stu-id="45ebf-133">**Note:** To learn more about the different presence states, see [User presence in Teams](/microsoftteams/presence-admins).</span></span> 

## <a name="relationships"></a><span data-ttu-id="45ebf-134">关系</span><span class="sxs-lookup"><span data-stu-id="45ebf-134">Relationships</span></span>

<span data-ttu-id="45ebf-135">无。</span><span class="sxs-lookup"><span data-stu-id="45ebf-135">None.</span></span>

## <a name="json-representation"></a><span data-ttu-id="45ebf-136">JSON 表示形式</span><span class="sxs-lookup"><span data-stu-id="45ebf-136">JSON representation</span></span>

<span data-ttu-id="45ebf-137">下面是资源的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="45ebf-137">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
  ],
  "@odata.type": "microsoft.graph.presence"
}-->
```json
{
   "id":"string",
   "availability":"string",
   "activity":"string"
}
```
