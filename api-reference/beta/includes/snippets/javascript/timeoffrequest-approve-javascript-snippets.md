---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 0b5f30ba7e830a5a7eac19b15c06e4856b876cd0
ms.sourcegitcommit: f27e81daeff242e623d1a3627405667310395734
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/25/2019
ms.locfileid: "40863658"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const timeOffRequest = {
  message: "message-value"
};

let res = await client.api('/teams/{id}/schedule/timeOffRequests/approve')
    .version('beta')
    .post(timeOffRequest);

```