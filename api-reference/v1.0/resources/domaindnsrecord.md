---
title: domainDnsRecord 资源类型
description: DomainDnsRecord 实体用于显示 DNS 记录。
localization_priority: Normal
author: adimitui
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: a1c0e9938fd9967b159c273782bc674b695b842d
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48018660"
---
# <a name="domaindnsrecord-resource-type"></a>domainDnsRecord 资源类型

命名空间：microsoft.graph

对于租户中的每个域，您可能需要将 DNS 记录 (s) 添加到域的 DNS 区域文件中，然后 Microsoft Online Services 才能使用该域。 **DomainDnsRecord**实体用于提供此类 DNS 记录。 [DomainDnsCnameRecord](domaindnscnamerecord.md)、 [DomainDnsMxRecord](domaindnsmxrecord.md)、 [DomainDnsSrvRecord](domaindnssrvrecord.md)和[DomainDnsTxtRecord](domaindnstxtrecord.md)实体的基本实体。

## <a name="methods"></a>方法
不支持直接向此资源进行查询。 有关如何查询域服务记录的信息，请参阅 [域](domain.md) 主题。

## <a name="properties"></a>属性
| 属性     | 类型   |说明|
|:---------------|:--------|:----------|
|id|String| 分配给此实体的唯一标识符。 不可为 null，只读。|
|isOptional|Boolean| 如果为 false，则客户必须在 DNS 主机上配置此记录，才能使 Microsoft Online Services 在域中正常运行。 |
|label|String| 在 DNS 主机上配置 DNS 记录名称时使用的值。 |
|recordType|String| 指示此实体表示的 DNS 记录的类型。</br></br>此值可以是下列值之一： *CName*、 *Mx*、 *Srv*、 *Txt*</br></br>键 |
|supportedService|String| 对此 DNS 记录具有依赖项的 Microsoft Online 服务或功能。</br></br>可以是下列值之一： **null**、 *Email*、 *Sharepoint*、 *EmailInternalRelayOnly*、 *OfficeCommunicationsOnline*、 *SharePointDefaultDomain*、 *FullRedelegation*、 *SharePointPublic*、 *OrgIdAuthentication*、 *Yammer*、 *Intune*|
|ttl|Int32| 在 DNS 主机上配置 DNS 记录的生存时间 (ttl) 属性时使用的值。 不可为 null |

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainDnsRecord"
}-->

```json
{
  "id": "String (identifier)",
  "isOptional": true,
  "label": "String",
  "recordType": "String",
  "supportedService": "String",
  "ttl": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "domainDnsRecord resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

