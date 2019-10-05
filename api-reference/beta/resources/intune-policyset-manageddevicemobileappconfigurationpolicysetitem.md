---
title: managedDeviceMobileAppConfigurationPolicySetItem 资源类型
description: 包含用于托管设备移动应用配置 PolicySetItem 的属性的类。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: 60245fb8543f207611be82844d91f6bacfbfab3d
ms.sourcegitcommit: 86903a4730bbd825eabb7f0a1b2429723cc8b1e6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/26/2019
ms.locfileid: "37199965"
---
# <a name="manageddevicemobileappconfigurationpolicysetitem-resource-type"></a>managedDeviceMobileAppConfigurationPolicySetItem 资源类型

> **重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

包含用于托管设备移动应用配置 PolicySetItem 的属性的类。


继承自[policySetItem](../resources/intune-policyset-policysetitem.md)

## <a name="methods"></a>方法
|方法|返回类型|说明|
|:---|:---|:---|
|[列出 managedDeviceMobileAppConfigurationPolicySetItems](../api/intune-policyset-manageddevicemobileappconfigurationpolicysetitem-list.md)|[managedDeviceMobileAppConfigurationPolicySetItem](../resources/intune-policyset-manageddevicemobileappconfigurationpolicysetitem.md)集合|列出[managedDeviceMobileAppConfigurationPolicySetItem](../resources/intune-policyset-manageddevicemobileappconfigurationpolicysetitem.md)对象的属性和关系。|
|[获取 managedDeviceMobileAppConfigurationPolicySetItem](../api/intune-policyset-manageddevicemobileappconfigurationpolicysetitem-get.md)|[managedDeviceMobileAppConfigurationPolicySetItem](../resources/intune-policyset-manageddevicemobileappconfigurationpolicysetitem.md)|读取[managedDeviceMobileAppConfigurationPolicySetItem](../resources/intune-policyset-manageddevicemobileappconfigurationpolicysetitem.md)对象的属性和关系。|
|[创建 managedDeviceMobileAppConfigurationPolicySetItem](../api/intune-policyset-manageddevicemobileappconfigurationpolicysetitem-create.md)|[managedDeviceMobileAppConfigurationPolicySetItem](../resources/intune-policyset-manageddevicemobileappconfigurationpolicysetitem.md)|创建新的[managedDeviceMobileAppConfigurationPolicySetItem](../resources/intune-policyset-manageddevicemobileappconfigurationpolicysetitem.md)对象。|
|[删除 managedDeviceMobileAppConfigurationPolicySetItem](../api/intune-policyset-manageddevicemobileappconfigurationpolicysetitem-delete.md)|无|删除[managedDeviceMobileAppConfigurationPolicySetItem](../resources/intune-policyset-manageddevicemobileappconfigurationpolicysetitem.md)。|
|[更新 managedDeviceMobileAppConfigurationPolicySetItem](../api/intune-policyset-manageddevicemobileappconfigurationpolicysetitem-update.md)|[managedDeviceMobileAppConfigurationPolicySetItem](../resources/intune-policyset-manageddevicemobileappconfigurationpolicysetitem.md)|更新[managedDeviceMobileAppConfigurationPolicySetItem](../resources/intune-policyset-manageddevicemobileappconfigurationpolicysetitem.md)对象的属性。|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|id|String|MobileAppPolicySetItem 的键。 继承自[policySetItem](../resources/intune-policyset-policysetitem.md)|
|createdDateTime|DateTimeOffset|PolicySetItem 的创建时间。 继承自[policySetItem](../resources/intune-policyset-policysetitem.md)|
|lastModifiedDateTime|DateTimeOffset|PolicySetItem 的上次修改时间。 继承自[policySetItem](../resources/intune-policyset-policysetitem.md)|
|payloadId|String|PolicySetItem 的 PayloadId。 继承自[policySetItem](../resources/intune-policyset-policysetitem.md)|
|itemType|String|PolicySetItem 的 policySetType。 继承自[policySetItem](../resources/intune-policyset-policysetitem.md)|
|displayName|String|PolicySetItem 的 DisplayName。 继承自[policySetItem](../resources/intune-policyset-policysetitem.md)|
|status|[policySetStatus](../resources/intune-policyset-policysetstatus.md)|PolicySetItem 的状态。 继承自[policySetItem](../resources/intune-policyset-policysetitem.md)。 可取值为：`unknown`、`validating`、`partialSuccess`、`success`、`error`、`notAssigned`。|
|errorCode|[错误](../resources/intune-policyset-errorcode.md)|错误代码（如果发生）。 继承自[policySetItem](../resources/intune-policyset-policysetitem.md)。 可取值为：`noError`、`unauthorized`、`notFound`、`deleted`。|
|guidedDeploymentTags|String collection|继承自[policySetItem](../resources/intune-policyset-policysetitem.md)的引导部署的标记|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedDeviceMobileAppConfigurationPolicySetItem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationPolicySetItem",
  "id": "String (identifier)",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "payloadId": "String",
  "itemType": "String",
  "displayName": "String",
  "status": "String",
  "errorCode": "String",
  "guidedDeploymentTags": [
    "String"
  ]
}
```


