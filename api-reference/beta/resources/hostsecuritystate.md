---
title: hostSecurityState 资源类型
description: " > **重要说明：** Microsoft Graph 中 /beta 版本下的 API 是预览版，可能会发生变化。 不支持在生产应用程序中使用这些 API。"
localization_priority: Normal
doc_type: resourcePageType
ms.prod: ''
author: preetikr
ms.openlocfilehash: a76797ed5660a80e1bbce73609617844de326863
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48013592"
---
# <a name="hostsecuritystate-resource-type"></a>hostSecurityState 资源类型

命名空间：microsoft.graph

 [!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

包含有关主机 (的状态信息，包括设备、计算机等) 。

## <a name="properties"></a>属性

| 属性   | 类型|说明|
|:---------------|:--------|:----------|
|域名|String|主机 FQDN (完全限定的域名)  (例如，machine.company.com) 。|
|isAzureAadJoined|Boolean|如此如果主机已加入域到 Azure Active Directory 域服务。|
|isAzureAadRegistered|Boolean|如果主机注册到 Azure Active Directory 设备注册 (BYOD 设备-即不是由企业) 完全管理的，则该属性值为 True。|
|isHybridAzureDomainJoined|Boolean|如此如果主机已加入域到本地 Active Directory 域。|
|netBiosName|String|本地主机名，不包含 DNS 域名。|
|os|String|主机操作系统。  (例如，Windows10、MacOS、RHEL 等 ) 。|
|privateIpAddress|String|专用 (不可路由) IPv4 或 IPv6 地址 (请参阅在发出警报时) [RFC 1918](https://tools.ietf.org/html/rfc1918) 。|
|publicIpAddress|String|可公开路由的 IPv4 或 IPv6 地址 (请参阅 [RFC 1918](https://tools.ietf.org/html/rfc1918)) 警报时间。|
|riskScore|String|主机的提供程序生成/计算的风险分数。  建议的值范围为0-1，这相当于一个百分比。|

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.hostSecurityState"
}-->

```json
{
  "fqdn": "String",
  "isAzureAadJoined": true,
  "isAzureAadRegistered": true,
  "isHybridAzureDomainJoined": true,
  "netBiosName": "String",
  "os": "String",
  "privateIpAddress": "String",
  "publicIpAddress": "String",
  "riskScore": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "hostSecurityState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


