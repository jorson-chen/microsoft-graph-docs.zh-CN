---
title: 查看应用程序身份验证库更改
description: 介绍如何更新身份验证库使用，以便将应用从 Azure Active Directory (Azure AD) API 应用迁移到 Microsoft Graph API。
author: dkershaw10
localization_priority: Normal
ms.prod: azure-active-directory
ms.openlocfilehash: 291b34b848892cb0294cc2e1a30c6452174690cc
ms.sourcegitcommit: 7370fb65d11d1347123a3f6d320d2c6d36f34224
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/02/2020
ms.locfileid: "48338142"
---
# <a name="review-app-authentication-library-changes"></a>查看应用程序身份验证库更改

本文是 *第3步：查看迁移应用程序的应用程序详细信息的第3步：查看* 该 [过程](migrate-azure-ad-graph-planning-checklist.md)的详细信息。

大多数应用使用身份验证库来获取和管理访问令牌，以调用 Microsoft Graph。  Microsoft 提供了两个身份验证库：

- [Azure Active Directory 身份验证库](/azure/active-directory/develop/active-directory-authentication-libraries) (ADAL) 
- [Microsoft 身份验证库](/azure/active-directory/develop/reference-v2-libraries) (MSAL) 

## <a name="updating-adal"></a>更新 ADAL

如果你的应用当前使用 ADAL，请使用两阶段迁移方法：

1. 更新您的应用程序以获取 Microsoft Graph 的访问令牌。 继续使用 ADAL 执行此步骤。 更新 **resourceURL**，其中包含表示资源 web API 的 URI，从：

    `https://graph.windows.net`  

    自：  

    `https://graph.microsoft.com`

    在此更改之后，新获取的令牌具有相同的作用域，但访问令牌的访问群体现在是 Microsoft Graph。  

    更新 **resourceURL** 和已验证的功能后，发布临时更新以获取用户的 up 和 runnning。

1.  接下来，开始将应用程序迁移到使用 MSAL （即，支持的库可供将来使用），现在将 ADAL 弃用。

## <a name="migrating-to-msal"></a>迁移到 MSAL

MSAL 提供了多个优于 ADAL 的优势，包括增量许可、更丰富的单一登录体验、对个人 Microsoft 帐户的支持、使用基于标准的协议等。  

当您将应用程序切换到 MSAL 时，您需要进行一些更改，包括在令牌采集请求中设置 **scope** 参数：

``` csharp
var scopes = new string[] { "https://graph.microsoft.com/.default" };
```

上面的表达式将权限范围请求限制为在 Azure 门户中的应用程序注册过程中配置的请求，并将现有用户保存为不得不再次同意您的应用程序。

请参阅 [将 ADAL 迁移到 MSAL](https://aka.ms/adal-net-to-msal-net) ，以在过程中提供直接和广泛的帮助，包括故障排除和帮助常见错误。

迁移到 MSAL 后，您可以动态请求其他作用域，并且在下次使用您的应用程序时，系统会提示用户提供增量许可。

## <a name="next-steps"></a>后续步骤

- 了解 Azure AD Graph 和 Microsoft Graph 之间的 [.net 客户端库](migrate-azure-ad-graph-client-libraries.md) 差异。
- 再次查看 [检查表](migrate-azure-ad-graph-planning-checklist.md) 。