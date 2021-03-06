---
title: deviceAndAppManagementAssignmentFilter 资源类型
description: 包含用于工作分配筛选器的属性的类。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 89cafdf4d01b4652ed5a59ebba57b9bbb835b799
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49300960"
---
# <a name="deviceandappmanagementassignmentfilter-resource-type"></a>deviceAndAppManagementAssignmentFilter 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

包含用于工作分配筛选器的属性的类。

## <a name="methods"></a>Methods
|方法|返回类型|Description|
|:---|:---|:---|
|[列出 deviceAndAppManagementAssignmentFilters](../api/intune-policyset-deviceandappmanagementassignmentfilter-list.md)|[deviceAndAppManagementAssignmentFilter](../resources/intune-policyset-deviceandappmanagementassignmentfilter.md) 集合|列出 [deviceAndAppManagementAssignmentFilter](../resources/intune-policyset-deviceandappmanagementassignmentfilter.md) 对象的属性和关系。|
|[获取 deviceAndAppManagementAssignmentFilter](../api/intune-policyset-deviceandappmanagementassignmentfilter-get.md)|[deviceAndAppManagementAssignmentFilter](../resources/intune-policyset-deviceandappmanagementassignmentfilter.md)|读取 [deviceAndAppManagementAssignmentFilter](../resources/intune-policyset-deviceandappmanagementassignmentfilter.md) 对象的属性和关系。|
|[创建 deviceAndAppManagementAssignmentFilter](../api/intune-policyset-deviceandappmanagementassignmentfilter-create.md)|[deviceAndAppManagementAssignmentFilter](../resources/intune-policyset-deviceandappmanagementassignmentfilter.md)|创建新的 [deviceAndAppManagementAssignmentFilter](../resources/intune-policyset-deviceandappmanagementassignmentfilter.md) 对象。|
|[删除 deviceAndAppManagementAssignmentFilter](../api/intune-policyset-deviceandappmanagementassignmentfilter-delete.md)|无|删除 [deviceAndAppManagementAssignmentFilter](../resources/intune-policyset-deviceandappmanagementassignmentfilter.md)。|
|[更新 deviceAndAppManagementAssignmentFilter](../api/intune-policyset-deviceandappmanagementassignmentfilter-update.md)|[deviceAndAppManagementAssignmentFilter](../resources/intune-policyset-deviceandappmanagementassignmentfilter.md)|更新 [deviceAndAppManagementAssignmentFilter](../resources/intune-policyset-deviceandappmanagementassignmentfilter.md) 对象的属性。|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|id|字符串|工作分配筛选器的键。|
|createdDateTime|DateTimeOffset|工作分配筛选器的创建时间。|
|lastModifiedDateTime|DateTimeOffset|工作分配筛选器的上次修改时间。|
|displayName|字符串|工作分配筛选器的 DisplayName。|
|description|字符串|工作分配筛选器的说明。|
|平台|[devicePlatformType](../resources/intune-shared-deviceplatformtype.md)|工作分配筛选器将适用的设备的平台类型。 可取值为：`android`、`androidForWork`、`iOS`、`macOS`、`windowsPhone81`、`windows81AndLater`、`windows10AndLater`、`androidWorkProfile`、`unknown`。|
|标尺|字符串|工作分配筛选器的规则定义。|
|roleScopeTags|String 集合|RoleScopeTags 的工作分配筛选器。|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentFilter"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceAndAppManagementAssignmentFilter",
  "id": "String (identifier)",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "description": "String",
  "platform": "String",
  "rule": "String",
  "roleScopeTags": [
    "String"
  ]
}
```




