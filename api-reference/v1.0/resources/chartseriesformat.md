---
title: ChartSeriesFormat 资源类型
description: 封装图表系列的格式属性
author: lumine2008
localization_priority: Normal
ms.prod: excel
doc_type: resourcePageType
ms.openlocfilehash: 3b6003df060fbb657dc3c67375f2c942ad8cff57
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48059227"
---
# <a name="chartseriesformat-resource-type"></a>ChartSeriesFormat 资源类型

命名空间：microsoft.graph

封装图表系列的格式属性


## <a name="methods"></a>方法
无

## <a name="properties"></a>属性
无

## <a name="relationships"></a>关系
| 关系 | 类型   |说明|
|:---------------|:--------|:----------|
|fill|[WorkbookChartFill](chartfill.md)|表示图表系列的填充格式，包括背景格式信息。只读。|
|line|[WorkbookChartLineFormat](chartlineformat.md)|表示线条格式。 只读。|


## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartSeriesFormat"
}-->

```json
{
  "fill": {"@odata.type": "microsoft.graph.workbookChartFill"},
  "line": {"@odata.type": "microsoft.graph.workbookChartLineFormat"}
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartSeriesFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

