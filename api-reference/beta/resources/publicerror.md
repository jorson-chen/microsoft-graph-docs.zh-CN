---
title: publicError 资源类型
description: 表示一般错误及其详细信息。
localization_priority: Normal
doc_type: resourcePageType
ms.prod: microsoft-teams
author: AkJo
ms.openlocfilehash: 65a75b6eb2756b92f9da6386390fae3b254f818b
ms.sourcegitcommit: f9f95402b8a15152ede90dd736b03d532204fc2e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2020
ms.locfileid: "49660084"
---
# <a name="publicerror-resource-type"></a>publicError 资源类型

命名空间：microsoft.graph

表示一般错误及其详细信息。

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|code|string| 表示错误代码。
|详细信息|[publicErrorDetail](publicerrordetail.md) 集合|错误的详细信息。|
|innerError|[publicInnerError](publicinnererror.md)|内部错误的详细信息。|
|message|字符串| 针对开发人员的未本地化邮件。
|target|String|错误的目标值。|

## <a name="relationships"></a>关系
无。

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.publicError"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.publicError",
  "code": "String",
  "message": "String",
  "target": "String",
  "details": [
    {
      "@odata.type": "microsoft.graph.publicErrorDetail"
    }
  ],
  "innerError": {
    "@odata.type": "microsoft.graph.publicInnerError"
  }
}
```

