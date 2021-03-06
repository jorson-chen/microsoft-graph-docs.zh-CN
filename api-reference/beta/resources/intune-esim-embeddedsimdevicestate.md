---
title: embeddedSIMDeviceState 资源类型
description: 介绍与设备相关的嵌入的 SIM 激活代码部署状态。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 44f5980881a52428efb655c5f37c8579d445fa84
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49288423"
---
# <a name="embeddedsimdevicestate-resource-type"></a>embeddedSIMDeviceState 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

介绍与设备相关的嵌入的 SIM 激活代码部署状态。

## <a name="methods"></a>Methods
|方法|返回类型|Description|
|:---|:---|:---|
|[列出 embeddedSIMDeviceStates](../api/intune-esim-embeddedsimdevicestate-list.md)|[embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md) 集合|列出 [embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md) 对象的属性和关系。|
|[获取 embeddedSIMDeviceState](../api/intune-esim-embeddedsimdevicestate-get.md)|[embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md)|读取 [embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md) 对象的属性和关系。|
|[创建 embeddedSIMDeviceState](../api/intune-esim-embeddedsimdevicestate-create.md)|[embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md)|创建新的 [embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md) 对象。|
|[删除 embeddedSIMDeviceState](../api/intune-esim-embeddedsimdevicestate-delete.md)|无|删除 [embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md)。|
|[更新 embeddedSIMDeviceState](../api/intune-esim-embeddedsimdevicestate-update.md)|[embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md)|更新 [embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md) 对象的属性。|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|id|字符串|嵌入的 SIM 卡设备状态的唯一标识符。 创建时分配的系统生成值。|
|createdDateTime|DateTimeOffset|嵌入的 SIM 设备状态的创建时间。 生成的服务端。|
|modifiedDateTime|DateTimeOffset|上次修改嵌入的 SIM 设备状态的时间。 更新了服务端。|
|lastSyncDateTime|DateTimeOffset|嵌入的 SIM 设备上次签入的时间。 更新了服务端。|
|universalIntegratedCircuitCardIdentifier|字符串|通用集成电路卡标识符 (UICCID) 标识配置文件要部署到的硬件。|
|deviceName|String|订阅预配到的设备名称，例如，桌面 JOE|
|userName|String|订阅预配到的用户名，例如 joe@contoso.com|
|state|[embeddedSIMDeviceStateValue](../resources/intune-esim-embeddedsimdevicestatevalue.md)|应用于设备的配置文件操作的状态。 可取值为：`notEvaluated`、`failed`、`installing`、`installed`、`deleting`、`error`、`deleted`、`removedByUser`。|
|stateDetails|字符串|设置状态的字符串说明。|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.embeddedSIMDeviceState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.embeddedSIMDeviceState",
  "id": "String (identifier)",
  "createdDateTime": "String (timestamp)",
  "modifiedDateTime": "String (timestamp)",
  "lastSyncDateTime": "String (timestamp)",
  "universalIntegratedCircuitCardIdentifier": "String",
  "deviceName": "String",
  "userName": "String",
  "state": "String",
  "stateDetails": "String"
}
```




