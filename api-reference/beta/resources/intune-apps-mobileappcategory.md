---
title: mobileAppCategory 资源类型
description: 包含单个 Intune 应用类别的属性。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 441ced8824a84ca11efbea9fe5cdf32f871791b1
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49281115"
---
# <a name="mobileappcategory-resource-type"></a>mobileAppCategory 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

包含单个 Intune 应用类别的属性。

## <a name="methods"></a>Methods
|方法|返回类型|Description|
|:---|:---|:---|
|[列出 mobileAppCategories](../api/intune-apps-mobileappcategory-list.md)|[mobileAppCategory](../resources/intune-apps-mobileappcategory.md) 集合|列出 [mobileAppCategory](../resources/intune-apps-mobileappcategory.md) 对象的属性和关系。|
|[获取 mobileAppCategory](../api/intune-apps-mobileappcategory-get.md)|[mobileAppCategory](../resources/intune-apps-mobileappcategory.md)|读取 [mobileAppCategory](../resources/intune-apps-mobileappcategory.md) 对象的属性和关系。|
|[创建 mobileAppCategory](../api/intune-apps-mobileappcategory-create.md)|[mobileAppCategory](../resources/intune-apps-mobileappcategory.md)|创建新的 [mobileAppCategory](../resources/intune-apps-mobileappcategory.md) 对象。|
|[删除 mobileAppCategory](../api/intune-apps-mobileappcategory-delete.md)|无|删除 [mobileAppCategory](../resources/intune-apps-mobileappcategory.md)。|
|[更新 mobileAppCategory](../api/intune-apps-mobileappcategory-update.md)|[mobileAppCategory](../resources/intune-apps-mobileappcategory.md)|更新 [mobileAppCategory](../resources/intune-apps-mobileappcategory.md) 对象的属性。|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|id|字符串|实体的键。|
|displayName|字符串|应用类别的名称。|
|lastModifiedDateTime|DateTimeOffset|上次修改 mobileAppCategory 的日期和时间。|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileAppCategory"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppCategory",
  "id": "String (identifier)",
  "displayName": "String",
  "lastModifiedDateTime": "String (timestamp)"
}
```




