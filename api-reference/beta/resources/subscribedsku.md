---
title: subscribedSku 资源类型
description: 表示订阅的 SKU 类型。
localization_priority: Normal
author: SumitParikh
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 9d9ccb4bd30a3b14bdfd2527dedde0a0030cb2bd
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "47997520"
---
# <a name="subscribedsku-resource-type"></a>subscribedSku 资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

只支持在订阅的 SKU 上执行读取操作；不支持执行创建、更新和删除操作。不支持查询筛选表达式。继承自 [directoryObject](directoryobject.md)。


## <a name="methods"></a>方法
| 方法           | 返回类型    |说明|
|:---------------|:--------|:----------|
|[获取 subscribedSku](../api/subscribedsku-get.md) | [subscribedSku](subscribedsku.md) |获取组织已获取的特定商业订阅。|
|[列出 subscribedsku](../api/subscribedsku-list.md) | [subscribedSku](subscribedsku.md) 集合 |获取组织已获取的商业版订阅的列表。|

## <a name="properties"></a>属性
| 属性     | 类型   |说明|
|:---------------|:--------|:----------|
|appliesTo|String| 例如，“用户”或“公司”。 |
|capabilityStatus|String| 可取值为：`Enabled`、`Warning`、`Suspended`、`Deleted`、`LockedOut`。 |
|consumedUnits|Int32| 已分配的许可证数量。 |
|id|String| 订阅的 sku 对象的唯一标识符。 键，不可为 null。 |
|prepaidUnits|[licenseUnitsDetail](licenseunitsdetail.md)| 有关预付许可证的数量和状态的信息。 |
|servicePlans|[servicePlanInfo](serviceplaninfo.md) collection| 有关 SKU 可用服务计划的信息。 不可为 null |
|skuId|Guid| 服务 SKU 的唯一标识符 (GUID)。 |
|skuPartNumber|String| SKU 商品编号；例如：“AAD_PREMIUM”或“RMSBASIC”。 若要获取组织获取的商业订阅的列表，请参阅 [List subscribedsku](../api/subscribedsku-list.md)。 |

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.subscribedSku"
}-->

```json
{
  "appliesTo": "string",
  "capabilityStatus": "string",
  "consumedUnits": 1024,
  "id": "string (identifier)",
  "prepaidUnits": {"@odata.type": "microsoft.graph.licenseUnitsDetail"},
  "servicePlans": [{"@odata.type": "microsoft.graph.servicePlanInfo"}],
  "skuId": "guid",
  "skuPartNumber": "string"
}

```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "subscribedSku resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


