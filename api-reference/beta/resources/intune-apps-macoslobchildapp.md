---
title: macOSLobChildApp 资源类型
description: 包含捆绑包包中的 MacOS LOB 应用程序的属性
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: b3c115e312333a448318fb718140f5b6e8305494
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49281829"
---
# <a name="macoslobchildapp-resource-type"></a>macOSLobChildApp 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

包含捆绑包包中的 MacOS LOB 应用程序的属性

## <a name="properties"></a>属性
|属性|类型|Description|
|:---|:---|:---|
|bundleId|String|标识名称。|
|buildNumber|String|MacOS 业务线 (LoB) 应用程序的内部版本号。|
|versionNumber|String|MacOS 业务线 (LoB) 应用程序的版本号。|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.macOSLobChildApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.macOSLobChildApp",
  "bundleId": "String",
  "buildNumber": "String",
  "versionNumber": "String"
}
```




