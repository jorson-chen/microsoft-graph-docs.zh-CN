---
title: softwareUpdateStatusSummary 资源类型
description: 尚未记录
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 2aee8b02e3baf150cf760116c9c993ce37a353c6
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49276600"
---
# <a name="softwareupdatestatussummary-resource-type"></a>softwareUpdateStatusSummary 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

尚未记录

## <a name="methods"></a>方法
|方法|返回类型|说明|
|:---|:---|:---|
|[获取 softwareUpdateStatusSummary](../api/intune-deviceconfig-softwareupdatestatussummary-get.md)|[softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md)|读取 [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md) 对象的属性和关系。|
|[更新 softwareUpdateStatusSummary](../api/intune-deviceconfig-softwareupdatestatussummary-update.md)|[softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md)|更新 [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md) 对象的属性。|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|id|字符串|实体的键。|
|displayName|字符串|策略的名称。|
|compliantDeviceCount|Int32|兼容设备的数量。|
|nonCompliantDeviceCount|Int32|不兼容设备的数量。|
|remediatedDeviceCount|Int32|已修复设备的数量。|
|errorDeviceCount|Int32|出现错误的设备数量。|
|unknownDeviceCount|Int32|未知设备的数量。|
|conflictDeviceCount|Int32|冲突设备的数量。|
|notApplicableDeviceCount|Int32|不适用设备的数量。|
|compliantUserCount|Int32|兼容用户的数量。|
|nonCompliantUserCount|Int32|不兼容用户的数量。|
|remediatedUserCount|Int32|已修复用户的数量。|
|errorUserCount|Int32|出现错误的用户数量。|
|unknownUserCount|Int32|未知用户的数量。|
|conflictUserCount|Int32|冲突用户的数量。|
|notApplicableUserCount|Int32|不适用用户的数量。|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.softwareUpdateStatusSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.softwareUpdateStatusSummary",
  "id": "String (identifier)",
  "displayName": "String",
  "compliantDeviceCount": 1024,
  "nonCompliantDeviceCount": 1024,
  "remediatedDeviceCount": 1024,
  "errorDeviceCount": 1024,
  "unknownDeviceCount": 1024,
  "conflictDeviceCount": 1024,
  "notApplicableDeviceCount": 1024,
  "compliantUserCount": 1024,
  "nonCompliantUserCount": 1024,
  "remediatedUserCount": 1024,
  "errorUserCount": 1024,
  "unknownUserCount": 1024,
  "conflictUserCount": 1024,
  "notApplicableUserCount": 1024
}
```




