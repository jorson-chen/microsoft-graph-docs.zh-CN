---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 5c72a577f5cca9b31fa170abaa5624f9b06b05c3
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/20/2020
ms.locfileid: "48617690"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var privilegedRole = await graphClient.PrivilegedRoles["{id}"]
    .Request()
    .GetAsync();

```