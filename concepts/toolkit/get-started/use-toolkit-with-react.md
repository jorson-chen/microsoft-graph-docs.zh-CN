---
title: 将 Microsoft Graph Toolkit React
description: 在 React 应用程序中开始使用 Microsoft Graph Toolkit。
localization_priority: Normal
author: waldekmastykarz
ms.openlocfilehash: 57e9901c8b7ee1f8a5474f21ff4b09def053e7db
ms.sourcegitcommit: 7902607a1e5a030d46e907d08e16644a47a47006
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/12/2020
ms.locfileid: "49664133"
---
# <a name="use-the-microsoft-graph-toolkit-with-react"></a>将 Microsoft Graph Toolkit React

Microsoft Graph Toolkit是一组 Web 组件，可简化连接到 Microsoft Graph，并允许您专注于应用程序。 Microsoft Graph Toolkit作为通过 npm 包分发的通用 `@microsoft/mgt` Web 组件集提供。

如果你使用 React 生成应用，可以使用程序包，该程序包[ `@microsoft/mgt-react` ](./mgt-react.md)将 Microsoft Graph Toolkit Web 组件包装在 React 组件中，并更轻松地传递复杂数据。

本文介绍了使用 Microsoft Graph Toolkit创建 React 应用并连接到 Microsoft 365 的分步过程。 完成这些步骤后，你将拥有一个 React 应用，该应用显示 Microsoft 365 中当前已登录用户的即将进行的约会。

## <a name="prerequisites"></a>先决条件

若要按照本文中的步骤操作，你需要 Microsoft 365 开发环境和一些工具。 有关详细信息，请参阅 [入门](./overview.md)。

## <a name="create-a-react-app"></a>创建 React 应用

通过运行以下命令创建新的 React 应用。 这将使用 TypeScript 创建新的 React 应用，这将帮助你编写更可靠的代码并避免运行时错误。

```cmd
npx create-react-app my-m365-app --template typescript
```

将工作目录更改为新创建的应用。

```cmd
cd my-m365-app
```

接下来，安装 `mgt-react` npm 包，其中包含 Microsoft Graph Toolkit React 组件。

```cmd
npm i @microsoft/mgt-react
```

同时安装包含 MSAL 身份验证提供程序的 `mgt-msal-provider` `mgt-element` 和 npm 包。

```cmd
npm i @microsoft/mgt-element @microsoft/mgt-msal-provider
```

确认你可以运行应用。

```cmd
npm start
```

你应该能够通过在浏览器中打开你的应用 `http://localhost:3000` 。

[!INCLUDE [AAD with implicit flow app registration](../includes/aad-app-registration-spa.md)]

## <a name="connect-react-app-to-microsoft-365"></a>将 React 应用连接到 Microsoft 365

现在，你已在 Azure AD (Azure Active Directory) ，可以将 React 应用连接到 Microsoft 365。 首先，允许用户使用其 Microsoft 帐户登录应用。

### <a name="copy-the-azure-ad-application-registration-id"></a>复制 Azure AD 应用程序注册 ID

1. 在 Azure 门户中，转到应用程序注册。
1. 验证是否位于"概述 **"页上** 。
1. 从 **Essentials** 部分，复制 Application (**客户端) ID** 属性的值

### <a name="configure-the-microsoft-graph-toolkit-authentication-provider"></a>配置 Microsoft Graph Toolkit身份验证提供程序

接下来，配置 Microsoft Graph Toolkit使用的身份验证提供程序。 在这种情况下，你将使用 MSAL，这是生成独立应用程序的良好默认值。 如果你使用 Microsoft 365 中的任意扩展点，如 Teams 或 SharePoint，你将使用 [其他提供程序](../providers/providers.md)。

1. 在代码编辑器中，打开 **src/index。** 文件，并添加到导入列表中，添加：

    ```tsx
    import { Providers } from '@microsoft/mgt-element';
    import { MsalProvider } from '@microsoft/mgt-msal-provider';
    ```

1. 最后一 `import` 个语句之后，使用 MSAL Toolkit初始化 Microsoft Graph 应用程序。

    ```tsx
    Providers.globalProvider = new MsalProvider({
      clientId: 'REPLACE_WITH_CLIENTID'
    });
    ```

    将属性的值替换为之前在 Azure 门户中 `clientId` `Application (client) ID` 复制的属性的值。

