---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 1f6dea9c171af2c9a525639d528c5821d1288711
ms.sourcegitcommit: f27e81daeff242e623d1a3627405667310395734
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/25/2019
ms.locfileid: "37997295"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/profile/languages/{id}')
    .version('beta')
    .get();

```