---
title: deviceGeoLocation 资源类型
description: 设备位置
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 5aa5c419acea39c48ab14ac503b34dcdf0110aec
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49293036"
---
# <a name="devicegeolocation-resource-type"></a>deviceGeoLocation 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

设备位置

## <a name="properties"></a>属性
|属性|类型|Description|
|:---|:---|:---|
|lastCollectedDateTimeUtc|DateTimeOffset|记录位置时的时间，相对于 UTC|
|lastCollectedDateTime|DateTimeOffset|记录位置时的时间，相对于 UTC|
|longitude|Double|设备位置的经度坐标|
|latitude|Double|设备位置的纬度坐标|
|altitude|Double|高度，以高出海平面的米数表示|
|horizontalAccuracy|Double|经度和纬度的准确度，以米为单位|
|verticalAccuracy|Double|高度的准确度，以米为单位|
|heading|Double|相对于真北的方位，以度为单位|
|speed|Double|设备的移动速度，以米/秒为单位|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceGeoLocation"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceGeoLocation",
  "lastCollectedDateTimeUtc": "String (timestamp)",
  "lastCollectedDateTime": "String (timestamp)",
  "longitude": "4.2",
  "latitude": "4.2",
  "altitude": "4.2",
  "horizontalAccuracy": "4.2",
  "verticalAccuracy": "4.2",
  "heading": "4.2",
  "speed": "4.2"
}
```




