---
title: 列出 roleDefinitions
description: 列出 roleDefinition 对象的属性和关系。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: apiPageType
ms.openlocfilehash: bbc40aa61dc262b2cdfe3c73c7ad5f2ac0d90887
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49304698"
---
# <a name="list-roledefinitions"></a>列出 roleDefinitions

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

列出 [roleDefinition](../resources/intune-rbac-roledefinition.md) 对象的属性和关系。

## <a name="prerequisites"></a>先决条件
要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。

|权限类型|权限（从最高特权到最低特权）|
|:---|:---|
|委派（工作或学校帐户）|DeviceManagementRBAC.ReadWrite.All、DeviceManagementRBAC.Read.All|
|委派（个人 Microsoft 帐户）|不支持。|
|应用程序|DeviceManagementRBAC.ReadWrite.All、DeviceManagementRBAC.Read.All|

## <a name="http-request"></a>HTTP 请求
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/roleDefinitions
```

## <a name="request-headers"></a>请求标头
|标头|值|
|:---|:---|
|Authorization|Bearer &lt;token&gt;。必需。|
|接受|application/json|

## <a name="request-body"></a>请求正文
请勿提供此方法的请求正文。

## <a name="response"></a>响应
如果成功，此方法在响应正文中返回 `200 OK` 响应代码和 [roleDefinition](../resources/intune-rbac-roledefinition.md) 对象集合。

## <a name="example"></a>示例

### <a name="request"></a>请求
下面是一个请求示例。
``` http
GET https://graph.microsoft.com/beta/deviceManagement/roleDefinitions
```

### <a name="response"></a>响应
下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1477

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.roleDefinition",
      "id": "70fdcd08-cd08-70fd-08cd-fd7008cdfd70",
      "displayName": "Display Name value",
      "description": "Description value",
      "permissions": [
        {
          "@odata.type": "microsoft.graph.rolePermission",
          "actions": [
            "Actions value"
          ],
          "resourceActions": [
            {
              "@odata.type": "microsoft.graph.resourceAction",
              "allowedResourceActions": [
                "Allowed Resource Actions value"
              ],
              "notAllowedResourceActions": [
                "Not Allowed Resource Actions value"
              ]
            }
          ]
        }
      ],
      "rolePermissions": [
        {
          "@odata.type": "microsoft.graph.rolePermission",
          "actions": [
            "Actions value"
          ],
          "resourceActions": [
            {
              "@odata.type": "microsoft.graph.resourceAction",
              "allowedResourceActions": [
                "Allowed Resource Actions value"
              ],
              "notAllowedResourceActions": [
                "Not Allowed Resource Actions value"
              ]
            }
          ]
        }
      ],
      "isBuiltInRoleDefinition": true,
      "isBuiltIn": true,
      "roleScopeTagIds": [
        "Role Scope Tag Ids value"
      ]
    }
  ]
}
```




