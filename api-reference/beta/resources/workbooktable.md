---
title: workbookTable 资源类型
description: 表示 Excel 表格。
author: lumine2008
localization_priority: Normal
ms.prod: excel
doc_type: resourcePageType
ms.openlocfilehash: 7110993ad38dd9673d36c2d6d1fb2eabc3872da2
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48023768"
---
# <a name="workbooktable-resource-type"></a>workbookTable 资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

表示 Excel 表格。

## <a name="methods"></a>方法

| 方法           | 返回类型    |说明|
|:---------------|:--------|:----------|
|[获取 workbookTable](../api/table-get.md) | [workbookTable](workbooktable.md) |读取 table 对象的属性和关系。|
|[创建 workbookTableColumn](../api/table-post-columns.md) |[workbookTableColumn](workbooktablecolumn.md)| 通过发布到列集合创建新的 TableColumn。|
|[List columns](../api/table-list-columns.md) |[workbookTableColumn](workbooktablecolumn.md) 集合| 获取 TableColumn 对象的集合。|
|[创建 workbookTableRow](../api/table-post-rows.md) |[workbookTableRow](workbooktablerow.md)| 通过发布到行集合创建新的 TableRow。|
|[List rows](../api/table-list-rows.md) |[workbookTableRow](workbooktablerow.md) 集合| 获取 TableRow 对象的集合。|
|[Update](../api/table-update.md) | [workbookTable](workbooktable.md)   |更新 Table 对象。 |
|[Databodyrange](../api/table-databodyrange.md)|[workbookRange](workbookrange.md)|获取与表的数据体相关的 range 对象。|
|[Headerrowrange](../api/table-headerrowrange.md)|[workbookRange](workbookrange.md)|获取与表的标头行相关的 range 对象。|
|[区域](../api/table-range.md)|[workbookRange](workbookrange.md)|获取与整个表相关的 range 对象。|
|[Totalrowrange](../api/table-totalrowrange.md)|[workbookRange](workbookrange.md)|获取与表的总计行相关的 range 对象。|
|[Clearfilters](../api/table-clearfilters.md)|无|清除当前表上应用的所有筛选器。|
|[Converttorange](../api/table-converttorange.md)|[workbookRange](workbookrange.md)|将表转换为普通单元格区域。保留所有数据。|
|[删除](../api/table-delete.md)|无|删除表。|
|[Reapplyfilters](../api/table-reapplyfilters.md)|无|重新应用当前表上的所有筛选器。|
|[List](../api/table-list.md) | [workbookTable](workbooktable.md) 集合 |获取 table 对象的集合。 |
|[Add](../api/tablecollection-add.md)|[workbookTable](workbooktable.md)|创建一个新表。区域源地址确定将在其下添加表的工作表。如果无法添加表（例如，由于地址无效，或者表与另一个表重叠），将抛出错误。|

## <a name="properties"></a>属性
| 属性     | 类型   |说明|
|:---------------|:--------|:----------|
|id|string|返回用于唯一标识指定工作簿中表的值。 即使表被重命名，标识符的值仍保持不变。 应将此属性解析为不透明的字符串值，不得将它解析为其他任何类型。 只读。|
|name|string|表的名称。|
|showHeaders|boolean|指示标头行是否可见。该值可以设置为显示或删除标头行。|
|showTotals|boolean|指示总计行是否可见。该值可以设置为显示或删除总计行。|
|style|string|表示表格样式的常量值。可能的值是：TableStyleLight1 thru TableStyleLight21、TableStyleMedium1 thru TableStyleMedium28、TableStyleStyleDark1 thru TableStyleStyleDark11。还可以指定工作簿中显示的用户定义的自定义样式。|
|highlightFirstColumn|Boolean|指明第一列是否包含特殊格式。   |
|highlightLastColumn|Boolean|指明最后一列是否包含特殊格式。 |
|showBandedColumns|Boolean|指明列是否采用镶边格式来以不同的方式突出显示奇数列与偶数列，让表更易于阅读。   |
|showBandedRows|Boolean|指明行是否采用镶边格式来以不同的方式突出显示奇数行与偶数行，让表更易于阅读。    |
|showFilterButton|Boolean|指明是否在每个列标题的顶部显示筛选器按钮。仅当 table 中包含标题行时，才允许设定此设置。   |
|legacyId|String|旧版 Excel 客户端中使用的旧 ID。 即使表格已重命名，标识符值也仍保持不变。 应将此属性解析为不透明的字符串值，不得将它解析为其他任何类型。 只读。   |

## <a name="relationships"></a>关系
| 关系 | 类型   |说明|
|:---------------|:--------|:----------|
|columns|[workbookTableColumn](workbooktablecolumn.md) 集合|表示表中所有列的集合。只读。|
|rows|[workbookTableRow](workbooktablerow.md) 集合|表示表中所有行的集合。只读。|
|sort|[workbookTableSort](workbooktablesort.md)|表示表的排序。只读。|
|worksheet|[workbookWorksheet](workbookworksheet.md)|包含当前表的工作表。只读。|

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [
     "legacyId"
  ],
  "keyProperty": "id",
  "baseType":"microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookTable"
}-->

```json
{
  "highlightFirstColumn": true,
  "highlightLastColumn": true,
  "id": "String (identifier)",
  "name": "String",
  "showBandedColumns": true,
  "showBandedRows": true,
  "showFilterButton": true,
  "showHeaders": true,
  "showTotals": true,
  "style": "String",
  "legacyId": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Table resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


