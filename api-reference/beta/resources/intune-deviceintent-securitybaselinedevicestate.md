---
title: securityBaselineDeviceState 资源类型
description: 设备安全基准的安全基准合规性状态摘要。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 9188446a5c270b7dc25e21b9880ecec479dfa90f
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49209330"
---
# <a name="securitybaselinedevicestate-resource-type"></a>securityBaselineDeviceState 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

设备安全基准的安全基准合规性状态摘要。

## <a name="methods"></a>方法
|方法|返回类型|说明|
|:---|:---|:---|
|[列出 securityBaselineDeviceStates](../api/intune-deviceintent-securitybaselinedevicestate-list.md)|[securityBaselineDeviceState](../resources/intune-deviceintent-securitybaselinedevicestate.md) 集合|列出 [securityBaselineDeviceState](../resources/intune-deviceintent-securitybaselinedevicestate.md) 对象的属性和关系。|
|[获取 securityBaselineDeviceState](../api/intune-deviceintent-securitybaselinedevicestate-get.md)|[securityBaselineDeviceState](../resources/intune-deviceintent-securitybaselinedevicestate.md)|读取 [securityBaselineDeviceState](../resources/intune-deviceintent-securitybaselinedevicestate.md) 对象的属性和关系。|
|[创建 securityBaselineDeviceState](../api/intune-deviceintent-securitybaselinedevicestate-create.md)|[securityBaselineDeviceState](../resources/intune-deviceintent-securitybaselinedevicestate.md)|创建新的 [securityBaselineDeviceState](../resources/intune-deviceintent-securitybaselinedevicestate.md) 对象。|
|[删除 securityBaselineDeviceState](../api/intune-deviceintent-securitybaselinedevicestate-delete.md)|无|删除 [securityBaselineDeviceState](../resources/intune-deviceintent-securitybaselinedevicestate.md)。|
|[更新 securityBaselineDeviceState](../api/intune-deviceintent-securitybaselinedevicestate-update.md)|[securityBaselineDeviceState](../resources/intune-deviceintent-securitybaselinedevicestate.md)|更新 [securityBaselineDeviceState](../resources/intune-deviceintent-securitybaselinedevicestate.md) 对象的属性。|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|id|String|实体的唯一标识符|
|managedDeviceId|String|Intune 设备 id|
|deviceDisplayName|String|设备的显示名称|
|userPrincipalName|String|用户主体名称|
|state|[securityBaselineComplianceState](../resources/intune-deviceintent-securitybaselinecompliancestate.md)|安全基准合规性状态。 可取值为：`unknown`、`secure`、`notApplicable`、`notSecure`、`error`、`conflict`。|
|lastReportedDateTime|DateTimeOffset|策略报告的上次修改日期时间|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.securityBaselineDeviceState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.securityBaselineDeviceState",
  "id": "String (identifier)",
  "managedDeviceId": "String",
  "deviceDisplayName": "String",
  "userPrincipalName": "String",
  "state": "String",
  "lastReportedDateTime": "String (timestamp)"
}
```




