---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 11db73c436ae6ce93a24506c02425ca3cced2638
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/05/2019
ms.locfileid: "37994948"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const removePassword = {
    keyId: "f0b0b335-1d71-4883-8f98-567911bfdca6"
};

let res = await client.api('/applications/{id}/removePassword')
    .version('beta')
    .post(removePassword);

```