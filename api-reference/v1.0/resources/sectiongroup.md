---
title: sectionGroup 资源类型
description: OneNote 笔记本中的分区组。 节组可以包含节和节组。
localization_priority: Normal
author: jewan-microsoft
ms.prod: onenote
doc_type: resourcePageType
ms.openlocfilehash: 1a3f31f4de8d3453003f87bd30ca0dcc61267af9
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "47984115"
---
# <a name="sectiongroup-resource-type"></a>sectionGroup 资源类型

命名空间：microsoft.graph

OneNote 笔记本中的分区组。 节组可以包含节和节组。

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.onenoteEntityHierarchyModel",
  "optionalProperties": [
    "parentNotebook",
    "parentSectionGroup",
    "sectionGroups",
    "sections"
  ],
  "@odata.type": "microsoft.graph.sectionGroup"
}-->

```json
{
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "string",
  "sectionGroupsUrl": "string",
  "sectionsUrl": "string",
  "self": "string"
}

```
## <a name="properties"></a>属性
| 属性     | 类型   |说明|
|:---------------|:--------|:----------|
|createdBy|[identitySet](identityset.md)|识别创建项目的用户、设备和应用程序。只读。|
|createdDateTime|DateTimeOffset|节组的创建日期和时间。 时间戳表示使用 ISO 8601 格式的日期和时间信息，并且始终处于 UTC 时间。 例如，2014 年 1 月 1 日午夜 UTC 如下所示：`'2014-01-01T00:00:00Z'`。 只读。|
|id|String|节组的唯一标识符。 只读。|
|lastModifiedBy|[identitySet](identityset.md)|识别创建项目的用户、设备和应用程序。只读。|
|lastModifiedDateTime|DateTimeOffset|上次修改节组的日期和时间。 时间戳表示使用 ISO 8601 格式的日期和时间信息，并且始终处于 UTC 时间。 例如，2014 年 1 月 1 日午夜 UTC 如下所示：`'2014-01-01T00:00:00Z'`。 只读。|
|displayName|String|节组的名称。|
|sectionGroupsUrl|String|导航属性的 URL `sectionGroups` ，该 URL 返回节组中的所有节组。 只读。|
|sectionsUrl|String|导航属性的 URL `sections` ，该 URL 返回节组中的所有节。 只读。|
|自学|String|终结点，您可在此处获取关于节组的详细信息。 只读。|

## <a name="relationships"></a>关系
| 关系 | 类型   |说明|
|:---------------|:--------|:----------|
|parentNotebook|[笔记本](notebook.md)|包含分区组的笔记本。 只读。|
|parentSectionGroup|[SectionGroup](sectiongroup.md)|包含节组的节组。 只读。|
|sectionGroups|[SectionGroup](sectiongroup.md) 集合|节中的节组。 只读。 可为 NULL。|
|sections|[OnenoteSection](section.md) 集合|分区组中的节。 只读。 可为 Null。|

## <a name="methods"></a>方法

| 方法           | 返回类型    |说明|
|:---------------|:--------|:----------|
|[获取分区组](../api/sectiongroup-get.md) | [SectionGroup](sectiongroup.md) |读取分区组的属性和关系。|
|[创建分区组](../api/sectiongroup-post-sectiongroups.md) |[SectionGroup](sectiongroup.md)| 通过发布到指定分区组中的 sectionGroups 集合创建分区组。|
|[列出分区组](../api/sectiongroup-list-sectiongroups.md) |[SectionGroup](sectiongroup.md) 集合| 获取指定分区组中的分区组的集合。|
|[创建分区](../api/sectiongroup-post-sections.md) |[OnenoteSection](section.md)| 通过发布到指定分区组中的节集合来创建节。|
|[列出节](../api/sectiongroup-list-sections.md) |[OnenoteSection](section.md) 集合| 获取指定分区组中的节的集合。|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "sectionGroup resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

