---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 048407e27da9fe2cc54f7e432b663f710a1c0d3f
ms.sourcegitcommit: c650b95ef4d0c3e93e2eb36cd6b52ed31200164f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/10/2020
ms.locfileid: "44685221"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var educationUser = new EducationUser
{
    AdditionalData = new Dictionary<string, object>()
    {
        {"@odata.id", "https://graph.microsoft.com/beta/education/users/14008"}
    }
};

await graphClient.Education.Schools["{id}"].Users.References
    .Request()
    .AddAsync(educationUser);

```