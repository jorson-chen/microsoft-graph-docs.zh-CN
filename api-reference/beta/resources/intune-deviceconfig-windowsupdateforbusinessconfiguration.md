---
title: windowsUpdateForBusinessConfiguration 资源类型
description: 适用于企业的 Windows 更新配置。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 1a2d6dd94136fba462b51dc3bc4553048d967da3
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49231322"
---
# <a name="windowsupdateforbusinessconfiguration-resource-type"></a>windowsUpdateForBusinessConfiguration 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

适用于企业的 Windows 更新配置。


继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)

## <a name="methods"></a>方法
|方法|返回类型|说明|
|:---|:---|:---|
|[List windowsUpdateForBusinessConfigurations](../api/intune-deviceconfig-windowsupdateforbusinessconfiguration-list.md)|[windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) 集合|列出 [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) 对象的属性和关系。|
|[Get windowsUpdateForBusinessConfiguration](../api/intune-deviceconfig-windowsupdateforbusinessconfiguration-get.md)|[windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md)|读取 [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) 对象的属性和关系。|
|[Create windowsUpdateForBusinessConfiguration](../api/intune-deviceconfig-windowsupdateforbusinessconfiguration-create.md)|[windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md)|创建新的 [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) 对象。|
|[Delete windowsUpdateForBusinessConfiguration](../api/intune-deviceconfig-windowsupdateforbusinessconfiguration-delete.md)|无|删除 [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md)。|
|[Update windowsUpdateForBusinessConfiguration](../api/intune-deviceconfig-windowsupdateforbusinessconfiguration-update.md)|[windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md)|更新 [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) 对象的属性。|
|[extendFeatureUpdatesPause 操作](../api/intune-deviceconfig-windowsupdateforbusinessconfiguration-extendfeatureupdatespause.md)|无|为 Windows Update for Business 振铃扩展功能更新暂停。|
|[extendQualityUpdatesPause 操作](../api/intune-deviceconfig-windowsupdateforbusinessconfiguration-extendqualityupdatespause.md)|无|为 Windows Update for Business 振铃扩展质量更新暂停。|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|id|String|实体的键。 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|上次修改对象的日期/时间。 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|roleScopeTagIds|String 集合|此实体实例的范围标记列表。 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|supportsScopeTags|Boolean|指示基础设备配置是否支持作用域标记的分配。 如果此值为 false，则不允许分配给 ScopeTags 属性，并且实体将对作用域用户不可见。 这适用于在 Silverlight 中创建的旧版策略，可以通过在 Azure 门户中删除并重新创建策略来解决此事件。 此属性是只读的。 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|deviceManagementApplicabilityRuleOsEdition|[deviceManagementApplicabilityRuleOsEdition](../resources/intune-deviceconfig-devicemanagementapplicabilityruleosedition.md)|适用于此策略的操作系统版本。 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|deviceManagementApplicabilityRuleOsVersion|[deviceManagementApplicabilityRuleOsVersion](../resources/intune-deviceconfig-devicemanagementapplicabilityruleosversion.md)|此策略的操作系统版本适用性规则。 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|deviceManagementApplicabilityRuleDeviceMode|[deviceManagementApplicabilityRuleDeviceMode](../resources/intune-deviceconfig-devicemanagementapplicabilityruledevicemode.md)|此策略的设备模式适用性规则。 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|createdDateTime|DateTimeOffset|创建对象的日期/时间。 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|description|String|管理员提供的设备配置的说明。 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|displayName|String|管理员提供的设备配置的名称。 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|version|Int32|设备配置的版本。 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|deliveryOptimizationMode|[windowsDeliveryOptimizationMode](../resources/intune-deviceconfig-windowsdeliveryoptimizationmode.md)|传递优化模式。 可取值为：`userDefined`、`httpOnly`、`httpWithPeeringNat`、`httpWithPeeringPrivateGroup`、`httpWithInternetPeering`、`simpleDownload` 或 `bypassMode`。|
|prereleaseFeatures|[prereleaseFeatures](../resources/intune-deviceconfig-prereleasefeatures.md)|预发布功能。 可取值为：`userDefined`、`settingsOnly`、`settingsAndExperimentations`、`notAllowed`。|
|automaticUpdateMode|[automaticUpdateMode](../resources/intune-deviceconfig-automaticupdatemode.md)|自动更新模式。 可取值为：`userDefined`、`notifyDownload`、`autoInstallAtMaintenanceTime`、`autoInstallAndRebootAtMaintenanceTime`、`autoInstallAndRebootAtScheduledTime`、`autoInstallAndRebootWithoutEndUserControl` 或 `windowsDefault`。|
|microsoftUpdateServiceAllowed|Boolean|允许 Microsoft 更新服务|
|driversExcluded|Boolean|排除 Windows 更新驱动程序|
|installationSchedule|[windowsUpdateInstallScheduleType](../resources/intune-deviceconfig-windowsupdateinstallscheduletype.md)|安装计划|
|qualityUpdatesDeferralPeriodInDays|Int32|推迟质量更新的天数|
|featureUpdatesDeferralPeriodInDays|Int32|推迟功能更新的天数|
|qualityUpdatesPaused|Boolean|暂停质量更新|
|featureUpdatesPaused|Boolean|暂停功能更新|
|qualityUpdatesPauseExpiryDateTime|DateTimeOffset|质量更新暂停到期日期/时间|
|featureUpdatesPauseExpiryDateTime|DateTimeOffset|功能更新暂停到期日期/时间|
|businessReadyUpdatesOnly|[windowsUpdateType](../resources/intune-deviceconfig-windowsupdatetype.md)|确定将从哪些分支设备接收其更新。 可取值为：`userDefined`、`all`、`businessReadyOnly`、`windowsInsiderBuildFast`、`windowsInsiderBuildSlow`、`windowsInsiderBuildRelease`。|
|skipChecksBeforeRestart|Boolean|设置为在重新启动之前跳过所有复选：电池级别 = 40%、用户状态、需要显示、演示模式、全屏模式、电话呼叫状态、游戏模式等。 |
|updateWeeks|[windowsUpdateForBusinessUpdateWeeks](../resources/intune-deviceconfig-windowsupdateforbusinessupdateweeks.md)|在每月的几周安排更新安装。 可取值为：`userDefined`、`firstWeek`、`secondWeek`、`thirdWeek`、`fourthWeek`、`everyWeek`。|
|qualityUpdatesPauseStartDate|日期|质量更新暂停开始日期。 此属性是只读的。|
|featureUpdatesPauseStartDate|日期|功能更新暂停开始日期。 此属性是只读的。|
|featureUpdatesRollbackWindowInDays|Int32|回滚对其有效的功能更新后的天数|
|qualityUpdatesWillBeRolledBack|Boolean|指定是否在下一个设备签入时回滚质量更新|
|featureUpdatesWillBeRolledBack|Boolean|指定是否在下一个设备签入时回滚功能更新|
|qualityUpdatesRollbackStartDateTime|DateTimeOffset|质量更新回滚开始日期/时间|
|featureUpdatesRollbackStartDateTime|DateTimeOffset|功能更新回滚的开始日期时间|
|engagedRestartDeadlineInDays|Int32|在非活动时段自动安排和执行挂起的重启的期限（以天为单位），有效范围为2到30天|
|engagedRestartSnoozeScheduleInDays|Int32|用户可推迟预定重启提醒通知的天数，有效范围为1到3天|
|engagedRestartTransitionScheduleInDays|Int32|从主动时段之外的计划的自动重启转换为预定重启（需要用户进行计划，有效范围为0到30天）的天数|
|deadlineForFeatureUpdatesInDays|Int32|自动安装具有介于2到30天的有效范围的功能更新之前的天数|
|deadlineForQualityUpdatesInDays|Int32|自动安装质量更新前的天数介于2到30天的有效范围内|
|deadlineGracePeriodInDays|Int32|使用有效范围（范围为0到7天）自动重新启动之前的最后期限的天数|
|postponeRebootUntilAfterDeadline|Boolean|指定设备是否应等到最后期限结束后才能在 active 时段之外进行重新启动|
|autoRestartNotificationDismissal|[autoRestartNotificationDismissalMethod](../resources/intune-deviceconfig-autorestartnotificationdismissalmethod.md)|指定用于消除 "需要自动重新启动" 通知的方法。 可取值为：`notConfigured`、`automatic`、`user`。|
|scheduleRestartWarningInHours|Int32|指定自动重新启动警告提醒通知的期限。 受支持的值：2、4、8、12或 24 (小时) 。|
|scheduleImminentRestartWarningInMinutes|Int32|指定自动重启即将发生的警告通知的期限。 支持的值：15、30或 60 (分钟) 。|
|userPauseAccess|[启用](../resources/intune-shared-enablement.md)|指定是否允许最终用户访问暂停软件更新。 可取值为：`notConfigured`、`enabled`、`disabled`。|
|userWindowsUpdateScanAccess|[启用](../resources/intune-shared-enablement.md)|指定是否禁用用户对扫描 Windows 更新的访问权限。 可取值为：`notConfigured`、`enabled`、`disabled`。|
|updateNotificationLevel|[windowsUpdateNotificationDisplayOption](../resources/intune-deviceconfig-windowsupdatenotificationdisplayoption.md)|指定用户看到的 Windows 更新通知的具体内容。 可取值为：`notConfigured`、`defaultNotifications`、`restartWarningsOnly`、`disableAllNotifications`。|

