---
title: authenticationMethodsRoot： usersRegisteredByMethod
description: 获取每个身份验证方法注册的用户数。
author: danielwood95
localization_priority: Normal
ms.prod: reports
doc_type: apiPageType
ms.openlocfilehash: 684603da36a4d5dcf08fc575042b49055e581e7b
ms.sourcegitcommit: 90f08b197a9b13593143618c105a4049c07811b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2021
ms.locfileid: "50052555"
---
# <a name="authenticationmethodsroot-usersregisteredbymethod"></a>authenticationMethodsRoot： usersRegisteredByMethod
命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

获取每个身份验证方法注册的用户数。

## <a name="permissions"></a>权限
要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。

|权限类型|权限（从最低特权到最高特权）|
|:---|:---|
|委派（工作或学校帐户）|Reports.Read.All|
|委派（个人 Microsoft 帐户）|不支持。|
|应用程序|不支持。|

若要访问 API，需要以下 [角色之](/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles) 一：

* 报表阅读人员
* 安全读者
* 安全管理员
* 全局读取者
* 全局管理员

## <a name="http-request"></a>HTTP 请求

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports/authenticationMethods/usersRegisteredByMethod
```

## <a name="function-parameters"></a>函数参数
下表显示了可用于此函数的参数。

|参数|类型|说明|
|:---|:---|:---|
|includedUserTypes|includedUserTypes|用户类型。 可取值为：`all`、`member`、`guest`。|
|includedUserRoles|includedUserRoles|用户角色类型。 可取值为：`all`、`privilegedAdmin`、`admin`、`user`。|

该值 `privilegedAdmin` 由以下特权管理员角色组成：

* 全局管理员
* 安全管理员
* 条件访问管理员
* Exchange 管理员
* SharePoint 管理员
* 支持管理员
* 帐务管理员
* 用户管理员
* 身份验证管理员

该值 `admin` 包括所有 Azure AD 管理员角色。 

## <a name="request-headers"></a>请求标头
|名称|说明|
|:---|:---|
|Authorization|Bearer {token}。必需。|

## <a name="request-body"></a>请求正文
请勿提供此方法的请求正文。

## <a name="response"></a>响应

如果成功，此函数在响应正文中返回响应代码和 `200 OK` [userRegistrationMethodSummary。](../resources/userregistrationmethodsummary.md)

## <a name="examples"></a>示例

### <a name="request"></a>请求
<!-- {
  "blockType": "request",
  "name": "authenticationmethodsroot_usersregisteredbymethod"
}
-->
``` http
GET https://graph.microsoft.com/beta/reports/authenticationMethods/usersRegisteredByMethod(includedUserTypes='all',includedUserRoles='all')
```


### <a name="response"></a>响应
**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.userRegistrationFeatureSummary"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.type": "#microsoft.graph.userRegistrationMethodSummary",
    "userTypes": "all",
    "userRoles": "all",
    "userRegistrationMethodCounts": [{
            "authenticationMethod": "password",
            "userCount": 12209
        },
        {
            "authenticationMethod": "windowsHelloForBusiness",
            "userCount": 223
        },
        {
            "authenticationMethod": "mobilePhone",
            "userCount": 4234
        }
    ]
}
```
