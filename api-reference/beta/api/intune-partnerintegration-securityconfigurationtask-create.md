---
title: 创建 securityConfigurationTask
description: 创建新的 securityConfigurationTask 对象。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: apiPageType
ms.openlocfilehash: d3e0a0cbe66d3cdebdff6297dae192cad4abd787
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49274542"
---
# <a name="create-securityconfigurationtask"></a>创建 securityConfigurationTask

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

创建新的 [securityConfigurationTask](../resources/intune-partnerintegration-securityconfigurationtask.md) 对象。

## <a name="prerequisites"></a>先决条件
要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。

|权限类型|权限（从最高特权到最低特权）|
|:---|:---|
|委派（工作或学校帐户）|DeviceManagementApps.ReadWrite.All|
|委派（个人 Microsoft 帐户）|不支持。|
|应用程序|DeviceManagementApps.ReadWrite.All|

## <a name="http-request"></a>HTTP 请求
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/deviceAppManagementTasks
```

## <a name="request-headers"></a>请求标头
|标头|值|
|:---|:---|
|Authorization|Bearer &lt;token&gt;。必需。|
|接受|application/json|

## <a name="request-body"></a>请求正文
在请求正文中，提供 securityConfigurationTask 对象的 JSON 表示形式。

下表显示创建 securityConfigurationTask 时所需的属性。

|属性|类型|说明|
|:---|:---|:---|
|id|字符串|实体键。 继承自 [deviceAppManagementTask](../resources/intune-partnerintegration-deviceappmanagementtask.md)|
|displayName|字符串|名称。 继承自 [deviceAppManagementTask](../resources/intune-partnerintegration-deviceappmanagementtask.md)|
|description|字符串|说明。 继承自 [deviceAppManagementTask](../resources/intune-partnerintegration-deviceappmanagementtask.md)|
|createdDateTime|DateTimeOffset|创建日期。 继承自 [deviceAppManagementTask](../resources/intune-partnerintegration-deviceappmanagementtask.md)|
|dueDateTime|DateTimeOffset|到期日期。 继承自 [deviceAppManagementTask](../resources/intune-partnerintegration-deviceappmanagementtask.md)|
|“类别”|[deviceAppManagementTaskCategory](../resources/intune-partnerintegration-deviceappmanagementtaskcategory.md)|类别。 继承自 [deviceAppManagementTask](../resources/intune-partnerintegration-deviceappmanagementtask.md)。 可取值为：`unknown`、`advancedThreatProtection`。|
|priority|[deviceAppManagementTaskPriority](../resources/intune-partnerintegration-deviceappmanagementtaskpriority.md)|优先级。 继承自 [deviceAppManagementTask](../resources/intune-partnerintegration-deviceappmanagementtask.md)。 可取值为：`none`、`high`、`low`。|
|Creator|字符串|创建者的电子邮件地址。 继承自 [deviceAppManagementTask](../resources/intune-partnerintegration-deviceappmanagementtask.md)|
|creatorNotes|字符串|来自创建者的注释。 继承自 [deviceAppManagementTask](../resources/intune-partnerintegration-deviceappmanagementtask.md)|
|assignedTo|String|将此任务分配到的管理员的姓名或电子邮件。 继承自 [deviceAppManagementTask](../resources/intune-partnerintegration-deviceappmanagementtask.md)|
|status|[deviceAppManagementTaskStatus](../resources/intune-partnerintegration-deviceappmanagementtaskstatus.md)|状态。 继承自 [deviceAppManagementTask](../resources/intune-partnerintegration-deviceappmanagementtask.md)。 可取值为：`unknown`、`pending`、`active`、`completed`、`rejected`。|
|endpointSecurityPolicy|[endpointSecurityConfigurationType](../resources/intune-partnerintegration-endpointsecurityconfigurationtype.md)|终结点安全策略类型。 可取值为：`unknown`、`antivirus`、`diskEncryption`、`firewall`、`endpointDetectionAndResponse`、`attackSurfaceReduction` 或 `accountProtection`。|
|applicablePlatform|[endpointSecurityConfigurationApplicablePlatform](../resources/intune-partnerintegration-endpointsecurityconfigurationapplicableplatform.md)|适用的平台。 可取值为：`unknown`、`macOS`、`windows10AndLater`、`windows10AndWindowsServer`。|
|endpointSecurityPolicyProfile|[endpointSecurityConfigurationProfileType](../resources/intune-partnerintegration-endpointsecurityconfigurationprofiletype.md)|终结点安全策略配置文件。 可能的值为：、、、、、、、、、、、、、、 `unknown` `antivirus` `windowsSecurity` `bitLocker` `fileVault` `firewall` `firewallRules` `endpointDetectionAndResponse` `deviceControl` `appAndBrowserIsolation` `exploitProtection` `webProtection` `applicationControl` `attackSurfaceReductionRules` `accountProtection` 。|
|insights|字符串|有关缓解措施的信息。|
|managedDeviceCount|Int32|易受攻击设备的数量。|
|intendedSettings|[keyValuePair](../resources/intune-shared-keyvaluepair.md) 集合|预期的设置及其值。|



## <a name="response"></a>响应
如果成功，此方法 `201 Created` 在响应正文中返回响应代码和 [securityConfigurationTask](../resources/intune-partnerintegration-securityconfigurationtask.md) 对象。

## <a name="example"></a>示例

### <a name="request"></a>请求
下面是一个请求示例。
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/deviceAppManagementTasks
Content-type: application/json
Content-length: 746

{
  "@odata.type": "#microsoft.graph.securityConfigurationTask",
  "displayName": "Display Name value",
  "description": "Description value",
  "dueDateTime": "2017-01-01T00:02:18.1994089-08:00",
  "category": "advancedThreatProtection",
  "priority": "high",
  "creator": "Creator value",
  "creatorNotes": "Creator Notes value",
  "assignedTo": "Assigned To value",
  "status": "pending",
  "endpointSecurityPolicy": "antivirus",
  "applicablePlatform": "macOS",
  "endpointSecurityPolicyProfile": "antivirus",
  "insights": "Insights value",
  "managedDeviceCount": 2,
  "intendedSettings": [
    {
      "@odata.type": "microsoft.graph.keyValuePair",
      "name": "Name value",
      "value": "Value value"
    }
  ]
}
```

### <a name="response"></a>响应
下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 854

{
  "@odata.type": "#microsoft.graph.securityConfigurationTask",
  "id": "5d630f12-0f12-5d63-120f-635d120f635d",
  "displayName": "Display Name value",
  "description": "Description value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "dueDateTime": "2017-01-01T00:02:18.1994089-08:00",
  "category": "advancedThreatProtection",
  "priority": "high",
  "creator": "Creator value",
  "creatorNotes": "Creator Notes value",
  "assignedTo": "Assigned To value",
  "status": "pending",
  "endpointSecurityPolicy": "antivirus",
  "applicablePlatform": "macOS",
  "endpointSecurityPolicyProfile": "antivirus",
  "insights": "Insights value",
  "managedDeviceCount": 2,
  "intendedSettings": [
    {
      "@odata.type": "microsoft.graph.keyValuePair",
      "name": "Name value",
      "value": "Value value"
    }
  ]
}
```




