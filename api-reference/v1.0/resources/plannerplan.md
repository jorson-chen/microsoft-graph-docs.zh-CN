---
title: plannerPlan 资源类型
description: '**plannerPlan** 资源表示 Microsoft 365 中的计划。 计划可以由组所有，并包含 plannerTasks 集合。 其也可以有 plannerBuckets 集合。 每个计划对象具有可以包含此计划的更多信息的详细信息对象。 有关组、计划和任务之间的关系的详细信息，请参阅“Planner”。'
localization_priority: Priority
author: TarkanSevilmis
ms.prod: planner
doc_type: resourcePageType
ms.openlocfilehash: dc369ce0f97659c907fcb9bf94ae3f43c978f41a
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48037393"
---
# <a name="plannerplan-resource-type"></a>plannerPlan 资源类型

命名空间：microsoft.graph

**plannerPlan** 资源表示 Microsoft 365 中的计划。 计划可以由[组](group.md)所有，并包含 [plannerTasks](plannertask.md) 集合。 其也可以有 [plannerBuckets](plannerbucket.md) 集合。 每个计划对象具有可以包含此计划的更多信息的[详细信息](plannerplandetails.md)对象。 有关组、计划和任务之间的关系的详细信息，请参阅 [Planner](planner-overview.md)。

## <a name="methods"></a>方法

| 方法           | 返回类型    |说明|
|:---------------|:--------|:----------|
|[Get plannerPlan](../api/plannerplan-get.md) | [plannerPlan](plannerplan.md) |读取 **plannerPlan** 对象的属性和关系。|
|[List buckets](../api/plannerplan-list-buckets.md) |[plannerBucket](plannerbucket.md) collection| 获取 **plannerBucket** 对象集合。|
|[List tasks](../api/plannerplan-list-tasks.md) |[plannerTask](plannertask.md) collection| 获取 **plannerTask** 对象集合。|
|[Update](../api/plannerplan-update.md) | [plannerPlan](plannerplan.md) |更新 **plannerPlan** 对象。 |

## <a name="properties"></a>属性
| 属性     | 类型   |说明|
|:---------------|:--------|:----------|
|createdDateTime|DateTimeOffset|只读。创建计划的日期和时间时间戳类型表示使用 ISO 8601 格式的日期和时间信息，并且始终处于 UTC 时间。例如，2014 年 1 月 1 日午夜 UTC 如下所示：`'2014-01-01T00:00:00Z'`|
|id|String| 只读。 计划的 ID。 长度为 28 个字符，区分大小写。 [格式验证](planner-identifiers-disclaimer.md)在服务上完成。|
|Owner|String|拥有计划的[组](group.md)的 ID。 必须存在有效的组才能设置此字段。 设置后，此属性无法更新。|
|title|String|必填。 计划的标题|
|createdBy|[identitySet](identityset.md)|只读。 创建计划的用户。|

## <a name="relationships"></a>关系
| 关系 | 类型   |说明|
|:---------------|:--------|:----------|
|buckets|[plannerBucket](plannerbucket.md) collection| 只读。可为 Null。计划中的存储桶集合。|
|详细信息|[plannerPlanDetails](plannerplandetails.md)| 只读。 可为 NULL。 关于计划的其他详细信息。|
|tasks|[plannerTask](plannertask.md) collection| 只读。 可为 Null。 计划中的任务集合。|

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerPlan"
}-->

```json
{
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "owner": "String",
  "title": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerPlan resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

