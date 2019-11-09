---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 80bc4aab423acd04552fac50163c7b00a2ce2ff1
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/05/2019
ms.locfileid: "37994439"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const informationProtectionAction = {
  contentInfo: {
    @odata.type: "#microsoft.graph.contentInfo",
    format@odata.type: "#microsoft.graph.contentFormat",
    format: "default",
    identifier: null,
    state@odata.type: "#microsoft.graph.contentState",
    state: "rest",
    metadata@odata.type: "#Collection(microsoft.graph.keyValuePair)",
    metadata: [
      {
        @odata.type: "#microsoft.graph.keyValuePair",
        name: "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Enabled",
        value: "True"
      },
      {
        @odata.type: "#microsoft.graph.keyValuePair",
        name: "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Method",
        value: "Standard"
      },
      {
        @odata.type: "#microsoft.graph.keyValuePair",
        name: "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_SetDate",
        value: "1/1/0001 12:00:00 AM"
      },
      {
        @odata.type: "#microsoft.graph.keyValuePair",
        name: "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_SiteId",
        value: "cfa4cf1d-a337-4481-aa99-19d8f3d63f7c"
      },
      {
        @odata.type: "#microsoft.graph.keyValuePair",
        name: "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Name",
        value: "General"
      },
      {
        @odata.type: "#microsoft.graph.keyValuePair",
        name: "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_ContentBits",
        value: "0"
      },
      {
        @odata.type: "#microsoft.graph.keyValuePair",
        name: "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_ActionId",
        value: "00000000-0000-0000-0000-000000000000"
      }
    ]
  },
  labelingOptions: {
    @odata.type: "#microsoft.graph.labelingOptions",
    assignmentMethod@odata.type: "#microsoft.graph.assignmentMethod",
    assignmentMethod: "standard",
    labelId@odata.type: "#Guid",
    labelId: "97309856-9c28-4ac6-9382-5f8bc20c457b",
    downgradeJustification: null,
    extendedProperties@odata.type: "#Collection(microsoft.graph.keyValuePair)",
    extendedProperties: []
  }
};

let res = await client.api('/informationprotection/policy/labels/evaluateApplication')
    .version('beta')
    .post(informationProtectionAction);

```