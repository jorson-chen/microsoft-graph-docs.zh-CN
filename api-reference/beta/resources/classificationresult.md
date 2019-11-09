---
title: classificationResult 资源类型
description: 表示分类请求的结果。
localization_priority: Normal
author: tommoser
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 51b03cf4a579ccab642fe9bdce2e71becebba4be
ms.sourcegitcommit: 62507617292d5ad8598e83a8a253c986d9bac787
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/02/2019
ms.locfileid: "37938763"
---
# <a name="classificationresult-resource-type"></a>classificationResult 资源类型

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

表示来自 Microsoft 分类引擎的分类操作的结果。 来自 Azure 信息保护、Office 和其他 Microsoft 服务的数据分类结果可能会返回一[组定义完善的分类类型](https://docs.microsoft.com/office365/securitycompliance/what-the-sensitive-information-types-look-for)。 可以向[evaluateClassificationResults](../api/informationprotectionlabel-evaluateclassificationresults.md) API 提供这些类型，以将敏感信息解析为 Microsoft 信息保护标签。 

## <a name="properties"></a>属性

| 属性        | 类型  | 描述                                                            |
| :-------------- | :---- | :--------------------------------------------------------------------- |
| confidenceLevel | Int32 | 结果的置信度（0到100）。                         |
| count           | Int32 | 输入中特定信息类型的实例数。 |
| sensitiveTypeId | GUID  | 发现的敏感信息类型的 GUID。                 |

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.classificationResult",
  "baseType": null
}-->

```json
{
  "confidenceLevel": 1024,
  "count": 1024,
  "sensitiveTypeId": "Guid"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "classificationResult resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->