---
description: 自动生成的文件。 不修改
ms.openlocfilehash: f76c74bfe85e4eadafecbef9f039789fb43c3c1e
ms.sourcegitcommit: f50b1feff72182d1e19bfa346304beaf29558b68
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/19/2019
ms.locfileid: "36460965"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/education/me/assignments/{id}/submissions/{id}/outcomes')
    .version('beta')
    .get();

```