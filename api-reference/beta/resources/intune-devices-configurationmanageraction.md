---
title: configurationManagerAction 资源类型
description: Action triggerConfigurationManagerAction 的参数
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: edaefe3dfcb21052fabdeecbe75267e7a7af2570
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49214657"
---
# <a name="configurationmanageraction-resource-type"></a>configurationManagerAction 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

Action triggerConfigurationManagerAction 的参数

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|action|[configurationManagerActionType](../resources/intune-devices-configurationmanageractiontype.md)|要在 Configuration Manager 客户端上触发的操作类型。 可取值为：`refreshMachinePolicy`、`refreshUserPolicy`、`wakeUpClient`、`appEvaluation`。|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.configurationManagerAction"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.configurationManagerAction",
  "action": "String"
}
```




