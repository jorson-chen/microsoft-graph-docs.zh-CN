---
title: deviceManagementScript 资源类型
description: Intune 将向客户提供在已注册的 windows 10 Azure Active Directory 联接设备上运行其 Powershell 脚本的功能。 脚本可以运行一次，也可以定期运行。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: 1ed2e4a12d7070a93bd47662714d646a640989c1
ms.sourcegitcommit: 86903a4730bbd825eabb7f0a1b2429723cc8b1e6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/26/2019
ms.locfileid: "37199934"
---
# <a name="devicemanagementscript-resource-type"></a>deviceManagementScript 资源类型

> **重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

Intune 将向客户提供在已注册的 windows 10 Azure Active Directory 联接设备上运行其 Powershell 脚本的功能。 脚本可以运行一次，也可以定期运行。

## <a name="methods"></a>方法
|方法|返回类型|说明|
|:---|:---|:---|
|[列出 deviceManagementScripts](../api/intune-shared-devicemanagementscript-list.md)|[deviceManagementScript](../resources/intune-shared-devicemanagementscript.md)集合|列出[deviceManagementScript](../resources/intune-shared-devicemanagementscript.md)对象的属性和关系。|
|[获取 deviceManagementScript](../api/intune-shared-devicemanagementscript-get.md)|[deviceManagementScript](../resources/intune-shared-devicemanagementscript.md)|读取[deviceManagementScript](../resources/intune-shared-devicemanagementscript.md)对象的属性和关系。|
|[创建 deviceManagementScript](../api/intune-shared-devicemanagementscript-create.md)|[deviceManagementScript](../resources/intune-shared-devicemanagementscript.md)|创建新的[deviceManagementScript](../resources/intune-shared-devicemanagementscript.md)对象。|
|[删除 deviceManagementScript](../api/intune-shared-devicemanagementscript-delete.md)|无|删除[deviceManagementScript](../resources/intune-shared-devicemanagementscript.md)。|
|[更新 deviceManagementScript](../api/intune-shared-devicemanagementscript-update.md)|[deviceManagementScript](../resources/intune-shared-devicemanagementscript.md)|更新[deviceManagementScript](../resources/intune-shared-devicemanagementscript.md)对象的属性。|
|**设备管理**|
|[分配操作](../api/intune-shared-devicemanagementscript-assign.md)|无|尚未记录|
|**策略集**|
|[hasPayloadLinks 操作](../api/intune-shared-devicemanagementscript-haspayloadlinks.md)|[hasPayloadLinkResultItem](../resources/intune-policyset-haspayloadlinkresultitem.md)集合|尚未记录|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|id|字符串|设备管理脚本的唯一标识符。|
|displayName|字符串|设备管理脚本的名称。|
|说明|String|设备管理脚本的可选说明。|
|runSchedule|[runSchedule](../resources/intune-devices-runschedule.md)|脚本运行的间隔。 如果未定义，脚本将运行一次|
|scriptContent|Binary|脚本内容。|
|createdDateTime|DateTimeOffset|设备管理脚本的创建日期和时间。 此属性是只读的。|
|lastModifiedDateTime|DateTimeOffset|上次修改设备管理脚本的日期和时间。 此属性是只读的。|
|runAsAccount|[runAsAccountType](../resources/intune-shared-runasaccounttype.md)|指示执行上下文的类型。 可取值为：`system`、`user`。|
|enforceSignatureCheck|Boolean|指示是否需要检查脚本签名。|
|fileName|String|脚本文件名。|
|roleScopeTagIds|String collection|此 PowerShellScript 实例的范围标记 Id 的列表。|
|runAs32Bit|Boolean|一个指示 PowerShell 脚本是否应作为32位运行的值|

## <a name="relationships"></a>关系
|关系|类型|说明|
|:---|:---|:---|
|**设备管理**|
|groupAssignments|deviceManagementScriptGroupAssignment 集合|设备管理脚本的组分配的列表。|
|assignments|deviceManagementScriptAssignment 集合|设备管理脚本的组分配的列表。|
|runSummary|deviceManagementScriptRunSummary|设备管理脚本的运行摘要。|
|deviceRunStates|deviceManagementScriptDeviceState 集合|此脚本在所有设备上的运行状态列表。|
|userRunStates|deviceManagementScriptUserState 集合|此脚本在所有用户中的运行状态列表。|

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagementScript"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementScript",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "runSchedule": {
    "@odata.type": "microsoft.graph.runSchedule"
  },
  "scriptContent": "binary",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "runAsAccount": "String",
  "enforceSignatureCheck": true,
  "fileName": "String",
  "roleScopeTagIds": [
    "String"
  ],
  "runAs32Bit": true
}
```


