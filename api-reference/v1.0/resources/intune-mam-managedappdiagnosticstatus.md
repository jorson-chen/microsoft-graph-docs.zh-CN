---
title: managedAppDiagnosticStatus 资源类型
description: 表示诊断状态。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: c708da33594087b61b1c28e2ebac5b8872541838
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48041307"
---
# <a name="managedappdiagnosticstatus-resource-type"></a>managedAppDiagnosticStatus 资源类型

命名空间：microsoft.graph

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

表示诊断状态。

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|validationName|String|验证友好名称|
|state|String|操作状态|
|mitigationInstruction|String|有关如何降低失败验证的说明|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managedAppDiagnosticStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppDiagnosticStatus",
  "validationName": "String",
  "state": "String",
  "mitigationInstruction": "String"
}
```









