---
title: mobileAppContent 资源类型
description: 包含特定应用版本的内容属性。 每个 mobileAppContent 都可以具有多个 mobileAppContentFile。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: fd09faa187f6621f07d2811a90ca706a6da24db6
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49281066"
---
# <a name="mobileappcontent-resource-type"></a>mobileAppContent 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

包含特定应用版本的内容属性。 每个 mobileAppContent 都可以具有多个 mobileAppContentFile。

## <a name="methods"></a>Methods
|方法|返回类型|Description|
|:---|:---|:---|
|[列出 mobileAppContents](../api/intune-apps-mobileappcontent-list.md)|[mobileAppContent](../resources/intune-apps-mobileappcontent.md) 集合|列出 [mobileAppContent](../resources/intune-apps-mobileappcontent.md) 对象的属性和关系。|
|[获取 mobileAppContent](../api/intune-apps-mobileappcontent-get.md)|[mobileAppContent](../resources/intune-apps-mobileappcontent.md)|读取 [mobileAppContent](../resources/intune-apps-mobileappcontent.md) 对象的属性和关系。|
|[创建 mobileAppContent](../api/intune-apps-mobileappcontent-create.md)|[mobileAppContent](../resources/intune-apps-mobileappcontent.md)|创建新的 [mobileAppContent](../resources/intune-apps-mobileappcontent.md) 对象。|
|[删除 mobileAppContent](../api/intune-apps-mobileappcontent-delete.md)|无|删除 [mobileAppContent](../resources/intune-apps-mobileappcontent.md)。|
|[更新 mobileAppContent](../api/intune-apps-mobileappcontent-update.md)|[mobileAppContent](../resources/intune-apps-mobileappcontent.md)|更新 [mobileAppContent](../resources/intune-apps-mobileappcontent.md) 对象的属性。|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|id|字符串|应用内容版本。|

## <a name="relationships"></a>关系
|关系|类型|Description|
|:---|:---|:---|
|files|[mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) 集合|此应用内容版本的文件列表。|
|containedApps|[mobileContainedApp](../resources/intune-apps-mobilecontainedapp.md) 集合|充当包的 MobileLobApp 中包含的应用程序的集合。|

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileAppContent"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppContent",
  "id": "String (identifier)"
}
```




