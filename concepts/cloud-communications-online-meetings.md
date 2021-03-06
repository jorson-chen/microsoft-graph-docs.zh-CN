---
title: 使用云通信 API 创建或加入联机会议
description: 你可以灵活地创建将来或即时举行的会议
author: ananmishr
localization_priority: Normal
ms.prod: cloud-communications
ms.openlocfilehash: 08d7195f3eb91ba896e8045b4576e46f12aaf795
ms.sourcegitcommit: 3fbc2249b307e8d3a9de18f22ef6911094ca272c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/26/2020
ms.locfileid: "48289349"
---
# <a name="use-the-cloud-communications-api-to-create-or-join-online-meetings"></a>使用云通信 API 创建或加入联机会议

联机会议提供了指定特定详细信息（如会议主题和所有与会者）的功能。 您还可以设置会议开始和结束的日期和时间。

在线会议提供了创建将来或即时召开会议的灵活性。 设置在创建后立即启动的会议的功能对于需要立即关注与会者的意外问题和其他事件来说是理想之选。

> **注释** 这组 Api 可提供与 Microsoft 团队或 Skype 功能的灵活性和更丰富的集成;它不会更新或创建日历中的任何事件。 若要方便地向 Outlook 日历中添加联机会议，请使用日历 API。 有关详细信息，请参阅[在 Microsoft Graph 中选择 API 以创建和加入联机会议](choose-online-meeting-api.md)。

## <a name="create-an-online-meeting"></a>创建联机会议

创建联机会议时，将接收会议的 [坐标](/graph/api/resources/onlinemeeting) 。 当参与者使用这些会议坐标加入会议时，将会创建一个组呼叫。

当所有参与者都离开组呼叫时，组呼叫将结束。 参与者仍可以使用相同的会议坐标在随后重新加入会议，但这将创建另一个组呼叫。

>**注意：** 创建的会议不会显示在日历上。

## <a name="join-an-online-meeting"></a>加入联机会议
在创建联机会议之后，用户可以通过以下两种方式加入：

1. 通过浏览器，使用作为[会议坐标](/graph/api/resources/onlinemeeting)一部分返回的**joinWebURL** 。

2. 通过 [创建调用 API](/graph/api/application-post-calls#example-5-join-scheduled-meeting-with-service-hosted-media)，它需要您提供 [会议坐标](/graph/api/resources/onlinemeeting)、 ([organizermeetinginfo](/graph/api/resources/organizermeetinginfo)和 [chatInfo](/graph/api/resources/chatinfo)) 。

## <a name="see-also"></a>另请参阅

- [联机会议权限](./permissions-reference.md#online-meetings-permissions)
- [在 Microsoft Graph 中选择 API 以创建和加入联机会议](choose-online-meeting-api.md)