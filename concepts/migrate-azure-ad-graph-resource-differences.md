---
title: Azure AD Graph 与 Microsoft Graph 之间的资源类型差异
description: 介绍了 Azure AD Graph 中的资源与 Microsoft Graph 中的资源之间的差异，以便帮助迁移应用。
author: dkershaw10
localization_priority: Normal
ms.prod: azure-active-directory
ms.openlocfilehash: 7844235b1665c06911b8280f8f95517796b34348
ms.sourcegitcommit: 3fbc2249b307e8d3a9de18f22ef6911094ca272c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/26/2020
ms.locfileid: "48289097"
---
# <a name="resource-type-differences-between-azure-ad-graph-and-microsoft-graph"></a>Azure AD Graph 与 Microsoft Graph 之间的资源类型差异

本文是*第1步：查看*[迁移应用程序](migrate-azure-ad-graph-planning-checklist.md)的 API 差异的过程的一部分。

将应用程序从 Azure AD Graph 迁移到 Microsoft Graph 时，请注意，某些资源的名称和类型不同。  例如，如果您的 Azure AD Graph 应用使用 **tenantInfo** 资源，则需要更新代码以改为引用 [组织](/graph/api/resources/organization?view=graph-rest-1.0) 。

下表重点介绍了 Azure AD Graph 和 Microsoft Graph 资源之间的差异。  它显示具有不同名称或不可用的资源。它还突出显示了 Microsoft Graph beta 版中的可用资源，而不是在 v1.0 版本中。

如果某个资源未 **显示在** 此列表中，则它已在第 [1.0 版](/graph/api/overview?view=graph-rest-1.0) Microsoft Graph 中可用，与 Azure AD Graph 中的名称相同。

> **注意**： Azure AD Graph 中的资源类型名称是 pascal 大小写形式的，而在 Microsoft Graph 中，它们的大小写混合。

|Azure AD Graph <br> (1.6) 资源 |Microsoft Graph<br>resource|备注|
|---|---|---|
| [CertificateAuthorityInformation](/previous-versions/azure/ad/graph/api/entity-and-complex-type-reference) | beta &nbsp; - &nbsp; [certificateAuthority](/graph/api/resources/certificateauthority?view=graph-rest-beta)<br>v1.0 &nbsp; - &nbsp; [certificateAuthority](/graph/api/resources/certificateauthority?view=graph-rest-1.0) | |
| [联系人](/previous-versions/azure/ad/graph/api/entity-and-complex-type-reference) | beta &nbsp; - &nbsp; [orgContact](/graph/api/resources/orgContact?view=graph-rest-beta)<br>v1.0 &nbsp; - &nbsp; [orgContact](/graph/api/resources/orgContact?view=graph-rest-1.0) | |
| [DirectoryLinkChange](/previous-versions/azure/ad/graph/api/entity-and-complex-type-reference) | beta &nbsp; - &nbsp; _新 &nbsp; 方法_ <br>1.0 版 &nbsp; - &nbsp; _新 &nbsp; 方法_ | Delta 查询支持具有不需要此资源的机制的关系更改检测。 请参阅 [AZURE AD Graph 和 Microsoft Graph 之间的功能差异](migrate-azure-ad-graph-feature-differences.md)。 |
| [OAuth2Permission](/previous-versions/azure/ad/graph/api/entity-and-complex-type-reference) | beta &nbsp; - &nbsp; [permissionScope](/graph/api/resources/permissionScope?view=graph-rest-beta) <br> v1.0 &nbsp; - &nbsp; [permissionScope](/graph/api/resources/permissionScope?view=graph-rest-1.0) ||
 [策略](/previous-versions/azure/ad/graph/api/entity-and-complex-type-reference) | beta &nbsp; - &nbsp; [策略](/graph/api/resources/policy-overview?view=graph-rest-beta) <br> 1.0 版 &nbsp; - &nbsp; [策略](/graph/api/resources/policy-overview?view=graph-rest-1.0)| 每种类型的策略在 Microsoft Graph 中的 **策略** URL 路径段下都有一个唯一的类型名称和结构。 在 Azure AD Graph 中，这是一种策略类型。 例如，对于 Azure AD Graph，您将使用 **策略** 资源，并将 **type** 属性设置为 `TokenIssuancePolicy` ，而在 Microsoft Graph 中，这就是 **tokenIssuancePolicy** 资源。 |
| [ProvisioningError](/previous-versions/azure/ad/graph/api/entity-and-complex-type-reference) | beta &nbsp; - &nbsp; _不可用_ <br> v1.0 1.0 &nbsp; - &nbsp; _不可用_ | 此资源已被弃用。  但是，可以在 [onPremisesProvisioningError](/graph/api/resources/onPremisesProvisioningError?view=graph-rest-1.0)中找到描述任何 AD Connect 相关设置错误的新资源。 |
| [ServiceEndpoint](/previous-versions/azure/ad/graph/api/entity-and-complex-type-reference) | beta &nbsp; - &nbsp; [终结点](/graph/api/resources/endpoint?view=graph-rest-beta) <br> v1.0 &nbsp; - &nbsp; [终结点](/graph/api/resources/endpoint?view=graph-rest-1.0) | **终结点** 仅可作为 beta 中的 [组](/graph/api/resources/group?view=graph-rest-beta) 资源的一部分，以及 beta 和 v1.0 中的 [servicePrincipal](/graph/api/resources/serviceprincipal?view=graph-rest-1.0) 资源。|
| [SignInName](/previous-versions/azure/ad/graph/api/entity-and-complex-type-reference) | beta &nbsp; - &nbsp; _新方法_ <br> 1.0 版 &nbsp; - &nbsp; _新方法_ | 用于登录到用户帐户的标识符的新建模。 有关更多详细信息，请参阅 [objectIdentity](/graph/api/resources/objectIdentity?view=graph-rest-1.0) 资源类型。 支持 Azure AD B2C 方案。 |
| [TenantDetail](/previous-versions/azure/ad/graph/api/entity-and-complex-type-reference) | beta &nbsp; - &nbsp; [组织](/graph/api/resources/organization?view=graph-rest-beta) <br> v1.0 &nbsp; - &nbsp; [组织](/graph/api/resources/organization?view=graph-rest-1.0) | |
| [TrustedCasForPasswordAuth](/previous-versions/azure/ad/graph/api/entity-and-complex-type-reference) | beta &nbsp; - &nbsp; [certificateBasedAuthConfiguration](/graph/api/resources/certificatebasedcuthconfiguration?view=graph-rest-beta) <br> v1.0 &nbsp; - &nbsp; [certificateBasedAuthConfiguration](/graph/api/resources/certificatebasedcuthconfiguration?view=graph-rest-1.0) | |
| [UserIdentity](/previous-versions/azure/ad/graph/api/entity-and-complex-type-reference) | beta &nbsp; - &nbsp; [objectIdentity](/graph/api/resources/objectidentity?view=graph-rest-beta) <br> v1.0 &nbsp; - &nbsp; [objectIdentity](/graph/api/resources/objectidentity?view=graph-rest-1.0) |  用于登录到用户帐户（称为 " **objectIdentity**"）的标识符的新建模。 支持 Azure AD B2C 方案。 |

## <a name="next-steps"></a>后续步骤

- 了解 Azure AD Graph 与 Microsoft Graph 之间的 [实体属性差异](migrate-azure-ad-graph-property-differences.md) 。
- 再次查看 [检查表](migrate-azure-ad-graph-planning-checklist.md) 。