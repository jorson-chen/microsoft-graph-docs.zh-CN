---
title: 获取 governanceResource
description: 检索 governanceResource 对象的属性和关系。
localization_priority: Normal
doc_type: apiPageType
ms.prod: microsoft-identity-platform
author: shauliu
ms.openlocfilehash: 58bfab0115fabc835d62bfa02f5da0a96b34a6f3
ms.sourcegitcommit: 21481acf54471ff17ab8043b3a96fcb1d2f863d7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/21/2020
ms.locfileid: "48635073"
---
# <a name="get-governanceresource"></a>获取 governanceResource

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

检索 [governanceResource](../resources/governanceresource.md) 对象的属性和关系。

## <a name="permissions"></a>权限
要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference#privileged-access-permissions)。

### <a name="azure-resources"></a>Azure 资源

| 权限类型 | 权限 |
|:--------------- |:----------- |
| 委派（工作或学校帐户） | PrivilegedAccess.ReadWrite.AzureResources |
| 委派（个人 Microsoft 帐户） | 不支持。 |
| 应用程序 | PrivilegedAccess。 AzureResources |

### <a name="azure-ad"></a>Azure AD

| 权限类型 | 权限 |
|:--------------- |:----------- |
| 委派（工作或学校帐户） | PrivilegedAccess.ReadWrite.AzureAD |
| 委派（个人 Microsoft 帐户） | 不支持。 |
| 应用程序 | PrivilegedAccess。 AzureAD |

### <a name="groups"></a>组

|权限类型 | 权限 |
|:-------------- |:----------- |
| 委派（工作或学校帐户） | PrivilegedAccess AzureADGroups |
| 委派（个人 Microsoft 帐户） | 不支持。 |
| 应用程序 | PrivilegedAccess。 AzureADGroups |

除了权限范围之外，此 API 还要求请求者具有对资源的至少一个角色分配。

## <a name="http-request"></a>HTTP 请求
<!-- { "blockType": "ignored" } -->
```http
GET /privilegedAccess/azureResources/resources/{id}
```

## <a name="optional-query-parameters"></a>可选查询参数
此方法 **仅** 支持  `$select` 和 `$expand` [OData 查询参数](/graph/query-parameters) 来帮助自定义响应。

## <a name="request-headers"></a>请求标头
| 名称      |说明|
|:----------|:----------|
| Authorization  | Bearer {code}|

## <a name="request-body"></a>请求正文
请勿提供此方法的请求正文。
## <a name="response"></a>响应
如果成功，此方法 `200 OK` 在响应正文中返回响应代码和 [governanceResource](../resources/governanceresource.md) 对象。

## <a name="example"></a>示例
本示例演示如何获取订阅 Wingtip 玩具-生产 (e5e7d29d-5465-45ac-885f-4716a5ee74b5) 的详细信息。
<!-- {
  "blockType": "request",
  "name": "get_governanceresource"
}-->
##### <a name="request"></a>请求
```http
GET https://graph.microsoft.com/beta/privilegedAccess/azureResources/resources/e5e7d29d-5465-45ac-885f-4716a5ee74b5
```
##### <a name="response"></a>响应
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.governanceResource"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-Length: 459

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#governanceResources/$entity",
    "id": "e5e7d29d-5465-45ac-885f-4716a5ee74b5",
    "externalId": "/subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d",
    "type": "subscription",
    "displayName": "Wingtip Toys - Prod",
    "status": "Active",
    "registeredDateTime": "2018-04-05T22:30:37.13Z",
    "registeredRoot": "/subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d",    
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Get governanceResource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


