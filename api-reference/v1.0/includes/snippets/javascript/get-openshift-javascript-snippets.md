---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 61320e5afaa27e58b91f82147bd137113154aaa4
ms.sourcegitcommit: d4114bac58628527611e83e436132c6581a19c52
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/13/2020
ms.locfileid: "44216562"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/teams/{id}/schedule/openShifts')
    .get();

```