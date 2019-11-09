---
title: addIn 资源类型
description: 下面是资源的 JSON 表示形式。
localization_priority: Normal
doc_type: resourcePageType
ms.prod: microsoft-identity-platform
author: davidmu1
ms.openlocfilehash: ad65d0a9a3bed59bcb630082807004a7ca89ba5f
ms.sourcegitcommit: 62507617292d5ad8598e83a8a253c986d9bac787
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/02/2019
ms.locfileid: "37938995"
---
# <a name="addin-resource-type"></a>addIn 资源类型

定义使用服务可用于调用特定上下文中的应用程序的自定义行为。 例如，可以呈现文件流的应用程序[可能会](https://docs.microsoft.com/en-us/onedrive/developer/file-handlers/?view=odsp-graph-online)为其 "FileHandler" 功能配置 addIns。 这将允许 Office 365 等服务在用户正在使用的文档的上下文中调用应用程序。

## <a name="properties"></a>属性
| 属性     | 类型   |说明|
|:---------------|:--------|:----------|
|id|containerparentjob||
|properties|[keyValue](keyvalue.md) 集合||
|类型|string||

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.addIn"
}-->

```json
{
  "id": "guid",
  "properties": [{"@odata.type": "microsoft.graph.keyValue"}],
  "type": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "addIn resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->