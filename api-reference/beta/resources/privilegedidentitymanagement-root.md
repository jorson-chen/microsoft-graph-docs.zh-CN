---
title: Privileged Identity Management
description: 适合于 Azure AD Privileged Identity Management 的 API，用于管理 Azure Active Directory 角色和 Azure 资源角色。
localization_priority: Priority
doc_type: conceptualPageType
ms.prod: microsoft-identity-platform
author: shauliu
ms.openlocfilehash: 4ee71199c096eeef61cfad619c9fc70e389b389f
ms.sourcegitcommit: 82da4012294b046416c9ae93d2294d80dab217f6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/04/2020
ms.locfileid: "48905937"
---
# <a name="privileged-identity-management"></a>Privileged Identity Management

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

[Azure Active Directory (Azure AD) Privileged Identity Management (PIM)](/azure/active-directory/privileged-identity-management/pim-configure) 是可便于管理、控制和监视对组织中重要资源的访问的服务。 这包括访问 Azure AD、Azure 资源和其他 Microsoft Online Services（例如 Microsoft 365 或 Microsoft Intune）中的资源。 Microsoft Graph 提供有你可用于管理 Azure AD 角色和 Azure 资源角色的 API。

- [适用于 Azure AD 橘色的 API](privilegedidentitymanagement-directory.md)
- [适用于 Azure 资源角色 的 API](privilegedidentitymanagement-resources.md)

> [!IMPORTANT]
> 用于管理 Azure AD 角色的 API 对于大多数租户已弃用，但使用较旧版本 Privileged Identity Management (PIM) 的少数租户除外。 有关 PIM 版本的详细信息，请参阅[确定 PIM 的版本](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-how-to-activate-role?tabs=new#determine-your-version-of-pim)。 如果你使用的是新版本，并且收到 **TenantEnabledInAadRoleMigration** 错误，你可以等待，直至新 API 在 Azure AD 角色的 [unifiedRoleManagement](/graph/api/resources/unifiedroledefinition?view=graph-rest-beta) API 下可用于 PIM 功能，或者你可以使用 Azure AD 角色的 [Azure 资源](/graph/api/resources/privilegedidentitymanagement-resources?view=graph-rest-beta) API。 若要使用 **Azure 资源** API，请将 `azureResources` 替换为 `provider_id` 的 `aadRoles`，然后将租户 ID 用于 `resource_id`。 建议等待新 API。 新 API 可用后，你将能够继续使用 **Azure 资源** API。 Azure 门户中提供的任何新功能也将通过新 API 专门提供。

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Service root",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
