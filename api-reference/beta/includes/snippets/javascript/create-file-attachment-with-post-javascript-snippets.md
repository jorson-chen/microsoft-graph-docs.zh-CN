---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 852ae44b258da8707aaa3afd211d430372195ec5
ms.sourcegitcommit: d8a425766aa6a56027b8576bbec6a9d1ae3e079c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/21/2019
ms.locfileid: "36633557"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const reply = {
  post: {
    body: {
      contentType: "text",
      content: "Which quarter does that file cover? See my attachment."
    },
    attachments: [{
      @odata.type: "#microsoft.graph.fileAttachment",
      name: "Another file as attachment",
      contentBytes: "VGhpcyBpcyBhIGZpbGUgdG8gYmUgYXR0YWNoZWQu"
    } ]
  }
};

let res = await client.api('/groups/1848753d-185d-4c08-a4e4-6ee40521d115/threads/AAQkADJUdfolA==/reply')
    .version('beta')
    .post(reply);

```