---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: e9f30271f1d4e997e66a0b20ce2b8dbe40238461
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/20/2020
ms.locfileid: "48618212"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/security/secureScoreControlProfiles')
    .version('beta')
    .get();

```