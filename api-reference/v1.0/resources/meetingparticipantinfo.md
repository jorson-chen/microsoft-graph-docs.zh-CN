---
title: meetingParticipantInfo 资源类型
description: 会议参与者的相关信息。
author: VinodRavichandran
localization_priority: Normal
ms.prod: cloud-communications
doc_type: resourcePageType
ms.openlocfilehash: 6f3b8bc4b373f28f8f35fe891f7498a0560c38b9
ms.sourcegitcommit: f27e81daeff242e623d1a3627405667310395734
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/25/2019
ms.locfileid: "40865777"
---
# <a name="meetingparticipantinfo-resource-type"></a>meetingParticipantInfo 资源类型

会议参与者的相关信息。

## <a name="properties"></a>属性

| 属性       | 类型                          | 说明                              |
|:---------------|:------------------------------|:-----------------------------------------|
| 窃取       | [identitySet](identityset.md) | 参与者的标识信息。 |
| upn            | String                        | 参与者的用户主体名称。  |

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.meetingParticipantInfo"
}-->
```json
{
  "identity": {"@odata.type": "#microsoft.graph.identitySet"},
  "upn": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "meetingParticipantInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->