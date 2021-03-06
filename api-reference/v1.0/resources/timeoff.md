---
title: timeOff 资源类型
description: 计划中的非工作单位。
author: akumar39
localization_priority: Normal
ms.prod: microsoft-teams
doc_type: resourcePageType_
ms.openlocfilehash: 1c33ed74b52983b9adc3ce0d1c729caaa35dce09
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48090828"
---
# <a name="timeoff-resource-type"></a>timeOff 资源类型

命名空间：microsoft.graph

计划中非工作的单位。

## <a name="methods"></a>方法

| 方法       | 返回类型  |Description|
|:---------------|:--------|:----------|
|[List](../api/schedule-list-timesoff.md) | [timeOff](timeoff.md) 集合 | 获取此计划中的 **timeOff** 对象的列表。|
|[Create](../api/schedule-post-timesoff.md) | [timeOff](timeoff.md) | 创建新的 **timeOff** 对象。|
|[Get](../api/timeoff-get.md) | [timeOff](timeoff.md) | 按 ID 获取 **timeOff** 对象。|
|[Replace](../api/timeoff-put.md) | [timeOff](timeoff.md) | 替换 **timeOff** 对象。|
|[删除](../api/timeoff-delete.md) | 无 | 从计划中删除 **timeOff** 对象。|

## <a name="properties"></a>属性
|名称          |类型           |说明                                                                                                                                      |
|--------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| id            |`string`      |**TimeOff**的 ID。|
| userId            |`string`      |分配给 **timeOff**的用户的 ID。 必需。|
| sharedTimeOff     | [timeOffItem](timeoffitem.md)  |由员工和经理查看的此 **timeOff** 的共享版本。 必需。|
| draftTimeOff      | [timeOffItem](timeoffitem.md)        |由经理查看的此 **timeOff** 的草稿版本。 必需。|
| createdDateTime       |`DateTimeOffset`        |首次创建此 **timeOff** 时所处的时间戳。 时间戳类型表示采用 ISO 8601 格式的日期和时间信息，始终采用 UTC 时间。 例如，2014 年 1 月 1 日午夜 (UTC) 如下所示：“2014-01-01T00:00:00Z”。 |
| lastModifiedDateTime      |`DateTimeOffset`        |上次更新此 **timeOff** 的时间戳。 时间戳类型表示采用 ISO 8601 格式的日期和时间信息，始终采用 UTC 时间。 例如，2014 年 1 月 1 日午夜 (UTC) 如下所示：“2014-01-01T00:00:00Z”。 |
| lastModifiedBy        | [identitySet](identityset.md)        |上次更新此 **timeOff**的标识。 |

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.timeOff",
   "baseType":"microsoft.graph.changeTrackedEntity"
}-->

```json
{
  "userId": "string (identifier)",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "lastModifiedBy": {"@odata.type":"microsoft.graph.identitySet"},
  "sharedTimeOff": {"@odata.type":"microsoft.graph.timeOffItem"},
  "draftTimeOff": {"@odata.type":"microsoft.graph.timeOffItem"}
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "timeOff resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->

