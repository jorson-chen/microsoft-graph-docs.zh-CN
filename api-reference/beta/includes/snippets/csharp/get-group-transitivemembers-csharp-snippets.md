---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: f06acd154b19fbc5676645059d41fe9e6e612be3
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/20/2020
ms.locfileid: "48620805"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var transitiveMembers = await graphClient.Groups["{id}"].TransitiveMembers
    .Request()
    .GetAsync();

```