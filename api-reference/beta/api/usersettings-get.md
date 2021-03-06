---
title: 获取设置
description: 阅读用户和组织设置对象。
author: krbain
localization_priority: Normal
ms.prod: users
doc_type: apiPageType
ms.openlocfilehash: 51a9943be51a2127366d91cbf9e5dc0e0fc4a354
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48022062"
---
# <a name="get-settings"></a>获取设置

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

读取用户和组织 [userSettings](../resources/usersettings.md) 对象。
若要了解如何更新 [userSettings](../resources/usersettings.md) 对象的属性，请参阅[更新用户设置](usersettings-update.md)。

## <a name="permissions"></a>权限

要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。

|权限类型      | 权限（从最低特权到最高特权）              |
|:--------------------|:---------------------------------------------------------|
|委托（工作或学校帐户） | User.Read.All、User.ReadWrite.All    |
|委托（个人 Microsoft 帐户） | 不支持。    |
|应用程序 | User.Read.All,User.ReadWrite.All |

## <a name="http-request"></a>HTTP 请求

```http
GET /me/settings/
```

具有“用户ID”或“userPrincipalName”的请求只能由用户或具有 User.ReadWrite.All 权限的用户访问。 若要了解详细信息，请参阅[权限](/graph/permissions-reference)。

```http
GET /users/{id | userPrincipalName}/settings/
```

## <a name="request-body"></a>请求正文

请勿提供此方法的请求正文。

## <a name="response"></a>响应

如果成功，此方法在响应正文中返回 `200 OK` 响应代码和 [userSettings](../resources/usersettings.md) 对象。

## <a name="example"></a>示例

##### <a name="request"></a>请求

```http
GET https://graph.microsoft.com/beta/me/settings
```

##### <a name="response"></a>响应

下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 72

{
  "contributionToContentDiscoveryAsOrganizationDisabled": false,
  "contributionToContentDiscoveryDisabled": false
}
```


