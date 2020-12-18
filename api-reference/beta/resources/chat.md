---
title: 聊天资源类型
description: 聊天是一个或多个参与者之间的 chatMessages 集合。
author: AkJo
localization_priority: Normal
ms.prod: microsoft-teams
doc_type: resourcePageType
ms.openlocfilehash: 2a5fefdff40c60951c07d26df2962fbba1249a16
ms.sourcegitcommit: 0d4377b0153bc339ab7b3b1a6ee4d52848b622d4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/18/2020
ms.locfileid: "49714298"
---
# <a name="chat-resource-type"></a>聊天资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

聊天是一个或多个参与者之间的 [chatMessages](chatmessage.md) 集合。 参与者可以是用户或应用。

> **注意**：如果聊天与 [onlineMeeting](../resources/onlinemeeting.md) 实例关联，则列出的一些方法将可传递地影响会议。

## <a name="methods"></a>方法

|  方法       |  返回类型  | 说明| 
|:---------------|:--------|:----------|
|[列出聊天](../api/chat-list.md) | [chat](chat.md) 集合 | 获取用户参与的聊天列表。| 
|[创建聊天](../api/chat-post.md) | [聊天](chat.md) | 创建新聊天。| 
|[获取聊天](../api/chat-get.md) | [聊天](chat.md) | 读取聊天的属性和关系。| 
|[列出聊天成员](../api/chat-list-members.md) | [conversationMember](conversationmember.md) 集合 | 获取聊天中所有用户的列表。| 
|[添加聊天成员](../api/chat-post-members.md) | 位置标头 | 向聊天中添加用户。| 
|[获取聊天成员](../api/chat-get-members.md) | [conversationMember](conversationmember.md) | 获取聊天中的单个用户。| 
|[删除聊天成员](../api/chat-delete-members.md)|无|从聊天中删除用户。|
|[列出聊天中的消息](../api/chat-list-message.md)  | [chatMessage](../resources/chatmessage.md) | 获取一对一聊天或群组聊天中的消息。 | 
|[获取聊天中的消息](../api/chat-get-message.md)  | [chatMessage](../resources/chatmessage.md) | 获取聊天中的单个消息。 | 
|[获取用户和应用之间的聊天](../api/userscopeteamsappinstallation-get-chat.md) | [聊天](chat.md)| 获取用户与应用之间的一对一聊天 |
|[获取所有聊天消息](../api/chats-getallmessages.md)| [chat](chat.md) 集合| 从用户参与的所有聊天（包括一对一聊天、群聊和会议聊天）获取消息。 |
|[列出聊天中的应用](../api/chat-list-installedapps.md) |[teamsAppInstallation](teamsappinstallation.md) 集合 | 列出安装在聊天聊天 (关联的会议) 。|
|[获取聊天中的应用](../api/chat-get-installedapps.md) | [teamsAppInstallation](teamsappinstallation.md) | 获取在聊天聊天和关联会议 (安装的特定) 。|
|[在聊天中添加应用](../api/chat-post-installedapps.md) | | 添加 (在) 和关联的会议 (中安装) 。|
|[升级聊天中的应用](../api/chat-teamsappinstallation-upgrade.md) | 无 | 更新到安装在聊天会话和相关会议 (应用的) 。|
|[从聊天中卸载应用](../api/chat-delete-installedapps.md) | 无 | 从 (会议) 中删除 (应用程序) 。|
|[列出聊天中的选项卡](../api/chat-list-tabs.md) | [teamsTab](teamstab.md) | 列出固定到聊天聊天 (关联的会议) 。|
|[获取聊天中的选项卡](../api/chat-get-tabs.md) | [teamsTab](teamstab.md) | 获取固定到聊天会话和关联 (的特定选项卡) 。|
|[向聊天添加选项卡](../api/chat-post-tabs.md) | [teamsTab](teamstab.md) | 将 (固定) 选项卡添加到聊天 (关联的会议) 。|
|[聊天中的"更新"选项卡](../api/chat-patch-tabs.md) | [teamsTab](teamstab.md) | 更新聊天会话和关联会议 (选项卡) 。|
|[从聊天中删除选项卡](../api/chat-delete-tabs.md) | 无 | 从 (活动) 关联的会议选项卡 (取消固定) 。|

>**注意：** 使用应用程序权限时，请确保你了解如何获取聊天 ID。 由于不支持列出具有应用程序权限的聊天，因此并非所有方案都可行。 可以获取具有委派权限的聊天 ID，以及从具有应用程序权限 [的 /chats/getAllMessages](../api/subscription-post-subscriptions.md) 更改通知获取。

## <a name="properties"></a>属性

| 属性   | 类型 |说明|
|:---------------|:--------|:----------|
| id| String| 聊天的唯一标识符。 只读。|
| topic| String|   (聊天) 主题或主题的可选选项。 仅适用于群聊。|
| createdDateTime| dateTimeOffset|  创建聊天的日期和时间。 只读。|
| lastUpdatedDateTime| dateTimeOffset|  上次更改聊天或成员列表的日期和时间。 只读。|
| chatType| [chatType](../resources/chat.md#chattype-values) | 指定聊天类型。 可能的值是： `group` 和 `oneOnOne` `meeting` 。|

### <a name="chattype-values"></a>chatType 值 

| 成员             | 值 | 说明               |
| :----------------- | :---- | :------------------------ |
|oneOnOne            | 0     | 指示聊天为一对一聊天。 对于此类聊天，名单大小是固定的;无法删除/添加成员。|
|group               | 1     | 指示聊天是群聊。 可以针对 (更新至少两) 用户名单大小。 稍后可以删除/添加成员。|
|meeting             | 2     | 指示聊天与联机会议关联。 此类聊天仅作为联机会议创建的一部分创建。|
|unknownFutureValue  | 3     | 指示未来值的 Sentinel 值。 |

## <a name="relationships"></a>关系

| 关系 | 类型 |说明|
|:---------------|:--------|:----------|
| installedApps | [teamsAppInstallation](teamsappinstallation.md) 集合 | 聊天中所有应用的集合。 可为 Null。 |
| members | [conversationMember](conversationmember.md) 集合 | 聊天中所有成员的集合。 可为 Null。 |
| messages | [chatMessage](chatmessage.md) 集合 | 聊天中所有消息的集合。 可为 Null。 |

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.chat"
}-->

```json
{
  "id": "string (identifier)",
  "topic": "string",
  "createdDateTime": "dateTimeOffset",
  "lastUpdatedDateTime": "dateTimeOffset",
  "chatType": "String"
}
```

## <a name="see-also"></a>另请参阅

- [频道](channel.md)
- [chatMessage](chatmessage.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "chat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}
-->


