---
title: 更新组
description: 更新 [组](../resources/group.md) 对象的属性。
author: yyuank
localization_priority: Normal
ms.prod: groups
doc_type: apiPageType
ms.openlocfilehash: ca2f6815f1206807d680100c04951bec6115ea91
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2020
ms.locfileid: "48953745"
---
# <a name="update-group"></a>更新组

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

更新 [组](../resources/group.md) 对象的属性。

## <a name="permissions"></a>权限

要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。

|权限类型      | 权限（从最低特权到最高特权）              |
|:--------------------|:---------------------------------------------------------|
|委派（工作或学校帐户） | Group.ReadWrite.All、Directory.ReadWrite.All、Directory.AccessAsUser.All  |
|委派（个人 Microsoft 帐户） | 不支持。    |
|应用程序 | Group.ReadWrite.All、Directory.ReadWrite.All |

## <a name="http-request"></a>HTTP 请求

<!-- { "blockType": "ignored" } -->

```http
PATCH /groups/{id}
```

## <a name="request-headers"></a>请求标头

| 名称       | 类型 | 说明|
|:-----------|:------|:----------|
| Authorization  | string  | Bearer {token}。必需。 |

## <a name="request-body"></a>请求正文

在请求正文中，提供应更新的相关字段的值。请求正文中不包括的现有属性将保留其以前的值，或根据对其他属性值的更改重新计算。为了获得最佳性能，不应包括尚未更改的现有值。

| 属性   | 类型 |说明|
|:---------------|:--------|:----------|
|allowExternalSenders|Boolean|默认为 **false** 。指明组织外部人员能否向群组发送邮件。|
|autoSubscribeNewMembers|Boolean|默认为 **false** 。指示添加到组中的新成员是否将自动订阅接收电子邮件通知。|
|description|String|可选的组说明。 |
|displayName|String|组的显示名称。此属性是在创建组时所必需的，并且在更新过程中不能清除。 |
|groupTypes|String collection|指定组类型及其成员身份。  <br><br>如果集合包含 **Unified** ，则该组是 Microsoft 365 组，否则它就是一个安全组。  <br><br>如果该集合包含 **DynamicMembership** ，则该组具有动态成员身份；否则，成员身份是静态的。 |
|mailEnabled|布尔|指定是否为启用邮件的组。 |
|mailNickname|String|组的邮件别名。 创建组时必须指定此属性。 |
|securityEnabled|布尔|指定该组是否为安全组，包括 Microsoft 365 组。 |
|visibility|字符串|指定 Microsoft 365 组的可见性。 可能的值是： **专用** 、 **公用** 或空（解释为 **公用** ）。|

由于 **组** 资源支持 [扩展](/graph/extensibility-overview)，因此您可以使用该 `PATCH` 操作在现有 **组** 实例中的扩展的自定义属性中添加、更新或删除您自己的应用程序特定的数据。


> **注意：**
>
> - 可以更新 **autoSubscribeNewMembers** ，方法是在其自身的 PATCH 请求中指定它，而不包括上表中的其他属性。
> - 只有一部分与核心组管理和管理相关的组 API 才同时支持应用程序权限和委派权限。其他所有的组 API 成员（包括更新 **autoSubscribeNewMembers** ）仅支持委派权限。有关示例，请参阅 [已知问题](/graph/known-issues#group)。
> - 在 Microsoft Exchange Server 中更新启用邮件的安全组的规则可能很复杂；若要了解详细信息，请参阅[在 Exchange Server 中管理启用邮件的安全组](/Exchange/recipients/mail-enabled-security-groups?view=exchserver-2019)。



## <a name="response"></a>响应

如果成功，此方法返回 `204 No Content` 响应代码。

## <a name="examples"></a>示例

### <a name="example-1-update-display-name-and-description-of-a-group"></a>示例1：更新组的显示名称和说明
#### <a name="request"></a>请求

下面展示了示例请求。


# <a name="http"></a>[HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "update_group"
}-->

```http
PATCH https://graph.microsoft.com/beta/groups/{id}
Content-type: application/json
Content-length: 211

{
  "description": "description-value",
  "displayName": "displayName-value",
}
```
# <a name="c"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/update-group-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/update-group-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/update-group-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/update-group-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


#### <a name="response"></a>响应

下面展示了示例响应。
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.group"
} -->

```http
HTTP/1.1 204 No Content
```
### <a name="example-2-apply-sensitivity-label-to-a-microsoft-365-group"></a>示例2：将敏感度标签应用于 Microsoft 365 组
#### <a name="request"></a>请求

您可以使用 [列表标签](informationprotectionpolicy-list-labels.md)获取要应用于 Microsoft 365 组的标签的 ID。 然后，可以使用标签 ID 更新组的 [assignedLabels](../resources/assignedlabel.md) 属性。 

<!-- {
  "blockType": "request",
  "name": "update_group"
}-->

```http
PATCH https://graph.microsoft.com/beta/groups/{id}
Content-type: application/json
Content-length: 211

{
  "assignedLabels": 
  [
    {
        "labelId" : "45cd0c48-c540-4358-ad79-a3658cdc5b88"
    }
  ]
}
```

#### <a name="response"></a>响应

下面展示了示例响应。
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.group"
} -->

```http
HTTP/1.1 204 No Content
```

## <a name="see-also"></a>另请参阅

- [使用扩展向资源添加自定义数据](/graph/extensibility-overview)
- [使用开放扩展向用户添加自定义数据（预览）](/graph/extensibility-open-users)
- [使用架构扩展向组添加自定义数据（预览）](/graph/extensibility-schema-groups)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Update group",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
