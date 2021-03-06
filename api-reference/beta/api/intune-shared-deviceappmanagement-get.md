---
title: 获取 deviceAppManagement
description: 读取 deviceAppManagement 对象的属性和关系。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: apiPageType
ms.openlocfilehash: b09e8fd6a4bf72973f7fb55d2331785e0a9684be
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49304040"
---
# <a name="get-deviceappmanagement"></a>获取 deviceAppManagement

命名空间：microsoft.graph

> **重要说明：** Microsoft Graph 中的/beta 版本下的 Api 可能会发生变化。 不支持在生产应用程序中使用这些 API。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

读取 [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md) 对象的属性和关系。

## <a name="prerequisites"></a>先决条件

若要调用此 API，必须有以下权限之一。 若要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。  请注意，相应的权限根据工作流的不同而有所不同。

|权限类型|权限（从最高特权到最低特权）|
|:---|:---|
| 委派（工作或学校帐户） | |
| &nbsp;&nbsp;**应用**、**图书**、**加入**、**合作伙伴集成** 或 **策略集** | Devicemanagementapps.readwrite.all、Devicemanagementapps.readwrite.all 和所有 ReadW |
| &nbsp;&nbsp;**设备管理** | DeviceManagementManagedDevices.ReadWrite.All、DeviceManagementManagedDevices.Read.All |
|委派（个人 Microsoft 帐户）|不支持。|
|应用程序| |
| &nbsp;&nbsp;**应用**、**图书**、**加入**、**合作伙伴集成** 或 **策略集** | Devicemanagementapps.readwrite.all、Devicemanagementapps.readwrite.all 和所有 ReadW |
| &nbsp;&nbsp;**设备管理** | DeviceManagementManagedDevices.ReadWrite.All、DeviceManagementManagedDevices.Read.All |

## <a name="http-request"></a>HTTP 请求
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement
```

## <a name="optional-query-parameters"></a>可选的查询参数

此方法支持 [OData 查询参数](https://developer.microsoft.com/graph/docs/concepts/query_parameters) 来帮助自定义响应。

## <a name="request-headers"></a>请求标头

|标头|值|
|:---|:---|
|Authorization|Bearer &lt;token&gt;。必需。|
|接受|application/json|

## <a name="request-body"></a>请求正文

请勿提供此方法的请求正文。

## <a name="response"></a>响应

如果成功，此方法将在响应正文中返回 `200 OK` 响应代码和 [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md) 对象。

## <a name="example"></a>示例

### <a name="request"></a>请求

下面是一个请求示例。

``` http
GET https://graph.microsoft.com/beta/deviceAppManagement
```

### <a name="response"></a>响应

下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 133

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceAppManagement",
    "id": "bbb801a3-01a3-bbb8-a301-b8bba301b8bb"
  }
}
```










