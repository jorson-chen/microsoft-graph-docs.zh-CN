---
title: protectDoNotForwardAction 资源类型
description: 通知应用程序应用 "请勿转发保护"。
localization_priority: Normal
author: tommoser
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 1d9687460a549438db1c9076bef2184b0b1ee5d3
ms.sourcegitcommit: 62507617292d5ad8598e83a8a253c986d9bac787
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/02/2019
ms.locfileid: "37939185"
---
# <a name="protectdonotforwardaction-resource-type"></a>protectDoNotForwardAction 资源类型

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

通知应用程序应用 "请勿转发保护"。 如果生成的标签已配置为 "应用不[转发保护](https://docs.microsoft.com/azure/information-protection/configure-usage-rights#do-not-forward-option-for-emails)"，则[evaluateApplication](../api/informationprotectionlabel-evaluateapplication.md)或[evaluateClassificationResults](../api/informationprotectionlabel-evaluateclassificationresults.md)可能会返回**protectionDoNotForwardAction** 。 使用的应用程序必须使用客户端库通过 Azure 信息保护来应用保护。

## <a name="properties"></a>属性

无

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.protectDoNotForwardAction",
  "baseType": "microsoft.graph.informationProtectionAction"
}-->

```json
{
  
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "protectDoNotForwardAction resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->