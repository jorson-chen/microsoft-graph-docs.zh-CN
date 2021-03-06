---
title: publishedResource 资源类型
description: publishedResource 资源类型。
localization_priority: Normal
author: japere
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 4a5f75b6bd12299275e8002abc5c3991984d06e8
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48026406"
---
# <a name="publishedresource-resource-type"></a>publishedResource 资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

表示本地发布的资源。 租户管理员可以发布各种类型的本地资源-企业应用程序、域控制器、服务器等。可将租户管理员安装的 [本地代理](onpremisesagent.md) 配置为访问/处理特定的已发布资源的请求。

## <a name="methods"></a>方法

| 方法       | 返回类型 | 说明 |
|:-------------|:------------|:------------|
| [列出 publishedResources](../api/publishedresource-list.md) | [publishedResource](publishedresource.md) 对象集合 | 获取 **publishedResources** 对象集合。 |
| [获取 publishedResource](../api/publishedresource-get.md) | [publishedResource](publishedresource.md) | 读取 **publishedResource** 对象的属性和关系。 |
| [创建 publishedResource](../api/publishedresource-post.md) |  [publishedResource](publishedresource.md)  | 创建新的 **publishedResource**。 |
| [更新 publishedResource](../api/publishedresource-update.md) | [publishedResource](publishedresource.md) | 更新 **publishedResource** 对象。 |
| [删除 publishedResource](../api/publishedresource-delete.md) | 无 | 删除 **publishedResource** 对象。 |
| [将 publishedResource 分配给 onPremisesAgentGroup](../api/publishedresource-post-agentgroups.md) | 无 | 将 **publishedResource** 对象分配给 **onPremisesAgentGroup**。 |
| [从 onPremisesAgentGroup 中删除 publishedResource](../api/publishedresource-delete-agentgroups.md) | 无 |  从**onPremisesAgentGroup**中删除**publishedResource**对象。|

## <a name="properties"></a>属性

| 属性     | 类型        | 说明 |
|:-------------|:------------|:------------|
|displayName|String| PublishedResource 的显示名称。|
|id|String| PublishedResource 的对象 id。 只读。|
|publishingType|string| 可取值为：`applicationProxy`、`exchangeOnline`、`authentication`、`provisioning`、`adAdministration`。|
|resourceName|String|PublishedResource 的名称。|

## <a name="relationships"></a>关系

| 关系 | 类型        | 说明 |
|:-------------|:------------|:------------|
|agentGroups|[onPremisesAgentGroup](onpremisesagentgroup.md) 集合| 向其分配**publishedResource**的**onPremisesAgentGroups**的列表。 只读。 可为 Null。|

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.publishedResource",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "displayName": "String",
  "id": "String (identifier)",
  "publishingType": "string",
  "resourceName": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "publishedResource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


