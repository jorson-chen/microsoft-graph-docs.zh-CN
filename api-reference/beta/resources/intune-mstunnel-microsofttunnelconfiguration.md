---
title: microsoftTunnelConfiguration 资源类型
description: 表示 Microsoft 隧道设置集合的实体
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 4cd85d798085ed5d8caf12ae2becc58e2bf10a33
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49301541"
---
# <a name="microsofttunnelconfiguration-resource-type"></a>microsoftTunnelConfiguration 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

表示 Microsoft 隧道设置集合的实体

## <a name="methods"></a>方法
|方法|返回类型|说明|
|:---|:---|:---|
|[列出 microsoftTunnelConfigurations](../api/intune-mstunnel-microsofttunnelconfiguration-list.md)|[microsoftTunnelConfiguration](../resources/intune-mstunnel-microsofttunnelconfiguration.md) 集合|列出 [microsoftTunnelConfiguration](../resources/intune-mstunnel-microsofttunnelconfiguration.md) 对象的属性和关系。|
|[获取 microsoftTunnelConfiguration](../api/intune-mstunnel-microsofttunnelconfiguration-get.md)|[microsoftTunnelConfiguration](../resources/intune-mstunnel-microsofttunnelconfiguration.md)|读取 [microsoftTunnelConfiguration](../resources/intune-mstunnel-microsofttunnelconfiguration.md) 对象的属性和关系。|
|[创建 microsoftTunnelConfiguration](../api/intune-mstunnel-microsofttunnelconfiguration-create.md)|[microsoftTunnelConfiguration](../resources/intune-mstunnel-microsofttunnelconfiguration.md)|创建新的 [microsoftTunnelConfiguration](../resources/intune-mstunnel-microsofttunnelconfiguration.md) 对象。|
|[删除 microsoftTunnelConfiguration](../api/intune-mstunnel-microsofttunnelconfiguration-delete.md)|无|删除 [microsoftTunnelConfiguration](../resources/intune-mstunnel-microsofttunnelconfiguration.md)。|
|[更新 microsoftTunnelConfiguration](../api/intune-mstunnel-microsofttunnelconfiguration-update.md)|[microsoftTunnelConfiguration](../resources/intune-mstunnel-microsofttunnelconfiguration.md)|更新 [microsoftTunnelConfiguration](../resources/intune-mstunnel-microsofttunnelconfiguration.md) 对象的属性。|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|id|字符串|MicrosoftTunnelConfiguration 的 Id|
|displayName|字符串|MicrosoftTunnelConfiguration 的显示名称|
|description|字符串|MicrosoftTunnelConfiguration 的说明|
|network|字符串|将用于为客户端分配虚拟地址的子网|
|dnsServers|String 集合|客户端将使用的 DNS 服务器|
|defaultDomainSuffix|字符串|客户端将使用的默认域附录|
|routesInclude|String 集合|将由服务器路由的将|
|routesExclude|String 集合|将不会由服务器路由的路由的子集|
|splitDNS|String 集合|将使用所提供的 dns 服务器进行解析的域|
|listenPort|Int32|TCP 和 UPD 将在服务器上侦听的端口|
|advancedSettings|[keyValuePair](../resources/intune-shared-keyvaluepair.md) 集合|可能适用于服务器的其他设置|
|lastUpdateDateTime|DateTimeOffset|上次更新 MicrosoftTunnelConfiguration 的时间|
|roleScopeTagIds|String 集合|此实体实例的范围标记列表。|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.microsoftTunnelConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.microsoftTunnelConfiguration",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "network": "String",
  "dnsServers": [
    "String"
  ],
  "defaultDomainSuffix": "String",
  "routesInclude": [
    "String"
  ],
  "routesExclude": [
    "String"
  ],
  "splitDNS": [
    "String"
  ],
  "listenPort": 1024,
  "advancedSettings": [
    {
      "@odata.type": "microsoft.graph.keyValuePair",
      "name": "String",
      "value": "String"
    }
  ],
  "lastUpdateDateTime": "String (timestamp)",
  "roleScopeTagIds": [
    "String"
  ]
}
```




