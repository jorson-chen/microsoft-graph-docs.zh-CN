---
title: deviceHealthScriptRunOnceSchedule 资源类型
description: 设备运行状况脚本运行一次计划。
author: dougeby
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: d043e60793376b636b826f10728c60607eb812a5
ms.sourcegitcommit: d961d83d2792328c9b64421325299e4b56d8dabd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/09/2020
ms.locfileid: "44178533"
---
# <a name="devicehealthscriptrunonceschedule-resource-type"></a>deviceHealthScriptRunOnceSchedule 资源类型

命名空间：microsoft.graph

> **重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

设备运行状况脚本运行一次计划。


继承自[deviceHealthScriptTimeSchedule](../resources/intune-devices-devicehealthscripttimeschedule.md)

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|interval|Int32|每小时计划的 x 值，每隔 x 小时在每日计划的每 x 小时，每周计划的 x 周，每个 x 个月的日程安排。 从[DeviceHealthScriptRunSchedule](../resources/intune-devices-devicehealthscriptrunschedule.md)继承的有效值1到23|
|useUtc|Boolean|指示时间是 Utc 还是客户端本地时间。 继承自[deviceHealthScriptTimeSchedule](../resources/intune-devices-devicehealthscripttimeschedule.md)|
|time|TimeOfDay|在什么时候计划运行脚本。 此集合最多可包含20个元素。 继承自[deviceHealthScriptTimeSchedule](../resources/intune-devices-devicehealthscripttimeschedule.md)|
|date|Date|计划运行脚本的日期。 此集合最多可包含20个元素。|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceHealthScriptRunOnceSchedule"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceHealthScriptRunOnceSchedule",
  "interval": 1024,
  "useUtc": true,
  "time": "String (time of day)",
  "date": "String (Date)"
}
```


