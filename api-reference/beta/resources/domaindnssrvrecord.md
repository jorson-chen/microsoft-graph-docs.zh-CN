---
title: domainDnsSrvRecord 资源类型
description: 表示添加到租户中特定域的 DNS 区域文件中的 SRV 记录。
author: adimitui
localization_priority: Normal
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 6854b30dec759726fefaf93e13ad23a49195e381
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48010325"
---
# <a name="domaindnssrvrecord-resource-type"></a>domainDnsSrvRecord 资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

表示添加到租户中特定域的 DNS 区域文件中的 SRV 记录。 继承自 [DomainDnsRecord](domaindnsrecord.md) 实体。

## <a name="methods"></a>方法
不支持直接向此资源进行查询。 有关如何查询域服务记录的信息，请参阅 [域](domain.md) 主题。

## <a name="properties"></a>属性
| 属性     | 类型   |说明|
|:---------------|:--------|:----------|
|id|String| 分配给此实体的唯一标识符。 不可为 null，只读。|
|isOptional|Boolean| 如果为 false，则客户必须在 DNS 主机上配置 SRV 记录，才能使 Microsoft Online Services 在域中正常运行。 |
|label|String| 配置 DNS 主机上的 SRV 记录的 *name* 属性时使用的值。 |
|nameTarget|String| 配置 DNS 主机上的 SRV 记录的 *目标* 属性时要使用的值。 |
|端口|Int32| 配置 DNS 主机上的 SRV 记录的 *port* 属性时要使用的值。 |
|priority|Int32| 配置 DNS 主机上的 SRV 记录的 *优先级* 属性时要使用的值。 |
|协议|String| 配置 DNS 主机上的 SRV 记录的 *协议* 属性时要使用的值。 |
|recordType|String|  DNS 记录的类型。 该值始终为 *Srv*。 键 |
|service|String| 配置 DNS 主机上的 SRV 记录的 *服务* 属性时使用的值。 |
|supportedService|String| 依赖于此 SRV 记录的 Microsoft Online 服务或功能。</br></br>可以是下列值之一： **null**、 *Email*、 *Sharepoint*、 *EmailInternalRelayOnly*、 *OfficeCommunicationsOnline*、 *SharePointDefaultDomain*、 *FullRedelegation*、 *SharePointPublic*、 *OrgIdAuthentication*、 *Yammer*、 *Intune* |
|ttl|Int32| 配置 DNS 主机上的 SRV 记录的 *生存时间 (ttl) * 属性时使用的值。 不可为 null |
|weight|Int32| 配置 DNS 主机上的 SRV 记录的 *权重* 属性时要使用的值。 |

## <a name="relationships"></a>关系
无


## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainDnsSrvRecord"
}-->

```json
{
  "canonicalName": "String",
  "id": "String (identifier)",
  "isOptional": true,
  "label": "String",
  "nameTarget": "String",
  "port": 1024,
  "priority": 1024,
  "protocol": "String",
  "recordType": "String",
  "service": "String",
  "supportedService": "String",
  "ttl": 1024,
  "weight": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "domainDnsSrvRecord resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


