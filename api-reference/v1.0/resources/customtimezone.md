---
title: customTimeZone 资源类型
description: 表示从标准时间到夏令时的切换不标准（反之亦然）的时区。
localization_priority: Normal
author: svpsiva
ms.prod: ''
doc_type: resourcePageType
ms.openlocfilehash: 0686f23738c65129008681126b8e75d41a81325d
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48091829"
---
# <a name="customtimezone-resource-type"></a>customTimeZone 资源类型

命名空间：microsoft.graph

表示从标准时间到夏令时的切换不标准（反之亦然）的时区。


## <a name="properties"></a>属性
| 属性     | 类型   |说明|
|:---------------|:--------|:----------|
| bias | Edm.Int32 | 时区与协调世界时 (UTC) 的时间偏移量。 此值以分钟为单位。早于 UTC 的时区为正偏移；晚于 UTC 的时区为负偏移。|
| daylightOffset | [daylightTimeZoneOffset](daylighttimezoneoffset.md) | 指定时区何时从标准时间切换到夏令时。 |
| name | string | 自定义时区的名称。 |
| standardOffset | [standardTimeZoneOffset](standardtimezoneoffset.md) | 指定时区何时从夏令时切换到标准时间。 |


## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "baseType": "microsoft.graph.timeZoneBase",
  "@odata.type": "microsoft.graph.customTimeZone"
}-->

```json
{
  "bias": "Int32",
  "daylightOffset": {"@odata.type": "microsoft.graph.daylightTimeZoneOffset"},
  "name": "string",
  "standardOffset": {"@odata.type": "microsoft.graph.standardTimeZoneOffset"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "customTimeZone resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

