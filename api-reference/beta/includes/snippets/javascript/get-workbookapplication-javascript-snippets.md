---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: f8cb1f2e23b095557abd15ad53fd4d6e1506aa78
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/20/2020
ms.locfileid: "48611581"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/items/{id}/workbook/application')
    .version('beta')
    .get();

```