---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: e927c96885d72f701e8ea18d5dc6b01a2e13e5d4
ms.sourcegitcommit: d4114bac58628527611e83e436132c6581a19c52
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/13/2020
ms.locfileid: "44216894"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Print.Shares["{id}"]
    .Request()
    .DeleteAsync();

```