---
title: 邮件：取消订阅
description: 代表已登录用户提交电子邮件请求，以从电子邮件通讯组列表中取消订阅。 使用标头中的信息 `List-Unsubscribe` 。
author: svpsiva
localization_priority: Normal
ms.prod: outlook
doc_type: apiPageType
ms.openlocfilehash: d27479b86f7c825768a11a99cd13550749116060
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2020
ms.locfileid: "48970526"
---
# <a name="message-unsubscribe"></a>邮件：取消订阅

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

代表已登录用户提交电子邮件请求，以从电子邮件通讯组列表中取消订阅。 使用标头中的信息 `List-Unsubscribe` 。

邮件发件人可以通过包含一个用于选择收件人的选项，以用户友好的方式使用邮寄列表。可以通过 `List-Unsubscribe` 在 [RFC-2369](https://www.faqs.org/rfcs/rfc2369.html)之后的每封邮件中指定标头来执行此操作。

**注释** 特别是，要使 **取消订阅** 操作正常运行，发件人必须指定 `mailto:` 而不是基于 URL 的取消订阅信息。

设置该标头也会将 [消息](../resources/message.md)实例的 **unsubscribeEnabled** 属性设置为 `true` ，并将 **unsubscribeData** 属性设置为标头数据。

如果邮件的 **unsubscribeEnabled** 属性为，则 `true` 可以使用 " **取消订阅** " 操作从邮件发件人托管的类似的未来邮件中取消订阅用户。

成功的 **取消订阅** 操作将邮件移动到 " **已删除邮件** " 文件夹。 用户从将来的邮件分发中实际排除的用户由发件人管理。

## <a name="permissions"></a>权限
要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。

|权限类型      | 权限（从最低特权到最高特权）              |
|:--------------------|:---------------------------------------------------------|
|委派（工作或学校帐户） | Mail.Send    |
|委派（个人 Microsoft 帐户） | Mail.Send    |
|应用程序 | Mail.Send |

## <a name="http-request"></a>HTTP 请求
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/messages/{id}/unsubscribe
```
## <a name="request-headers"></a>请求标头
| 名称       | 类型 | 说明|
|:---------------|:--------|:----------|
| Authorization  | string  | Bearer {token}。必需。 |

## <a name="request-body"></a>请求正文
请勿提供此方法的请求正文。

## <a name="response"></a>响应

如果成功，此方法返回 `202 Accepted` 响应代码。它不在响应正文中返回任何内容。

## <a name="example"></a>示例
下面是一个如何调用此 API 的示例。
##### <a name="request"></a>请求
下面是一个请求示例。

# <a name="http"></a>[HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "message_unsubscribe"
}-->
```http
POST https://graph.microsoft.com/beta/me/messages/{id}/unsubscribe
```
# <a name="c"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/message-unsubscribe-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/message-unsubscribe-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/message-unsubscribe-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/message-unsubscribe-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a>响应
下面是一个响应示例。 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 202 Accepted
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "message: unsubscribe",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->


