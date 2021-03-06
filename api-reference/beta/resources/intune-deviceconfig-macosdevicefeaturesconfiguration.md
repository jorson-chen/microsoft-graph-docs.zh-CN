---
title: macOSDeviceFeaturesConfiguration 资源类型
description: MacOS 设备功能配置的配置文件。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: f3f2e3fc28f68aaec04e75d8e6d082077d821976
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49268641"
---
# <a name="macosdevicefeaturesconfiguration-resource-type"></a>macOSDeviceFeaturesConfiguration 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

MacOS 设备功能配置的配置文件。


继承自 [appleDeviceFeaturesConfigurationBase](../resources/intune-deviceconfig-appledevicefeaturesconfigurationbase.md)

## <a name="methods"></a>方法
|方法|返回类型|说明|
|:---|:---|:---|
|[列出 macOSDeviceFeaturesConfigurations](../api/intune-deviceconfig-macosdevicefeaturesconfiguration-list.md)|[macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md) 集合|列出 [macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md) 对象的属性和关系。|
|[获取 macOSDeviceFeaturesConfiguration](../api/intune-deviceconfig-macosdevicefeaturesconfiguration-get.md)|[macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md)|读取 [macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md) 对象的属性和关系。|
|[创建 macOSDeviceFeaturesConfiguration](../api/intune-deviceconfig-macosdevicefeaturesconfiguration-create.md)|[macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md)|创建新的 [macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md) 对象。|
|[删除 macOSDeviceFeaturesConfiguration](../api/intune-deviceconfig-macosdevicefeaturesconfiguration-delete.md)|无|删除 [macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md)。|
|[更新 macOSDeviceFeaturesConfiguration](../api/intune-deviceconfig-macosdevicefeaturesconfiguration-update.md)|[macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md)|更新 [macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md) 对象的属性。|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|id|字符串|实体的键。 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|上次修改对象的日期/时间。 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|roleScopeTagIds|String 集合|此实体实例的范围标记列表。 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|supportsScopeTags|Boolean|指示基础设备配置是否支持作用域标记的分配。 如果此值为 false，则不允许分配给 ScopeTags 属性，并且实体将对作用域用户不可见。 这适用于在 Silverlight 中创建的旧版策略，可以通过在 Azure 门户中删除并重新创建策略来解决此事件。 此属性是只读的。 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|deviceManagementApplicabilityRuleOsEdition|[deviceManagementApplicabilityRuleOsEdition](../resources/intune-deviceconfig-devicemanagementapplicabilityruleosedition.md)|适用于此策略的操作系统版本。 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|deviceManagementApplicabilityRuleOsVersion|[deviceManagementApplicabilityRuleOsVersion](../resources/intune-deviceconfig-devicemanagementapplicabilityruleosversion.md)|此策略的操作系统版本适用性规则。 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|deviceManagementApplicabilityRuleDeviceMode|[deviceManagementApplicabilityRuleDeviceMode](../resources/intune-deviceconfig-devicemanagementapplicabilityruledevicemode.md)|此策略的设备模式适用性规则。 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|createdDateTime|DateTimeOffset|创建对象的日期/时间。 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|description|字符串|管理员提供的设备配置的说明。 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|displayName|字符串|管理员提供的设备配置的名称。 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|version|Int32|设备配置的版本。 继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)|
|airPrintDestinations|[airPrintDestination](../resources/intune-deviceconfig-airprintdestination.md) 集合|应始终显示的 AirPrint 打印机的数组。 该集合最多可包含 500 个元素。 继承自 [appleDeviceFeaturesConfigurationBase](../resources/intune-deviceconfig-appledevicefeaturesconfigurationbase.md)|
|autoLaunchItems|[macOSLaunchItem](../resources/intune-deviceconfig-macoslaunchitem.md) 集合|用户登录时要启动的应用程序、文件、文件夹和其他项目的列表。 该集合最多可包含 500 个元素。|
|adminShowHostInfo|Boolean|是否在登录窗口中显示管理员主机信息。|
|loginWindowText|字符串|要在登录窗口中显示的自定义文本。|
|authorizedUsersListHidden|Boolean|是否在登录窗口中显示 "名称" 和 "密码" 对话框或用户列表。|
|authorizedUsersListHideLocalUsers|Boolean|是否在登录窗口的授权用户列表中仅显示网络和系统用户。|
|authorizedUsersListHideMobileAccounts|Boolean|是否在登录窗口上的授权用户列表中隐藏移动用户。|
|authorizedUsersListIncludeNetworkUsers|Boolean|是否在登录窗口上的授权用户列表中显示网络用户。|
|authorizedUsersListHideAdminUsers|Boolean|是否在登录窗口的授权用户列表中隐藏管理员用户。|
|authorizedUsersListShowOtherManagedUsers|Boolean|是否在登录窗口上的授权用户列表中显示其他用户。|
|shutDownDisabled|Boolean|是否在登录窗口中隐藏 "关机" 按钮项。|
|restartDisabled|Boolean|是否在登录窗口中隐藏 "重新启动" 按钮项。|
|sleepDisabled|Boolean|是否在登录窗口中隐藏 "睡眠" 菜单项。|
|consoleAccessDisabled|Boolean|其他用户是否会忽略使用 ">控制台> 特殊用户名。|
|shutDownDisabledWhileLoggedIn|Boolean|用户登录时是否禁用登录窗口上的 "关闭" 菜单项。|
|restartDisabledWhileLoggedIn|Boolean|用户登录时是否禁用登录窗口上的重启菜单项。|
|powerOffDisabledWhileLoggedIn|Boolean|用户登录时登录窗口上的 "断电" 菜单项是否将被禁用。|
|logOutDisabledWhileLoggedIn|Boolean|用户登录时，登录窗口上的注销菜单项是否会被禁用。|
|screenLockDisableImmediate|Boolean|是否禁用即时屏幕锁定功能。|
|associatedDomains|[keyValuePair](../resources/intune-shared-keyvaluepair.md) 集合|弃用：改用 appAssociatedDomains。 获取或设置一个列表，该列表将应用程序映射到其关联的域。 键应与应用程序的 ID 匹配，并且值应为 "服务：域" 形式的字符串，其中 domain 是完全限定的主机名 (例如，webcredentials:example) 。 该集合最多可包含 500 个元素。|
|appAssociatedDomains|[macOSAssociatedDomainsItem](../resources/intune-deviceconfig-macosassociateddomainsitem.md) 集合|获取或设置一个列表，该列表将应用程序映射到其关联的域。 应用程序标识符必须是唯一的。 该集合最多可包含 500 个元素。|
|singleSignOnExtension|[singleSignOnExtension](../resources/intune-deviceconfig-singlesignonextension.md)|获取或设置单一登录扩展配置文件。 弃用：改用 MacOSSingleSignOnExtension。|
|macOSSingleSignOnExtension|[macOSSingleSignOnExtension](../resources/intune-deviceconfig-macossinglesignonextension.md)|获取或设置单一登录扩展配置文件。|
|contentCachingEnabled|Boolean|启用内容缓存，并防止用户对其禁用。|
|contentCachingType|[macOSContentCachingType](../resources/intune-deviceconfig-macoscontentcachingtype.md)|确定允许由 Apple 的内容缓存服务缓存的内容类型。 可取值为：`notConfigured`、`userContentOnly`、`sharedContentOnly`。|
|contentCachingMaxSizeBytes|Int32|将用于内容缓存的磁盘空间的最大字节数。 值 0 (默认值) 指示不受限制的磁盘空间。 |
|contentCachingDataPath|字符串|用于存储缓存内容的目录的路径。 该值必须是 (或 end with) /Library/Application 支持/Apple/AssetCache/Data|
|contentCachingDisableConnectionSharing|Boolean|禁用 internet 连接共享。|
|contentCachingForceConnectionSharing|Boolean|强制 internet 连接共享。 contentCachingDisableConnectionSharing 将覆盖此设置。|
|contentCachingClientPolicy|[macOSContentCachingClientPolicy](../resources/intune-deviceconfig-macoscontentcachingclientpolicy.md)|确定内容缓存服务器将在其中侦听客户端的方法。 可取值为：`notConfigured`、`clientsInLocalNetwork`、`clientsWithSamePublicIpAddress`、`clientsInCustomLocalNetworks`、`clientsInCustomLocalNetworksWithFallback`。|
|contentCachingClientListenRanges|[ipRange](../resources/intune-shared-iprange.md) 集合|自定义 IP 范围的列表将用于侦听客户端。 该集合最多可包含 500 个元素。|
|contentCachingPeerPolicy|[macOSContentCachingPeerPolicy](../resources/intune-deviceconfig-macoscontentcachingpeerpolicy.md)|确定内容缓存对等方和其他缓存的方法。 可取值为：`notConfigured`、`peersInLocalNetwork`、`peersWithSamePublicIpAddress`、`peersInCustomLocalNetworks`。|
|contentCachingPeerListenRanges|[ipRange](../resources/intune-shared-iprange.md) 集合|将使用自定义 IP 范围的列表来侦听对等缓存的内容缓存。 该集合最多可包含 500 个元素。|
|contentCachingPeerFilterRanges|[ipRange](../resources/intune-shared-iprange.md) 集合|自定义 IP 范围的列表中，内容缓存将用于查询来自对等缓存的内容。 该集合最多可包含 500 个元素。|
|contentCachingParentSelectionPolicy|[macOSContentCachingParentSelectionPolicy](../resources/intune-deviceconfig-macoscontentcachingparentselectionpolicy.md)|确定内容缓存服务器将选择父项（如果有多个）的方法。 可取值为：`notConfigured`、`roundRobin`、`firstAvailable`、`urlPathHash`、`random`、`stickyAvailable`。|
|contentCachingParents|String 集合|表示父内容缓存的 IP 地址的列表。|
|contentCachingLogClientIdentities|Boolean|启用对请求缓存内容的客户端的 IP 地址和端口的日志记录。|
|contentCachingPublicRanges|[ipRange](../resources/intune-shared-iprange.md) 集合|Apple 的内容缓存服务应用于将客户端与内容缓存匹配的自定义 IP 范围的列表。 该集合最多可包含 500 个元素。|
|contentCachingBlockDeletion|Boolean|防止内容缓存清除内容以释放磁盘空间以用于其他应用程序。|
|contentCachingShowAlerts|Boolean|将内容缓存警报显示为系统通知。|
|contentCachingKeepAwake|Boolean|如果启用了内容缓存，则阻止设备进入睡眠状态。|
|contentCachingPort|Int32|设置用于内容缓存的端口。 如果值为0，则将选择随机可用端口。 有效值为0至65535|

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
|singleSignOnExtensionPkinitCertificate|[macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md)|用于使用单一登录扩展的身份验证的 PKINIT 证书。|

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.macOSDeviceFeaturesConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.macOSDeviceFeaturesConfiguration",
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
  "airPrintDestinations": [
    {
      "@odata.type": "microsoft.graph.airPrintDestination",
      "ipAddress": "String",
      "resourcePath": "String",
      "port": 1024,
      "forceTls": true
    }
  ],
  "autoLaunchItems": [
    {
      "@odata.type": "microsoft.graph.macOSLaunchItem",
      "path": "String",
      "hide": true
    }
  ],
  "adminShowHostInfo": true,
  "loginWindowText": "String",
  "authorizedUsersListHidden": true,
  "authorizedUsersListHideLocalUsers": true,
  "authorizedUsersListHideMobileAccounts": true,
  "authorizedUsersListIncludeNetworkUsers": true,
  "authorizedUsersListHideAdminUsers": true,
  "authorizedUsersListShowOtherManagedUsers": true,
  "shutDownDisabled": true,
  "restartDisabled": true,
  "sleepDisabled": true,
  "consoleAccessDisabled": true,
  "shutDownDisabledWhileLoggedIn": true,
  "restartDisabledWhileLoggedIn": true,
  "powerOffDisabledWhileLoggedIn": true,
  "logOutDisabledWhileLoggedIn": true,
  "screenLockDisableImmediate": true,
  "associatedDomains": [
    {
      "@odata.type": "microsoft.graph.keyValuePair",
      "name": "String",
      "value": "String"
    }
  ],
  "appAssociatedDomains": [
    {
      "@odata.type": "microsoft.graph.macOSAssociatedDomainsItem",
      "applicationIdentifier": "String",
      "domains": [
        "String"
      ],
      "directDownloadsEnabled": true
    }
  ],
  "singleSignOnExtension": {
    "@odata.type": "microsoft.graph.credentialSingleSignOnExtension",
    "extensionIdentifier": "String",
    "teamIdentifier": "String",
    "domains": [
      "String"
    ],
    "realm": "String",
    "configurations": [
      {
        "@odata.type": "microsoft.graph.keyStringValuePair",
        "key": "String",
        "value": "String"
      }
    ]
  },
  "macOSSingleSignOnExtension": {
    "@odata.type": "microsoft.graph.macOSKerberosSingleSignOnExtension",
    "realm": "String",
    "domains": [
      "String"
    ],
    "blockAutomaticLogin": true,
    "cacheName": "String",
    "credentialBundleIdAccessControlList": [
      "String"
    ],
    "domainRealms": [
      "String"
    ],
    "isDefaultRealm": true,
    "passwordBlockModification": true,
    "passwordExpirationDays": 1024,
    "passwordExpirationNotificationDays": 1024,
    "userPrincipalName": "String",
    "passwordRequireActiveDirectoryComplexity": true,
    "passwordPreviousPasswordBlockCount": 1024,
    "passwordMinimumLength": 1024,
    "passwordMinimumAgeDays": 1024,
    "passwordRequirementsDescription": "String",
    "requireUserPresence": true,
    "activeDirectorySiteCode": "String",
    "passwordEnableLocalSync": true,
    "blockActiveDirectorySiteAutoDiscovery": true,
    "passwordChangeUrl": "String"
  },
  "contentCachingEnabled": true,
  "contentCachingType": "String",
  "contentCachingMaxSizeBytes": 1024,
  "contentCachingDataPath": "String",
  "contentCachingDisableConnectionSharing": true,
  "contentCachingForceConnectionSharing": true,
  "contentCachingClientPolicy": "String",
  "contentCachingClientListenRanges": [
    {
      "@odata.type": "microsoft.graph.iPv6Range",
      "lowerAddress": "String",
      "upperAddress": "String"
    }
  ],
  "contentCachingPeerPolicy": "String",
  "contentCachingPeerListenRanges": [
    {
      "@odata.type": "microsoft.graph.iPv6Range",
      "lowerAddress": "String",
      "upperAddress": "String"
    }
  ],
  "contentCachingPeerFilterRanges": [
    {
      "@odata.type": "microsoft.graph.iPv6Range",
      "lowerAddress": "String",
      "upperAddress": "String"
    }
  ],
  "contentCachingParentSelectionPolicy": "String",
  "contentCachingParents": [
    "String"
  ],
  "contentCachingLogClientIdentities": true,
  "contentCachingPublicRanges": [
    {
      "@odata.type": "microsoft.graph.iPv6Range",
      "lowerAddress": "String",
      "upperAddress": "String"
    }
  ],
  "contentCachingBlockDeletion": true,
  "contentCachingShowAlerts": true,
  "contentCachingKeepAwake": true,
  "contentCachingPort": 1024
}
```




