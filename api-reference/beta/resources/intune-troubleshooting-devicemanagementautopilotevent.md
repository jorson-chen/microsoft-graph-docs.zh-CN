---
title: deviceManagementAutopilotEvent 资源类型
description: 表示 Autopilot 流事件。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: 0ceaf629e9955fedb80910c7363caabfecfa290d
ms.sourcegitcommit: 86903a4730bbd825eabb7f0a1b2429723cc8b1e6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/26/2019
ms.locfileid: "37199891"
---
# <a name="devicemanagementautopilotevent-resource-type"></a>deviceManagementAutopilotEvent 资源类型

> **重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

表示 Autopilot 流事件。

## <a name="methods"></a>方法
|方法|返回类型|说明|
|:---|:---|:---|
|[列出 deviceManagementAutopilotEvents](../api/intune-troubleshooting-devicemanagementautopilotevent-list.md)|[deviceManagementAutopilotEvent](../resources/intune-troubleshooting-devicemanagementautopilotevent.md)集合|列出[deviceManagementAutopilotEvent](../resources/intune-troubleshooting-devicemanagementautopilotevent.md)对象的属性和关系。|
|[获取 deviceManagementAutopilotEvent](../api/intune-troubleshooting-devicemanagementautopilotevent-get.md)|[deviceManagementAutopilotEvent](../resources/intune-troubleshooting-devicemanagementautopilotevent.md)|读取[deviceManagementAutopilotEvent](../resources/intune-troubleshooting-devicemanagementautopilotevent.md)对象的属性和关系。|
|[创建 deviceManagementAutopilotEvent](../api/intune-troubleshooting-devicemanagementautopilotevent-create.md)|[deviceManagementAutopilotEvent](../resources/intune-troubleshooting-devicemanagementautopilotevent.md)|创建新的[deviceManagementAutopilotEvent](../resources/intune-troubleshooting-devicemanagementautopilotevent.md)对象。|
|[删除 deviceManagementAutopilotEvent](../api/intune-troubleshooting-devicemanagementautopilotevent-delete.md)|无|删除[deviceManagementAutopilotEvent](../resources/intune-troubleshooting-devicemanagementautopilotevent.md)。|
|[更新 deviceManagementAutopilotEvent](../api/intune-troubleshooting-devicemanagementautopilotevent-update.md)|[deviceManagementAutopilotEvent](../resources/intune-troubleshooting-devicemanagementautopilotevent.md)|更新[deviceManagementAutopilotEvent](../resources/intune-troubleshooting-devicemanagementautopilotevent.md)对象的属性。|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|id|String|对象的 UUID|
|eventDateTime|DateTimeOffset|事件发生的时间。|
|deviceRegisteredDateTime|DateTimeOffset|设备注册日期。|
|enrollmentStartDateTime|DateTimeOffset|设备注册开始日期。|
|enrollmentType|[windowsAutopilotEnrollmentType](../resources/intune-troubleshooting-windowsautopilotenrollmenttype.md)|注册类型。 可取值为：`unknown`、`azureADJoinedWithAutopilotProfile`、`offlineDomainJoined`、`azureADJoinedUsingDeviceAuthWithAutopilotProfile`、`azureADJoinedUsingDeviceAuthWithoutAutopilotProfile`、`azureADJoinedWithOfflineAutopilotProfile`、`azureADJoinedWithWhiteGlove`、`offlineDomainJoinedWithWhiteGlove`、`offlineDomainJoinedWithOfflineAutopilotProfile`。|
|deviceSerialNumber|String|设备序列号。|
|managedDeviceName|String|托管设备名称。|
|userPrincipalName|String|用于注册设备的用户主体名称。|
|windowsAutopilotDeploymentProfileDisplayName|String|Autopilot 配置文件名称。|
|enrollmentState|[enrollmentState](../resources/intune-shared-enrollmentstate.md)|注册状态，如 "已注册"，失败。 可取值为：`unknown`、`enrolled`、`pendingReset`、`failed`、`notContacted`、`blocked`。|
|windows10EnrollmentCompletionPageConfigurationDisplayName|String|注册状态页面配置文件名称|
|deploymentState|[windowsAutopilotDeploymentState](../resources/intune-troubleshooting-windowsautopilotdeploymentstate.md)|部署状态，如成功、失败、InProgress、SuccessWithTimeout。 可取值为：`unknown`、`success`、`inProgress`、`failure`、`successWithTimeout`。|
|osVersion|String|设备操作系统版本。|
|deploymentDuration|持续时间|包含注册的 Autopilot 部署持续时间。|
|deploymentTotalDuration|持续时间|从注册到桌面屏幕的总部署持续时间。|
|devicePreparationDuration|持续时间|在设备注册中花费的时间。|
|deviceSetupDuration|持续时间|在设备 ESP 中花费的时间。|
|accountSetupDuration|持续时间|用户 ESP 中所用的时间。|
|deploymentStartDateTime|DateTimeOffset|部署开始时间。|
|deploymentEndDateTime|DateTimeOffset|部署结束时间。|
|targetedAppCount|Int32|目标应用程序的计数。|
|targetedPolicyCount|Int32|目标策略的计数。|
|enrollmentFailureDetails|String|注册失败详细信息。|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagementAutopilotEvent"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementAutopilotEvent",
  "id": "String (identifier)",
  "eventDateTime": "String (timestamp)",
  "deviceRegisteredDateTime": "String (timestamp)",
  "enrollmentStartDateTime": "String (timestamp)",
  "enrollmentType": "String",
  "deviceSerialNumber": "String",
  "managedDeviceName": "String",
  "userPrincipalName": "String",
  "windowsAutopilotDeploymentProfileDisplayName": "String",
  "enrollmentState": "String",
  "windows10EnrollmentCompletionPageConfigurationDisplayName": "String",
  "deploymentState": "String",
  "osVersion": "String",
  "deploymentDuration": "String (duration)",
  "deploymentTotalDuration": "String (duration)",
  "devicePreparationDuration": "String (duration)",
  "deviceSetupDuration": "String (duration)",
  "accountSetupDuration": "String (duration)",
  "deploymentStartDateTime": "String (timestamp)",
  "deploymentEndDateTime": "String (timestamp)",
  "targetedAppCount": 1024,
  "targetedPolicyCount": 1024,
  "enrollmentFailureDetails": "String"
}
```


