---
title: managementCondition 资源类型
description: 管理条件是可以动态触发的事件，如地域时限、时限和网络时限。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 52cb6a93270ecdbe74c16b6a96e1386f01c3b27e
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49299063"
---
# <a name="managementcondition-resource-type"></a>managementCondition 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

管理条件是可以动态触发的事件，如地域时限、时限和网络时限。

## <a name="methods"></a>Methods
|方法|返回类型|Description|
|:---|:---|:---|
|[列出 managementConditions](../api/intune-fencing-managementcondition-list.md)|[managementCondition](../resources/intune-fencing-managementcondition.md) 集合|列出 [managementCondition](../resources/intune-fencing-managementcondition.md) 对象的属性和关系。|
|[获取 managementCondition](../api/intune-fencing-managementcondition-get.md)|[managementCondition](../resources/intune-fencing-managementcondition.md)|读取 [managementCondition](../resources/intune-fencing-managementcondition.md) 对象的属性和关系。|
|[getManagementConditionsForPlatform 函数](../api/intune-fencing-managementcondition-getmanagementconditionsforplatform.md)|[managementCondition](../resources/intune-fencing-managementcondition.md) 集合|尚未记录|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|id|字符串|管理条件的唯一标识符。 创建时分配的系统生成值。|
|uniqueName|字符串|管理条件的唯一名称。 在管理条件表达式中使用。|
|displayName|字符串|管理条件的管理员定义名称。|
|description|字符串|管理条件的管理员定义的说明。|
|createdDateTime|DateTimeOffset|管理条件的创建时间。 生成的服务端。|
|modifiedDateTime|DateTimeOffset|上次修改管理条件的时间。 更新了服务端。|
|eTag|String|管理条件的 ETag。 更新了服务端。|
|applicablePlatforms|[devicePlatformType](../resources/intune-shared-deviceplatformtype.md) 集合|适用于此管理条件的平台。|

## <a name="relationships"></a>关系
|关系|类型|Description|
|:---|:---|:---|
|managementConditionStatements|[managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md) 集合|与管理条件相关联的管理条件语句。|

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managementCondition"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managementCondition",
  "id": "String (identifier)",
  "uniqueName": "String",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "modifiedDateTime": "String (timestamp)",
  "eTag": "String",
  "applicablePlatforms": [
    "String"
  ]
}
```




