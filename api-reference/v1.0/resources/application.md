---
title: 应用程序资源类型
description: 表示应用程序。
localization_priority: Priority
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: ed9921939613a06ec6dc41435552d7c42dadb24a
ms.sourcegitcommit: 2f3e7325b5bc1f0cdc12a8acdf34d31cea3b8bdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/07/2019
ms.locfileid: "38023210"
---
# <a name="application-resource-type"></a>应用程序资源类型

表示应用程序。 任何将身份验证外包到 Azure Active Directory (Azure AD) 的应用程序都必须在目录中注册。 应用程序注册涉及告知 Azure AD 有关应用程序的信息，包括其所在的 URL、身份验证后发送回复的 URL、标识应用程序的 URI 等。 有关详细信息，请参阅[在 Azure AD 中注册应用程序的基础知识](https://azure.microsoft.com/documentation/articles/active-directory-authentication-scenarios/#basics-of-registering-an-application-in-azure-ad)。 继承自 [directoryObject](directoryobject.md)。 

## <a name="methods"></a>方法

| 方法 | 返回类型 | Description |
|:---------------|:--------|:----------|
|[列出应用程序](../api/application-list.md) | [application](application.md) 集合 | 检索该组织中应用程序的列表。 |
|[创建应用程序](../api/application-post-applications.md) | [application](application.md) | 创建（注册）新应用程序。|
|[获取应用程序](../api/application-get.md) | [application](application.md) |读取 application 对象的属性和关系。|
|[更新应用程序](../api/application-update.md) | [application](application.md) |更新 application 对象。 |
|[删除应用程序](../api/application-delete.md) | 无 |删除 application 对象。 |
|[列出已删除的应用程序](../api/directory-deleteditems-list.md) | [directoryObject](directoryobject.md) 集合 | 检索最近删除的应用程序的列表。 |
|[获取已删除的应用程序](../api/directory-deleteditems-get.md) | [directoryObject](directoryobject.md) | 检索最近删除的应用程序的属性。 |
|[永久删除应用程序](../api/directory-deleteditems-delete.md) | 无 | 永久删除应用程序。 |
|[还原已删除的应用程序](../api/directory-deleteditems-restore.md) | [directoryObject](directoryobject.md) | 还原最近删除的应用程序。 |
|[添加密码](../api/application-addpassword.md)|[passwordCredential](passwordcredential.md)|向应用程序添加强密码。|
|[删除密码](../api/application-removepassword.md)|[passwordCredential](passwordcredential.md)|从应用程序删除密码。|
| [创建扩展](../api/application-post-extensionproperty.md) | [extensionProperty](extensionProperty.md) | 在应用程序对象上创建扩展属性。 |
| [列出扩展](../api/application-list-extensionproperty.md) | [extensionProperty](extensionProperty.md) 集合 | 列出应用程序对象上的扩展属性。 |
| [删除扩展](../api/application-delete-extensionproperty.md) | 无 | 从应用程序对象删除扩展属性。 |
|[列出所有者](../api/application-list-owners.md) |[directoryObject](directoryobject.md) 集合| 获取所有者对象集合。|
|[添加所有者](../api/application-post-owners.md) |[directoryObject](directoryobject.md)| 通过发布到所有者集合添加所有者。|
|[删除所有者](../api/application-delete-owners.md) |无| 从应用程序删除所有者。|

## <a name="properties"></a>属性

| 属性 | 类型 | Description |
|:---------------|:--------|:----------|
| addIns | [addIn](addin.md) | 定义使用服务可用于调用特定上下文中的应用的自定义行为。 例如，呈现文件流的应用程序可能会为其“FileHandler”功能[设置 addIns 属性](https://docs.microsoft.com/onedrive/developer/file-handlers/?view=odsp-graph-online)。 这将使 Office 365 之类的服务在用户正在处理的文档上下文中调用应用程序。 |
| api | [apiApplication](apiapplication.md) | 指定实现 Web API 的应用程序的设置。 |
| appId | String | Azure AD 分配给应用程序的应用程序唯一标识符。 不可为 Null。 只读。 |
| appRoles | [appRole](approle.md) 集合 | 应用程序可声明的应用程序角色的集合。 这些角色可以分配给用户、组或服务主体。 不可为 Null。 |
| createdDateTime | DateTimeOffset | 注册应用程序的日期和时间。 只读。 |
| deletedDateTime | DateTimeOffset | 删除应用程序的日期和时间。 只读。 |
| displayName | String | 应用程序的显示名称。 |
| groupMembershipClaims | 字符串 | 配置应用程序所需的用户访问令牌或 OAuth 2.0 访问令牌中颁发的 `groups` 声明。 要设置此属性，请使用以下有效字符串值之一：<ul><li>`None`</li><li>`SecurityGroup`：适用于安全组和 Azure AD 角色</li><li>`All`：该操作可获取登录用户所属的所有安全组、通讯组和 Azure AD 目录角色</li></ul> |
| id | String | 应用程序的唯一标识符。 继承自 [directoryObject](directoryobject.md)。 键。 不可为 null。 只读。 |
| identifierUris | String collection | URI，用于在应用程序的 Azure AD 租户中标识该应用程序；如果应用程序是多租户的，则用于在已验证的自定义域中标识该应用程序。 有关详细信息，请参阅[应用程序对象和服务主体对象](https://docs.microsoft.com/azure/active-directory/develop/app-objects-and-service-principals)。 需要多值属性筛选器表达式的 *any* 运算符。 不可为 Null。 |
| info | [informationalUrl](informationalurl.md) | 应用程序的基本配置文件信息，如应用的市场营销、支持、服务条款和隐私声明 URL。 服务条款和隐私声明通过用户同意体验展示给用户。 有关详细信息，请参阅[如何：为已注册的 Azure AD 应用添加服务条款和隐私声明](https://docs.microsoft.com/azure/active-directory/develop/howto-add-terms-of-service-privacy-statement)。 |
| isFallbackPublicClient | Boolean | 将回退应用程序类型指定为公共客户端，例如在移动设备上运行的已安装应用程序。 默认值为 `false`，这意味着，回退应用程序类型为机密客户端，例如 Web 应用。 在某些情况下，Azure AD 无法确定客户端应用程序类型（例如 [ROPC](https://tools.ietf.org/html/rfc6749#section-4.3) 流，其中在不指定重定向 URI 的情况下配置客户端应用类型）。 在这种情况下，Azure AD 将基于此属性的值解释应用程序类型。|
| keyCredentials | [keyCredential](keycredential.md) 集合 | 与应用程序关联的密钥凭据集合，不可为 Null。 |
| logo | Stream | 应用程序的主徽标。 不可为 Null。 |
| optionalClaims | [optionalClaims](optionalclaims.md) | 应用程序开发人员可以在其 Azure AD 应用中配置可选声明，以指定 Microsoft 安全令牌服务发送到他们应用程序的令牌中所需的声明。 有关详细信息，请参阅[向 Azure AD 应用提供可选声明](https://docs.microsoft.com/azure/active-directory/develop/active-directory-optional-claims)。|
| parentalControlSettings | [parentalControlSettings](parentalcontrolsettings.md) |指定应用程序的家长控制设置。 |
| passwordCredentials | [passwordCredential](passwordcredential.md) 集合|与应用程序关联的密码凭据集合。 不可为 Null。|
| publicClient | [publicClientApplication](publicclientapplication.md) | 指定已安装客户端（如台式设备或移动设备）的设置。 |
| publisherDomain | String | 应用程序的已验证发布者域。 只读。|
| requiredResourceAccess |[requiredResourceAccess](requiredresourceaccess.md) 集合|指定此应用程序需要访问的资源以及在每个资源下所需的 OAuth 权限范围和应用程序角色集。 这种预配置的所需资源访问权限可驱动同意体验。 不可为 Null。|
| signInAudience | String | 指定当前应用程序支持的 Microsoft 帐户。 支持的值为：<ul><li>`AzureADMyOrg`：在我的组织的 Azure AD 租户（即单租户）中拥有 Microsoft 工作或学校帐户的用户</li><li>`AzureADMultipleOrgs`：在任何组织的 Azure AD 租户（即多租户）中拥有 Microsoft 工作或学校帐户的用户</li> <li>`AzureADandPersonalMicrosoftAccount`：拥有个人 Microsoft 帐户或任意组织的 Azure AD 租户中的工作或学校帐户的用户</li></ul> |
| tags |String 集合| 可用于分类和标识应用程序的自定义字符串。 不可为空。|
| tokenEncryptionKeyId |字符串|指定 keyCredentials 集合中的公共密钥的 keyId。 配置后，Azure AD 将使用此属性指向的密钥对其发出的所有令牌进行加密。 接收加密令牌的应用程序代码必须先使用匹配的私钥来解密该令牌，然后才能将该令牌用于登录用户。|
| web |[webApplication](webapplication.md)| 指定 Web 应用程序的设置。 |

## <a name="relationships"></a>关系

| 关系 | 类型 | Description |
|:---------------|:--------|:----------|
|createdOnBehalfOf|[directoryObject](directoryobject.md)| 只读。|
|extensionProperties|[extensionProperty](extensionproperty.md) 集合| 只读。可为 Null。|
|owners|[directoryObject](directoryobject.md) 集合|拥有此应用程序的目录对象。 所有者是一组允许修改此对象的非管理员用户。 需要版本 2013-11-08 或更高版本。 只读。 可为 Null。|

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "keyProperty":"id",
  "optionalProperties": [
    "createdOnBehalfOf",
    "owners"
  ],
  "@odata.type": "microsoft.graph.application"
}-->

```json
{
  "addIns": {"@odata.type": "microsoft.graph.addIn"},
  "api": {"@odata.type": "microsoft.graph.apiApplication"},
  "appId": "String",
  "appRoles": [{"@odata.type": "microsoft.graph.appRole"}],
  "createdDateTime": "String (timestamp)",
  "deletedDateTime": "String (timestamp)",
  "displayName": "String",
  "groupMembershipClaims": "String",
  "id": "String (identifier)",
  "identifierUris": ["String"],
  "info": {"@odata.type": "microsoft.graph.informationalUrl"},
  "isFallbackPublicClient": false,
  "keyCredentials": [{"@odata.type": "microsoft.graph.keyCredential"}],
  "logo": "Stream",
  "optionalClaims": {"@odata.type": "microsoft.graph.optionalClaims"},
  "parentalControlSettings": {"@odata.type": "microsoft.graph.parentalControlSettings"},
  "passwordCredentials": [{"@odata.type": "microsoft.graph.passwordCredential"}],
  "publicClient": {"@odata.type": "microsoft.graph.publicClientApplication"},
  "publisherDomain": "String",
  "requiredResourceAccess": [{"@odata.type": "microsoft.graph.requiredResourceAccess"}],
  "signInAudience": "String",
  "tags": ["String"],
  "tokenEncryptionKeyId": "String",
  "web": {"@odata.type": "microsoft.graph.webApplication"}
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "application resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->