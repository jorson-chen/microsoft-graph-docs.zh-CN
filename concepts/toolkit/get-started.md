---
title: Microsoft Graph 工具包入门
description: 开始在应用程序中使用 Microsoft 工具包。
localization_priority: Normal
author: elisenyang
ms.openlocfilehash: 1537a686d25d885a898603ca576f688abdaab3e4
ms.sourcegitcommit: f2dffaca3e1c5b74a01b59e1b76dba1592a6a5d1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/14/2020
ms.locfileid: "42639931"
---
# <a name="get-started-with-the-microsoft-graph-toolkit"></a>Microsoft Graph 工具包入门

可以轻松地将 Microsoft Graph 工具包包含在 web 应用程序、SharePoint web 部件或 Microsoft "团队" 选项卡中。这些组件基于现有的 web 标准构建，并与任何 web 框架和新式浏览器兼容。 本主题介绍如何开始在项目中使用 Microsoft Graph 工具包。

> [!VIDEO https://www.youtube-nocookie.com/embed/oZCGb2MMxa0]

您可以通过直接引用加载程序（通过 unpkg）或安装 npm 程序包，在应用程序中使用 Microsoft Graph 工具包。

## <a name="use-via-mgt-loader"></a>通过预加载加载程序使用

若要通过预加载加载程序使用该工具包，请参阅以下示例。

```html
<script src="https://unpkg.com/@microsoft/mgt/dist/bundle/mgt-loader.js"></script>
```

然后，您可以开始在 HTML 页面中使用这些组件。 下面是 MSAL 提供程序的完整工作示例。

```html
<script src="https://unpkg.com/@microsoft/mgt/dist/bundle/mgt-loader.js"></script>
<mgt-msal-provider client-id="[CLIENT-ID]"></mgt-msal-provider>
<mgt-login></mgt-login>

<!-- <script>
    // alternatively, you can set the provider in code and provide more options
    mgt.Providers.globalProvider = new mgt.MsalProvider({clientId: '[CLIENT-ID]'});
</script> -->
```

> **注意：** MSAL 要求将页面托管在用于身份验证重定向的 web 服务器中。 如果只是开始并且想要进行播放，可以在 Visual Studio Code 中使用[live server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) 。

## <a name="use-via-npm-es6-modules"></a>通过 NPM （es6 模块）使用

通过使用 es6 模块，可以完全控制捆绑过程，并且可以仅捆绑网站所需的代码。 首先，添加 npm 包：

```bash
npm install @microsoft/mgt
```

现在，您可以引用正在使用的页面上的所有组件：

```html
<script src="node_modules/@microsoft/mgt/dist/es6/components.js"></script>
```

或者，只引用所需的组件，避免加载其他所有内容：

```html
<script src="node_modules/@microsoft/mgt/dist/es6/components/mgt-login/mgt-login.js"></script>
```

同样，若要添加提供程序，可以将其添加为组件：

```html
<script src="node_modules/@microsoft/mgt/dist/es6/components/providers/mgt-msal-provider.js"></script>

<mgt-msal-provider client-id="[CLIENT-ID]"></mgt-msal-provider>
```

或者，将其添加到代码中：

```html
<script type="module">
  import { Providers, MsalProvider } from '@microsoft/mgt';

  Providers.globalProvider = new MsalProvider({ clientId: '[CLIENT-ID]' });
</script>
```

## <a name="providers"></a>提供程序

与[提供程序](./providers.md)配合使用时，组件的工作效果最佳。 提供程序公开了组件用来调用 Microsoft Graph 的身份验证和 Api。

该工具包包含适用于[MSAL](./providers/msal.md)、 [SharePoint](./providers/sharepoint.md)和[团队](./providers/teams.md)的提供程序。 您还可以通过创建[自定义提供程序](./providers/custom.md)或将[ProxyProvider](./providers/proxy.md)与您自己的后端身份验证结合使用来使用自己的身份验证逻辑。 

## <a name="polyfills"></a>Polyfills.ts

如果您正在使用 npm 程序包中的 es6 模块，请确保在项目中包含 polyfills.ts，因为它们不会自动包括在内。 若要了解详细信息，请参阅[polyfills.ts](https://www.webcomponents.org/polyfills)。

如果要在 unpkg 上的捆绑包中使用 mgt-loader 脚本，则已包含 polyfills.ts。


## <a name="using-the-components-with-react-angular-and-other-frameworks"></a>将组件与响应、角度和其他框架结合使用

Web 组件基于几个 web 标准，可用于任何已在使用的框架。 但是，并非所有框架都以相同的方式处理 web 组件。 若要了解根据您的框架可能应用的注意事项的详细信息，请参阅 project 中的[自定义元素](https://custom-elements-everywhere.com/)。

以下各节简要介绍了如何将 Microsoft Graph 工具包组件与响应和角结合使用。

### <a name="react"></a>React

"响应" 将所有数据以 HTML 属性的形式传递给自定义元素。 对于基元数据，这是很好的，但它在传递丰富数据（如对象或数组）时不起作用。 在这些情况下，您需要使用将`ref`传递到对象中的。

Ex

```jsx
// import all the components
import '@microsoft/mgt';

class App extends Component {
  render() {
    return <mgt-person show-name ref={el => (el.personDetails = { displayName: 'Nikola Metulev' })} />;
  }
}
```

由于反应实现其自己的合成事件系统，因此它无法侦听来自自定义元素的 DOM 事件，而不使用替代方法。 您需要使用`ref`来引用工具包组件，并手动将事件侦听器附加到 addEventListener，如下面的示例所示。

```jsx
// you can just import a single component
import '@microsoft/mgt/dist/es6/components/mgt-login/mgt-login.js';

class App extends Component {
  render() {
    return <mgt-login ref="loginComponent" />;
  }

  componentDidMount() {
    this.refs.loginComponent.addEventListener('loginCompleted', e => {
      // handle event
    });
  }
}
```

#### <a name="react-typescript-and-tsx"></a>响应、Typescript 和 TSX

当您将自定义元素与响应和 Typescript 一起使用时，可能会出现已知问题。 在尝试使用 tsx 中的组件时，Typescript 将引发错误。 解决方法是在代码中定义自定义元素，如下所示。

```ts
declare global {
  namespace JSX {
    interface IntrinsicElements {
      'mgt-login': any;
    }
  }
}
```

然后，您可以在 tsx 中使用它`<mgt-login></mgt-login>`。

### <a name="angular"></a>Angular

角度的默认绑定语法将始终设置元素的属性。 这适用于丰富的数据（如对象和数组），也适用于基元值。

若要使用自定义元素，首先将添加`app.module.ts` `CUSTOM_ELEMENT_SCHEMA`到`@NgModule() decorator`中的自定义元素，如下面的示例所示。

```ts
import { BrowserModule } from '@angular/platform-browser';
import { NgModule, CUSTOM_ELEMENTS_SCHEMA } from '@angular/core';

import { AppComponent } from './app.component';

@NgModule({
  declarations: [AppComponent],
  imports: [BrowserModule],
  schemas: [CUSTOM_ELEMENTS_SCHEMA],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule {}
```

然后，您可以导入要在组件\*的 ts 文件中使用的组件。

```ts
import { Component } from '@angular/core';
import '@microsoft/mgt/dist/es6/components/mgt-person/mgt-person';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  person = {
    displayName: 'Nikola Metulev'
  };
}
```

最后，按您在模板中的通常方式使用组件。

```html
<mgt-person [personDetails]="person" show-name></mgt-person>
```