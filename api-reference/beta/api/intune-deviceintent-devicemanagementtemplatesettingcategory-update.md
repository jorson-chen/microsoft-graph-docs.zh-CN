---
title: 更新 deviceManagementTemplateSettingCategory
description: 更新 deviceManagementTemplateSettingCategory 对象的属性。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: apiPageType
ms.openlocfilehash: a5b9e9bf33a5dc62219d00644af04e267e1b227a
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49311138"
---
# <a name="update-devicemanagementtemplatesettingcategory"></a>更新 deviceManagementTemplateSettingCategory

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

更新 [deviceManagementTemplateSettingCategory](../resources/intune-deviceintent-devicemanagementtemplatesettingcategory.md) 对象的属性。

## <a name="prerequisites"></a>先决条件
要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。

|权限类型|权限（从最高特权到最低特权）|
|:---|:---|
|委派（工作或学校帐户）|DeviceManagementConfiguration.ReadWrite.All|
|委派（个人 Microsoft 帐户）|不支持。|
|应用程序|DeviceManagementConfiguration.ReadWrite.All|

## <a name="http-request"></a>HTTP 请求
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/templates/{deviceManagementTemplateId}/categories/{deviceManagementTemplateSettingCategoryId}
```

## <a name="request-headers"></a>请求标头
|标头|值|
|:---|:---|
|Authorization|Bearer &lt;token&gt;。必需。|
|接受|application/json|

## <a name="request-body"></a>请求正文
在请求正文中，提供 [deviceManagementTemplateSettingCategory](../resources/intune-deviceintent-devicemanagementtemplatesettingcategory.md) 对象的 JSON 表示形式。

下表显示创建 [deviceManagementTemplateSettingCategory](../resources/intune-deviceintent-devicemanagementtemplatesettingcategory.md)时所需的属性。

|属性|类型|说明|
|:---|:---|:---|
|id|字符串|从[DeviceManagementSettingCategory](../resources/intune-deviceintent-devicemanagementsettingcategory.md)继承的类别 ID|
|displayName|字符串|继承自[deviceManagementSettingCategory](../resources/intune-deviceintent-devicemanagementsettingcategory.md)的类别名称|
|hasRequiredSetting|Boolean|类别包含继承自[deviceManagementSettingCategory](../resources/intune-deviceintent-devicemanagementsettingcategory.md)的顶级 "必需" 设置|



## <a name="response"></a>响应
如果成功，此方法 `200 OK` 在响应正文中返回响应代码和更新的 [deviceManagementTemplateSettingCategory](../resources/intune-deviceintent-devicemanagementtemplatesettingcategory.md) 对象。

## <a name="example"></a>示例

### <a name="request"></a>请求
下面是一个请求示例。
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/templates/{deviceManagementTemplateId}/categories/{deviceManagementTemplateSettingCategoryId}
Content-type: application/json
Content-length: 152

{
  "@odata.type": "#microsoft.graph.deviceManagementTemplateSettingCategory",
  "displayName": "Display Name value",
  "hasRequiredSetting": true
}
```

### <a name="response"></a>响应
下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 201

{
  "@odata.type": "#microsoft.graph.deviceManagementTemplateSettingCategory",
  "id": "cd213562-3562-cd21-6235-21cd623521cd",
  "displayName": "Display Name value",
  "hasRequiredSetting": true
}
```




