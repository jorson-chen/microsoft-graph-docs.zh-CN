---
description: 自动生成的文件。 不修改
ms.openlocfilehash: d83aad3b0076054a0c2460a6be6ca0dda9d4ef1c
ms.sourcegitcommit: 1066aa4045d48f9c9b764d3b2891cf4f806d17d5
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/15/2019
ms.locfileid: "36413310"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/planner/plans/{id}')
    .version('beta')
    .get();

```