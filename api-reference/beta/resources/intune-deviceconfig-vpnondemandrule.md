---
title: vpnOnDemandRule 资源类型
description: VPN 按需规则定义。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 648214bac549b13605211aa47d5e12201db02bab
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49299609"
---
# <a name="vpnondemandrule-resource-type"></a>vpnOnDemandRule 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

VPN 按需规则定义。

## <a name="properties"></a>属性
|属性|类型|Description|
|:---|:---|:---|
|ssid|String 集合|网络服务 (Ssid) 设置标识符。|
|dnsSearchDomains|String 集合|DNS 搜索域。|
|probeUrl|字符串|要探测的 URL。 如果此 URL 已成功获取 (返回 200 HTTP 状态代码) 而不进行重定向，则此规则匹配。|
|action|[vpnOnDemandRuleConnectionAction](../resources/intune-deviceconfig-vpnondemandruleconnectionaction.md)|退货. 可取值为：`connect`、`evaluateConnection`、`ignore`、`disconnect`。|
|domainAction|[vpnOnDemandRuleConnectionDomainAction](../resources/intune-deviceconfig-vpnondemandruleconnectiondomainaction.md)|域操作 (仅当操作评估连接) 时才适用。 可取值为：`connectIfNeeded`、`neverConnect`。|
|域|String 集合|域 (仅当操作评估连接) 时才适用。|
|probeRequiredUrl|字符串|探测器必需 Url (仅在操作评估连接时适用，如果需要，DomainAction 将进行连接）) 。|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.vpnOnDemandRule"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.vpnOnDemandRule",
  "ssids": [
    "String"
  ],
  "dnsSearchDomains": [
    "String"
  ],
  "probeUrl": "String",
  "action": "String",
  "domainAction": "String",
  "domains": [
    "String"
  ],
  "probeRequiredUrl": "String"
}
```




