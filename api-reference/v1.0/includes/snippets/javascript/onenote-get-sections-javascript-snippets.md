---
description: 自动生成的文件。 不修改
ms.openlocfilehash: 398ab8439e89bb308cd275f7f09b5833a4b84a37
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/25/2019
ms.locfileid: "35887976"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/onenote/sections')
    .get();

```