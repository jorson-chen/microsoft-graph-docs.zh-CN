---
title: 放置资源类型
description: 代表一个位置。 这是聊天室或 roomList 的基类型。
localization_priority: Normal
author: vrod9429
ms.prod: outlook
doc_type: resourcePageType
ms.openlocfilehash: ff8944e9aa46bf52354af2f9762c089f9e0d1446
ms.sourcegitcommit: 7ceec757fd82ef3fd80aa3089ef46d3807aa3aa2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2020
ms.locfileid: "48406168"
---
# <a name="place-resource-type"></a>放置资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

表示基本位置属性，如名称、物理地址和地理坐标。 这是更丰富的位置类型（如 [聊天室](room.md) 和 [roomList](roomlist.md)）的基类型。

### <a name="using-the-places-api"></a>使用位置 API
Exchange Online 管理员可将租户中的会议室组织到会议室列表中。 使用 "位置" API，您可以获取租户中的所有会议室列表或会议室，或获取特定会议室列表中的所有会议室。

位置，如 [会议室](room.md) 和 [roomList](roomlist.md) 包含基本 **id**、显示名称和电子邮件地址。 此外，它们还包含诸如物理地址和地理坐标等导航信息，在会议室的情况下，其他相关信息（如 AV 功能、楼层号和容量）。

[FindRooms](../api/user-findrooms.md)和[findRoomLists](../api/user-findroomlists.md)函数支持对租户中的会议室和会议室列表进行类似的查找。 以下是位置 API 和这些函数之间的比较。  如果要创建生产应用程序，请选择 "位置" API，因为 API 现在在 v1.0 中通常可用。 计划更新使用 **findRooms** 或 **findRoomLists** 的任何现有代码以使用位置 API，因为 **findRooms** 或 **findRoomLists** 将被弃用，并将发布一个时间线。

|位置 API |findRooms 和 findRoomLists 函数|
|:------------------------------------|:-----------------------------|
|支持获取租户中的所有会议室或会议室列表，以及会议室列表中的所有会议室 | 类似的支持-获取租户中的所有会议室或会议室列表，以及会议室列表中的所有会议室|
|[列表位置](../api/place-list.md) 可在租户中返回100个以上的聊天室 | [findRooms](../api/user-findrooms.md) 返回到租户中的前100个聊天室 |
|支持[获取租户中的单个会议室或会议室列表](../api/place-get.md) | 不支持在租户中获取单个会议室或会议室列表
|定义 [会议室](room.md) 和 [roomList](roomlist.md) 的特定实体，除了显示名称和 SMTP 地址之外，还可指定更丰富的属性集。 | 每个会议室和会议室列表都是重量较轻的 [emailAddress](emailaddress.md) 类型，仅指定显示名称和 SMTP 地址|
|仅支持委派 (工作或学校帐户) 或应用程序权限的组织方案 | 仅对具有委派或应用程序权限的组织方案的类似支持|
|支持[更新租户中的单个会议室或会议室列表](../api/place-update.md) | 不支持更新租户中的单个会议室或会议室列表

## <a name="methods"></a>方法

| 方法                              | 返回类型                  | 说明 |
|:------------------------------------|:-----------------------------|:--------|
| [列表位置](../api/place-list.md) | 所请求的派生类型的[位置](place.md)的集合 | 获取在租户中定义的指定类型的 **位置** 对象的集合。 |
| [获取位置](../api/place-get.md)    | 所请求的派生类型的 [位置](place.md)            | 获取指定的 **place** 对象的属性和关系。 |
| [更新位置](../api/place-update.md)    | 所请求的派生类型的 [位置](place.md)            | 更新指定的 **place** 对象的属性和关系。 |

## <a name="properties"></a>属性

| 属性       | 类型                                              | 说明 |
|:---------------|:--------------------------------------------------|:--------|
| address        | [physicalAddress](physicaladdress.md)             | 地点的街道地址。 |
| displayName    | 字符串                                            | 与位置关联的名称。 |
| geoCoordinates | [outlookGeoCoordinates](outlookgeocoordinates.md) | 指定纬度、经度和 (中的位置（可选）) 海拔坐标。 |
| id             | 字符串                                            | 位置的唯一标识符。 只读。 |
| phone          | String                                            | 地点的电话号码。 |

## <a name="relationships"></a>关系

无。

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.place",
  "baseType": ""
}-->

```json
{
  "address": {"@odata.type": "microsoft.graph.physicalAddress"},
  "displayName": "String",
  "id": "String (identifier)",
  "geoCoordinates": {"@odata.type": "microsoft.graph.outlookGeoCoordinates"},
  "phone": "String"
}
```

## <a name="see-also"></a>另请参阅
- 若要使管理员能够创建会议室列表，请使用 Exchange PowerShell cmdlet [new-distributiongroup](/powershell/module/exchange/users-and-groups/new-distributiongroup)。
- 若要使管理员向会议室列表中添加聊天室，请使用 Exchange Powershell cmdlet [外接程序 get-distributiongroupmember](/powershell/module/exchange/users-and-groups/add-distributiongroupmember)。

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "place resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
