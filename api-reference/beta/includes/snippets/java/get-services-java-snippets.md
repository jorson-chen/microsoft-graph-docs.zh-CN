---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 48455efcddf9a9cc24452b03c17165a20f18b03a
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2020
ms.locfileid: "48960740"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IPrintServiceCollectionPage services = graphClient.print().services()
    .buildRequest()
    .get();

```