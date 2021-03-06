---
title: 查看应用注册、权限和同意迁移问题
description: 介绍从 Azure Active Directory (Azure AD) 到 Microsoft Graph API 的应用注册、权限和许可迁移。
author: dkershaw10
localization_priority: Normal
ms.prod: azure-active-directory
ms.openlocfilehash: 8cca43199d8549841087a84d1bd275e38f09efdb
ms.sourcegitcommit: 3fbc2249b307e8d3a9de18f22ef6911094ca272c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/26/2020
ms.locfileid: "48288341"
---
# <a name="review-app-registration-permissions-and-consent"></a>查看应用注册、权限和同意

本文是 *第3步：查看迁移应用程序的应用程序详细信息的第3步：查看* 该 [过程](migrate-azure-ad-graph-planning-checklist.md)的详细信息。

对于任何应用程序更新，有三个要考虑的方面：

- **应用注册**：您可以继续 `appId` 在应用程序代码中使用现有的应用注册 () 。  

    您无 **需重新** 注册您的应用程序即可迁移到 Microsoft Graph。 只需更新代码，对其进行大量测试，然后再部署更新。  

- **权限**：您可以继续为您的应用程序使用现有配置的权限。 您无需请求新的权限，因为 Azure AD Graph 权限与 Microsoft Graph 共享。

    例如，如果现有的应用程序具有 _User. all_ 和 _Group。 read. all_ 权限，这些权限也被隐式授予为 Microsoft Graph 的更新的应用程序。

    如果您的更新还 incudes 使用不适用于 Azure AD Graph 的功能或功能，则您可能需要请求这些新功能的权限。 如果是这种情况，您可以切换应用程序以使用 MSAL 和 v2 终结点，并动态请求其他/增量许可。 在 [审阅应用程序身份验证库更改](./migrate-azure-ad-graph-authentication-library.md)中查找有关切换到 MSAL 的更多详细信息。

- **同意**：最终用户可以继续使用您的应用程序，而无需再次向您授予许可。

    已向你的应用程序授予访问其数据的同意的用户可以继续使用你的应用程序以使用 Microsoft Graph，而不要求再次同意。

简单迁移项目在这些领域中不应遇到任何问题。

但是，如果您使用新的功能、服务或添加其他功能，则可能需要新权限，并且可能需要最终用户同意。  在这种情况下，会在刷新令牌时请求同意。

## <a name="next-steps"></a>后续步骤

- 了解 Azure AD Graph 和 Microsoft Graph 之间的 [身份验证库](migrate-azure-ad-graph-authentication-library.md) 差异。
- 再次查看 [检查表](migrate-azure-ad-graph-planning-checklist.md) 。