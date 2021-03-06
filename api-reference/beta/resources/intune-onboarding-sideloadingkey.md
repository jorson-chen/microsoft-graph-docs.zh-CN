---
title: sideLoadingKey 资源类型
description: 对于租户，Windows 8 和8.1 设备需要 SideLoadingKey 实体为 intall 的业务线应用程序。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: a37eae80f3628f5fa8952cf8c2cde225e4f5fc0c
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49266457"
---
# <a name="sideloadingkey-resource-type"></a>sideLoadingKey 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

对于租户，Windows 8 和8.1 设备需要 SideLoadingKey 实体为 intall 的业务线应用程序。

## <a name="methods"></a>方法
|方法|返回类型|说明|
|:---|:---|:---|
|[列出 sideLoadingKeies](../api/intune-onboarding-sideloadingkey-list.md)|[sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md) 集合|列出 [sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md) 对象的属性和关系。|
|[获取 sideLoadingKey](../api/intune-onboarding-sideloadingkey-get.md)|[sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md)|读取 [sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md) 对象的属性和关系。|
|[创建 sideLoadingKey](../api/intune-onboarding-sideloadingkey-create.md)|[sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md)|创建新的 [sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md) 对象。|
|[删除 sideLoadingKey](../api/intune-onboarding-sideloadingkey-delete.md)|无|删除 [sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md)。|
|[更新 sideLoadingKey](../api/intune-onboarding-sideloadingkey-update.md)|[sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md)|更新 [sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md) 对象的属性。|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|id|字符串|侧加载密钥唯一 Id。|
|value|String|侧加载密钥值，它是一个5x5 值，由 hiphens 分隔。|
|displayName|字符串|向 It 专业管理员显示的侧加载密钥名称。|
|description|字符串|向 It 专业管理员显示的侧加载密钥说明。|
|totalActivation|Int32|向 It 专业管理员显示的端加载密钥总激活数。|
|lastUpdatedDateTime|字符串|向 It 专业管理员显示的侧加载密钥上次更新日期。|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.sideLoadingKey"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.sideLoadingKey",
  "id": "String (identifier)",
  "value": "String",
  "displayName": "String",
  "description": "String",
  "totalActivation": 1024,
  "lastUpdatedDateTime": "String"
}
```




