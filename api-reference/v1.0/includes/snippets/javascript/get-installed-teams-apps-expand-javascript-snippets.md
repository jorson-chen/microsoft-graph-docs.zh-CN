---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: d6f3c04656f7202b842414a4d66bd0d84eee2533
ms.sourcegitcommit: 75428fc7535662f34e965c6b69fef3a53fdaf1cb
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/16/2020
ms.locfileid: "49692588"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/teams/{id}/installedApps/{id}')
    .expand('teamsAppDefinition')
    .get();

```