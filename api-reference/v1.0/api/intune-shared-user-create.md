---
title: 创建用户
description: 新建用户对象。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: apiPageType
ms.openlocfilehash: d5e3fe1d4b1b2dcf27de3915ffd49cd38ccb91d0
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48028789"
---
# <a name="create-user"></a>创建用户

命名空间：microsoft.graph

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

创建新的 [user](../resources/intune-shared-user.md) 对象。

## <a name="prerequisites"></a>先决条件
若要调用此 API，必须有以下权限之一。 若要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。  所需的特定权限取决于上下文。

|权限类型|权限（从最高特权到最低特权）|
|:---|:---|
|委派（工作或学校帐户）| _因上下文而异_ |
| &nbsp;&nbsp;设备管理 | DeviceManagementManagedDevices.ReadWrite.All |
| &nbsp;&nbsp;MAM | DeviceManagementApps.ReadWrite.All |
| &nbsp;&nbsp;载入 | DeviceManagementServiceConfig.ReadWrite.All |
| &nbsp;&nbsp;故障排除 | DeviceManagementManagedDevices.ReadWrite.All |
|委派（个人 Microsoft 帐户）|不支持。|
|应用程序|不支持。|

## <a name="http-request"></a>HTTP 请求
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users
```

## <a name="request-headers"></a>请求标头
|标头|值|
|:---|:---|
|Authorization|Bearer &lt;token&gt;。必需。|
|接受|application/json|

## <a name="request-body"></a>请求正文
在请求正文中，提供 user 对象的 JSON 表示形式。

下表显示创建 user 时所需的属性。

|属性|类型|说明|
|:---|:---|:---|
|id|String|用户的唯一标识符。|
|**载入**|
|deviceEnrollmentLimit|Int32|允许用户注册的最大设备数的限制。 允许的值为 5 或 1000。|

请求正文属性支持根据上下文的不同而不同。

## <a name="response"></a>响应
如果成功，此方法会在响应正文中返回 `201 Created` 响应代码和 [user](../resources/intune-shared-user.md) 对象。

## <a name="example"></a>示例

### <a name="request"></a>请求
下面是一个请求示例。

``` http
POST https://graph.microsoft.com/v1.0/users
Content-type: application/json
Content-length: 46

{
  "@odata.type": "#microsoft.graph.user"
}
```

### <a name="response"></a>响应
下面是一个响应示例。 注意：为简洁起见，可能会截断此处显示的响应对象。 从实际调用返回的属性根据上下文的不同而不同。

``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 95

{
  "@odata.type": "#microsoft.graph.user",
  "id": "d36894ae-94ae-d368-ae94-68d3ae9468d3"
}
```









