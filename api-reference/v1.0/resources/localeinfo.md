---
title: localeInfo 资源类型
description: 有关已登录用户的区域设置信息，包括首选语言和国家/地区。
localization_priority: Normal
author: svpsiva
ms.prod: outlook
doc_type: resourcePageType
ms.openlocfilehash: 75797fa96e28c20b5d9bbec3178b64ebfc75218d
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48079121"
---
# <a name="localeinfo-resource-type"></a>localeInfo 资源类型

命名空间：microsoft.graph

有关已登录用户的区域设置信息，包括首选语言和国家/地区。


## <a name="properties"></a>属性
| 属性     | 类型   |说明|
|:---------------|:--------|:----------|
|区域设置|string|用户的区域设置表示形式，其中包括用户的首选语言和国家/地区。例如，“en-us”。根据 [ISO 639-1](https://www.iso.org/iso/home/standards/language_codes.htm) 中的定义，语言组件前面是 2 个字母的代码；根据 [ISO 3166-1 alpha-2](https://www.iso.org/iso/country_codes.htm) 中的定义，国家/地区组件前面是 2 个字母的代码。|
|displayName|string|用自然语言表示用户区域设置的名称，例如“English (United States)”。|

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.localeInfo"
}-->

```json
{
  "locale": "string",
  "displayName": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "localeInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

