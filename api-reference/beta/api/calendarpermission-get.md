---
title: 获取 calendarPermission
description: 获取 calendarpermission 对象的属性和关系。
localization_priority: Normal
author: sochowdh
ms.prod: outlook
doc_type: apiPageType
ms.openlocfilehash: 1921c42d5c573f6471e4ae325695fa999182a8d5
ms.sourcegitcommit: 1a3ca53422fc9a8254e78af7c058e876fc9f9ef8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2019
ms.locfileid: "37942636"
---
# <a name="get-calendarpermission"></a>获取 calendarPermission

获取已共享的用户或组日历的指定权限对象。

## <a name="permissions"></a>权限

根据事件所处日历类型和所请求的权限类型（委派型或应用程序），需要下列某一权限来调用此 API。 要了解详细信息（包括如何选择权限），请参阅[权限](/graph/permissions-reference)。

| 日历 | 委派（工作或学校帐户） | 委派（个人 Microsoft 帐户） | 应用程序 |
|:-----|:-----|:-----|:-----|
| 用户日历 | Calendars.Read、Calendars.ReadWrite | Calendars.Read、Calendars.ReadWrite | Calendars.Read、Calendars.ReadWrite |
| 组日历 | Group.Read.All、Group.ReadWrite.All | 不支持。 | 不支持。 |

## <a name="http-request"></a>HTTP 请求

获取用户的主日历的指定权限：
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id}/calendar/calendarPermissions/{id}
```

获取组日历的指定权限：
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/calendar/calendarPermissions/{id}
```

获取包含标识的事件的用户日历的指定权限：
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id}/events/{id}/calendar/calendarPermissions/{id}
```

## <a name="optional-query-parameters"></a>可选的查询参数

此方法支持一些 OData 查询参数来帮助自定义响应。 有关一般信息，请参阅[OData 查询参数](/graph/query-parameters)。

## <a name="request-headers"></a>请求标头

| 名称      |说明|
|:----------|:----------|
| Authorization | 持有者 {token} |

## <a name="request-body"></a>请求正文

请勿提供此方法的请求正文。

## <a name="response"></a>响应

如果成功，此方法在响应`200 OK`正文中返回响应代码和请求的[calendarPermission](../resources/calendarpermission.md)对象。

## <a name="examples"></a>示例

### <a name="request"></a>请求

下面展示了示例请求。
<!-- {
  "blockType": "request",
  "name": "get_calendarpermission"
}-->

```http
GET https://graph.microsoft.com/beta/users/{id}/calendar/calendarPermissions/{id}
```

### <a name="response"></a>响应

下面展示了示例响应。

> **注意：** 为了提高可读性，可能缩短了此处显示的响应对象。所有属性都将通过实际调用返回。

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendarPermission"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "emailAddress": {
    "name": "My Organization",
  },
  "isRemovable": true,
  "isInsideOrganization": true,
  "role": "write",
  "allowedRoles": [
    "none",
    "freeBusyRead",
    "limitedRead",
    "read",
    "write"
  ],
  "id": "RGVmYXVsdA=="
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get calendarPermission",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->