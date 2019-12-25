---
title: audioConferencing 资源类型
description: 表示联机会议的电话访问信息。
author: VinodRavichandran
localization_priority: Normal
ms.prod: cloud-communications
doc_type: resourcePageType
ms.openlocfilehash: d2eab9732660f53c7e003b49f6c6ca780c8a4610
ms.sourcegitcommit: f27e81daeff242e623d1a3627405667310395734
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/25/2019
ms.locfileid: "40865789"
---
# <a name="audioconferencing-resource-type"></a>audioConferencing 资源类型

表示[onlineMeeting](onlinemeeting.md)的电话访问信息。

## <a name="properties"></a>属性

| 属性            | 类型    | 说明                                                                    |
|:--------------------|:--------|:-------------------------------------------------------------------------------|
| dialinUrl           | String  | 包含拨入信息的可从外部访问的网页的 URL。 |
| ConferenceId        | String  | 联机会议的会议 id。      |
| tollFreeNumber      | String  | 连接到音频会议提供商的免费电话号码。              |
| tollNumber          | String  | 连接到音频会议提供商的收费号码。                   |

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.audioConferencing"
}-->
```json
{
  "dialinUrl": "String",
  "ConferenceId": "String",
  "tollFreeNumber": "String",
  "tollNumber": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "audioConferencing resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->