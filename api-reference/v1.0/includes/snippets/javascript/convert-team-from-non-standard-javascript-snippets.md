---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: fe8be75d13c75a85f54c1f87a7dcf4f8646f5397
ms.sourcegitcommit: c20276369a8834a259f24038e7ee5c33de02660b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/07/2020
ms.locfileid: "48374060"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const team = {
  template@odata.bind: "https://graph.microsoft.com/v1.0/teamsTemplates('educationClass')",
  displayName: "My Class Team",
  description: "My Class Team’s Description"
};

let res = await client.api('/teams')
    .post(team);

```