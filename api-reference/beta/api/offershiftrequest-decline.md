---
title: offerShiftRequest：拒绝
description: 拒绝促销活动请求。
localization_priority: Normal
author: akumar39
ms.prod: microsoft-teams
doc_type: apiPageType
ms.openlocfilehash: 960532d3d278bc01ae89bc74a8624030c96c6d96
ms.sourcegitcommit: ed03445225e98cf0881de08273c36be8d0e576ea
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/07/2020
ms.locfileid: "40952172"
---
# <a name="offershiftrequest-decline"></a>offerShiftRequest：拒绝

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

拒绝[offershiftrequest](../resources/offershiftrequest.md)对象。

## <a name="permissions"></a>Permissions

要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。

| 权限类型                        | 权限（从最低特权到最高特权） |
|:---------------------------------------|:--------------------------------------------|
| 委派（工作或学校帐户）     | Group.ReadWrite.All |
| 委派（个人 Microsoft 帐户） | 不支持。 |
| 应用程序                            | 计划的所有写。 * |

>\***重要说明：** 应用程序权限当前仅在专用预览中，不可供公众使用。

## <a name="http-request"></a>HTTP 请求

<!-- { "blockType": "ignored" } -->

```http
POST /teams/schedule/offerShiftRequests/decline
```

## <a name="request-headers"></a>请求标头

| 名称          | 说明   |
|:--------------|:--------------|
| Authorization | Bearer {token}。必需。 |
| Content-type | application/json. Required. |

## <a name="request-body"></a>请求正文

在请求正文中，提供具有以下参数的 JSON 对象。

| 参数    | 类型        | 描述 |
|:-------------|:------------|:------------|
|message|String|在拒绝时发送自定义邮件。|

## <a name="response"></a>响应

如果成功，此方法返回 `200 OK` 响应代码。它不在响应正文中返回任何内容。

## <a name="examples"></a>示例

### <a name="request"></a>请求

以下示例显示了一个请求。
<!-- {
  "blockType": "request",
  "name": "offershiftrequest_decline"
}-->

```http
POST https://graph.microsoft.com/beta/teams/schedule/offerShiftRequests/decline
Content-type: application/json

{
  "message": "Sorry, you can't offer this shift."
}
```

### <a name="response"></a>响应

以下示例显示了相应的响应。
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->

```http
HTTP/1.1 200 OK
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "offerShiftRequest: decline",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->