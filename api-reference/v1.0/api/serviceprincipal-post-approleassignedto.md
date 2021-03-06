---
title: 向服务主体授予 appRoleAssignment
description: 向服务主体授予应用角色分配。
localization_priority: Priority
doc_type: apiPageType
ms.prod: microsoft-identity-platform
author: sureshja
ms.openlocfilehash: b57c927815e371c79cf27fa4c732e81e0da5e7ba
ms.sourcegitcommit: eacd2a6e46c19dd3cd8519592b1668fabe14d85d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "49873568"
---
# <a name="grant-an-approleassignment-for-a-service-principal"></a>为服务主体授予 appRoleAssignment

命名空间：microsoft.graph


将资源服务主体的应用角色，分配给用户、组或客户端服务主体。

分配给服务主体的应用角色也被称为[应用程序权限](/azure/active-directory/develop/v2-permissions-and-consent#permission-types)。 应用程序权限可以通过应用角色分配直接授予，或通过[协议体验](/azure/active-directory/develop/application-consent-experience)授予。

若要授予应用角色分配，需使用三个标识符：

- `principalId`： **用户** 的 `id`，**组** 或要向其分配应用程序角色的客户端 **servicePrincipal**。
- `resourceId`：已定义应用角色的资源 **servicePrincipal** 的 `id`。
- `appRoleId`： **appRole** 中的 `id`来分配给用户、组或服务主体。

## <a name="permissions"></a>权限

要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。

|权限类型      | 权限（从最低特权到最高特权）              |
|:--------------------|:---------------------------------------------------------|
|委派（工作或学校帐户） | AppRoleAssignment.ReadWrite.All、AccessAsUser.All    |
|委派（个人 Microsoft 帐户） | 不支持。    |
|应用程序 | AppRoleAssignment.ReadWrite.All, |

## <a name="http-request"></a>HTTP 请求

<!-- { "blockType": "ignored" } -->
```http
POST /servicePrincipals/{id}/appRoleAssignedTo
```

## <a name="request-headers"></a>请求标头

| 名称       | 说明|
|:-----------|:----------|
| Authorization | Bearer {token}。必需。  |
| Content-type | application/json. Required. |

## <a name="request-body"></a>请求正文

在请求正文中，提供 [appRoleAssignment](../resources/approleassignment.md) 对象的 JSON 表示形式。

## <a name="response"></a>响应

如果成功，此运营商将在响应正文中返回 `201 Created` 响应代码和 [appRoleAssignment](../resources/approleassignment.md) 对象。

## <a name="examples"></a>示例

### <a name="request"></a>请求

下面是一个请求示例。


# <a name="http"></a>[HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "serviceprincipal_create_approleassignedto"
}-->

```http
POST https://graph.microsoft.com/v1.0/servicePrincipals/{id}/appRoleAssignedTo
Content-Type: application/json
Content-Length: 110

{
  "principalId": "principalId-value",
  "resourceId": "resourceId-value",
  "appRoleId": "appRoleId-value"
}
```
# <a name="c"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/serviceprincipal-create-approleassignedto-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/serviceprincipal-create-approleassignedto-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/serviceprincipal-create-approleassignedto-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/serviceprincipal-create-approleassignedto-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


在此示例中，`{id}` 和 `{resourceId-value}` 是资源服务主体的 `id`，`{principalId}` 是分配的用户、组或客户端服务主体的 `id`。

### <a name="response"></a>响应

下面是一个响应示例。 

> **注意：** 为了提高可读性，可能缩短了此处显示的响应对象。所有属性都将通过实际调用返回。

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.appRoleAssignment"
} -->

```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 253

{
  "id": "id-value",
  "creationTimestamp": "2016-10-19T10:37:00Z",
  "principalType": "principalType-value",
  "principalId": "principalId-value",
  "principalDisplayName": "principalDisplayName-value",
  "resourceId": "resourceId-value",
  "resourceDisplayName": "resourceDisplayName-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Create appRoleAssignment",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
