---
description: 自动生成的文件。 不修改
ms.openlocfilehash: f2f5239dd0153d657e0d8c9f2de4f5991fe110e4
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/25/2019
ms.locfileid: "35891597"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

ISecureScoreCollectionPage secureScores = graphClient.security().secureScores()
    .buildRequest()
    .top(1)
    .get();

```