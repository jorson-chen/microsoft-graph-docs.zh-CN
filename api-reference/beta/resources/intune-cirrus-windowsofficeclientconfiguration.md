---
title: windowsOfficeClientConfiguration 资源类型
description: 描述 Windows 的 office 策略设置的实体。
localization_priority: Normal
author: dougeby
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: f13a84fa242c2728f03c9bc392dea4d858b8f6b0
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49294989"
---
# <a name="windowsofficeclientconfiguration-resource-type"></a>windowsOfficeClientConfiguration 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

描述 Windows 的 office 策略设置的实体。

继承自 [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)

## <a name="methods"></a>Methods
|方法|返回类型|Description|
|:---|:---|:---|
|[列出 windowsOfficeClientConfigurations](../api/intune-cirrus-windowsofficeclientconfiguration-list.md)|[windowsOfficeClientConfiguration](../resources/intune-cirrus-windowsofficeclientconfiguration.md) 集合|列出 [windowsOfficeClientConfiguration](../resources/intune-cirrus-windowsofficeclientconfiguration.md) 对象的属性和关系。|
|[获取 windowsOfficeClientConfiguration](../api/intune-cirrus-windowsofficeclientconfiguration-get.md)|[windowsOfficeClientConfiguration](../resources/intune-cirrus-windowsofficeclientconfiguration.md)|读取 [windowsOfficeClientConfiguration](../resources/intune-cirrus-windowsofficeclientconfiguration.md) 对象的属性和关系。|
|[创建 windowsOfficeClientConfiguration](../api/intune-cirrus-windowsofficeclientconfiguration-create.md)|[windowsOfficeClientConfiguration](../resources/intune-cirrus-windowsofficeclientconfiguration.md)|创建新的 [windowsOfficeClientConfiguration](../resources/intune-cirrus-windowsofficeclientconfiguration.md) 对象。|
|[删除 windowsOfficeClientConfiguration](../api/intune-cirrus-windowsofficeclientconfiguration-delete.md)|无|删除 [windowsOfficeClientConfiguration](../resources/intune-cirrus-windowsofficeclientconfiguration.md)。|
|[更新 windowsOfficeClientConfiguration](../api/intune-cirrus-windowsofficeclientconfiguration-update.md)|[windowsOfficeClientConfiguration](../resources/intune-cirrus-windowsofficeclientconfiguration.md)|更新 [windowsOfficeClientConfiguration](../resources/intune-cirrus-windowsofficeclientconfiguration.md) 对象的属性。|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|id|字符串|Office 客户端配置策略的 Id。 继承自 [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)|
|userPreferencePayload|Stream|首选项设置 JSON string 二进制格式，则用户可以重写这些值。 继承自 [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)|
|policyPayload|Stream|策略设置 JSON string 二进制格式，用户不能更改这些值。 继承自 [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)|
|description|字符串|管理员提供的 office 客户端配置策略的说明。 继承自 [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)|
|displayName|字符串|管理员提供的 office 客户端配置策略的名称。 继承自 [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)|
|priority|Int32|对于租户下的每个策略，优先级值应为唯一值，并将用于冲突解决，较低值意味着优先级较高。 继承自 [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)|
|lastModifiedDateTime|日期时间|策略的上次修改日期时间戳。 继承自 [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)|
|userCheckinSummary|[officeUserCheckinSummary](../resources/intune-cirrus-officeusercheckinsummary.md)|策略的用户签入摘要。 继承自 [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)|
|checkinStatuses|[officeClientCheckinStatus](../resources/intune-cirrus-officeclientcheckinstatus.md) 集合|Office 客户端签入状态的列表。 继承自 [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)|

## <a name="relationships"></a>关系
|关系|类型|Description|
|:---|:---|:---|
|assignments|[officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) 集合|策略的组分配列表。 继承自 [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)|

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsOfficeClientConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsOfficeClientConfiguration",
  "id": "String (identifier)",
  "userPreferencePayload": "<Unknown Primitive Type Edm.Stream>",
  "policyPayload": "<Unknown Primitive Type Edm.Stream>",
  "description": "String",
  "displayName": "String",
  "priority": 1024,
  "userCheckinSummary": {
    "@odata.type": "microsoft.graph.officeUserCheckinSummary",
    "succeededUserCount": 1024,
    "failedUserCount": 1024
  },
  "checkinStatuses": [
    {
      "@odata.type": "microsoft.graph.officeClientCheckinStatus",
      "userPrincipalName": "String",
      "deviceName": "String",
      "devicePlatform": "String",
      "devicePlatformVersion": "String",
      "wasSuccessful": true,
      "userId": "String",
      "checkinDateTime": "String (timestamp)",
      "errorMessage": "String",
      "appliedPolicies": [
        "String"
      ]
    }
  ]
}
```




