---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: b8bb39028dbdc091fb4a57147eaf48a9a893208f
ms.sourcegitcommit: a9731e19589dcb5c0c6fe2e24b008c86573ef803
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/13/2021
ms.locfileid: "49845972"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IAccessReviewCollectionPage accessReviews = graphClient.accessReviews()
    .buildRequest()
    .filter("businessFlowTemplateId eq '6e4f3d20-c5c3-407f-9695-8460952bcc68',")
    .skip(0)
    .top(100)
    .get();

```