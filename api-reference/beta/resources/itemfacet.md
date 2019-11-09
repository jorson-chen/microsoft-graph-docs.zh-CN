---
title: itemFacet 资源类型
description: itemFacet 资源类型
localization_priority: Normal
author: kevinbellinger
ms.prod: people
doc_type: resourcePageType
ms.openlocfilehash: bb89037b3d5b88e57ec12b2b02a5e2ed37cb2601
ms.sourcegitcommit: 62507617292d5ad8598e83a8a253c986d9bac787
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/02/2019
ms.locfileid: "37939325"
---
# <a name="itemfacet-resource-type"></a>itemFacet 资源类型

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

表示[配置文件](profile.md)entityset 中的所有资源类型继承自的抽象基类型。

## <a name="properties"></a>属性

| 属性             | 类型                            | 描述 |
|:---------------------|:--------------------------------|:------------|
|allowedAudiences      |string                           | 可取值为：`me`、`family`、`contacts`、`groupMembers`、`organization`、`federatedOrganizations`、`everyone`、`unknownFutureValue`。  |
|createdBy             |[identitySet](identityset.md)    | 实体最初创建时。   |
|createdDateTime       |DateTimeOffset                   |时间戳类型表示使用 ISO 8601 格式的日期和时间信息，并且始终处于 UTC 时间。例如，2014 年 1 月 1 日午夜 UTC 如下所示：`'2014-01-01T00:00:00Z'`|
|id                    |字符串                           | 只读。|
|推导             |[inferenceData](inferencedata.md)| 如果对实体进行推断，则包含推理详细信息。 |
|lastModifiedBy        |[identitySet](identityset.md)    | 上次修改实体的合作伙伴或用户的标识符。 |
|lastModifiedDateTime  |DateTimeOffset                   |时间戳类型表示使用 ISO 8601 格式的日期和时间信息，并且始终处于 UTC 时间。例如，2014 年 1 月 1 日午夜 UTC 如下所示：`'2014-01-01T00:00:00Z'`|

## <a name="relationships"></a>关系

无

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.itemFacet",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "allowedAudiences": "string",
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "inference": {"@odata.type": "microsoft.graph.inferenceData"},
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "itemFacet resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->