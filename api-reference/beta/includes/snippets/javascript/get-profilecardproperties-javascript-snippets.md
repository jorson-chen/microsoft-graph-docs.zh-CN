---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 8dca269be8f22860c46b74aa16ad3f4d8da80057
ms.sourcegitcommit: 2c8a12389b82ee5101b2bd17eae11b42e65e52c0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/15/2020
ms.locfileid: "45142505"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/organization/{organizationId}/settings/profileCardProperties')
    .version('beta')
    .get();

```