---
title: workbookTableSort 资源类型
description: 管理对 Table 对象的排序操作。
author: lumine2008
localization_priority: Normal
ms.prod: excel
doc_type: resourcePageType
ms.openlocfilehash: 77f4fb1dcaed54c2b4cd992b7d6105e194812149
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48023742"
---
# <a name="workbooktablesort-resource-type"></a>workbookTableSort 资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

管理对 Table 对象的排序操作。


## <a name="methods"></a>方法

| 方法           | 返回类型    |说明|
|:---------------|:--------|:----------|
|[获取 TableSort](../api/tablesort-get.md) | [workbookTableSort](workbooktablesort.md) |读取 tableSort 对象的属性和关系。|
|[应用](../api/tablesort-apply.md)|无|执行排序操作。|
|[清除](../api/tablesort-clear.md)|None|清除表上的当前排序。尽管这不能修改表的排序，但它会清除标题按钮的状态。|
|[重新应用](../api/tablesort-reapply.md)|无|对表重新应用当前的排序参数。|

## <a name="properties"></a>属性
| 属性     | 类型   |说明|
|:---------------|:--------|:----------|
|matchCase|boolean|表示最后一次对表进行排序时大小写是否有影响。只读。|
|方法|string|表示最后一次对表排序所使用的中文字符排序方法。可能的值是：`PinYin`、`StrokeCount`。只读。|

## <a name="relationships"></a>关系
| 关系 | 类型   |说明|
|:---------------|:--------|:----------|
|域|[workbookSortField](workbooksortfield.md)|表示最后一次对表排序所使用的当前条件。 只读。|

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
 
  "optionalProperties": [

  ],
  "keyProperty": "id",
  "baseType":"microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookTableSort"
}-->

```json
{
  "id": "string",
  "matchCase": true,
  "method": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "TableSort resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


