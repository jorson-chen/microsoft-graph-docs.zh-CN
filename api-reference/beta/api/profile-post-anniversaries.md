---
title: 创建 personAnniversary
description: 使用此 API 创建新的 personAnniversary。
localization_priority: Normal
author: kevinbellinger
ms.prod: people
doc_type: apiPageType
ms.openlocfilehash: e6e73919913f710bee6721ec1710847cc742ba4d
ms.sourcegitcommit: 62507617292d5ad8598e83a8a253c986d9bac787
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/02/2019
ms.locfileid: "37937719"
---
# <a name="create-personanniversary"></a>创建 personAnniversary

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

使用此 API 在用户的[配置文件](../resources/profile.md)中创建新的[personAnniversary](../resources/personanniversary.md)对象。

## <a name="permissions"></a>权限

要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。

| 权限类型                        | 权限（从最低特权到最高特权） |
|:---------------------------------------|:--------------------------------------------|
| 委派（工作或学校帐户）     | 所有用户读写。          |
| 委派（个人 Microsoft 帐户） | 所有用户读写。          |
| 应用程序                            | User.ReadWrite.All                          |

## <a name="http-request"></a>HTTP 请求

<!-- { "blockType": "ignored" } -->

```http
POST /me/profile/anniversaries 
```

## <a name="request-headers"></a>请求标头

| 名称      |说明|
|:---------------|:----------|
| Authorization  | Bearer {token}。必需。   |
| Content-Type   | application/json. Required. |

## <a name="request-body"></a>请求正文

在请求正文中，提供[personAnniversary](../resources/personanniversary.md)对象的 JSON 表示形式。

## <a name="response"></a>响应

如果成功，此方法在`201, Created`响应正文中返回响应代码和新的[personAnniversary](../resources/personanniversary.md)对象。

## <a name="examples"></a>示例

### <a name="request"></a>请求

下面展示了示例请求。
<!-- {
  "blockType": "request",
  "name": "create_personanniversary_from_profile"
}-->

```http
POST https://graph.microsoft.com/beta/me/profile/anniversaries
Content-type: application/json

{
  "type": "type-value",
  "date": "datetime-value"
}
```

### <a name="response"></a>响应

下面展示了示例响应。

> **注意：** 为了提高可读性，可能缩短了此处显示的响应对象。所有属性都将通过实际调用返回。

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.personAnniversary"
} -->

```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "type": "type-value",
  "date": "datetime-value"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create personAnniversary",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->