---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 3dda599cff6e8515d6f02e00de45c814fd0e276e
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2020
ms.locfileid: "48966522"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

graphClient.education().classes("11021").assignments("19002")
    .publish()
    .buildRequest()
    .post();

```