通过这些更改 **，src/index.tsx** 文件将如下所示。

  ```tsx
  import React from 'react';
  import ReactDOM from 'react-dom';
  import App from './App';
  import './index.css';
  import * as serviceWorker from './serviceWorker';

  import { Providers } from '@microsoft/mgt-element';
  import { MsalProvider } from '@microsoft/mgt-msal-provider';
  
  Providers.globalProvider = new MsalProvider({
    clientId: 'REPLACE_WITH_CLIENTID'
  });
  
  ReactDOM.render(
    <React.StrictMode>
      <App />
    </React.StrictMode>,
    document.getElementById('root')
  );
  
  // If you want your app to work offline and load faster, you can change
  // unregister() to register() below. Note this comes with some pitfalls.
  // Learn more about service workers: https://bit.ly/CRA-PWA
  serviceWorker.unregister();
  ```

### <a name="add-the-sign-in-button"></a>添加"登录"按钮

添加 **登录** Microsoft Graph Toolkit React 组件，该组件将显示用户可使用其 Microsoft 帐户登录应用的登录按钮。

1. 在代码编辑器中，打开 **src/App.tsx** 文件，并添加到导入列表中：

    ```tsx
    import { Login } from '@microsoft/mgt-react';
    ```

1. 在函数中，将子句的内容替换为基本结构， `App` `return` 包括 Microsoft Graph Toolkit登录组件：

    ```tsx
    <div className="App">
      <header>
        <Login />
      </header>
    </div>
    ```

通过这些更改 **，src/App.tsx** 文件将如下所示。
```tsx

import { Login } from '@microsoft/mgt-react';
import React from 'react';
import './App.css';

function App() {
  return (
    <div className="App">
      <header>
        <Login />
      </header>
    </div>
  );
}

export default App;
```

### <a name="test-signing-in-to-your-application"></a>测试应用程序登录

你现在应该能够使用 Microsoft 帐户登录应用程序。

1. 返回到运行 React 应用的浏览器。 现在应该会看到"登录 **"** 按钮。
1. 单击"登录"按钮时，系统将提示你使用 Microsoft 帐户登录 (可以使用与通过) 访问 Azure 门户的帐户相同的帐户。
1. 因为这是你第一次使用此 Azure AD 应用程序，你需要同意在组织中使用它。
1. 登录后，你将重定向到 React 应用。 请注意 **，"登录"** 按钮已更改，显示用户名称 React 应用，该应用显示使用 Microsoft Graph Toolkit ![ 从 Microsoft 365 检索到的用户 ](../images/mgt-react-userinfo.png) Toolkit。

## <a name="load-data-from-microsoft-365"></a>从 Microsoft 365 加载数据

Microsoft Graph Toolkit不仅简化了对 Microsoft 365 的身份验证，还加载了数据。 本示例中，将显示登录人的日历。

### <a name="specify-permissions-needed-for-your-application"></a>指定应用程序所需的权限

在可以从 Microsoft 365 加载数据之前，需要指定必须授予应用程序的权限范围列表才能访问用户数据。 这些范围因要显示的信息类型而不同。 在这种情况下，你将需要访问人员日历以及访问日历中也显示的人的信息的基本访问权限。 可以在 [Microsoft Graph API](/graph/api/overview)文档中找到每个 API 所需的范围。

1. 在代码编辑器中，打开 **src/index.tsx** 文件，并更新提供程序初始化代码。

    ```tsx
    Providers.globalProvider = new MsalProvider({
      clientId: 'd7cb93c9-9097-4e38-8f06-7c0088ac3318',
      scopes: ['calendars.read', 'user.read', 'openid', 'profile', 'people.read', 'user.readbasic.all']
    });
    ```

### <a name="show-users-data-after-signing-in"></a>登录后显示用户数据

接下来，扩展应用程序以显示用户日历数据。 只有在用户登录后，才能访问此信息。 为此，你需要跟踪用户的登录状态，在用户使用其 Microsoft 帐户登录后显示日历数据。

#### <a name="track-users-sign-in-state"></a>跟踪用户的登录状态

若要跟踪应用程序中的用户登录状态，你将 React 和挂钩与提供程序 `useState` `useEffect` 事件处理程序结合使用。

