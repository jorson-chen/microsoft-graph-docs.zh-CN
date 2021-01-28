---
title: workbookTableColumn 资源类型
description: 代表表格中的一列。
author: lumine2008
localization_priority: Normal
ms.prod: excel
doc_type: resourcePageType
ms.openlocfilehash: 27a44c0b75cfe62d27b1187616f9626772575cf4
ms.sourcegitcommit: 9a03b719d1316729dd022bf4d268894e91515475
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2021
ms.locfileid: "50034014"
---
# <a name="workbooktablecolumn-resource-type"></a>workbookTableColumn 资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

代表表格中的一列。


## <a name="methods"></a>方法

| 方法           | 返回类型    |说明|
|:---------------|:--------|:----------|
|[获取 TableColumn](../api/tablecolumn-get.md) | [workbookTableColumn](workbooktablecolumn.md) |读取 tablecolumn 对象的属性和关系。|
|[更新](../api/tablecolumn-update.md) | [workbookTableColumn](workbooktablecolumn.md) |更新 TableColumn 对象 |
|[Databodyrange](../api/tablecolumn-databodyrange.md)|[workbookRange](workbookrange.md)|获取与列的数据体相关的 range 对象。|
|[Headerrowrange](../api/tablecolumn-headerrowrange.md)|[workbookRange](workbookrange.md)|获取与列的标头行相关的 range 对象。|
|[Range](../api/tablecolumn-range.md)|[workbookRange](workbookrange.md)|获取与整个列相关的 range 对象。|
|[Totalrowrange](../api/tablecolumn-totalrowrange.md)|[workbookRange](workbookrange.md)|获取与列的总计行相关的 range 对象。|
|[删除](../api/tablecolumn-delete.md)|无|从表中删除列。|
|[列出](../api/tablecolumn-list.md) | [workbookTableColumn](workbooktablecolumn.md) 集合 |获取 tableColumn 对象的集合。 |
|[Itemat](../api/tablecolumncollection-itemat.md)|[workbookTableColumn](workbooktablecolumn.md)|根据其在集合中的位置获取列。|
|[添加](../api/tablecolumncollection-add.md)|[workbookTableColumn](workbooktablecolumn.md)|向表中添加新列。|

## <a name="properties"></a>属性
| 属性     | 类型   |说明|
|:---------------|:--------|:----------|
|id|string|返回标识表内的列的唯一键。只读。|
|Index|int|返回表的列集合内列的索引编号。从零开始编制索引。只读。|
|name|string|返回表格列的名称。|
|values|Json|表示指定区域的原始值。返回的数据类型可能是字符串、数字或布尔值。包含一个将返回错误字符串的错误的单元格。|

## <a name="relationships"></a>关系
| 关系 | 类型   |说明|
|:---------------|:--------|:----------|
|筛选器|[workbookFilter](workbookfilter.md)|检索应用于列的筛选器。只读。|

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "keyProperty": "id",
  "baseType":"microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookTableColumn"
}-->

```json
{
  "id": "1024",
  "index": 1024,
  "name": "string",
  "values": "json"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "TableColumn resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


