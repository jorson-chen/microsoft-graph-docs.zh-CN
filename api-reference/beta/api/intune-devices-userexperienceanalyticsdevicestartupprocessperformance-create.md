---
title: 创建 userExperienceAnalyticsDeviceStartupProcessPerformance
description: 创建新的 userExperienceAnalyticsDeviceStartupProcessPerformance 对象。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: apiPageType
ms.openlocfilehash: 1a342229f1b470c15ed501ce8e181749ca4a8271
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49263797"
---
# <a name="create-userexperienceanalyticsdevicestartupprocessperformance"></a>创建 userExperienceAnalyticsDeviceStartupProcessPerformance

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

创建新的 [userExperienceAnalyticsDeviceStartupProcessPerformance](../resources/intune-devices-userexperienceanalyticsdevicestartupprocessperformance.md) 对象。

## <a name="prerequisites"></a>先决条件
要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。

|权限类型|权限（从最高特权到最低特权）|
|:---|:---|
|委派（工作或学校帐户）|DeviceManagementManagedDevices.ReadWrite.All|
|委派（个人 Microsoft 帐户）|不支持。|
|应用程序|DeviceManagementManagedDevices.ReadWrite.All|

## <a name="http-request"></a>HTTP 请求
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/userExperienceAnalyticsDeviceStartupProcessPerformance
```

## <a name="request-headers"></a>请求标头
|标头|值|
|:---|:---|
|Authorization|Bearer &lt;token&gt;。必需。|
|接受|application/json|

## <a name="request-body"></a>请求正文
在请求正文中，提供 userExperienceAnalyticsDeviceStartupProcessPerformance 对象的 JSON 表示形式。

下表显示创建 userExperienceAnalyticsDeviceStartupProcessPerformance 时所需的属性。

|属性|类型|说明|
|:---|:---|:---|
|id|String|User experience analytics 设备启动过程性能的唯一标识符。|
|processName|String|User experience analytics 设备启动过程名称。|
|productName|String|User experience analytics 设备启动过程产品名称。|
|发布者|String|User experience analytics 设备启动过程发布者。|
|deviceCount|Int64|User experience analytics 设备启动过程汇总计数。|
|medianImpactInMs|Int32|User experience analytics 设备启动过程的中间影响（以毫秒为单位）。|
|totalImpactInMs|Int32|User experience analytics 设备启动过程以毫秒为单位的总影响。|



## <a name="response"></a>响应
如果成功，此方法 `201 Created` 在响应正文中返回响应代码和 [userExperienceAnalyticsDeviceStartupProcessPerformance](../resources/intune-devices-userexperienceanalyticsdevicestartupprocessperformance.md) 对象。

## <a name="example"></a>示例

### <a name="request"></a>请求
下面是一个请求示例。
``` http
POST https://graph.microsoft.com/beta/deviceManagement/userExperienceAnalyticsDeviceStartupProcessPerformance
Content-type: application/json
Content-length: 285

{
  "@odata.type": "#microsoft.graph.userExperienceAnalyticsDeviceStartupProcessPerformance",
  "processName": "Process Name value",
  "productName": "Product Name value",
  "publisher": "Publisher value",
  "deviceCount": 11,
  "medianImpactInMs": 0,
  "totalImpactInMs": 15
}
```

### <a name="response"></a>响应
下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 334

{
  "@odata.type": "#microsoft.graph.userExperienceAnalyticsDeviceStartupProcessPerformance",
  "id": "86c4355c-355c-86c4-5c35-c4865c35c486",
  "processName": "Process Name value",
  "productName": "Product Name value",
  "publisher": "Publisher value",
  "deviceCount": 11,
  "medianImpactInMs": 0,
  "totalImpactInMs": 15
}
```




