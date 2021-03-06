---
title: deviceHealthScriptRunSummary 资源类型
description: 包含设备管理脚本的运行摘要的属性。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: ef09482999fdff50ebbd1bd0e0df5320aad6f206
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49299357"
---
# <a name="devicehealthscriptrunsummary-resource-type"></a>deviceHealthScriptRunSummary 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

包含设备管理脚本的运行摘要的属性。

## <a name="methods"></a>Methods
|方法|返回类型|Description|
|:---|:---|:---|
|[获取 deviceHealthScriptRunSummary](../api/intune-devices-devicehealthscriptrunsummary-get.md)|[deviceHealthScriptRunSummary](../resources/intune-devices-devicehealthscriptrunsummary.md)|读取 [deviceHealthScriptRunSummary](../resources/intune-devices-devicehealthscriptrunsummary.md) 对象的属性和关系。|
|[更新 deviceHealthScriptRunSummary](../api/intune-devices-devicehealthscriptrunsummary-update.md)|[deviceHealthScriptRunSummary](../resources/intune-devices-devicehealthscriptrunsummary.md)|更新 [deviceHealthScriptRunSummary](../resources/intune-devices-devicehealthscriptrunsummary.md) 对象的属性。|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|id|字符串|设备运行状况脚本的键运行摘要实体。 此属性是只读的。|
|noIssueDetectedDeviceCount|Int32|检测脚本找不到问题且设备正常运行的设备数|
|issueDetectedDeviceCount|Int32|检测脚本发现问题的设备数|
|detectionScriptErrorDeviceCount|Int32|检测脚本执行时遇到错误且未完成的设备数量|
|detectionScriptPendingDeviceCount|Int32|尚未运行的设备运行状况脚本的最新版本的设备数量|
|issueRemediatedDeviceCount|Int32|修正脚本能够解决检测到的问题的设备数|
|remediationSkippedDeviceCount|Int32|跳过修正的设备数|
|issueReoccurredDeviceCount|Int32|已成功执行修正脚本但未能解决检测到的问题的设备数量|
|remediationScriptErrorDeviceCount|Int32|修正脚本执行时遇到错误且未完成的设备数量|
|lastScriptRunDateTime|DateTimeOffset|在所有设备上的脚本的上次运行时间|
|issueRemediatedCumulativeDeviceCount|Int32|最近30天内修正的设备数量|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceHealthScriptRunSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceHealthScriptRunSummary",
  "id": "String (identifier)",
  "noIssueDetectedDeviceCount": 1024,
  "issueDetectedDeviceCount": 1024,
  "detectionScriptErrorDeviceCount": 1024,
  "detectionScriptPendingDeviceCount": 1024,
  "issueRemediatedDeviceCount": 1024,
  "remediationSkippedDeviceCount": 1024,
  "issueReoccurredDeviceCount": 1024,
  "remediationScriptErrorDeviceCount": 1024,
  "lastScriptRunDateTime": "String (timestamp)",
  "issueRemediatedCumulativeDeviceCount": 1024
}
```




