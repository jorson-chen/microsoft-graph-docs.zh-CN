---
description: 自动生成的文件。 不修改
ms.openlocfilehash: d117881035d62a934ed17e78a86afa0885ba72c4
ms.sourcegitcommit: f50b1feff72182d1e19bfa346304beaf29558b68
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/19/2019
ms.locfileid: "36461190"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var educationRubric = await graphClient.Education.Me.Assignments["{id}"].Rubric
    .Request()
    .GetAsync();

```