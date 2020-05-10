---
title: deviceHealthScriptParameter 资源类型
description: Script 参数的 Base 属性。
author: dougeby
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: 524dbccd94370dbab4c4294b6fa4b6577c325886
ms.sourcegitcommit: d961d83d2792328c9b64421325299e4b56d8dabd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/09/2020
ms.locfileid: "44178554"
---
# <a name="devicehealthscriptparameter-resource-type"></a>deviceHealthScriptParameter 资源类型

命名空间：microsoft.graph

> **重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

Script 参数的 Base 属性。

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|name|字符串|参数的名称|
|说明|String|参数的说明|
|isRequired|Boolean|Param 是否是必需的|
|applyDefaultValueWhenNotAssigned|Boolean|未赋值时是否应用 DefaultValue|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceHealthScriptParameter"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceHealthScriptParameter",
  "name": "String",
  "description": "String",
  "isRequired": true,
  "applyDefaultValueWhenNotAssigned": true
}
```


