---
title: policySetAssignment 资源类型
description: 包含用于 PolicySet 分配的属性的类。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 51cce7ad66c1374f27c861b1db602ffe6122088c
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49288024"
---
# <a name="policysetassignment-resource-type"></a>policySetAssignment 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

包含用于 PolicySet 分配的属性的类。

## <a name="methods"></a>Methods
|方法|返回类型|Description|
|:---|:---|:---|
|[列出 policySetAssignments](../api/intune-policyset-policysetassignment-list.md)|[policySetAssignment](../resources/intune-policyset-policysetassignment.md) 集合|列出 [policySetAssignment](../resources/intune-policyset-policysetassignment.md) 对象的属性和关系。|
|[获取 policySetAssignment](../api/intune-policyset-policysetassignment-get.md)|[policySetAssignment](../resources/intune-policyset-policysetassignment.md)|读取 [policySetAssignment](../resources/intune-policyset-policysetassignment.md) 对象的属性和关系。|
|[创建 policySetAssignment](../api/intune-policyset-policysetassignment-create.md)|[policySetAssignment](../resources/intune-policyset-policysetassignment.md)|创建新的 [policySetAssignment](../resources/intune-policyset-policysetassignment.md) 对象。|
|[删除 policySetAssignment](../api/intune-policyset-policysetassignment-delete.md)|无|删除 [policySetAssignment](../resources/intune-policyset-policysetassignment.md)。|
|[更新 policySetAssignment](../api/intune-policyset-policysetassignment-update.md)|[policySetAssignment](../resources/intune-policyset-policysetassignment.md)|更新 [policySetAssignment](../resources/intune-policyset-policysetassignment.md) 对象的属性。|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|id|字符串|PolicySetAssignment 的键。|
|lastModifiedDateTime|DateTimeOffset|PolicySetAssignment 的上次修改时间。|
|target|[deviceAndAppManagementAssignmentTarget](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|PolicySetAssignment 的目标组|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.policySetAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.policySetAssignment",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "target": {
    "@odata.type": "microsoft.graph.allDevicesAssignmentTarget",
    "deviceAndAppManagementAssignmentFilterId": "String",
    "deviceAndAppManagementAssignmentFilterType": "String"
  }
}
```




