---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 88189ffeb12f1350172d7bf41a83acf6b2f8798e
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2020
ms.locfileid: "48973464"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IProvisioningObjectSummaryCollectionPage provisioning = graphClient.auditLogs().provisioning()
    .buildRequest()
    .get();

```