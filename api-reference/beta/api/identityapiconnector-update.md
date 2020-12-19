---
title: 更新 identityApiConnector
description: 更新 identityApiConnector 对象的属性。
author: nickgmicrosoft
localization_priority: Normal
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: e06927b3058f78396d9df6d54e7336ff6ba1b521
ms.sourcegitcommit: 424735f8ab46de76b9d850e10c7d97ffd164f62a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/19/2020
ms.locfileid: "49720148"
---
# <a name="update-identityapiconnector"></a>更新 identityApiConnector

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

更新 [identityApiConnector 对象](../resources/identityapiconnector.md) 的属性。

## <a name="permissions"></a>权限

要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。

| 权限类型                        | 权限（从最高特权到最低特权） |
| :------------------------------------- | :------------------------------------------ |
| 委派（工作或学校帐户）     | APIConnectors.ReadWrite.All |
| 委派（个人 Microsoft 帐户） | 不支持。  |
| 应用程序                            | APIConnectors.ReadWrite.All |

工作或学校帐户需要属于以下角色之一：

* 全局管理员
* 外部标识用户流管理员

## <a name="http-request"></a>HTTP 请求

<!-- {
  "blockType": "ignored"
}
-->

``` http
PATCH /identity/apiConnectors/{identityApiConnectorId}
```

## <a name="request-headers"></a>请求标头
|名称|说明|
|:---|:---|
|Authorization|Bearer {token}。必需。|
|Content-Type|application/json. Required.|

## <a name="request-body"></a>请求正文
在请求正文中，提供 [identityApiConnector](../resources/identityapiconnector.md) 对象的 JSON 表示形式。

下表显示了可以更新 [的 identityApiConnector](../resources/identityapiconnector.md) 的属性。


|属性|类型|说明|
|:---|:---|:---|
|displayName|String| API 连接器的名称。 |
|targetUrl|String| 要调用的 API 终结点的 URL。 |
|authenticationConfiguration|[apiAuthenticationConfigurationBase](../resources/apiauthenticationconfigurationbase.md)|描述用于调用 API 的身份验证配置详细信息的对象。 目前 [仅](../resources/basicauthentication.md) 支持基本身份验证。 apiAuthenticationConfigurationBase 的所有属性必须同时设置，如用户名和密码。|

## <a name="response"></a>响应

如果成功，此方法返回 `204 No Content` 响应代码。

## <a name="examples"></a>示例

### <a name="request"></a>请求

下面展示了示例请求。

<!-- {
  "blockType": "request",
  "name": "update_identityapiconnector"
}
-->

``` http
PATCH https://graph.microsoft.com/beta/identity/apiConnectors/{identityApiConnectorId}
Content-Type: application/json

{
  "displayName": "New Test API",
  "targetUrl": "https://otherapi.com/api/endpoint",
  "authenticationConfiguration": {
    "@odata.type": "microsoft.graph.basicAuthentication",
    "username":"<NEW_USERNAME>", 
    "password":"<NEW_PASSWORD>"
  }
}
```

### <a name="response"></a>响应

下面展示了示例响应。

<!-- {
  "blockType": "response",
}
-->

``` http
HTTP/1.1 204 No Content
```
