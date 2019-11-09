---
title: personWebsite 资源类型
description: personWebsite 资源类型
localization_priority: Normal
author: kevinbellinger
ms.prod: people
doc_type: resourcePageType
ms.openlocfilehash: b5e6b8c3013c647087ab3d8db28b0196d0c79036
ms.sourcegitcommit: dd94c3a0f7663699825b6dbc119cdcef494cd130
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/04/2019
ms.locfileid: "37949494"
---
# <a name="personwebsite-resource-type"></a>personWebsite 资源类型

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

表示有关与各种服务中的用户相关联的网站的详细信息。

继承自[itemFacet](itemfacet.md)。

## <a name="methods"></a>方法

| 方法                                           | 返回类型                       | 说明                                                |
|:-------------------------------------------------|:----------------------------------|:-----------------------------------------------------------|
| [获取 personWebsite](../api/personwebsite-get.md) | [personWebsite](personwebsite.md) | 读取**personWebsite**对象的属性和关系。 |
| [更新 personWebsite](../api/personwebsite-update.md)         | [personWebsite](personwebsite.md) | 更新**personWebsite**对象。                               |
| [删除 personWebsite](../api/personwebsite-delete.md)         | 无                              | 删除**personWebsite**对象。                               |

## <a name="properties"></a>属性

| 属性     | 类型              | 描述                                                                         |
|:-------------|:------------------|:------------------------------------------------------------------------------------|
|类别    |String collection  | 包含用户与网站相关联的类别（例如，个人、食谱）。  |
|description   |字符串             | 包含网站的说明。                                              |
|displayName   |String             | 包含网站的友好名称。                                           |
|webUrl        |String             | 包含指向网站本身的链接。                                              |

## <a name="relationships"></a>关系

无。

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。 

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.personWebsite",
  "baseType": ""
}-->

```json
{
  "categories": ["String"],
  "description": "String",
  "displayName": "String",
  "webUrl": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "personWebsite resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->