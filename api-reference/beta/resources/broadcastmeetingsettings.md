---
title: broadcastMeetingSettings 资源类型
description: 与实时事件相关的设置
author: frankpeng7
localization_priority: Normal
ms.prod: cloud-communications
doc_type: resourcePageType
ms.openlocfilehash: 42ac666817b6f259dd888e479939216fc3e39c6c
ms.sourcegitcommit: dbbf77c732ae8d982e59865432b9b6147002a30a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/14/2021
ms.locfileid: "49866248"
---
# <a name="broadcastmeetingsettings-resource-type"></a>broadcastMeetingSettings 资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

与实时事件相关的设置。

> [!IMPORTANT]
> 此 API 不验证由策略管理的活动 [事件设置](/microsoftteams/teams-live-events/set-teams-live-events-policies-using-powershell)。
> 例如，如果管理员使用设置实时事件策略，将阻止用户在 Teams 客户端中设置实时事件权限，但可以通过 Microsoft Graph 将 `Set-CsTeamsMeetingBroadcastPolicy -Identity Global -BroadcastAttendeeVisibility EveryoneInCompany` `public` **allowedAudience** 设置为创建实时事件 `everyone` 。 

## <a name="properties"></a>属性

| 属性                   | 类型                     | 说明                                                                     |
| -------------------------- | ------------------------ | ------------------------------------------------------------------------------- |
| allowedAudience            | broadcastMeetingAudience | 定义可加入实时事件的人。 下表列出了可能的值。 |
| isRecordingEnabled         | 布尔                  | 指示是否为此实时事件启用录制。 默认值为 `false`。          |
| isAttendeeReportEnabled    | 布尔                  | 指示是否为此实时事件启用与会者报告。 默认值为 `false`。    |
| isQuestionAndAnswerEnabled | 布尔                  | 指示是否为此实时&启用问答。 默认值为 `false`。                |
| isVideoOnDemandEnabled     | 布尔                  | 指示是否为此实时事件启用视频按需播放。 默认值为 `false`。    |

### <a name="broadcastmeetingaudience-values"></a>broadcastMeetingAudience 值

| 值              | 说明                                                       |
| ------------------ | ----------------------------------------------------------------- |
| everyone           | 实时事件将向任何人开放。 此值为默认值。 |
| 组织       | 组织中的每个人都可以加入实时事件。                     |
| roleIsAttendee     | 只有指定的人员才能加入实时事件。                |
| unknownFutureValue | 未知未来值。                                             |

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [],
  "@odata.type": "microsoft.graph.broadcastMeetingSettings"
}-->
```json
{
  "allowedAudience": "String",
  "isRecordingEnabled": "Boolean",
  "isAttendeeReportEnabled": "Boolean",
  "isQuestionAndAnswerEnabled": "Boolean",
  "isVideoOnDemandEnabled": "Boolean"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "broadcastSettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
