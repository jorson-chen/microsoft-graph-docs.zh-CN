---
title: profileCardProperty 资源类型
description: 用于将新的属性指定为在共享、人员体验或应用了自定义的显示名称或批注的情况下进行呈现。 管理员可以为其组织中支持的语言定义默认的显示名称字符串和一组替代转换。
localization_priority: Normal
author: kevinbellinger
ms.prod: people
doc_type: resourcePageType
ms.openlocfilehash: 0dc09ae31f2b0189f0b3f3e0be83a72ea76e2448
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48029090"
---
# <a name="profilecardproperty-resource-type"></a>profileCardProperty 资源类型

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

表示适用于组织的 Microsoft 365 配置文件卡片上的用户的属性，用于在共享、人员体验中进行呈现。

该属性可以是 azure AD) 的 Azure Active Directory (的内置属性（例如 `Alias` 或）， `UserPrincipalName` 也可以是自定义属性。 对于自定义属性，管理员可以为 `en-us` 其组织中支持的语言定义默认的显示名称字符串和一组替代转换。

有关向组织的配置文件卡片添加属性的详细信息，请参阅 [自定义配置文件卡片](/graph/add-properties-profilecard)。

## <a name="methods"></a>方法

| 方法       | 返回类型 | Description |
|:-------------------------------------------------------------|:----------------------------------------------|:-----------------------------------------------------------------|
| [List](../api/organizationsettings-list-profilecardproperties.md) | [profileCardProperty](profilecardproperty.md) | 获取组织的 **profileCardProperty** 资源的集合。 |
| [创建](../api/organizationsettings-post-profilecardproperties.md) | [profileCardProperty](profilecardproperty.md) | 为组织创建新的 **profileCardProperty** 资源。 |
| [获取](../api/profilecardproperty-get.md) | [profileCardProperty](profilecardproperty.md) | 阅读 **profileCardProperty** 资源的属性和关系，其中包含在给定字段的 Microsoft 365 组织中存在的配置文件卡片自定义项。 |
| [更新](../api/profilecardproperty-update.md)               | [profileCardProperty](profilecardproperty.md) | 更新 **profileCardProperty** 对象。                               |
| [删除](../api/profilecardproperty-delete.md)               | 无                                          | 删除 **profileCardProperty** 对象。                               |

## <a name="properties"></a>属性

| 属性             | 类型                                                        | 说明 |
|:---------------------|:------------------------------------------------------------|:------------|
|批注           |[profileCardAnnotation](profilecardannotation.md) 集合 | 允许管理员为目录属性设置自定义显示标签，并针对其租户中的用户对其进行本地化。|
|directoryPropertyName |String                                                       | 标识[获取](../api/profilecardproperty-get.md)、[更新](../api/profilecardproperty-update.md)或[删除](../api/profilecardproperty-delete.md)操作中的**profileCardProperty**资源。 允许管理员在其租户内的 Microsoft 365 配置文件卡上 (Azure AD) 属性呈现隐藏的 Azure Active Directory。 如果存在，则此字段中引用的 Azure AD 字段将在配置文件卡片的联系人窗格中对租户中的所有用户可见。 此字段允许的值为：、、、、、、、、、、、、、、、、、、、、 `UserPrincipalName` `Fax` `StreetAddress` `PostalCode` `StateOrProvince` `Alias` `CustomAttribute1`  `CustomAttribute2` `CustomAttribute3` `CustomAttribute4` `CustomAttribute5` `CustomAttribute6` `CustomAttribute7` `CustomAttribute8` `CustomAttribute9` `CustomAttribute10` `CustomAttribute11` `CustomAttribute12` `CustomAttribute13` `CustomAttribute14` `CustomAttribute15` 。 |

## <a name="relationships"></a>关系

无。

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.profileCardProperty",
  "baseType": ""
}-->

```json
{
  "annotations": [
    {
      "displayName": "String",
      "localizations": [
        {
          "languageTag": "String",
          "displayName": "String"
        }
      ]
    }
  ],
  "directoryPropertyName": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "profileCardProperty resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

