---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 0ba7c1161064bbdea7e895322b40cb063ad26aeb
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/20/2020
ms.locfileid: "48616214"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/security/alerts/{alert_id}')
    .get();

```