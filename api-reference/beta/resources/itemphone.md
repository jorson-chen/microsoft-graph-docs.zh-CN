---
title: itemPhone 资源类型
description: itemPhone 资源类型
localization_priority: Normal
author: kevinbellinger
ms.prod: people
doc_type: resourcePageType
ms.openlocfilehash: 2ba1fce4492bfacb3a44f21a0fc55ddd8d37b068
ms.sourcegitcommit: dd94c3a0f7663699825b6dbc119cdcef494cd130
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/04/2019
ms.locfileid: "37950435"
---
# <a name="itemphone-resource-type"></a>itemPhone 资源类型

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

表示有关与各种服务中的用户关联的电话号码的详细信息。

## <a name="methods"></a>方法

| 方法                                     | 返回类型               | 说明                                            |
|:-------------------------------------------|:--------------------------|:-------------------------------------------------------|
| [获取 itemPhone](../api/itemphone-get.md)   | [itemPhone](itemphone.md) | 读取**itemPhone**对象的属性和关系。 |
| [更新 itemPhone](../api/itemphone-update.md)       | [itemPhone](itemphone.md) | 更新**itemPhone**对象。                               |
| [删除 itemPhone](../api/itemphone-delete.md)       | 无                      | 删除**itemPhone**对象。                               |

## <a name="properties"></a>属性

| 属性     | 类型        | 说明                                                                                                                     |
|:-------------|:------------|:--------------------------------------------------------------------------------------------------------------------------------|
|displayName   |String       | 包含电话号码的友好名称。                                                                                  |
|number        |String       | 包含电话号码。                                                                                                       |
|类型          |字符串       | 可取值为：`home`、`business`、`mobile`、`other`、`assistant`、`homeFax`、`businessFax`、`otherFax`、`pager`、`radio`。|

## <a name="relationships"></a>关系

无

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.itemPhone",
  "baseType": ""
}-->

```json
{
  "displayName": "String",
  "number": "String",
  "type": "string"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "itemPhone resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->