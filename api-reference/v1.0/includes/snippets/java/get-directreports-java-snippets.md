---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: ebd9ad705529ce583faf96872fc907a95abe630b
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2020
ms.locfileid: "48983507"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IDirectoryObjectCollectionWithReferencesPage directReports = graphClient.me().directReports()
    .buildRequest()
    .get();

```