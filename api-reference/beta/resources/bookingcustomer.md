---
title: bookingCustomer 资源类型
description: " > **重要说明：** Microsoft Graph 中 /beta 版本下的 API 是预览版，可能会发生变化。 不支持在生产应用程序中使用这些 API。"
localization_priority: Normal
author: arvindmicrosoft
ms.prod: bookings
doc_type: resourcePageType
ms.openlocfilehash: 5b527902c5d6e39bb752e07838c6a5e1c3022bb0
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48071785"
---
# <a name="bookingcustomer-resource-type"></a>bookingCustomer 资源类型

命名空间：microsoft.graph

 [!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]
 
表示 [bookingBusiness](bookingbusiness.md)的客户。


## <a name="methods"></a>方法

| 方法           | 返回类型    |说明|
|:---------------|:--------|:----------|
|[列出客户](../api/bookingbusiness-list-customers.md) | [bookingCustomer](bookingcustomer.md) 集合 | 获取 **bookingCustomer** 对象的列表。 |
|[创建 bookingCustomer](../api/bookingbusiness-post-customers.md) | [bookingCustomer](bookingcustomer.md) | 创建新的 **bookingCustomer** 对象。 |
|[获取 bookingCustomer](../api/bookingcustomer-get.md) | [bookingCustomer](bookingcustomer.md) |读取 **bookingCustomer** 对象的属性和关系。|
|[更新](../api/bookingcustomer-update.md) | [bookingCustomer](bookingcustomer.md) |更新 **bookingCustomer** 对象。 |
|[删除](../api/bookingcustomer-delete.md) | 无 |删除 **bookingCustomer** 对象。 |

## <a name="properties"></a>属性
| 属性     | 类型   |说明|
|:---------------|:--------|:----------|
|displayName|String|客户的名称。|
|emailAddress|String|客户的 SMTP 地址。|
|id|String| 客户的 ID。 只读。|

## <a name="relationships"></a>关系
无


## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.bookingCustomer"
}-->

```json
{
  "displayName": "String",
  "emailAddress": "String",
  "id": "String (identifier)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "bookingCustomer resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


