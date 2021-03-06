---
title: plannerRecentPlanReference 资源类型
description: '**PlannerRecentPlanReference**资源类型代表一个对用户最近查看过的 plannerPlan 的引用。 '
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
doc_type: resourcePageType
ms.openlocfilehash: eefbcf79da1ae2ef76010eace5248708b6c61010
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48063998"
---
# <a name="plannerrecentplanreference-resource-type"></a>plannerRecentPlanReference 资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

**PlannerRecentPlanReference**资源类型代表一个对用户最近查看过的[plannerPlan](plannerplan.md)的引用。 用户的 **plannerRecentPlanReferences** 由应用程序显式维护。 任何实现最近计划功能的应用程序都应记录用户上次查看计划的时间，并相应地更新 **plannerRecentPlanReference** 项。
应用应注意， **plannerRecentPlanReference** 条目可以引用已删除的 **plannerPlans** 、用户无法再访问或已使用其他标题进行更新。
我们建议应用在存在差异时通知用户，并将这些条目保持为最新。

## <a name="properties"></a>属性
| 属性     | 类型   |说明|
|:---------------|:--------|:----------|
|lastAccessedDateTime|DateTimeOffset|用户上次查看计划的日期和时间。 时间戳类型表示采用 ISO 8601 格式的日期和时间信息，始终采用 UTC 时区。 例如，2014 年 1 月 1 日午夜 UTC 如下所示：`'2014-01-01T00:00:00Z'`。|
|planTitle|String|用户查看计划时的标题。|

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerRecentPlanReference"
}-->

```json
{
  "lastAccessedDateTime": "String (timestamp)",
  "planTitle": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "plannerRecentPlanReference resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


