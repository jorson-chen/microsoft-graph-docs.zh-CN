---
title: 频道资源类型
description: '频道是的团队中的 chatMessages 集合。 '
author: nkramer
localization_priority: Priority
ms.prod: microsoft-teams
doc_type: resourcePageType
ms.openlocfilehash: e941379cbe9253ed79eb193f4cbc49284213b0a3
ms.sourcegitcommit: 0d4377b0153bc339ab7b3b1a6ee4d52848b622d4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/18/2020
ms.locfileid: "49714261"
---
# <a name="channel-resource-type"></a>频道资源类型

命名空间：microsoft.graph

[Teams](../resources/team.md) 由频道组成，是你与团队成员的对话。 每个频道专用于特定主题、部门或项目。 频道是工作实际完成的地方 - 对整个团队开放的文本、音频和视频对话的位置、共享文件的位置以及添加标签的位置。

## <a name="methods"></a>方法

| 方法       | 返回类型  |说明|
|:---------------|:--------|:----------|
|[列出频道](../api/channel-list.md) | [频道](channel.md)集合 | 获取此团队中的频道列表。|
|[创建频道](../api/channel-post.md) | [频道](channel.md) | 通过包含显示名称和描述来新建频道。|
|[获取频道](../api/channel-get.md) | [频道](channel.md) | 读取频道的属性和关系。|
|[更新频道](../api/channel-patch.md) | [频道](channel.md) | 更新频道属性。|
|[删除频道](../api/channel-delete.md) | 无 | 删除通道。|
|[获取消息 Delta](../api/chatmessage-delta.md)  | [chatMessage](../resources/chatmessage.md) | 获取频道中的增量消息。 |
|[列出频道消息](../api/channel-list-messages.md)  | [chatMessage](../resources/chatmessage.md) | 获取频道中的消息 |
|[创建频道消息发布](../api/channel-post-message.md) | [chatMessage](../resources/chatmessage.md) | 向频道发送消息。 |
|[创建回复频道消息发布](../api/channel-post-messagereply.md) | [chatMessage](../resources/chatmessage.md) | 在频道中回复消息。|
|[获取文件文件夹](../api/channel-get-filesfolder.md)| [driveItem](driveitem.md) | 检索用于存储频道文件的 SharePoint 文件夹的详细信息。 |
|[列出频道成员](../api/channel-list-members.md) | [conversationMember](conversationmember.md) 集合 | 获取频道中的成员列表。|
|[添加频道成员](../api/channel-post-members.md) | [conversationMember](conversationmember.md) | 向频道添加成员。 仅支持 membershipType 为 `private` 的 `channel`。|
|[获取频道成员](../api/channel-get-members.md) | [conversationMember](conversationmember.md) 集合 | 获取频道中的成员。|
|[更新频道成员角色](../api/channel-update-members.md) | [conversationMember](conversationmember.md) | 更新频道成员的属性。 仅支持 membershipType 为 `private` 的频道。|
|[删除频道成员](../api/channel-delete-members.md) | 无 | 从频道中删除一个成员。 仅支持用于 `private` 的 `channelType`。|
|[列出频道中的选项卡](../api/channel-list-tabs.md) | [teamsTab](teamstab.md) | 列出固定到频道的选项卡。|
|[将选项卡添加到频道](../api/channel-post-tabs.md) | [teamsTab](teamstab.md) | 将选项卡添加（固定）到频道。|
|[获取频道中的选项卡](../api/channel-get-tabs.md) | [teamsTab](teamstab.md) | 获取固定到频道的特定选项卡。|
|[更新频道中的选项卡](../api/channel-patch-tabs.md) | [teamsTab](teamstab.md) | 更新频道中的选项卡的属性。|
|[从频道中删除选项卡](../api/channel-delete-tabs.md) | 无 | 从频道中删除（取消固定）选项卡。|

## <a name="properties"></a>属性

| 属性   | 类型 |说明|
|:---------------|:--------|:----------|
|说明|String|频道的可选文本描述。|
|displayName|String|在 Microsoft Teams 中呈现在用户面前的频道名称。|
|id|String|频道的唯一标识符。 只读。|
|isFavoriteByDefault|Boolean|指示是否应对团队的所有成员将频道自动标记到“收藏夹”。 仅可使用“[创建团队](../api/team-post.md)”以编程方式设置。 默认值：`false`。|
|email|String| 用于向频道发送邮件的电子邮件地址。 只读。|
|webUrl|String|将转到 Microsoft Teams 中的频道的超链接。 在 Microsoft Teams 中右键单击某个频道并选择“获取频道链接”即可获得此 URL。 应将此 URL 视为不透明的 blob，而不对其进行解析。 只读。|
|membershipType|channelMembershipType|频道的类型。 可在创建期间设置，但不可更改。 可能的值有：`standard` - 频道继承父团队的成员列表；`private` - 频道可以具有父团队中所有成员的子集的成员。
|createdDateTime|dateTimeOffset|只读。 创建频道的时间戳。|

## <a name="relationships"></a>关系

| 关系 | 类型 |说明|
|:---------------|:--------|:----------|
|messages|[chatMessage](chatmessage.md) 集合|频道中的所有消息集合。 一种导航属性。 可为 NULL。|
|选项卡|[teamsTab](../resources/teamstab.md) 集合|频道中的所有选项卡集合。 一种导航属性。|
|成员|[conversationMember](conversationmember.md) 集合|与频道关联的成员资格记录的集合。|
|[filesFolder](../api/channel-get-filesfolder.md)|[driveItem](driveitem.md)|用于存储频道文件的位置的元数据。|
|operations|[teamsAsyncOperation](teamsasyncoperation.md) 集合| 在此团队中运行过或正在运行的异步操作。 |

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "messages"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.channel"
}-->

```json
{
  "description": "string",
  "displayName": "string",
  "id": "string (identifier)",
  "isFavoriteByDefault": true,
  "email": "string",
  "webUrl": "string",
  "membershipType": "string",
  "createdDateTime": "string (timestamp)"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "channel resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
