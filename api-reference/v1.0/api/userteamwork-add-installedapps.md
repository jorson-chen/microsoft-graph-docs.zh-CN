---
title: 为用户安装应用
description: 在指定用户的个人范围内安装应用。
author: clearab
doc_type: apiPageType
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 984157470aeceb019e234aa11c3bd693bcc6b9b0
ms.sourcegitcommit: 958b540f118ef3ce64d4d4e96b29264e2b56d703
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/03/2020
ms.locfileid: "49564029"
---
# <a name="install-app-for-user"></a>为用户安装应用

命名空间：microsoft.graph

在指定[用户](../resources/user.md)的个人作用域中安装[应用程序](../resources/teamsapp.md)。

## <a name="permissions"></a>权限

要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。

|权限类型      | 权限（从最低特权到最高特权）              |
|:--------------------|:---------------------------------------------------------|
|委派（工作或学校帐户） | ReadWriteSelfForUser、TeamsAppInstallation、TeamsAppInstallation TeamsAppInstallation |
|委派（个人 Microsoft 帐户） | 不支持。    |
|应用程序 | TeamsAppInstallation、TeamsAppInstallation、all、TeamsAppInstallation、All |

## <a name="http-request"></a>HTTP 请求
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id}/teamwork/installedApps
```

## <a name="request-headers"></a>请求标头

| 标头       | 值 |
|:---------------|:--------|
| Authorization  | Bearer {token}。必需。  |
| Content-type | application/json. Required.|

## <a name="request-body"></a>请求正文

请求正文应包含要添加的现有目录应用程序的 ID。

| 属性   | 类型 |说明|
|:---------------|:--------|:----------|
|teamsApp|String|要添加的应用程序的 ID。|

## <a name="response"></a>响应

如果成功，此方法返回 `201 Created` 响应代码。它不在响应正文中返回任何内容。

## <a name="example"></a>示例

### <a name="request"></a>请求

下面展示了示例请求。

<!-- {
  "blockType": "request",
  "name": "user_add_teamsApp"
}-->

```http
POST https://graph.microsoft.com/v1.0/users/5b649834-7412-4cce-9e69-176e95a394f5/teamwork/installedApps
Content-type: application/json

{
   "teamsApp@odata.bind":"https://graph.microsoft.com/v1.0/appCatalogs/teamsApps/12345678-9abc-def0-123456789a"
}
```

### <a name="response"></a>响应
下面展示了示例响应。

<!-- {
  "blockType": "response",
  "truncated": true
} -->

```http
HTTP/1.1 201 Created
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "User add teamsAppInstallations",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
