---
title: 货币资源类型
description: Dynamics 365 Business Central 中的货币对象
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
localization_priority: Normal
ms.prod: dynamics-365-business-central
doc_type: resourcePageType
ms.openlocfilehash: 42dc5fec859aff758b2f46812a63b10f49f0498a
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48071365"
---
# <a name="currencies-resource-type"></a>货币资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

表示 Dynamics 365 Business Central 中使用的货币。

## <a name="methods"></a>方法
| 方法                                                  |返回类型|说明       |
|:--------------------------------------------------------|:----------|:-----------------|
|[获取货币](../api/dynamics-currencies-get.md)      |货币 |获取货币。   |
|[过帐货币](../api/dynamics-create-currencies.md)  |货币 |创建货币。|
|[修补程序货币](../api/dynamics-currencies-update.md) |货币 |更新货币。|
|[删除货币](../api/dynamics-currencies-delete.md)|无       |删除货币。|

## <a name="properties"></a>属性
| 属性              | 类型   |说明                                                   |
|:----------------------|:-------|:-------------------------------------------------------------|
|id                     |GUID    |货币的唯一 ID。 不可编辑。                  |
|code                   |string  |指定货币代码。                                  |
|displayName            |string  |指定货币显示名称。                          |
|符号                 |string  |指定在支票上显示的此货币符号。|
|amountDecimalPlaces    |string  |指定系统将按此货币的金额显示的小数位数。|
|amountRoundingPrecision|数位 |指定此货币的舍入金额时要使用的时间间隔的大小。|
|lastModifiedDateTime   |datetime|修改了货币的最后一个日期/时间。 只读。       |  


## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式

下面是货币的 JSON 表示形式。


```json
{
  "id": "GUID",
  "code": "string",
  "displayName": "string",
  "symbol": "string",
  "amountDecimalPlaces": "string",
  "amountRoundingPrecision": "decimal",
  "lastModifiedDateTime": "datetime"
}

```



