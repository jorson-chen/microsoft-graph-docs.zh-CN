---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: bc23cd3d5428fbd77a022a619c05dc57fbe0afc3
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/20/2020
ms.locfileid: "48611211"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var messages = await graphClient.Teams["303d2c1c-f1c5-40ce-b68e-544343d7f42b"].Channels["19:fec4b0f2825d4c8c82abc09027a64184@thread.skype"].Messages
    .Request()
    .GetAsync();

```