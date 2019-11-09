---
title: 更新应用程序
description: 更新 application 对象的属性。
author: davidmu1
localization_priority: Normal
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: 59c905496ffcafc3ccc89eac947d6a30765b1285
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/05/2019
ms.locfileid: "37995963"
---
# <a name="update-application"></a>更新应用程序

更新[application](../resources/application.md)对象的属性。
## <a name="permissions"></a>Permissions
要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。


|权限类型      | 权限（从最低特权到最高特权）              |
|:--------------------|:---------------------------------------------------------|
|委派（工作或学校帐户） |  Directory.AccessAsUser.All    |
|委派（个人 Microsoft 帐户） | 不支持。    |
|应用程序 | Application.ReadWrite.OwnedBy、Application.ReadWrite.All、Directory.Read.All |

## <a name="http-request"></a>HTTP 请求
<!-- { "blockType": "ignored" } -->
```http
PATCH /applications/{id}
```
## <a name="request-headers"></a>请求标头
| 名称       | 说明|
|:-----------|:----------|
| Authorization | Bearer {token}。必需。  |
| Content-type | application/json. Required. |

## <a name="request-body"></a>请求正文
在请求正文中，提供应更新的相关字段的值。 请求正文中不包括的现有属性将保留其以前的值，或根据对其他属性值的更改重新计算。 为了获得最佳性能，请勿加入尚未更改的现有值。

| 属性 | 类型 | 说明 |
|:---------------|:--------|:----------|
| api | [apiApplication](../resources/apiapplication.md) | 指定实现 Web API 的应用程序的设置。 |
| appRoles | [appRole](../resources/approle.md) 集合 | 应用程序可声明的应用程序角色的集合。 这些角色可以分配给用户、组或服务主体。 不可为 null。 |
| displayName | 字符串 | 应用程序的显示名称。 |
| groupMembershipClaims | String | 配置在应用程序需要的用户或 OAuth 2.0 访问令牌中颁发的**组**声明。 要设置此属性，请使用以下有效字符串值之一：<ul><li>`None`</li><li>`SecurityGroup`：针对安全组和 Azure Active Directory （Azure AD）角色</li><li>`All`：该操作可获取登录用户所属的所有安全组、通讯组和 Azure AD 目录角色</li></ul> |
| identifierUris | String collection | URI，用于在应用程序的 Azure AD 租户中标识该应用程序；如果应用程序是多租户的，则用于在已验证的自定义域中标识该应用程序。 有关详细信息，请参阅[应用程序对象和服务主体对象](https://docs.microsoft.com/azure/active-directory/develop/app-objects-and-service-principals)。 需要多值属性筛选器表达式的 *any* 运算符。 不可为 NULL。 |
| info | [informationalUrl](../resources/informationalurl.md) | 应用程序的基本配置文件信息，如应用程序的营销、支持、服务条款和隐私声明 Url。 服务条款和隐私声明通过用户同意体验展示给用户。 有关详细信息，请参阅[为已注册的 AZURE AD 应用添加服务条款和隐私声明](https://docs.microsoft.com/azure/active-directory/develop/howto-add-terms-of-service-privacy-statement)。 |
| isFallbackPublicClient | Boolean | 将回退应用程序类型指定为公共客户端，例如在移动设备上运行的已安装应用程序。 默认值是`false`，这意味着回退应用程序类型是机密客户端，如 web app。 在某些情况下，Azure AD 无法确定客户端应用程序类型（例如，在未指定重定向 URI 的情况下配置它的[ROPC](https://tools.ietf.org/html/rfc6749#section-4.3)流）。 在这些情况下，Azure AD 将根据此属性的值解释应用程序类型。|
| keyCredentials | [keyCredential](../resources/keycredential.md) 集合 | 与应用程序关联的密钥凭据的集合。 不可为 null。 |
| logo | Stream | 应用程序的主徽标。 不可为空。 |
| optionalClaims | optionalClaims | 应用程序开发人员可以在其 Azure AD 应用中配置可选声明，以指定 Microsoft 安全令牌服务发送到他们应用程序的令牌中所需的声明。 有关详细信息，请参阅[可选声明](https://docs.microsoft.com/azure/active-directory/develop/active-directory-optional-claims)。 |
| parentalControlSettings | [parentalControlSettings](../resources/parentalcontrolsettings.md) |指定应用程序的家长控制设置。 |
| passwordCredentials | [passwordCredential](../resources/passwordcredential.md) 集合|与应用程序关联的密码凭据集合。 不可为 Null。|
| publicClient | [publicClientApplication](../resources/publicclientapplication.md) | 指定已安装客户端（如台式设备或移动设备）的设置。 |
| requiredResourceAccess |[requiredResourceAccess](../resources/requiredresourceaccess.md) 集合|指定此应用程序需要访问的资源以及在每个资源下所需的 OAuth 权限范围和应用程序角色集。 这种预配置的所需资源访问权限可驱动同意体验。 不可为 Null。|
| signInAudience | String | 指定当前应用程序支持的 Microsoft 帐户。 支持的值为：<ul><li>`AzureADMyOrg`：在我的组织的 Azure AD 租户（即单租户）中拥有 Microsoft 工作或学校帐户的用户</li><li>`AzureADMultipleOrgs`：在任何组织的 Azure AD 租户（即多租户）中拥有 Microsoft 工作或学校帐户的用户</li> <li>`AzureADandPersonalMicrosoftAccount`：拥有个人 Microsoft 帐户或任意组织的 Azure AD 租户中的工作或学校帐户的用户</li></ul> | `AzureADandPersonalMicrosoftAccount` |
| tags |String 集合| 可用于分类和标识应用程序的自定义字符串。 不可为空。|
| tokenEncryptionKeyId |String|指定 keyCredentials 集合中的公共密钥的 keyId。 配置后，Azure AD 将使用此属性指向的密钥对其发出的所有令牌进行加密。 接收加密令牌的应用程序代码必须先使用匹配的私钥来解密该令牌，然后才能将该令牌用于登录用户。|
| web |[webApplication](../resources/webapplication.md)| 指定 Web 应用程序的设置。 |

## <a name="response"></a>响应

如果成功，此方法将`204 No Content`返回响应代码，并且不会在响应正文中返回任何内容。
## <a name="example"></a>示例
##### <a name="request"></a>请求
下面是一个请求示例。


# <a name="httptabhttp"></a>[HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "update_application"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/applications/{id}
Content-type: application/json
Content-length: 72

{
  "displayName": "New display name"
}
```
# <a name="ctabcsharp"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/update-application-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/update-application-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/update-application-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/update-application-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a>响应

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.application"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Update application",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->