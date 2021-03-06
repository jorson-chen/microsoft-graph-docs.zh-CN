---
title: WorksheetProtectionOptions 资源类型
description: 代表工作表保护中的选项。
author: lumine2008
localization_priority: Normal
ms.prod: excel
doc_type: resourcePageType
ms.openlocfilehash: 8bc4745f31d5b2a6cffe89a4fb912739212a6c3e
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48015006"
---
# <a name="worksheetprotectionoptions-resource-type"></a>WorksheetProtectionOptions 资源类型

命名空间：microsoft.graph

代表工作表保护中的选项。

## <a name="properties"></a>属性
| 属性     | 类型   |说明|
|:---------------|:--------|:----------|
|allowAutoFilter|布尔|表示允许使用自动筛选功能的工作表保护选项。|
|allowDeleteColumns|布尔|表示允许删除列的工作表保护选项。|
|allowDeleteRows|布尔|表示允许删除行的工作表保护选项。|
|allowFormatCells|布尔|表示允许格式化单元格的工作表保护选项。|
|allowFormatColumns|布尔|表示允许格式化列的工作表保护选项。|
|allowFormatRows|布尔|表示允许格式化行的工作表保护选项。|
|allowInsertColumns|布尔|表示允许插入列的工作表保护选项。|
|allowInsertHyperlinks|布尔|表示允许插入超链接的工作表保护选项。|
|allowInsertRows|布尔|表示允许插入行的工作表保护选项。|
|allowPivotTables|布尔|表示允许使用数据透视表功能的工作表保护选项。|
|allowSort|布尔|表示允许使用排序功能的工作表保护选项。|

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookWorksheetProtectionOptions"
}-->

```json
{
  "allowAutoFilter": true,
  "allowDeleteColumns": true,
  "allowDeleteRows": true,
  "allowFormatCells": true,
  "allowFormatColumns": true,
  "allowFormatRows": true,
  "allowInsertColumns": true,
  "allowInsertHyperlinks": true,
  "allowInsertRows": true,
  "allowPivotTables": true,
  "allowSort": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "WorksheetProtectionOptions resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

