---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 9261a525a34374459833cbcda6c39d7a4f41f14b
ms.sourcegitcommit: fce7ce328f0c88c6310af9cc85d12bcebc88a6c3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/28/2019
ms.locfileid: "39637130"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const string = {
  ids: [
    "80a963dd-84af-4eb8-b2a6-781e444d4fb0",
    "62e90394-69f5-4237-9190-012177145e10",
    "86a64f51-3a64-4cc6-a8c8-6b8f000c0f52",
    "ac38546e-ddf3-437a-ac5c-27a94cd7a0f1"
  ]
};

let res = await client.api('/groups/{id}/checkMemberObjects')
    .post(string);

```