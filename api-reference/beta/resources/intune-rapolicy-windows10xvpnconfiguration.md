---
title: windows10XVpnConfiguration 资源类型
description: Windows X VPN 配置文件
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: cce0be552b22e52476ee704606bd43e7c20f4ec7
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49301852"
---
# <a name="windows10xvpnconfiguration-resource-type"></a>windows10XVpnConfiguration 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

Windows X VPN 配置文件


继承自 [deviceManagementResourceAccessProfileBase](../resources/intune-rapolicy-devicemanagementresourceaccessprofilebase.md)

## <a name="methods"></a>Methods
|方法|返回类型|Description|
|:---|:---|:---|
|[列出 windows10XVpnConfigurations](../api/intune-rapolicy-windows10xvpnconfiguration-list.md)|[windows10XVpnConfiguration](../resources/intune-rapolicy-windows10xvpnconfiguration.md) 集合|列出 [windows10XVpnConfiguration](../resources/intune-rapolicy-windows10xvpnconfiguration.md) 对象的属性和关系。|
|[获取 windows10XVpnConfiguration](../api/intune-rapolicy-windows10xvpnconfiguration-get.md)|[windows10XVpnConfiguration](../resources/intune-rapolicy-windows10xvpnconfiguration.md)|读取 [windows10XVpnConfiguration](../resources/intune-rapolicy-windows10xvpnconfiguration.md) 对象的属性和关系。|
|[创建 windows10XVpnConfiguration](../api/intune-rapolicy-windows10xvpnconfiguration-create.md)|[windows10XVpnConfiguration](../resources/intune-rapolicy-windows10xvpnconfiguration.md)|创建新的 [windows10XVpnConfiguration](../resources/intune-rapolicy-windows10xvpnconfiguration.md) 对象。|
|[删除 windows10XVpnConfiguration](../api/intune-rapolicy-windows10xvpnconfiguration-delete.md)|无|删除 [windows10XVpnConfiguration](../resources/intune-rapolicy-windows10xvpnconfiguration.md)。|
|[更新 windows10XVpnConfiguration](../api/intune-rapolicy-windows10xvpnconfiguration-update.md)|[windows10XVpnConfiguration](../resources/intune-rapolicy-windows10xvpnconfiguration.md)|更新 [windows10XVpnConfiguration](../resources/intune-rapolicy-windows10xvpnconfiguration.md) 对象的属性。|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|id|字符串|从[DeviceManagementResourceAccessProfileBase](../resources/intune-rapolicy-devicemanagementresourceaccessprofilebase.md)继承的配置文件标识符|
|version|Int32|继承自[deviceManagementResourceAccessProfileBase](../resources/intune-rapolicy-devicemanagementresourceaccessprofilebase.md)的配置文件的版本|
|displayName|字符串|从[DeviceManagementResourceAccessProfileBase](../resources/intune-rapolicy-devicemanagementresourceaccessprofilebase.md)继承的配置文件显示名称|
|description|字符串|从[DeviceManagementResourceAccessProfileBase](../resources/intune-rapolicy-devicemanagementresourceaccessprofilebase.md)继承的配置文件说明|
|creationDateTime|DateTimeOffset|已创建从[DeviceManagementResourceAccessProfileBase](../resources/intune-rapolicy-devicemanagementresourceaccessprofilebase.md)继承的 DateTime 配置文件|
|lastModifiedDateTime|DateTimeOffset|上次修改的日期时间配置文件继承自 [deviceManagementResourceAccessProfileBase](../resources/intune-rapolicy-devicemanagementresourceaccessprofilebase.md)|
|roleScopeTagIds|String 集合|继承自[deviceManagementResourceAccessProfileBase](../resources/intune-rapolicy-devicemanagementresourceaccessprofilebase.md)的范围标记|
|authenticationCertificateId|Guid|身份验证证书的 ID|
|customXmlFileName|字符串|自定义 Xml 文件名。|
|customXml|Binary|配置 VPN 连接的自定义 XML 命令。  (UTF8 字节编码) |

## <a name="relationships"></a>关系
|关系|类型|Description|
|:---|:---|:---|
|assignments|[deviceManagementResourceAccessProfileAssignment](../resources/intune-rapolicy-devicemanagementresourceaccessprofileassignment.md) 集合|设备配置文件的分配列表。 继承自 [deviceManagementResourceAccessProfileBase](../resources/intune-rapolicy-devicemanagementresourceaccessprofilebase.md)|

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windows10XVpnConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windows10XVpnConfiguration",
  "id": "String (identifier)",
  "version": 1024,
  "displayName": "String",
  "description": "String",
  "creationDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "roleScopeTagIds": [
    "String"
  ],
  "authenticationCertificateId": "Guid",
  "customXmlFileName": "String",
  "customXml": "binary"
}
```




