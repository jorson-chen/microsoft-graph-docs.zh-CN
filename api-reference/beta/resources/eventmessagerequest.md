---
title: eventMessageRequest 资源类型
description: 表示会议请求的邮件。
author: harini84
localization_priority: Normal
ms.prod: outlook
doc_type: resourcePageType
ms.openlocfilehash: 3452e51fb00514735451c598329f4ca9a89426fb
ms.sourcegitcommit: 3cd8584827fef6751d40979aa5f950f3c46ff27d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/24/2020
ms.locfileid: "48755720"
---
# <a name="eventmessagerequest-resource-type"></a>eventMessageRequest 资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

表示被邀请者邮箱中的会议请求的邮件。

**EventMessageRequest**实体是从[eventMessage](eventmessage.md)派生的。

若要响应会议请求，请先使用 **事件** 导航属性访问相应的事件，如以下 [示例](../api/eventmessage-get.md#example-2)所示。 然后， [接受](../api/event-accept.md)、 [tentativelyAccept](../api/event-tentativelyaccept.md)或 [拒绝](../api/event-decline.md) 与 **eventMessageRequest**关联的事件。

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.eventMessage",
  "optionalProperties": [
    "attachments",
    "event",
    "extensions",
    "mentions",
    "previousLocation",
    "previousStartDateTime",
    "previousEndDateTime"
  ],
  "@odata.type": "microsoft.graph.eventMessageRequest"
}-->

