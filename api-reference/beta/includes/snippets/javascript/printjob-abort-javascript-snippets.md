---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 2055bb0c00bc2eeed26a9132cc9ebf8b88ecdf3e
ms.sourcegitcommit: 75428fc7535662f34e965c6b69fef3a53fdaf1cb
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/16/2020
ms.locfileid: "49691054"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/print/printers/{id}/jobs/{id}/abort')
    .version('beta')
    .post();

```