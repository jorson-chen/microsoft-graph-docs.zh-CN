---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 836b58964d9730ab2029427a41ddf0028dec8a97
ms.sourcegitcommit: d8a425766aa6a56027b8576bbec6a9d1ae3e079c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/21/2019
ms.locfileid: "35858879"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/groups/{id}/owners/{id}/$ref')
    .version('beta')
    .delete();

```