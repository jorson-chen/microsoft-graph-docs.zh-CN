---
title: administrativeUnit 资源类型
description: 管理单元为用户和组目录对象提供了一个概念性容器。
localization_priority: Normal
author: anandyadavMSFT
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 901a01f4d854f76c9907cf96660eb2bdb48403dc
ms.sourcegitcommit: 3b9eb50b790d952c7f350433ef7531d5e6d4b963
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/22/2020
ms.locfileid: "48692336"
---
# <a name="administrativeunit-resource-type"></a>administrativeUnit 资源类型

命名空间：microsoft.graph

管理单元为用户和组目录对象提供了一个概念性容器。 通过使用管理单元，公司管理员现在可以将管理责任委派给区域或部门管理员，以管理包含在管理单元或范围内的用户和组。

来看一个示例。 假设 Contoso Corp 由两个部门组成-一个 West 海岸部门和一个东海岸部门。 Contoso 的目录角色的作用范围限定为整个租户。 先生，Contoso company administrator，想要委派管理责任，但将这些职责范围限定为 West 海岸部门或东海岸部门。  用户可以创建 *西海岸 admistrative 单元* ，并将所有 West 海岸用户放入此管理单元。  同样，他可以创建一个 *东海岸管理单元*。  现在，可以开始将管理责任委派给其他人，但 **范围限定** 为创建的新管理单元。 先生将 Jennifer 放在 *帮助台管理员* 角色中， **作用域** 为 *西海岸管理单元*。  这允许 Jennifer 重置任何用户的密码，但前提是这些用户位于 *西海岸管理单元*中。  同样，工作先生将 Dave 放在 *用户帐户管理员* 角色中，该角色的 **作用域** 为 *东海岸管理单元*。  这允许 Dave 更新用户、分配许可证和重置任何用户的密码，但前提是这些用户位于 " *东海岸" 管理单元*中。 有关视频概述，请参阅 [Azure Active Directory 管理单元简介](https://channel9.msdn.com/Series/Windows-Azure-Active-Directory/Introduction-to-Azure-Active-Directory-Administrative-Units)。


本主题提供由 administrativeUnit 实体公开的已声明属性和导航属性的说明，以及可在 administrativeUnits 资源上调用的操作和函数。


## <a name="methods"></a>Methods

| 方法   | 返回类型 | 说明 |
|:---------------|:--------|:----------|
|[创建](../api/administrativeunit-post-administrativeunits.md) | [administrativeUnit](administrativeunit.md) | 创建新的管理单元。|
|[List](../api/administrativeunit-list.md) | [administrativeUnit](administrativeunit.md) 集合 |列出所有 administrativeUnits 的属性。|
|[获取](../api/administrativeunit-get.md) | [administrativeUnit](administrativeunit.md) |读取特定 administrativeUnit 对象的属性和关系。|
|[更新](../api/administrativeunit-update.md) | [administrativeUnit](administrativeunit.md)    |更新 administrativeUnit 对象。 |
|[删除](../api/administrativeunit-delete.md) | 无 |删除 administrativeUnit 对象。 |
|[添加成员](../api/administrativeunit-post-members.md) |[directoryObject](directoryobject.md)| 将成员添加 (用户或组) 。|
|[列出成员](../api/administrativeunit-list-members.md) |[directoryObject](directoryobject.md) 集合| 获取 (的用户和组) 成员的列表。|
|[获取成员](../api/administrativeunit-get-members.md) |[directoryObject](directoryobject.md)| 获取特定成员。|
|[删除成员](../api/administrativeunit-delete-members.md) |[directoryObject](directoryobject.md)| 删除成员。|
|[添加作用域角色成员](../api/administrativeunit-post-scopedrolemembers.md) |[scopedRoleMembership](scopedrolemembership.md)| 添加作用域角色成员。|
|[列出作用域内的角色成员](../api/administrativeunit-list-scopedrolemembers.md) |[scopedRoleMembership](scopedrolemembership.md) 集合| 获取作用域角色管理员的列表。|
|[获取作用域角色成员](../api/administrativeunit-get-scopedrolemembers.md) |[scopedRoleMembership](scopedrolemembership.md)| 获取特定的作用域角色成员。|
|[删除作用域范围的角色成员](../api/administrativeunit-delete-scopedrolemembers.md) |[scopedRoleMembership](scopedrolemembership.md)| 删除作用域角色成员。|

## <a name="properties"></a>属性
| 属性     | 类型   |说明|
|:---------------|:--------|:----------|
|说明|string|管理单元的可选说明。|
|displayName|string|管理单元的显示名称。|
|id|string|管理单元的唯一标识符。 只读。|
|visibility|string|控制管理单元及其成员是隐藏还是公开的。 可以设置为 `HiddenMembership` 或 `Public` 。 如果未设置，则默认行为是公共行为。 如果设置为 HiddenMembership，则只有管理单元的成员可以列出管理单位的其他成员。|

## <a name="relationships"></a>关系
| 关系 | 类型   |说明|
|:---------------|:--------|:----------|
|成员|[directoryObject](directoryobject.md) collection|作为此 Adminsitrative 单位的成员的用户和组。 HTTP 方法：获取 (的列表成员) 、POST (添加成员) 、删除 (删除成员) 。|
|scopedRoleMembers|[scopedRoleMembership](scopedrolemembership.md) 集合| 此管理单元的作用域角色成员。  HTTP 方法： GET (list scopedRoleMemberships) ，POST (add scopedRoleMembership) ，DELETE (remove scopedRoleMembership) 。 |

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.administrativeUnit"
}-->

```json
{
  "description": "string",
  "displayName": "string",
  "id": "string (identifier)",
  "visibility": "string"
}

```


## <a name="see-also"></a>另请参阅

- [使用扩展向资源添加自定义数据](/graph/extensibility-overview)
- [使用开放扩展向用户添加自定义数据](/graph/extensibility-open-users)
- [使用架构扩展向组添加自定义数据](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "administrativeUnit resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
