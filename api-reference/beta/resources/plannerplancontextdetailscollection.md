---
title: plannerPlanContextDetailsCollection 资源类型
description: " 值是 plannerPlanContextDetails 对象。"
author: TarkanSevilmis
localization_priority: Normal
ms.prod: planner
doc_type: resourcePageType
ms.openlocfilehash: 622e30fa01776f945d4b3946f8bb0068ebc3f64e
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48064080"
---
# <a name="plannerplancontextdetailscollection-resource-type"></a>plannerPlanContextDetailsCollection 资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]


**PlannerPlanContextDetailsCollection**资源表示规划所链接到的外部上下文的集合。 此资源是打开的类型，并且是 [plannerPlanDetails](plannerplandetails.md) 对象的一部分。 属性值对中的属性名称是上下文特定于应用程序的标识符;值是 [plannerPlanContextDetails](plannerplancontextdetails.md) 对象。


## <a name="properties"></a>属性
可由客户端定义打开类型的属性。 在这种情况下，客户端应使用表示外部上下文的独特标识符作为属性名称。 属性值必须是 [plannerPlanContextDetails](plannerplancontextdetails.md) 对象。 根据 OData，开放式类型中的属性名称不能包含以下字符： `.` 、 `:` 、 `@` 、 `%` 。 需要使用 URL 编码格式对这些字符进行编码。 若要删除收藏夹列表中的项，需要从 [plannerPlanContextCollection](plannerplancontextcollection.md) 集合中删除此值，这将自动删除此对象中的条目。

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerPlanContextDetailsCollection"
}-->

```json
{
}

```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "plannerPlanContextDetailsCollection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


