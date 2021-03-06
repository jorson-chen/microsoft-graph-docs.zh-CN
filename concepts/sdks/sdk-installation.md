---
title: 安装 Microsoft Graph SDK
description: 提供 C#、Java、JavaScript、Objective-C、PHP 和 Ruby Microsoft Graph SDK 的安装说明。
localization_priority: Normal
author: MichaelMainer
ms.openlocfilehash: 7f96266c1ff774f52e559737fe67f032f1e54fdc
ms.sourcegitcommit: e68fdfb1124d16265deb8df268d4185d9deacac6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "49580954"
---
# <a name="install-the-microsoft-graph-sdks"></a>安装 Microsoft Graph SDK

Microsoft Graph SDK 现已通过 Github 和常用平台包管理器包含在你的项目中。 此主题说明了如何将 Microsoft Graph SDK 安装到你的项目中。

## <a name="install-the-microsoft-graph-net-sdk"></a>安装 Microsoft Graph .NET SDK

以下 NuGet 程序包中都包含了 Microsoft Graph .NET SDK：

- [Microsoft.Graph](https://github.com/microsoftgraph/msgraph-sdk-dotnet) - 包含模型和请求构建器，用于访问 `v1.0` 带有流畅 API 的终结点。 Microsoft.Graph 在 Microsoft.Graph.Core 上有一个依赖项。
- [Microsoft.Graph.Beta](https://github.com/microsoftgraph/msgraph-beta-sdk-dotnet) - 包含模型和请求构建器，用于访问 `beta` 带有流畅 API 的终结点。 Microsoft.Graph.Beta 在 Microsoft.Graph.Core 上有一个依赖项。
- [Microsoft.Graph.Core](https://github.com/microsoftgraph/msgraph-sdk-dotnet) - 呼叫 Microsoft Graph 的核心库。
- [Microsoft.Graph.Auth](https://github.com/microsoftgraph/msgraph-sdk-dotnet-auth) - 提供 Microsoft 身份验证库 (MSAL) 的基于身份验证场景包装器，可以和 Microsoft Graph SDK 配合使用。 Microsoft.Graph.Auth 依赖于 Microsoft.Graph.Core。

可以使用 [Visual Studio 中的程序包管理器 UI 或程序包管理器控制台](/nuget/quickstart/install-and-use-a-package-in-visual-studio) 将Microsoft.Graph 程序包安装到项目中。 以下程序包管理器控制台命令将安装 Microsoft.Graph、Microsoft.Graph.Core 和 Microsoft.Graph.Auth 库。 Microsoft.Graph.Core 依赖于 Microsoft.Graph。

```PowerShell
Install-Package Microsoft.Graph
Install-Package Microsoft.Graph.Auth -IncludePrerelease
```

## <a name="install-the-microsoft-graph-java-sdk"></a>安装 Microsoft Graph Java SDK

以下程序包中都包含了 Microsoft Graph Java SDK：

- [Microsoft-Graph](https://github.com/microsoftgraph/msgraph-sdk-java) - 包含模型和请求构建器，用于访问 `v1.0` 带有流畅 API 的终结点。
- [Microsoft-Graph-Beta](https://github.com/microsoftgraph/msgraph-beta-sdk-java) - 包含模型和请求构建器，用于访问 `beta` 带有流畅 API 的终结点。
- [Microsoft-Graph-Core](https://github.com/microsoftgraph/msgraph-sdk-java-core) - 呼叫 Microsoft Graph 的核心库。
- [Microsoft-Graph-Auth](https://github.com/microsoftgraph/msgraph-sdk-java-auth) - 提供 Microsoft 身份验证库 (MSAL) 的基于身份验证场景包装器，可以和 Microsoft Graph SDK 配合使用。

### <a name="install-the-microsoft-graph-java-sdk-via-gradle"></a>通过 Gradle 安装 Microsoft Graph Java SDK

将存储库和 microsoft-graph 的一个编译依赖项添加到项目的 build.gradle：

```Gradle
repository {
    jcenter()
    jcenter{
        url 'https://oss.jfrog.org/artifactory/oss-snapshot-local'
    }
}

dependency {
    // Include the sdk as a dependency
    implementation 'com.microsoft.graph:microsoft-graph:2.+'
    implementation 'com.microsoft.graph:microsoft-graph-auth:0.3.0'
}
```

### <a name="install-the-microsoft-graph-java-sdk-via-maven"></a>通过 Maven 安装 Microsoft Graph Java SDK

添加存储库到 `profiles`pom.xml 的元素中：

```xml
<profiles>
    <profile>
        <repositories>
            <repository>
                <snapshots>
                    <enabled>false</enabled>
                </snapshots>
                <id>bintray-microsoftgraph-Maven</id>
                <name>bintray</name>
                <url>https://dl.bintray.com/microsoftgraph/Maven</url>
            </repository>
        </repositories>
    </profile>
    <profile>
       <id>allow-snapshots</id>
          <activation><activeByDefault>true</activeByDefault></activation>
       <repositories>
         <repository>
           <id>snapshots-repo</id>
           <url>https://oss.sonatype.org/content/repositories/snapshots</url>
           <releases><enabled>false</enabled></releases>
           <snapshots><enabled>true</enabled></snapshots>
         </repository>
       </repositories>
     </profile>
</profiles>
```

添加依赖项到 `dependencies`pom.xml 的元素中：

```xml
<dependency>
    <groupId>com.microsoft.graph</groupId>
    <artifactId>microsoft-graph</artifactId>
    <version>[2.0,)</version>
</dependency>
<dependency>
    <groupId>com.microsoft.graph</groupId>
    <artifactId>microsoft-graph-auth</artifactId>
    <version>0.3.0</version>
</dependency>
```

## <a name="install-the-microsoft-graph-javascript-sdk"></a>安装 Microsoft Graph JavaScript SDK

以下程序包中都包含了 Microsoft Graph JavaScript SDK：

- @microsoft/microsoft-graph-client ([npm](https://www.npmjs.com/package/@microsoft/microsoft-graph-client)) - 呼叫 Microsoft Graph 的核心库。
- @microsoft/microsoft-graph-types ([npm](https://www.npmjs.com/package/@microsoft/microsoft-graph-types)) - 用于 Microsoft Graph 实体的 Typescript 类型。

可以使用 [npm](https://www.npmjs.com) 安装 Microsoft Graph JavaScript SDK：

```Shell
npm install @microsoft/microsoft-graph-client --save
npm install @microsoft/microsoft-graph-types --save-dev
```

## <a name="install-the-microsoft-graph-objective-c-sdk"></a>安装 Microsoft Graph Objective-C SDK

Microsoft Graph Objective-C SDK 支持 iOS 和 macOS 平台，可以通过 CocoaPod 或 Carthage 安装到项目中。

### <a name="install-the-microsoft-graph-objective-c-sdk-using-cocoapods"></a>使用 Cocoapod 安装 Microsoft Graph Objective-C SDK

添加 podflie 中的以下行，将 Objective-C Microsoft Graph SDK 和 Microsoft Graph Objective-C Auth SDK 安装到 xcode 项目中：

```ruby
pod 'MSGraphClientSDK'
pod 'MSGraphMSALAuthProvider'
```

### <a name="install-the-microsoft-graph-objective-c-sdk-using-carthage"></a>使用 Carthage 安装 Microsoft Graph Objective-C SDK

执行以下步骤使用 [Carthage](https://github.com/Carthage/Carthage) 程序包管理器安装 Microsoft Graph Objective-C SDK 和 Microsoft Graph Objective-C Auth SDK。

1. 创建 **Cartfile**，指定 Objective-C SDK Github 存储库 和目标的 [发行标记](https://github.com/microsoftgraph/msgraph-sdk-objc/releases)。

    ```text
    github "microsoftgraph/msgraph-sdk-objc" "tags/<latest_release_tag>"
    github "microsoftgraph/msgraph-sdk-objc-auth" "tags/<latest_release_tag>"
    ```

1. 运行 `carthage update`。 此操作将依赖项提取到 Carthage/Checkouts 文件夹，然后生成 MSGraphClientSDK 库。

1. 使用 Xcode，在应用程序目标的 **常规** 设置选项卡上的 **链接的框架和库** 部分，将 **MSGraphClientSDK.framework** 和 **MSGraphMSALAuthProvider.framework** 从磁盘上的 Carthage/Build 文件夹拖放到此处。

1. 在应用程序目标的 **生成阶段** 设置选项卡上，单击 **+** 图标，并选择 **新建运行脚本阶段**。 创建指定 Shell 的运行脚本（例如：/bin/sh），添加下列内容至 脚本：

    ```Shell
    /usr/local/bin/carthage copy-frameworks
    ```

1. 并添加路径至希望在 **Input Files** 下使用的框架。

    ```Shell
    $(SRCROOT)/Carthage/Build/iOS/MSGraphClientSDK.framework
    $(SRCROOT)/Carthage/Build/iOS/MSGraphMSALAuthProvider.framework
    ```

## <a name="install-the-microsoft-graph-php-sdk"></a>安装 Microsoft Graph PHP SDK

[Microsoft Graph PHP SDK](https://github.com/microsoftgraph/msgraph-sdk-php) 已在 [packagist.org](https://packagist.org/packages/microsoft/microsoft-graph) 中可用，可按以下方法安装：

### <a name="install-the-microsoft-graph-php-sdk-manually-using-composer"></a>使用 composer 手动安装 Microsoft Graph PHP SDK

```Shell
composer require microsoft/microsoft-graph
```

### <a name="install-the-microsoft-graph-php-sdk-using-composerjson"></a>使用 composer.json 安装 Microsoft Graph PHP SDK

```json
{
    "require": {
        "microsoft/microsoft-graph": "^1.8"
    }
}
```

## <a name="install-the-microsoft-powershell-sdk"></a>安装 Microsoft PowerShell

请参阅 [Microsoft Graph PowerShell SDK](../powershell/installation.md)。

## <a name="install-the-microsoft-graph-ruby-sdk"></a>安装 Microsoft Graph Ruby SDK

[Microsoft Graph Ruby SDK](https://github.com/microsoftgraph/msgraph-sdk-ruby) 已在 [packagist.org](https://rubygems.org/) 中可用，可按以下方法安装：

```ruby
gem install microsoft_graph
```
