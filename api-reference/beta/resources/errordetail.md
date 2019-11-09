---
title: errorDetail 资源类型
description: 介绍了失败请求以异步方式创建 Microsoft Search 连接架构的错误。
localization_priority: Normal
author: snlraju-msft
ms.prod: ''
doc_type: resourcePageType
ms.openlocfilehash: d52d2953a9ec282b55b021f653854b6c3b6054eb
ms.sourcegitcommit: 62507617292d5ad8598e83a8a253c986d9bac787
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/02/2019
ms.locfileid: "37938988"
---
# <a name="errordetail-resource-type"></a>errorDetail 资源类型

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

介绍了失败请求以异步方式创建 Microsoft Search 连接[架构](schema.md)的错误。

## <a name="properties"></a>属性

| 属性  | 类型                                               | 描述 |
|:----------|:---------------------------------------------------|:------------|
| 详细信息   | [innerErrorDetail](innererrordetail.md)集合 | 内部错误的集合（如果有）。 只读的，可空。 |
| errorCode | String                                             | 与错误相关联的错误代码（如果有）。 只读的，可空。 |
| message   | String                                             | 人类可读错误消息。 只读。 |

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "details",
    "errorCode"
  ],
  "@odata.type": "microsoft.graph.errorDetail",
  "baseType": null
}-->

```json
{
  "details": [{"@odata.type": "microsoft.graph.innerErrorDetail"}],
  "errorCode": "String",
  "message": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "errorDetail resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->