---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 0be3abf81bc052ec4f61bb4917ab2c20f1179f5f
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/05/2019
ms.locfileid: "37996840"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var webAccounts = await graphClient.Me.Profile.WebAccounts
    .Request()
    .GetAsync();

```