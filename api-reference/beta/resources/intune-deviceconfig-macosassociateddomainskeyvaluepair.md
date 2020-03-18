---
title: macOSAssociatedDomainsKeyValuePair 资源类型
description: 关联域的键值对
author: davidmu1
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: 08a59f0566da2e2dffa64c059cc913923ec5cf58
ms.sourcegitcommit: b38fd4c8c734243f6f82448045a1f6bf63311ec9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "42790319"
---
# <a name="macosassociateddomainskeyvaluepair-resource-type"></a>macOSAssociatedDomainsKeyValuePair 资源类型

> **重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

关联域的键值对


继承自[keyValuePair](../resources/intune-shared-keyvaluepair.md)

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|name|String|从[KeyValuePair](../resources/intune-shared-keyvaluepair.md)继承的此键/值对的名称|
|value|String|从[KeyValuePair](../resources/intune-shared-keyvaluepair.md)继承的此键/值对的值|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.macOSAssociatedDomainsKeyValuePair"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.macOSAssociatedDomainsKeyValuePair",
  "name": "String",
  "value": "String"
}
```


