---
title: iosWebContentFilterAutoFilter 资源类型
description: 表示 iOS Web 内容筛选器设置类型，该类型启用 iOS 自动筛选功能并允许其他 URL 访问控制。 在不使用属性值的情况下构建时，iOS 设备将启用自动筛选器（而不考虑）。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: c1c294ae84da91c6c61bb195fb79ea25c33134ac
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49215868"
---
# <a name="ioswebcontentfilterautofilter-resource-type"></a>iosWebContentFilterAutoFilter 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

表示 iOS Web 内容筛选器设置类型，该类型启用 iOS 自动筛选功能并允许其他 URL 访问控制。 在不使用属性值的情况下构建时，iOS 设备将启用自动筛选器（而不考虑）。


继承自 [iosWebContentFilterBase](../resources/intune-deviceconfig-ioswebcontentfilterbase.md)

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|allowedUrls|String 集合|允许访问的其他 Url|
|blockedUrls|String 集合|为 access 阻止的其他 Url|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosWebContentFilterAutoFilter"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosWebContentFilterAutoFilter",
  "allowedUrls": [
    "String"
  ],
  "blockedUrls": [
    "String"
  ]
}
```




