---
title: macOSWiFiConfiguration 资源类型
description: 通过提供此配置文件中的配置，可以指示 macOS 设备连接到所需的 Wi-Fi 终结点。 通过指定 Wi-Fi 终结点所需的身份验证方法和安全类型，可以为最终用户使 Wi-Fi 连接无缝。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 01c7da7d9441d8f0e296afee40db3c2edc1428d4
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49279736"
---
# <a name="macoswificonfiguration-resource-type"></a>macOSWiFiConfiguration 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

通过提供此配置文件中的配置，可以指示 macOS 设备连接到所需的 Wi-Fi 终结点。 通过指定 Wi-Fi 终结点所需的身份验证方法和安全类型，可以为最终用户使 Wi-Fi 连接无缝。


继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)

## <a name="methods"></a>方法
|方法|返回类型|说明|
|:---|:---|:---|
|[列出 macOSWiFiConfigurations](../api/intune-deviceconfig-macoswificonfiguration-list.md)|[macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md) 集合|列出 [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md) 对象的属性和关系。|
|[获取 macOSWiFiConfiguration](../api/intune-deviceconfig-macoswificonfiguration-get.md)|[macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md)|读取 [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md) 对象的属性和关系。|
|[创建 macOSWiFiConfiguration](../api/intune-deviceconfig-macoswificonfiguration-create.md)|[macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md)|创建新的 [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md) 对象。|
|[删除 macOSWiFiConfiguration](../api/intune-deviceconfig-macoswificonfiguration-delete.md)|无|删除 [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md)。|
|[更新 macOSWiFiConfiguration](../api/intune-deviceconfig-macoswificonfiguration-update.md)|[macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md)|更新 [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md) 对象的属性。|

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
|networkName|字符串|网络名称|
|ssid|字符串|这是广播到所有设备的 Wi-Fi 网络的名称。|
|connectAutomatically|Boolean|当此网络在范围内时自动连接。 将此设置为 true 将跳过用户提示，并自动将设备连接到 Wi-Fi 网络。|
|connectWhenNetworkNameIsHidden|Boolean|网络未广播其名称 (SSID) 时连接。 当设置为 true 时，此配置文件将强制设备连接到不会将其 SSID 广播给所有设备的网络。|
|wiFiSecurityType|[wiFiSecurityType](../resources/intune-deviceconfig-wifisecuritytype.md)|指示 Wi-Fi 终结点是否使用基于 EAP 的安全类型。 可取值为：`open`、`wpaPersonal`、`wpaEnterprise`、`wep`、`wpa2Personal`、`wpa2Enterprise`。|
|proxySettings|[wiFiProxySetting](../resources/intune-deviceconfig-wifiproxysetting.md)|此 Wi-Fi 连接的代理类型。 可取值为：`none`、`manual`、`automatic`。|
|proxyManualAddress|字符串|选择手动配置时代理服务器的 IP 地址或 DNS 主机名。|
|proxyManualPort|Int32|选择手动配置时代理服务器的端口。|
|proxyAutomaticConfigurationUrl|字符串|选择 "自动配置" 时代理服务器的 "自动配置" 脚本的 URL。 此 URL 通常是 PAC (代理自动配置) 文件的位置。|
|preSharedKey|字符串|这是 WPA 个人 Wi-Fi 网络的预共享密钥。|

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

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.macOSWiFiConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.macOSWiFiConfiguration",
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
  "networkName": "String",
  "ssid": "String",
  "connectAutomatically": true,
  "connectWhenNetworkNameIsHidden": true,
  "wiFiSecurityType": "String",
  "proxySettings": "String",
  "proxyManualAddress": "String",
  "proxyManualPort": 1024,
  "proxyAutomaticConfigurationUrl": "String",
  "preSharedKey": "String"
}
```




