---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: ae616837ae9bd23091ab21ffbaed019cc0981906
ms.sourcegitcommit: 60ced1be6ed8dd2d23263090a1cfbc16689bb043
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "48782569"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Print.Printers["{id}"].Jobs["{id}"]
    .Cancel()
    .Request()
    .PostAsync();

```