---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 12dcc62e6f850e7035558fa8070f9debe6802b83
ms.sourcegitcommit: a3fc420a5639c0f4e89af2b602db17392e176802
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2020
ms.locfileid: "48222948"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var trustFrameworkKey = await graphClient.TrustFramework.KeySets["{id}"]
    .GetActiveKey()
    .Request()
    .GetAsync();

```