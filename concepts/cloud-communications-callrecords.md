---
title: 呼叫记录概述
description: 呼叫记录可帮助您深入了解组织内发生的呼叫和会议。
author: stephenjust
localization_priority: Normal
ms.prod: cloud-communications
ms.openlocfilehash: 4999f4b0d479b6e618055d39a3fecab340deb650
ms.sourcegitcommit: d3b6e4d11012e6b4c775afcec4fe5444e3a99bd3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/03/2020
ms.locfileid: "42394637"
---
# <a name="call-records-overview"></a><span data-ttu-id="89447-103">呼叫记录概述</span><span class="sxs-lookup"><span data-stu-id="89447-103">Call records overview</span></span>

<span data-ttu-id="89447-104">呼叫记录提供了使用 Microsoft 团队或 Skype for Business 时在组织内发生的呼叫和联机会议的使用和诊断信息。</span><span class="sxs-lookup"><span data-stu-id="89447-104">Call records provide usage and diagnostic information about the calls and online meetings that occur within your organization when using Microsoft Teams or Skype for Business.</span></span> <span data-ttu-id="89447-105">可以使用使用率和诊断数据来为您的企业生成自定义报告，以帮助监控采用或解决呼叫质量问题。</span><span class="sxs-lookup"><span data-stu-id="89447-105">Usage and diagnostic data can be consumed to produce custom reporting for your business to help monitor adoption or to troubleshoot call quality issues.</span></span>

<span data-ttu-id="89447-106">组织可以使用 Microsoft Graph [webhook 订阅](/graph/api/resources/webhooks?view=graph-rest-beta)功能订阅对呼叫记录所做的更改，从而允许他们生成来自数据的近实时报告或在某些情况下（如紧急呼叫）发出警报。</span><span class="sxs-lookup"><span data-stu-id="89447-106">Organizations can subscribe to changes to call records using the Microsoft Graph [webhook subscriptions](/graph/api/resources/webhooks?view=graph-rest-beta) capability, allowing them to build near-real-time reports from the data or to alert on certain scenarios like emergency calls.</span></span>

> <span data-ttu-id="89447-107">**重要说明：** 授予对应用程序的 CallRecords 权限时，请务必谨慎。</span><span class="sxs-lookup"><span data-stu-id="89447-107">**Important:** Use discretion when granting the CallRecords.Read.All permission to applications.</span></span> <span data-ttu-id="89447-108">呼叫记录可提供业务运营的见解，因此可以成为恶意参与者的目标。</span><span class="sxs-lookup"><span data-stu-id="89447-108">Call records can provide insights into the operation of your business, and therefore can be a target for malicious actors.</span></span> <span data-ttu-id="89447-109">仅向你信任的应用程序授予此权限，以满足你的数据保护要求。</span><span class="sxs-lookup"><span data-stu-id="89447-109">Only grant this permission to applications you trust to meet your data protection requirements.</span></span>

## <a name="subscribe-to-call-records"></a><span data-ttu-id="89447-110">订阅呼叫记录</span><span class="sxs-lookup"><span data-stu-id="89447-110">Subscribe to call records</span></span>

<span data-ttu-id="89447-111">组织和合作伙伴通常拥有自己的工具来生成有关呼叫和联机会议的报告。</span><span class="sxs-lookup"><span data-stu-id="89447-111">Organizations and partners often have their own tooling for generating reports about calls and online meetings.</span></span> <span data-ttu-id="89447-112">使用 webhook，他们可以在创建呼叫记录时接收连续的呼叫记录源。</span><span class="sxs-lookup"><span data-stu-id="89447-112">Using webhooks, they can receive a continuous feed of call records as they are created.</span></span> <span data-ttu-id="89447-113">此推送模型使组织和合作伙伴能够构建自己的实时报告解决方案。</span><span class="sxs-lookup"><span data-stu-id="89447-113">This push-model enables organizations and partners to build their own real-time reporting solutions.</span></span>

## <a name="look-up-a-call-record-by-its-call-id"></a><span data-ttu-id="89447-114">按呼叫 ID 查找呼叫记录</span><span class="sxs-lookup"><span data-stu-id="89447-114">Look up a call record by its call ID</span></span>

<span data-ttu-id="89447-115">应用程序可以按其 ID 检索[呼叫记录](/graph/api/resources/callrecords-callrecord?view=graph-rest-beta)。</span><span class="sxs-lookup"><span data-stu-id="89447-115">Applications can retrieve a [call record](/graph/api/resources/callrecords-callrecord?view=graph-rest-beta) by its ID.</span></span> <span data-ttu-id="89447-116">可以从 webhook 通知或从管理工具检索到此 ID。</span><span class="sxs-lookup"><span data-stu-id="89447-116">This ID can be determined from a webhook notification or retrieved from administrative tools.</span></span>

## <a name="see-also"></a><span data-ttu-id="89447-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="89447-117">See also</span></span>

- [<span data-ttu-id="89447-118">呼叫记录权限</span><span class="sxs-lookup"><span data-stu-id="89447-118">Call records permissions</span></span>](/graph/permissions-reference#call-records-permissions)