```json
{
  "allowNewTimeProposals": "Boolean",
  "bccRecipients": [{"@odata.type": "microsoft.graph.recipient"}],
  "body": {"@odata.type": "microsoft.graph.itemBody"},
  "bodyPreview": "string",
  "categories": ["string"],
  "ccRecipients": [{"@odata.type": "microsoft.graph.recipient"}],
  "changeKey": "string",
  "conversationId": "string",
  "conversationIndex": "String (binary)",
  "createdDateTime": "String (timestamp)",
  "endDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "from": {"@odata.type": "microsoft.graph.recipient"},
  "hasAttachments": true,
  "id": "string (identifier)",
  "importance": "String",
  "inferenceClassification": "String",
  "isDelegated": true,
  "isDeliveryReceiptRequested": true,
  "isDraft": true,
  "isOutOfDate": "Boolean",
  "isRead": true,
  "isReadReceiptRequested": true,
  "lastModifiedDateTime": "String (timestamp)",
  "location": {"@odata.type": "microsoft.graph.location"},
  "meetingMessageType": "microsoft.graph.meetingMessageType",
  "mentionsPreview": {"@odata.type": "microsoft.graph.mentionsPreview"},
  "parentFolderId": "string",
  "previousEndDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "previousLocation": {"@odata.type": "microsoft.graph.location"},
  "previousStartDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "receivedDateTime": "String (timestamp)",
  "recurrence": {"@odata.type": "microsoft.graph.patternedRecurrence"},
  "replyTo": [{"@odata.type": "microsoft.graph.recipient"}],
  "responseRequested": "Boolean",
  "sender": {"@odata.type": "microsoft.graph.recipient"},
  "sentDateTime": "String (timestamp)",
  "startDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "subject": "string",
  "toRecipients": [{"@odata.type": "microsoft.graph.recipient"}],
  "type": "string",
  "uniqueBody": {"@odata.type": "microsoft.graph.itemBody"},
  "webLink": "string"
}

```
## <a name="properties"></a>属性
| 属性     | 类型   |说明|
|:---------------|:--------|:----------|
|allowNewTimeProposals| 布尔值 | 如果会议组织者允许被邀请者在响应时建议新时间，则为`True`；否则为 `false`。 可选。 默认值为 `true`。 |
|bccRecipients|[recipient](recipient.md) collection|邮件的密件抄送收件人。|
|body|[itemBody](itembody.md)|邮件的正文。|
|bodyPreview|String|邮件正文中的前 255 个字符。|
|categories|String collection|与邮件关联的类别。|
|ccRecipients|[recipient](recipient.md) collection|邮件的抄送收件人。|
|changeKey|String|邮件的版本。|
|conversationId|String|电子邮件所属对话的 ID。|
|conversationIndex|Edm.Binary|电子邮件所属对话的索引。|
|createdDateTime|DateTimeOffset|创建邮件的日期和时间。|
|endDateTime|[DateTimeTimeZone](datetimetimezone.md)|请求的会议的结束时间。|
|发件人|[recipient](recipient.md)|发送邮件邮箱的所有者。 在多数情况中，此数值与“**发件人**”属性相同，但共享或委派情景除外。 值必须对应于使用的实际邮箱。 查看更多有关为邮件[设置 from 和 sender 属性](/graph/outlook-create-send-messages#setting-the-from-and-sender-properties)的信息。|
|hasAttachments|Boolean|指示邮件是否包含附件。|
|id|String|只读。|
|importance|String| 邮件的重要性：`Low`、`Normal`、`High`。|
|inferenceClassification|String| 可取值为：`Focused`、`Other`。|
|isDelegated|Boolean|如果代理可访问此会议请求响应，则为 True，否则为 false。 默认为 false。|
|isDeliveryReceiptRequested|Boolean|指示是否需要发送邮件已读回执。|
|isDraft|Boolean|指示邮件是否为草稿。如果尚未发送，则此邮件是一封草稿。|
|isOutOfDate|Boolean|指示此会议请求是否已由较新的请求发出。|
|isRead|Boolean|指示是否已阅读该邮件。|
|isReadReceiptRequested|Boolean|指示是否需要发送邮件已读回执。|
|lastModifiedDateTime|DateTimeOffset|上次更改邮件的日期和时间。|
|位置|[位置](location.md)|请求的会议的位置。|
|meetingMessageType|String| 事件消息的类型：`none`、`meetingRequest`、`meetingCancelled`、`meetingAccepted`、`meetingTentativelyAccepted`、`meetingDeclined`。|
|mentionsPreview|[mentionsPreview](mentionspreview.md)|邮件中的提及的相关信息。处理 `GET` /messages 请求时，服务器会设置此属性并默认将其包含在响应中。若邮件中无提及，则服务器返回 NULL。可选。 |
|parentFolderId|String|邮件的父 MailFolder 的唯一标识符。|
|previousEndDateTime|[DateTimeTimeZone](datetimetimezone.md)| 如果会议更新更改了会议结束时间，则此属性指定上一个会议结束时间。|
|previousLocation|[位置](location.md)| 如果会议更新更改了会议位置，则此属性指定上一个会议位置。|
|previousStartDateTime|[DateTimeTimeZone](datetimetimezone.md)| 如果会议更新更改了会议开始时间，则此属性指定上一个会议的开始时间。|
|receivedDateTime|DateTimeOffset|收到邮件的日期和时间。|
|recurrence|[PatternedRecurrence](patternedrecurrence.md)|请求的会议的定期模式。|
|replyTo|[recipient](recipient.md) collection|在答复时使用的电子邮件地址。|
|responseRequested|Boolean|如果发件人希望被邀请者将响应发送给请求的会议，则设置为 true。|
|sender|[recipient](recipient.md)|实际用于生成邮件的帐户。 大多数情况下，此值与“**from**”属性相同。 从[共享邮箱](/exchange/collaboration/shared-mailboxes/shared-mailboxes)发送邮件时，可以将此属性设置为其他值，[对于共享日历，或设置为代理人](/graph/outlook-share-delegate-calendar.md)。 在任何情况下，此值必须对应于使用的实际邮箱。 查看更多有关为邮件[设置 from 和 sender 属性](/graph/outlook-create-send-messages#setting-the-from-and-sender-properties)的信息。|
|sentDateTime|DateTimeOffset|发送邮件的日期和时间。|
|startDateTime|[DateTimeTimeZone](datetimetimezone.md)|请求的会议的开始时间。|
|subject|String|邮件的主题。|
|toRecipients|[recipient](recipient.md) collection|邮件的收件人。|
|type|String|所需会议的类型： `singleInstance` 、 `occurence` 、 `exception` 、 `seriesMaster` 。|
|uniqueBody|[itemBody](itembody.md)|当前邮件专用的邮件正文部分。|
|webLink|String|用于打开 web 上的 Outlook 中的邮件的 URL。<br><br>可以将 ispopout 参数附加到此 URL 的末尾以更改邮件的显示方式。 如果 ispopout 不存在或设置为 1，则邮件显示在弹出窗口中。 如果将 ispopout 设置为0，则浏览器将在 web 审阅窗格中的 Outlook 中显示该邮件。<br><br>如果您通过 web 上的 Outlook 登录到您的邮箱，则邮件将在浏览器中打开。 如果尚未使用浏览器登录，系统将提示你登录。<br><br>无法从 iFrame 中访问此 URL。|

## <a name="relationships"></a>关系
| 关系 | 类型   |说明|
|:---------------|:--------|:----------|
|attachments|[附件](attachment.md) 集合|邮件的 [fileAttachment](fileattachment.md)、 [itemAttachment](itemattachment.md)和 [referenceAttachment](referenceattachment.md) 附件的集合。 只读。 可为 Null。|
|event|[event](event.md)| 与事件消息相关联的事件。对于与会者或会议室资源，假定已将日历助理设为在会议请求事件消息到达时自动更新包含事件的日历。导航属性。只读。|
|extensions|[扩展](extension.md)集合| 为 eventMessage 定义的开放扩展集合。只读。可为 NULL。|
|提及|[mention](mention.md) 集合 | 邮件中的提及集合，按 **createdDateTime** 由最新到最旧排序。默认情况下，`GET` /messages 不会返回此属性，在该属性上应用 `$expand` 时除外。|
|multiValueExtendedProperties|[multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md) 集合| 为 eventMessage 定义的多值扩展属性的集合。只读。可为 Null。|
|singleValueExtendedProperties|[singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md) collection| 为 eventMessage 定义的单值扩展属性的集合。只读。可为 Null。|


## <a name="methods"></a>方法

| 方法           | 返回类型    |说明|
|:---------------|:--------|:----------|
|[获取 eventMessage](../api/eventmessage-get.md) | [eventMessage](eventmessage.md) |读取 eventmessage 对象的属性和关系。|
|[更新](../api/eventmessage-update.md) | [eventMessage](eventmessage.md)  |更新 eventMessage 对象。|
|[删除](../api/eventmessage-delete.md) | 无 |更新 eventMessage 对象。|
|[copy](../api/message-copy.md)|[message](message.md)|将邮件复制到文件夹。|
|[createForward](../api/message-createforward.md)|[message](message.md)|创建转发邮件的草稿。然后，你可以 [更新](../api/message-update.md) 或 [发送](../api/message-send.md) 草稿。|
|[createReply](../api/message-createreply.md)|[message](message.md)|创建回复邮件的草稿。然后，你可以 [更新](../api/message-update.md) 或 [发送](../api/message-send.md) 草稿。|
|[createReplyAll](../api/message-createreplyall.md)|[message](message.md)|创建全部答复邮件的草稿。然后，可以[更新](../api/message-update.md)或[发送](../api/message-send.md)草稿。|
|[转发](../api/message-forward.md)|无|转发邮件。然后邮件保存在已发送邮件文件夹中。|
|[移动](../api/message-move.md)|[message](message.md)|将邮件移到文件夹。此操作会在目标文件夹中新建邮件副本。|
|[回复](../api/message-reply.md)|无|答复邮件发件人然后邮件保存在已发送邮件文件夹中。|
|[replyAll](../api/message-replyall.md)|无|答复邮件的所有收件人。然后邮件保存在已发送邮件文件夹中。|
|[发送](../api/message-send.md)|无|发送以前创建的邮件草稿。然后邮件保存在已发送邮件文件夹中。|
|[取消订阅](../api/message-unsubscribe.md)|无|使用 List-Unsubscribe 标头中的第一个 mailto 命令中指定的数据和地址发送邮件。|
|**附件**| | |
|[列出附件](../api/eventmessage-list-attachments.md) |[attachment](attachment.md) 集合| 获取 eventMessage 的所有附件。|
|[Add attachment](../api/eventmessage-post-attachments.md) |[附件](attachment.md)| 通过发布到附件集合，向 eventMessage 添加新附件。|
|**开放扩展**| | |
|[创建开放扩展](../api/opentypeextension-post-opentypeextension.md) |[openTypeExtension](opentypeextension.md)| 创建开放扩展，并在新建或现有的资源实例中添加自定义属性。|
|[获取开放扩展](../api/opentypeextension-get.md) |[openTypeExtension](opentypeextension.md) 集合| 获取按名称标识的开放扩展。|
|**扩展属性**| | |
|[创建单值扩展属性](../api/singlevaluelegacyextendedproperty-post-singlevalueextendedproperties.md) |[eventMessage](eventmessage.md)  |在新建或现有 eventMessage 中创建一个或多个单值扩展属性。   |
|[获取具有单值扩展属性的 eventMessage](../api/singlevaluelegacyextendedproperty-get.md)  | [eventMessage](eventmessage.md) | 通过使用 `$expand` 或 `$filter` 获取包含单值扩展属性的 eventMessage。 |
|[创建多值扩展属性](../api/multivaluelegacyextendedproperty-post-multivalueextendedproperties.md) | [eventMessage](eventmessage.md) | 在新建或现有的 eventMessage 中创建一个或多个多值扩展属性。  |
|[获取具有多值扩展属性的 eventMessage](../api/multivaluelegacyextendedproperty-get.md)  | [eventMessage](eventmessage.md) | 使用 `$expand` 获取包含一个多值扩展属性的 eventMessage。 |


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "eventMessageRequest resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


