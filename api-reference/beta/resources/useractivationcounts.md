---
title: userActivationCounts 资源类型
description: 下面是资源的 JSON 表示形式。
author: krbain
localization_priority: Normal
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: d81e8078d785761c09aa1070120924b2318415a9
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48057883"
---
# <a name="useractivationcounts-resource-type"></a>userActivationCounts 资源类型

命名空间：microsoft.graph

## <a name="properties"></a>属性

| 属性          | 类型   | 说明                              |
| :---------------- | :----- | ---------------------------------------- |
| productType       | String | 产品类型，如 "Microsoft 365 专业增强版" 或 "Project Client"。 |
| lastActivatedDate | 日期   | 最新激活的日期。       |
| 时间           | Int64  | Windows 上的激活计数。 此数字包括任何 Windows 计算机上的每次激活。 |
| mac               | Int64  | Mac OS 上的激活计数。          |
| windows10Mobile   | Int64  | Windows 10 移动版上的激活计数。 |
| ios               | Int64  | IOS 上的激活计数。             |
| android           | Int64  | Android 设备上的激活计数。  |
| activatedOnSharedComputer   | Boolean | 如此如果用户之前在共享计算机上使用过该产品。 |

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.userActivationCounts"
} -->

```json
{
  "productType": "String", 
  "lastActivatedDate": "Date", 
  "windows": 1024, 
  "mac": 1024, 
  "windows10Mobile": 1024, 
  "ios": 1024, 
  "android": 1024,
  "activatedOnSharedComputer": true 
}
```


