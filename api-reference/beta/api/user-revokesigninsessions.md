---
title: 用户： revokeSignInSessions
description: 通过将 **signInSessionsValidFromDateTime** 用户属性重置为当前的日期时间来使向应用 (程序发送的所有用户的刷新令牌（以及用户浏览器) 中的会话 cookie）失效。
localization_priority: Normal
author: krbain
ms.prod: users
doc_type: apiPageType
ms.openlocfilehash: a8d99e33d03d6800d51d814b8397547503a97cba
ms.sourcegitcommit: ea3b1a8b781a347015d9542826c5c0c24d50d35d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/19/2020
ms.locfileid: "49352422"
---
# <a name="user-revokesigninsessions"></a>用户： revokeSignInSessions

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

通过将 **signInSessionsValidFromDateTime** 用户属性重置为当前的日期时间，使用户 (的所有刷新令牌和用户浏览器中的会话 cookie) 。 通常情况下，如果用户的设备丢失或被盗， (由用户或管理员) 执行此操作。 此操作通过要求用户再次登录到之前已同意的所有应用程序（独立于设备）来阻止对组织中的应用程序的数据的访问。

如果应用程序尝试使用无效刷新令牌兑换此用户的委派访问令牌，应用程序将收到错误。 如果发生这种情况，应用程序将需要通过向授权终结点发出请求来获取新的刷新令牌，这将强制用户登录。

>[!NOTE]
>在调用 **revokeSignInSessions** 后，可能会有几分钟的短暂延迟才会被吊销令牌。

## <a name="permissions"></a>权限

要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。

|权限类型                        | 权限（从最低特权到最高特权）              |
|:--------------------------------------|:---------------------------------------------------------|
|委派（工作或学校帐户）     | User.ReadWrite.All、Directory.ReadWrite.All、Directory.AccessAsUser.All |
|委派（个人 Microsoft 帐户） | 不支持。 |
|应用程序                            | User.ReadWrite.All、Directory.ReadWrite.All |

## <a name="http-request"></a>HTTP 请求
<!-- { "blockType": "ignored" } -->
```http
POST /me/revokeSignInSessions
POST /users/{id | userPrincipalName}/revokeSignInSessions
```

## <a name="request-headers"></a>请求标头
| 标头       | 值 |
|:---------------|:--------|
| Authorization  | Bearer {token}。必需。  |
| Content-Type  | application/json  |

## <a name="request-body"></a>请求正文
此操作没有请求内容。

## <a name="response"></a>响应

如果成功，此方法返回 `204 No Content` 响应代码。

>[!NOTE]
>此 API 存在一个[已知问题](/graph/known-issues#revoke-sign-in-sessions-returns-wrong-HTTP-code)。 它返回不同的 HTTP 响应代码。

## <a name="example"></a>示例
以下示例演示如何调用此 API。

##### <a name="request"></a>请求

# <a name="http"></a>[HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "user_revokesigninsessionss"
}-->
```http
POST https://graph.microsoft.com/beta/me/revokeSignInSessions
```
# <a name="c"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/user-revokesigninsessionss-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/user-revokesigninsessionss-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/user-revokesigninsessionss-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/user-revokesigninsessionss-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a>响应
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "user: revokeSignInSessions",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->


