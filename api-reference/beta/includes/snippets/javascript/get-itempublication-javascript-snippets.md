---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: bef48acdcd8495e10e65ab0f88511a81fd5f5bc9
ms.sourcegitcommit: 239db9e961e42b505f52de9859963a9136935f2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/20/2020
ms.locfileid: "46820311"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/profile/publications/{id}')
    .version('beta')
    .get();

```