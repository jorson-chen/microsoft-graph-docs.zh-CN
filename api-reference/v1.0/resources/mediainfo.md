---
title: mediaInfo 资源类型
description: 在提示操作中使用的媒体信息。
author: VinodRavichandran
localization_priority: Normal
ms.prod: cloud-communications
doc_type: resourcePageType
ms.openlocfilehash: 9d9b8f4709d3379afda8e30fec2b7db64a474a0e
ms.sourcegitcommit: f27e81daeff242e623d1a3627405667310395734
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/25/2019
ms.locfileid: "40865779"
---
# <a name="mediainfo-resource-type"></a>mediaInfo 资源类型

在提示操作中使用的媒体信息。

## <a name="properties"></a>属性
| 属性       | 类型    | 说明                      |
|:---------------|:--------|:---------------------------------|
| resourceId     | String  | 可选。 用于唯一标识资源。 如果传入，则会将提示 uri 作为密钥缓存在此 resourceId 中。 |
| url            | String  | 将播放的提示的路径。 目前仅支持带有16000（16KHz）采样速率的波形文件（.wav）格式、单通道、16位样本。 |


## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.mediaInfo"
}-->
```json
{
  "resourceId": "String",
  "uri": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "mediaInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->