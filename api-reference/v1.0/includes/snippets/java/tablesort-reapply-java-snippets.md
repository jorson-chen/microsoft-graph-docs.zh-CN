---
description: 自动生成的文件。 不修改
ms.openlocfilehash: 0d875ca120744b8ecea3d1dcca2127bf84ecfe4c
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/25/2019
ms.locfileid: "35894061"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

graphClient.me().drive().items("{id}").workbook().tables("{id|name}").sort()
    .reapply()
    .buildRequest()
    .post();

```