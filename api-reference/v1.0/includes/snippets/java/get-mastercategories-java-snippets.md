---
description: 自动生成的文件。 不修改
ms.openlocfilehash: 3aa4674d212bbc46351f93610d02bb5773b3e150
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/25/2019
ms.locfileid: "35886837"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IOutlookCategoryCollectionPage masterCategories = graphClient.me().outlook().masterCategories()
    .buildRequest()
    .get();

```