---
title: optionalClaim 资源类型
description: 包含与应用程序关联的可选声明。
localization_priority: Normal
author: sureshja
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: f40574cb80ab458d1675507b796b43b95e19cf41
ms.sourcegitcommit: 7ceec757fd82ef3fd80aa3089ef46d3807aa3aa2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2020
ms.locfileid: "48401144"
---
# <a name="optionalclaim-resource-type"></a>optionalClaim 资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

包含与[应用程序](application.md)关联的可选声明 <!-- or a service principal -->. [OptionalClaims](optionalclaims.md)资源的**idToken**、 **AccessToken**和**saml2Token**属性是**optionalClaim**的集合。 如果特定声明支持，还可以使用属性修改 optionalClaim 的行为 `additionalProperties` 。 

有关详细信息，请参阅[向 Azure AD 应用提供可选声明](/azure/active-directory/develop/active-directory-optional-claims)。

## <a name="properties"></a>属性

| 属性     | 类型        | 说明 |
|:-------------|:------------|:------------|
|additionalProperties|字符串集合| 声明的其他属性。 如果某个属性存在于此集合中，它将修改在 name 属性中指定的可选声明的行为。 |
|组成部分|布尔| 如果值为 true，则客户端指定的声明是为确保最终用户请求的特定任务的平稳授权体验所必需的。 默认值为 false。|
|name|字符串| 可选声明的名称。 |
|source|字符串| 声明的源 (directory 对象) 。 来自扩展属性的预定义声明和用户定义的声明。 如果源值为 null，则声明是预定义的可选声明。 如果源值为 user，则 name 属性中的值是用户对象的扩展属性。 |

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.optionalClaim",
  "baseType": null
}-->

```json
{
  "additionalProperties": ["String"],
  "essential": true,
  "name": "String",
  "source": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "optionalClaim resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->