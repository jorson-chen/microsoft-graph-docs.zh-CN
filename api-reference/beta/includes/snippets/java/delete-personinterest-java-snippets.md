---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: d9d913ecff009a347314a964f195bebb4777e8be
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2020
ms.locfileid: "48972801"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

graphClient.me().profile().interests("{id}")
    .buildRequest()
    .delete();

```