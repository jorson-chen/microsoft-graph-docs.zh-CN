---
title: Skype for Business 对等活动报表
description: 可以获取组织中点对点活动的详细信息。 为组织调查、计划和做出其他业务决策时，便会发现这些详细信息非常有用。
localization_priority: Normal
ms.prod: reports
author: sarahwxy
doc_type: conceptualPageType
ms.openlocfilehash: 6980e17270db042535b07dd2550114e916827285
ms.sourcegitcommit: 479b366f3265b666fdc024b0f90b8d29764bb4b2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/26/2021
ms.locfileid: "49983039"
---
# <a name="skype-for-business-peer-to-peer-activity-reports"></a>Skype for Business 对等活动报表

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

可以获取组织中点对点活动的详细信息。 为组织调查、计划和做出其他业务决策时，便会发现这些详细信息非常有用。

> **注意：** 有关不同报告视图和名称的详细信息，请参阅 [Microsoft 365 报告 - Skype for Business 对等活动](https://support.office.com/client/Skype-for-Business-Online-peertopeer-activity-d3b2d569-4ee9-44b8-92bf-d518142f0713)。

## <a name="reports"></a>报告

| 函数                                 | CSV 返回类型 | JSON 返回类型                         | 说明                              |
| :--------------------------------------- | :-------------- | :--------------------------------------- | ---------------------------------------- |
| [获取活动计数](../api/reportroot-getskypeforbusinesspeertopeeractivitycounts.md) | Stream          | [skypeForBusinessPeerToPeerActivityCounts](../resources/skypeforbusinesspeertopeeractivitycounts.md) | 获取使用情况趋势，即组织中召开的会话的次数和类型。 会话类型包括 IM、音频、视频、应用共享和文件传输。 |
| [获取用户计数](../api/reportroot-getskypeforbusinesspeertopeeractivityusercounts.md) | Stream          | [skypeForBusinessPeerToPeerActivityUserCounts](../resources/skypeforbusinesspeertopeeractivityusercounts.md) | 获取使用情况趋势，即组织中召开的对等会话的唯一用户数和类型。 对等会话类型包括 IM、音频、视频、应用共享和文件传输。 |
| [获取分钟数](../api/reportroot-getskypeforbusinesspeertopeeractivityminutecounts.md) | Stream          | [skypeForBusinessPeerToPeerActivityMinuteCounts](../resources/skypeforbusinesspeertopeeractivityminutecounts.md) | 获取使用情况趋势，即组织中召开的对等会话的时长（以分钟为单位）和类型。 会话类型包括音频和视频。 |


