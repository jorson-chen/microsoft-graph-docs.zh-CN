---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 2b1f761dbb90b25f86beb7136360ba6fd2e5f626
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2020
ms.locfileid: "48956470"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

LinkedList<String> idsList = new LinkedList<String>();
idsList.add("80a963dd-84af-4eb8-b2a6-781e444d4fb0");
idsList.add("62e90394-69f5-4237-9190-012177145e10");
idsList.add("86a64f51-3a64-4cc6-a8c8-6b8f000c0f52");
idsList.add("ac38546e-ddf3-437a-ac5c-27a94cd7a0f1");

graphClient.devices("{id}")
    .checkMemberObjects(idsList)
    .buildRequest()
    .post();

```