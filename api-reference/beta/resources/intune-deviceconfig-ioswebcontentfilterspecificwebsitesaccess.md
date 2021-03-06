---
title: iosWebContentFilterSpecificWebsitesAccess 资源类型
description: 表示 iOS Web 内容筛选器设置类型，该类型将 URL 书签安装到 iOS 内置浏览器中。 在课堂中，教师希望学生通过在其 iOS 设备上配置的浏览器书签来导航网站，而不能访问其他网站，这是一个示例方案。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 46d83561851ea3fe240bbef35c3351c77ee4cb03
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49215826"
---
# <a name="ioswebcontentfilterspecificwebsitesaccess-resource-type"></a>iosWebContentFilterSpecificWebsitesAccess 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

表示 iOS Web 内容筛选器设置类型，该类型将 URL 书签安装到 iOS 内置浏览器中。 在课堂中，教师希望学生通过在其 iOS 设备上配置的浏览器书签来导航网站，而不能访问其他网站，这是一个示例方案。


继承自 [iosWebContentFilterBase](../resources/intune-deviceconfig-ioswebcontentfilterbase.md)

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|specificWebsitesOnly|[iosBookmark](../resources/intune-deviceconfig-iosbookmark.md) 集合|将安装到内置浏览器和用户的 URL 书签仅允许通过书签访问网站。 该集合最多可包含 500 个元素。|
|websiteList|[iosBookmark](../resources/intune-deviceconfig-iosbookmark.md) 集合|将安装到内置浏览器和用户的 URL 书签仅允许通过书签访问网站。 该集合最多可包含 500 个元素。|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosWebContentFilterSpecificWebsitesAccess"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosWebContentFilterSpecificWebsitesAccess",
  "specificWebsitesOnly": [
    {
      "@odata.type": "microsoft.graph.iosBookmark",
      "url": "String",
      "bookmarkFolder": "String",
      "displayName": "String"
    }
  ],
  "websiteList": [
    {
      "@odata.type": "microsoft.graph.iosBookmark",
      "url": "String",
      "bookmarkFolder": "String",
      "displayName": "String"
    }
  ]
}
```




