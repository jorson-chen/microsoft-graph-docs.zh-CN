---
description: 自动生成的文件。 不修改
ms.openlocfilehash: b21ef643896cce5d4b767322c60367e58606c110
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/25/2019
ms.locfileid: "35889403"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IGroupSettingTemplateCollectionPage groupSettingTemplates = graphClient.groupSettingTemplates()
    .buildRequest()
    .get();

```