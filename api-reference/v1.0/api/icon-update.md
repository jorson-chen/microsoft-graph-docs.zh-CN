---
title: 更新图标
description: 更新 icon 对象的属性。
localization_priority: Normal
author: ruoyingl
ms.prod: ''
doc_type: apiPageType
ms.openlocfilehash: 6472041ea42345a6b15bc3991b6d18ff2b7a3328
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "47973237"
---
# <a name="update-icon"></a>更新图标

命名空间：microsoft.graph

更新 icon 对象的属性。
## <a name="permissions"></a>权限
要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。

|权限类型      | 权限（从最低特权到最高特权）              |
|:--------------------|:---------------------------------------------------------|
|委派（工作或学校帐户） | Files.ReadWrite    |
|委派（个人 Microsoft 帐户） | 不支持。    |
|应用程序 | 不支持。 |

## <a name="http-request"></a>HTTP 请求
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/tables/{id|name}/sort/fields/icon
PATCH /workbook/worksheets/{id|name}/tables/{id|name}/sort/fields/icon
```
## <a name="optional-request-headers"></a>可选的请求标头
| 名称       | 说明|
|:-----------|:-----------|
| Authorization  | Bearer {token}。必需。 |


## <a name="request-body"></a>请求正文
在请求正文中，提供应更新的相关字段的值。请求正文中不包括的现有属性将保留其以前的值，或根据对其他属性值的更改重新计算。为了获得最佳性能，不应包括尚未更改的现有值。

| 属性     | 类型   |说明|
|:---------------|:--------|:----------|
|index|int|表示给定集合中图标的索引。|
|set|string|表示图标所属的集合。 可能的值为：、、、、、、、、、、、、、、、、、、、、 `Invalid` `ThreeArrows` `ThreeArrowsGray` `ThreeFlags` `ThreeTrafficLights1` `ThreeTrafficLights2` `ThreeSigns` `ThreeSymbols` `ThreeSymbols2` `FourArrows` `FourArrowsGray` `FourRedToBlack` `FourRating` `FourTrafficLights` `FiveArrows` `FiveArrowsGray` `FiveRating` `FiveQuarters` `ThreeStars` `ThreeTriangles` `FiveBoxes` 。|

## <a name="response"></a>响应

如果成功，此方法在响应正文中返回 `200 OK` 响应代码和更新的 [Icon](../resources/icon.md) 对象。
## <a name="example"></a>示例
##### <a name="request"></a>请求
下面是一个请求示例。
<!-- {
  "blockType": "request",
  "name": "update_icon"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/sort/fields/icon
Content-type: application/json
Content-length: 39

{
  "set": "set-value",
  "index": 99
}
```
##### <a name="response"></a>响应
下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookIcon"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 39

{
  "set": "set-value",
  "index": 99
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update icon",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

