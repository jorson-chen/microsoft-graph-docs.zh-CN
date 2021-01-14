---
title: onlineMeeting 资源类型
description: 包含有关会议的信息。
author: ananmishr
localization_priority: Normal
doc_type: resourcePageType
ms.prod: cloud-communications
ms.openlocfilehash: 139cd4a20a6097691189d1bd1f843850ba911a21
ms.sourcegitcommit: dbbf77c732ae8d982e59865432b9b6147002a30a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/14/2021
ms.locfileid: "49866107"
---
# <a name="onlinemeeting-resource-type"></a>onlineMeeting 资源类型

命名空间：microsoft.graph

包含有关会议的信息，包括用于加入会议的 URL、与会者列表和说明。

## <a name="methods"></a>Methods

| 方法                                                             | 返回类型                       | 说明                                                                                                  |
| :----------------------------------------------------------------- | :-------------------------------- | :----------------------------------------------------------------------------------------------------------- |
| [创建 onlineMeeting](../api/application-post-onlineMeetings.md)  | [onlineMeeting](onlinemeeting.md) | 创建联机会议。                                                                                    |
| [获取 onlineMeeting](../api/onlinemeeting-get.md)                   | [onlineMeeting](onlinemeeting.md) | 读取 **onlineMeeting 对象的属性和** 关系。                                        |
| [删除 onlineMeeting](../api/onlinemeeting-delete.md)             | 无                              | 删除联机会议。                                                                                    |
| [创建或获取 onlineMeeting](../api/onlinemeeting-createorget.md) | [onlineMeeting](onlinemeeting.md) | 使用自定义外部 ID 创建联机会议。 如果会议已存在，请检索其属性。 |

## <a name="properties"></a>属性

| 属性              | 类型                                          | 说明                                                                                                                |
| :-------------------- | :-------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------- |
| audioConferencing     | [audioConferencing](audioconferencing.md)     | 电话访问 (拨入) 联机会议的信息。 只读。                                                   |
| chatInfo              | [chatInfo](chatinfo.md)                       | 与此联机会议关联的聊天信息。                                                                  |
| creationDateTime      | 日期时间                                      | 会议创建时间（UTC）。 只读。                                                                               |
| startDateTime         | 日期时间                                      | 会议开始时间（UTC）。                                                                                             |
| endDateTime           | 日期时间                                      | 会议结束时间（UTC）。                                                                                               |
| id                    | String                                        | 与联机会议关联的默认 ID。 只读。                                                              |
| joinWebUrl            | String                                        | 联机会议加入 URL。 只读。                                                                             |
| participants          | [meetingParticipants](meetingparticipants.md) | 与联机会议关联的参与者。  这包括组织者和与会者。                       |
| subject               | String                                        | 联机会议的主题。                                                                                         |
| videoTeleconferenceId | String                                        | 视频电话会议 ID。 只读。                                                                                  |
| joinInformation       | [itemBody](itembody.md)                       | 请求 HTTP 标头中指定的语言和区域设置变量 `Accept-Language` 的联接信息。 只读。 |
| isEntryExitAnnounced  | 布尔                                       | 呼叫者加入或离开时是否宣布。                                                                     |
| lobbyBypassSettings   | [lobbyBypassSettings](lobbyBypassSettings.md) | 指定哪些参与者可以绕过会议厅。                                                               |
| allowedPresenters     | onlineMeetingPresenters                       | 指定可在会议中成为演示者的人。 下表列出了可能的值。                          |

### <a name="onlinemeetingpresenters-values"></a>onlineMeetingPresenters 值

| 值              | 说明                                                   |
| ------------------ | ------------------------------------------------------------- |
| everyone           | 每个人都是演示者 (这是默认选项) 。             |
| 组织       | 组织者组织中的每个人都是演示者。          |
| roleIsPresenter    | 只有其角色为演示者的参与者是演示者。 |
| 组织者          | 只有组织者是演示者。                           |
| unknownFutureValue | 未知未来值。                                          |

## <a name="json-representation"></a>JSON 表示形式

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onlineMeeting"
}-->
```json
{
  "audioConferencing": {"@odata.type": "#microsoft.graph.audioConferencing"},
  "chatInfo": {"@odata.type": "#microsoft.graph.chatInfo"},
  "creationDateTime": "String (timestamp)",
  "endDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "joinWebUrl": "String",
  "participants": {"@odata.type": "#microsoft.graph.meetingParticipants"},
  "startDateTime": "String (timestamp)",
  "subject": "String",
  "videoTeleconferenceId": "String",
  "isEntryExitAnnounced": "Boolean",
  "lobbyBypassSettings": {"@odata.type": "#microsoft.graph.lobbyBypassSettings"},
  "allowedPresenters": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onlineMeeting resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