## <a name="relationships"></a>关系
|关系|类型|说明|
|:---|:---|:---|
|groupAssignments|[deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md) 集合|设备配置文件的组分配列表。 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|assignments|[deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) 集合|设备配置文件的分配列表。 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|deviceStatuses|[deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md) 集合|按设备的设备配置安装状态。 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|userStatuses|[deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md) 集合|按用户的设备配置安装状态。 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|deviceStatusOverview|[deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md)|设备配置设备状态概述 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|userStatusOverview|[deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md)|设备配置用户状态概述 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|deviceSettingStateSummaries|[settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) 集合|设备配置设置状态设备摘要 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|deviceUpdateStates|[windowsUpdateState](../resources/intune-shared-windowsupdatestate.md) 集合|Windows update for business configuration 设备状态。|

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsUpdateForBusinessConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsUpdateForBusinessConfiguration",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "roleScopeTagIds": [
    "String"
  ],
  "supportsScopeTags": true,
  "deviceManagementApplicabilityRuleOsEdition": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleOsEdition",
    "osEditionTypes": [
      "String"
    ],
    "name": "String",
    "ruleType": "String"
  },
  "deviceManagementApplicabilityRuleOsVersion": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleOsVersion",
    "minOSVersion": "String",
    "maxOSVersion": "String",
    "name": "String",
    "ruleType": "String"
  },
  "deviceManagementApplicabilityRuleDeviceMode": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleDeviceMode",
    "deviceMode": "String",
    "name": "String",
    "ruleType": "String"
  },
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "version": 1024,
  "deliveryOptimizationMode": "String",
  "prereleaseFeatures": "String",
  "automaticUpdateMode": "String",
  "microsoftUpdateServiceAllowed": true,
  "driversExcluded": true,
  "installationSchedule": {
    "@odata.type": "microsoft.graph.windowsUpdateScheduledInstall",
    "scheduledInstallDay": "String",
    "scheduledInstallTime": "String (time of day)"
  },
  "qualityUpdatesDeferralPeriodInDays": 1024,
  "featureUpdatesDeferralPeriodInDays": 1024,
  "qualityUpdatesPaused": true,
  "featureUpdatesPaused": true,
  "qualityUpdatesPauseExpiryDateTime": "String (timestamp)",
  "featureUpdatesPauseExpiryDateTime": "String (timestamp)",
  "businessReadyUpdatesOnly": "String",
  "skipChecksBeforeRestart": true,
  "updateWeeks": "String",
  "qualityUpdatesPauseStartDate": "String (Date)",
  "featureUpdatesPauseStartDate": "String (Date)",
  "featureUpdatesRollbackWindowInDays": 1024,
  "qualityUpdatesWillBeRolledBack": true,
  "featureUpdatesWillBeRolledBack": true,
  "qualityUpdatesRollbackStartDateTime": "String (timestamp)",
  "featureUpdatesRollbackStartDateTime": "String (timestamp)",
  "engagedRestartDeadlineInDays": 1024,
  "engagedRestartSnoozeScheduleInDays": 1024,
  "engagedRestartTransitionScheduleInDays": 1024,
  "deadlineForFeatureUpdatesInDays": 1024,
  "deadlineForQualityUpdatesInDays": 1024,
  "deadlineGracePeriodInDays": 1024,
  "postponeRebootUntilAfterDeadline": true,
  "autoRestartNotificationDismissal": "String",
  "scheduleRestartWarningInHours": 1024,
  "scheduleImminentRestartWarningInMinutes": 1024,
  "userPauseAccess": "String",
  "userWindowsUpdateScanAccess": "String",
  "updateNotificationLevel": "String"
}
```




