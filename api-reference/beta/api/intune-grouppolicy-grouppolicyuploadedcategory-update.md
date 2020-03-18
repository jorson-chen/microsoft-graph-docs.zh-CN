---
title: 更新 groupPolicyUploadedCategory
description: 更新 groupPolicyUploadedCategory 对象的属性。
author: davidmu1
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 148c698c6bbc466fc4aef10bb62b09f61386f362
ms.sourcegitcommit: b38fd4c8c734243f6f82448045a1f6bf63311ec9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "42803769"
---
# <a name="update-grouppolicyuploadedcategory"></a>更新 groupPolicyUploadedCategory

> **重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

更新[groupPolicyUploadedCategory](../resources/intune-grouppolicy-grouppolicyuploadedcategory.md)对象的属性。

## <a name="prerequisites"></a>先决条件
要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。

|权限类型|权限（从最高特权到最低特权）|
|:---|:---|
|委派（工作或学校帐户）|DeviceManagementServiceConfig.ReadWrite.All|
|委派（个人 Microsoft 帐户）|不支持。|
|应用程序|DeviceManagementServiceConfig.ReadWrite.All|

## <a name="http-request"></a>HTTP 请求
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/groupPolicyCategories/{groupPolicyCategoryId}
PATCH /deviceManagement/groupPolicyConfigurations/{groupPolicyConfigurationId}/definitionValues/{groupPolicyDefinitionValueId}/presentationValues/{groupPolicyPresentationValueId}/presentation/definition/category
PATCH /deviceManagement/groupPolicyConfigurations/{groupPolicyConfigurationId}/definitionValues/{groupPolicyDefinitionValueId}/presentationValues/{groupPolicyPresentationValueId}/presentation/definition/category/parent
PATCH /deviceManagement/groupPolicyConfigurations/{groupPolicyConfigurationId}/definitionValues/{groupPolicyDefinitionValueId}/presentationValues/{groupPolicyPresentationValueId}/presentation/definition/category/children/{groupPolicyCategoryId}
```

## <a name="request-headers"></a>请求标头
|标头|值|
|:---|:---|
|Authorization|Bearer &lt;token&gt;。必需。|
|接受|application/json|

## <a name="request-body"></a>请求正文
在请求正文中，提供[groupPolicyUploadedCategory](../resources/intune-grouppolicy-grouppolicyuploadedcategory.md)对象的 JSON 表示形式。

下表显示创建[groupPolicyUploadedCategory](../resources/intune-grouppolicy-grouppolicyuploadedcategory.md)时所需的属性。

|属性|类型|说明|
|:---|:---|:---|
|displayName|String|从[GroupPolicyCategory](../resources/intune-grouppolicy-grouppolicycategory.md)继承的类别的显示名称的字符串 id|
|isRoot|布尔值|定义类别是否是从[GroupPolicyCategory](../resources/intune-grouppolicy-grouppolicycategory.md)继承的根类别|
|id|String|实体的键。 继承自[groupPolicyCategory](../resources/intune-grouppolicy-grouppolicycategory.md)|
|lastModifiedDateTime|DateTimeOffset|上次修改实体的日期和时间。 继承自[groupPolicyCategory](../resources/intune-grouppolicy-grouppolicycategory.md)|



## <a name="response"></a>响应
如果成功，此方法在响应`200 OK`正文中返回响应代码和更新的[groupPolicyUploadedCategory](../resources/intune-grouppolicy-grouppolicyuploadedcategory.md)对象。

## <a name="example"></a>示例

### <a name="request"></a>请求
下面是一个请求示例。
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/groupPolicyCategories/{groupPolicyCategoryId}
Content-type: application/json
Content-length: 128

{
  "@odata.type": "#microsoft.graph.groupPolicyUploadedCategory",
  "displayName": "Display Name value",
  "isRoot": true
}
```

### <a name="response"></a>响应
下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 241

{
  "@odata.type": "#microsoft.graph.groupPolicyUploadedCategory",
  "displayName": "Display Name value",
  "isRoot": true,
  "id": "7e373e80-3e80-7e37-803e-377e803e377e",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00"
}
```



