---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 44f196c8bab591c77b98bbcd949386116a2faaf5
ms.sourcegitcommit: d4114bac58628527611e83e436132c6581a19c52
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/13/2020
ms.locfileid: "44216583"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var openShifts = await graphClient.Teams["{id}"].Schedule.OpenShifts
    .Request()
    .GetAsync();

```