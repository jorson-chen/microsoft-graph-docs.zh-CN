---
title: 使用 Graph 浏览器尝试 Microsoft Graph API
description: 使用 Graph 浏览器在默认示例租户上尝试 Microsoft Graph API 以探索功能，或登录到你自己的租户，并使用它作为原型工具实现你的应用方案。
localization_priority: Normal
author: bettirosengugi
ms.openlocfilehash: 3f957d940d4dde483324492f1778ede970a5aefc
ms.sourcegitcommit: 6ec748ef00d025ee216274a608291be3c1257777
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/27/2021
ms.locfileid: "50013743"
---
# <a name="use-graph-explorer-to-try-microsoft-graph-apis"></a>使用 Graph 浏览器尝试 Microsoft Graph API

[Graph 浏览器](https://developer.microsoft.com/graph/graph-explorer/) 是一款开发人员工具，可方便你提出 Microsoft Graph REST API 请求并查看相应的响应。 使用 Graph 浏览器尝试默认示例租户上的 API 来浏览功能，或登录到你自己的租户，并使用它作为原型制作工具，以完成你的应用方案。 此工具包括有用的功能，如 C#、Java、JavaScript 和目标 C 中的代码段;Microsoft Graph Toolkit和自适应卡片集成;等。

使用 Graph 浏览器：

- 将 Microsoft Graph API 请求 (GET、POST、PUT、PATCH 和 DELETE) 查看响应，包括响应代码以及任何标头和正文。
- 同意权限。
- 向查询添加请求正文和请求标头。
- 查看和复制访问令牌。
- 查看 Microsoft Graph 中不同服务的示例查询。
- 查看、下载或删除最近 30 天内运行的查询。
- 查看和复制在 C#、Java、JavaScript 和目标 C 中运行的每个查询的代码段。
- 访问 Microsoft Graph Toolkit组件和自适应卡片，用于一些示例查询。
- 共享查询，包括请求正文和请求标头。

Graph 资源管理器会处理身份验证过程。 通过折叠边栏并更改主题来自定义体验。

## <a name="get-started"></a>入门

Graph 浏览器是一个托管在 Microsoft Graph 开发人员中心的 [Web 应用程序](https://developer.microsoft.com/en-us/graph/graph-explorer)。 这是一个开源项目，欢迎你在 GitHub 存储库中做出 [贡献和提供反馈](https://github.com/microsoftgraph/microsoft-graph-explorer-v4)。

Graph 资源管理器包括以下元素：

1. HTTP 谓词下拉列表
2. API 版本下拉列表
3. 请求查询地址栏
4. 示例查询
5. 示例查询的文档链接

![Graph 浏览器用户界面的屏幕截图](./images/getting-started.png)

### <a name="make-a-get-request-in-graph-explorer"></a>在 Graph 资源管理器中提出 GET 请求

若要在 Graph 资源管理器中运行 GET 请求，则不必登录。 只需单击示例查询，示例数据就会显示在响应预览中。 

![Graph 资源管理器中示例请求的屏幕截图](./images/making-a-get-request.png)

若要提出请求，请：

1. 选择一个示例查询并运行它。
2. 获取 HTTP 响应代码。
3. 使用示例数据查看来自 Microsoft Graph API 的响应。

当你登录到 Graph 浏览器并单击同一查询时，响应将返回你登录的租户中的真实数据。

### <a name="running-non-get-requests-in-graph-explorer"></a>在 Graph 资源管理器中运行非 GET 请求

若要尝试 POST、PUT、PATCH 和 DELETE 请求，请使用 Microsoft 365 帐户登录到 Graph 资源管理器。这可以是用于测试或演示的组织帐户。 若要获取免费的 Microsoft 365 E5 开发人员订阅示例，以及可帮助你构建 Microsoft 365 平台解决方案的工具和其他资源，请加入 [Microsoft 365 开发人员计划](https://developer.microsoft.com/microsoft-365/dev-program)。 

>[!IMPORTANT]
>如果选择使用组织帐户登录，则运行非 GET 请求可能会影响租户中的数据。

例如，若要运行 POST 请求，请在 HTTP 谓词的下拉列表中选择 POST，并根据需要添加请求正文和请求标头。

![Graph 资源管理器中 POST 请求的屏幕截图](./images/making-a-post-request.png)

1. 选择 POST 示例查询。
2. 更新 **请求正文**;例如，为应用程序命名。
3. 单击 **"运行查询"。**
4. 查看来自 Microsoft Graph API 的响应。

若要查看默认 JSON 格式的响应，请选择请求窗格中的"请求标头"选项卡，定义键/值对，然后单击"**添加"。**

![显示 Graph 资源管理器中的"请求标头"选项卡的屏幕截图](./images/adding-key-value-pairs.png)

## <a name="next-steps"></a>后续步骤

- 访问 [Graph 浏览器](https://developer.microsoft.com/graph/graph-explorer/)。
- 详细了解 [Graph 浏览器功能](./graph-explorer-features.md)。
- 在 GitHub 存储库中参与或 [提供反馈](https://github.com/microsoftgraph/microsoft-graph-explorer-v4/issues/new/choose)。
