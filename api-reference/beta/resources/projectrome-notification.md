---
title: 通知资源类型
description: '表示由面向指定用户的应用程序服务器发布的通知。 通知存储在 Microsoft Graph 中，并分发给用户拥有的不同设备终结点。 '
localization_priority: Normal
ms.prod: notifications
doc_type: resourcePageType
author: merzink
ms.openlocfilehash: 97b3d5be5039baff9f73019dbdc54947614d3c1b
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48078221"
---
# <a name="notification-resource-type"></a>通知资源类型

命名空间： microsoft. graph [!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

表示由面向指定用户的应用程序服务器发布的通知。 通知存储在 Microsoft Graph 中，并分发给用户拥有的不同设备终结点。 

通知可以是可由操作系统 (Windows、Android 和 iOS 平台) 解释的视觉通知负载。 它还可以是 (rawContent) 的数据有效负载，这些应用程序提供和处理 (包括 web) 的应用程序客户端，然后在每个设备上确定相应的用户体验。  这通常是本地生成的 visual 通知 UI，与原始数据有效负载中的内容相对应。 

当用户在视觉通知中进行操作时，应用程序客户端可以使用客户端通知 SDK 更新 Microsoft Graph 中相应通知源的状态（例如，通过将通知标记为已关闭）。 然后，该更新将分发到所有其他应用程序客户端终结点，客户端将相应地处理更改，例如，通过关闭通知阻止用户查看冗余信息。 应用程序客户端可以在过期之前在过期之前访问相同的通知资源 (即使是通过 [通知 SDK](https://aka.ms/GNSDK)将其标记为 "已消除") （如通知历史记录）也是如此。 

> [!NOTE]
> 通知状态更新（如 "已读" 或 "已消除"）将不会扇到 web 终结点。 这是因为跨不同浏览器的 web 推送需要向用户显示可视 toast 通知。 由于状态更改没有对应的可视化内容，因此将仅扇针对 Windows、iOS 或 Android 平台的通知。

## <a name="methods"></a>方法
|方法 | 返回类型 | 说明|
|:------|:------------|:-----------|
|[创建通知](../api/user-post-notifications.md) | [通告](projectrome-notification.md) |创建并发送通知。 |

## <a name="properties"></a>属性
|名称 | 类型 | 说明|
|:----|:-----|:-----------|
| targetHostName | String | 表示呼叫服务要为其发布通知的应用程序的主机名（针对给定用户）。 如果目标 web 终结点 (请参阅 **targetPolicy**) ，确保 **targetHostName** 与在应用程序 JSON 属性中的客户端创建订阅时使用的名称相同。 |
| appNotificationId | String | 通知的应用程序服务器设置的唯一 ID，用于标识和定位单个通知。 |
| 名 | String | 此通知所属的组的名称。 它由开发人员设置，用于将通知分组在一起。 |
| targetPolicy | [targetPolicyEndpoints](targetpolicyendpoints.md) | 目标策略对象处理应针对给定用户 (Windows、iOS、Android 和 WebPush) 目标的终结点类型的通知传递策略。 |
| payload | [payloadTypes](payloadtypes.md)| 这是原始或直观的用户通知的数据内容，这些通知将传递给应用客户端接收此通知并由其使用。 |
| displayTimeToLive | Int32 | 设置) 此通知内容将在每个平台的通知查看器中保留的时间（以秒为单位） (。 例如，将通知传递给 Windows 设备时，此属性的值将传递给 ToastNotification，以确定 toast 通知将在用户的 Windows 操作中心保留多长时间。 |
| expirationDateTime | DateTimeOffset | 使用 ISO 8601 格式设置 UTC 过期日期和用户通知的时间 (例如，1月1日午夜 UTC，2019将如下所示： `'2019-01-01T00:00:00Z'`) 。 当时间启动时，通知将从 Microsoft Graph 通知源存储中完全删除，并且不再是通知历史记录的一部分。 最大值为30天。 |
| priority | string | 指示原始用户通知的优先级。 默认情况下，视觉通知以高优先级发送。 有效值为 `None`、`High` 和 `Low`。 |
| fallbackPolicy | [fallbackpolicy](fallbackpolicy.md) | 可选回退策略对象仅处理 iOS 终结点的通知回退策略，旨在用于由于特定于平台的限制而无法发送到设备的高优先级原始通知 (例如，节电模式) 。 |


## <a name="relationships"></a>关系
无。


## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.notification",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "targetHostName": "String",
  "appNotificationid": "String (identifier)",
  "groupName": "String", 
  "targetPolicy": {"@odata.type": "microsoft.graph.targetPolicyEndpoints"},
  "payload": {"@odata.type": "microsoft.graph.payloadTypes"},
  "displayTimeToLive": 1024,
  "expirationDateTime": "String (timestamp)",
  "priority": "string",
  "fallbackPolicy": {"@odata.type": "microsoft.graph.fallbackpolicy"},  
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "notification resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


