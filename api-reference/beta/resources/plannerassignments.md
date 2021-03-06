---
title: plannerAssignments 资源类型
description: '**PlannerAssignments**资源表示 plannerTask 资源的工作分配。 此类型是开放类型。 此类型中的每个属性名称 '
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
doc_type: resourcePageType
ms.openlocfilehash: 8150e859ccee08a8272bc9a140e50ef7ae3bed68
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48026542"
---
# <a name="plannerassignments-resource-type"></a>plannerAssignments 资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

**PlannerAssignments**资源表示[plannerTask](plannertask.md)资源的工作分配。 此类型是开放类型。 此类型中的每个属性名称都是分配给任务的用户对象的 ID。 可以将用户分配给使用其 ID 命名的新属性的任务，并将 [plannerassignment](plannerassignment.md) 对象的 orderHint 属性填充为值。 通过将以其 ID 命名的 bookmark 设置为 null，可以从任务中取消分配工作负责人。


## <a name="properties"></a>属性
可由客户端定义打开类型的属性。 但在这种情况下，客户端必须提供指定用户的 Id 作为属性名称。 必须将属性设置为 **plannerAssignment** 对象，才能创建或修改工作负责人，并为 null 以删除它们。

示例：

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerAssignments"
}-->

```json
{
  "ca2a1df2-e36b-4987-9f6b-0ea462f4eb47": null,
  "4e98f8f1-bb03-4015-b8e0-19bb370949d8": { 
      "@odata.type": "microsoft.graph.plannerAssignment",
      "orderHint": "String"
    }
}
```
此示例从任务的代理人列表中删除 ID 为 ca2a1df2-e36b-4987-9f6b-0ea462f4eb47 的用户，同时更改具有用户 ID 4e98f8f1-bb03-4015-b8e0-19bb370949d8 的受理人的订单。 如果尚未为 ID 为4e98f8f1-bb03-4015-b8e0-19bb370949d8 的用户分配该任务，则使用此值更新工作分配时，会将该任务分配给此用户。

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "plannerAssignments resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


