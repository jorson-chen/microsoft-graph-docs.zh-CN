---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 97464b3632e34264e06bb3c05954623ef0145574
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2020
ms.locfileid: "48968804"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IScopedRoleMembershipCollectionPage scopedRoleMemberOf = graphClient.me().scopedRoleMemberOf()
    .buildRequest()
    .get();

```