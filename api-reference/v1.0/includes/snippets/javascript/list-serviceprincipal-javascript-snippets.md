---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 10c1c7b219edfc1ae8a138cb7f9c8c200af1d2fa
ms.sourcegitcommit: 82da4012294b046416c9ae93d2294d80dab217f6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/04/2020
ms.locfileid: "48905505"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/servicePrincipals')
    .get();

```