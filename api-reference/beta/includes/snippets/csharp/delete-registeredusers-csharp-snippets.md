---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 5c6cadd0acd0d310fd9a6a31a1e1bb17a0428453
ms.sourcegitcommit: 8e18d7fe3c869b2fd48872365116175d3bdce1b7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2020
ms.locfileid: "45224803"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Devices["{id}"].RegisteredUsers["{id}"].Reference
    .Request()
    .DeleteAsync();

```