---
title: skillProficiency 资源类型
description: skillProficiency 资源类型
localization_priority: Normal
author: kevinbellinger
ms.prod: people
doc_type: resourcePageType
ms.openlocfilehash: 0bb63903b5a3eb0eeed8683463b9927537180f53
ms.sourcegitcommit: dd94c3a0f7663699825b6dbc119cdcef494cd130
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/04/2019
ms.locfileid: "37950421"
---
# <a name="skillproficiency-resource-type"></a>skillProficiency 资源类型

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

表示有关与各种服务中的用户相关的技能的详细信息。

继承自[itemFacet](itemfacet.md)。

## <a name="methods"></a>方法
 
| 方法                                                 | 返回类型                             | 说明                                                   |
|:-------------------------------------------------------|:----------------------------------------|:--------------------------------------------------------------|
| [获取 skillProficiency](../api/skillproficiency-get.md) | [skillProficiency](skillproficiency.md) | 读取**skillProficiency**对象的属性和关系。 |
| [更新 skillProficiency](../api/skillproficiency-update.md)            | [skillProficiency](skillproficiency.md) | 更新**skillProficiency**对象。                               |
| [删除 skillProficiency](../api/skillproficiency-delete.md)            | 无                                    | 删除**skillProficiency**对象。                               |

## <a name="properties"></a>属性

| 属性     | 类型             | 描述                                                                                                                        |
|:-------------|:-----------------|:-----------------------------------------------------------------------------------------------------------------------------------|
|类别    |String collection | 包含用户与技能相关联的类别（例如，个人、职业、爱好）。                                       |
|displayName   |String            | 包含技能的友好名称。                                                                                            |      
|水平   |string            | 可取值为：`elementary`、`limitedWorking`、`generalProfessional`、`advancedProfessional`、`expert`、`unknownFutureValue`。|
|webUrl        |String            | 包含指向有关技能的信息源的链接。                                                                          |

## <a name="relationships"></a>关系

无。

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.skillProficiency",
  "baseType": ""
}-->

```json
{
  "categories": ["String"],
  "displayName": "String",
  "proficiency": "string",
  "webUrl": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "skillProficiency resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->