1. 在代码编辑器中，打开 **src/App.tsx** 文件并扩展现有的 React `import` 语句。

    ```tsx
    import React, { useState, useEffect } from 'react';
    ```

1. 通过添加到 `Provider` `ProviderState` 导入 `mgt-element` 来导入和类型。

    ```tsx
    import { Providers, ProviderState } from '@microsoft/mgt-element';
    ```

1. 添加一个名为的自定义函数，该函数可在应用程序中跟踪 `useIsSignedIn` 用户的登录状态。

    ```tsx
    function useIsSignedIn(): [boolean] {
      const [isSignedIn, setIsSignedIn] = useState(false);
    
      useEffect(() => {
        const updateState = () => {
          const provider = Providers.globalProvider;
          setIsSignedIn(provider && provider.state === ProviderState.SignedIn);
        };
    
        Providers.onProviderUpdated(updateState);
        updateState();
    
        return () => {
          Providers.removeProviderUpdatedListener(updateState);
        }
      }, []);
    
      return [isSignedIn];
    }
    ```

此函数执行两项操作。 首先，使用 React `useState` 挂钩，它可以在组件内启用跟踪状态。 只要状态发生更改，React 就会重新呈现你的组件。 其次，使用 React 挂钩，它通过跟踪 Microsoft Graph Toolkit提供程序中的更改并在必要时更新组件来扩展 `useEffect` 组件的生命周期。

#### <a name="load-users-calendar-if-user-is-signed-in"></a>如果用户已登录，则加载用户的日历

现在，在应用程序中跟踪用户的登录状态，可以在用户登录后显示其日历。

1. 在代码编辑器中，打开 **src/App.tsx** 文件，在 **App** 函数内添加：

    ```tsx
    const [isSignedIn] = useIsSignedIn();
    ```

    这将定义一个布尔常量，该常量可用于确定用户当前 `isSignedIn` 是否已登录到您的应用程序。

1. 使用附加组件 `return` 和 Microsoft Graph Toolkit `div` 扩展子句的内容。

    ```tsx
    <div>
      {isSignedIn &&
        <Agenda />}
    </div>
    ```

借助这些更改 **，src/App.tsx** 文件应如下所示。

```tsx
import { Providers, ProviderState } from '@microsoft/mgt';
import { Agenda, Login } from '@microsoft/mgt-react';
import React, { useState, useEffect } from 'react';
import './App.css';

function useIsSignedIn(): [boolean] {
  const [isSignedIn, setIsSignedIn] = useState(false);

  useEffect(() => {
    const updateState = () => {
      const provider = Providers.globalProvider;
      setIsSignedIn(provider && provider.state === ProviderState.SignedIn);
    };

    Providers.onProviderUpdated(updateState);
    updateState();

    return () => {
      Providers.removeProviderUpdatedListener(updateState);
    }
  }, []);

  return [isSignedIn];
}

function App() {
  const [isSignedIn] = useIsSignedIn();

  return (
    <div className="App">
      <header>
        <Login />
      </header>
      <div>
        {isSignedIn &&
          <Agenda />}
      </div>
    </div>
  );
}

export default App;
```

### <a name="test-showing-users-calendar-after-they-signed-in"></a>测试显示用户登录后的日历

借助这些更改，使用 Microsoft 帐户登录应用程序后，应该会看到日历。

1. To see the changes， close the browser and open it again， and go to `http://localhost:3000` . 你这样做是因为你更改了属性的值，这将影响从 `scopes` Azure AD 请求的访问令牌。
1. 选择 **"登录"** 按钮，然后使用 Microsoft 帐户登录。 请注意同意提示中请求的权限列表的新增内容。 这是因为属性中包含了其他 `scope` 权限。
1. 同意使用应用程序后，应看到有关当前用户及其日历的信息。

![已完成的应用](../images/mgt-finished-app.png)

## <a name="next-steps"></a>后续步骤

- 查看[Microsoft Graph Toolkit。](../overview.md)
- 尝试在运动场 [中的组件](https://mgt.dev)。
- 在 Stack [Overflow](https://aka.ms/mgt-question)上提问。
- 在 GitHub 上报告 Bug 或保留 [功能请求](https://aka.ms/mgt)。
