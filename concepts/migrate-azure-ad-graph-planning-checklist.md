---
title: 应用迁移规划清单
description: 将应用从 Azure AD Graph 迁移到 Microsoft Graph 的清单
author: dkershaw10
localization_priority: Normal
ms.prod: azure-active-directory
ms.openlocfilehash: f8e231166fdb39676ce2778b369c6962cae70cb0
ms.sourcegitcommit: 1d2adc4062c8e83d23768682cf66a731bccd313c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2021
ms.locfileid: "49882743"
---
# <a name="app-migration-planning-checklist"></a>应用迁移规划清单

> [!Important]
> Azure AD Graph API 现已弃用。 我们将继续提供技术支持和安全更新，但将不再提供功能更新。
> 从 2022 年 6 月 30 日开始，我们将停止对 Azure AD Graph 的支持，并且将不再提供技术支持或安全更新。 在此时间之后使用 Azure AD Graph 的应用将不再收到来自 Azure AD Graph 终结点的响应。

使用以下清单规划迁移。

## <a name="step-1-review-the-differences-between-the-apis"></a>步骤 1：查看 API 之间的差异

在很多方面，Microsoft Graph 与早期的 Azure AD Graph 类似。 在许多情况下，只需更改代码中的终结点服务名称和版本，所有内容都应继续工作。

尽管如此，仍存在差异。 某些资源、属性、方法和核心功能已更改。

具体来说，请查找以下方面的差异：

- [两个服务](migrate-azure-ad-graph-request-differences.md) 之间的请求调用语法
- [功能](migrate-azure-ad-graph-feature-differences.md)差异，如目录扩展、批处理、差异查询等
- [实体资源名称](migrate-azure-ad-graph-resource-differences.md) 及其类型
- [请求](migrate-azure-ad-graph-property-differences.md) 和响应对象的属性
- [方法](migrate-azure-ad-graph-method-differences.md)，包括参数和类型

## <a name="step-2-examine-api-use"></a>步骤 2：检查 API 使用

[检查你的应用使用的](migrate-azure-ad-graph-audit-api-use.md) API 及其所需的权限，并与已知差异列表进行比较。  

验证你的应用所需的 API 在 Microsoft Graph v1.0 中是否通常可用，以及这些 API 是否以相同方式工作。

在某些情况下，新功能和功能旨在替代早期方法。

使用 [Graph 浏览器](https://aka.ms/ge) 试验新调用并开发新方法。 为了获得最佳结果，使用测试租户中的测试用户的凭据登录，以便查看 API 对重要数据集执行哪些操作。

## <a name="step-3-review-app-details"></a>步骤 3：查看应用详细信息

- [应用注册](migrate-azure-ad-graph-app-registration.md) 和同意更改 (，这些更改不应) 。
- 令牌获取 [和身份验证库](migrate-azure-ad-graph-authentication-library.md)。
- 对于 .NET 应用程序，请使用 [客户端库](migrate-azure-ad-graph-client-libraries.md)。

## <a name="step-4-deploy-test-and-extend-your-app"></a>步骤 4：部署、测试和扩展应用

在为所有人更新应用之前，请确保进行全面测试，然后向客户受众阶段推出。

现在，你已切换到 Microsoft Graph，解锁现在触手可及的更多数据集和功能从未如此简单。 通过查看 [Microsoft Graph](./overview-major-services.md)中的一些主要服务和功能，你可以体验一下可能的功能。

如果当前使用 [ADAL](/azure/active-directory/develop/active-directory-authentication-libraries) (ADAL) ，请考虑切换到 [MSAL](/azure/active-directory/develop/reference-v2-libraries) (Microsoft 身份验证) 。

## <a name="next-steps"></a>后续步骤

- 了解开始 [步骤](migrate-azure-ad-graph-request-differences.md) 1 的请求调用语法：查看 API 差异。