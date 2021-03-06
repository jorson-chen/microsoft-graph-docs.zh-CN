---
title: userExperienceAnalyticsRegressionSummary 资源类型
description: User experience analytics 回归汇总摘要。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 23db3acb1fde40f8f43e9049a5dc82c120cdbdb1
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49256409"
---
# <a name="userexperienceanalyticsregressionsummary-resource-type"></a>userExperienceAnalyticsRegressionSummary 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

User experience analytics 回归汇总摘要。

## <a name="methods"></a>方法
|方法|返回类型|说明|
|:---|:---|:---|
|[获取 userExperienceAnalyticsRegressionSummary](../api/intune-devices-userexperienceanalyticsregressionsummary-get.md)|[userExperienceAnalyticsRegressionSummary](../resources/intune-devices-userexperienceanalyticsregressionsummary.md)|读取 [userExperienceAnalyticsRegressionSummary](../resources/intune-devices-userexperienceanalyticsregressionsummary.md) 对象的属性和关系。|
|[更新 userExperienceAnalyticsRegressionSummary](../api/intune-devices-userexperienceanalyticsregressionsummary-update.md)|[userExperienceAnalyticsRegressionSummary](../resources/intune-devices-userexperienceanalyticsregressionsummary.md)|更新 [userExperienceAnalyticsRegressionSummary](../resources/intune-devices-userexperienceanalyticsregressionsummary.md) 对象的属性。|
|[summarizeDeviceRegressionPerformance 函数](../api/intune-devices-userexperienceanalyticsregressionsummary-summarizedeviceregressionperformance.md)|[userExperienceAnalyticsRegressionSummary](../resources/intune-devices-userexperienceanalyticsregressionsummary.md)|尚未记录|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|id|String|User experience analytics 回归摘要的唯一标识符。|

## <a name="relationships"></a>关系
|关系|类型|描述|
|:---|:---|:---|
|modelRegression|[userExperienceAnalyticsMetric](../resources/intune-devices-userexperienceanalyticsmetric.md) 集合|User experience analytics 模型回归的指标值。|
|manufacturerRegression|[userExperienceAnalyticsMetric](../resources/intune-devices-userexperienceanalyticsmetric.md) 集合|User experience analytics 制造商回归的指标值。|
|operatingSystemRegression|[userExperienceAnalyticsMetric](../resources/intune-devices-userexperienceanalyticsmetric.md) 集合|User experience analytics 操作系统回归的指标值。|

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.userExperienceAnalyticsRegressionSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.userExperienceAnalyticsRegressionSummary",
  "id": "String (identifier)"
}
```




