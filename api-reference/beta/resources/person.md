---
title: person 资源类型
description: 有关来自邮件、联系人和社交网络的人员的信息聚合。用户可以是本地联系人、来自社交网络的联系人、组织的目录以及来自最近通信 (（如电子邮件和 Skype) ）的人员。
author: simonhult
localization_priority: Normal
ms.prod: insights
doc_type: resourcePageType
ms.openlocfilehash: cc63a75af497a2402955c39a2bcfc8efe370c782
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "47998038"
---
# <a name="person-resource-type"></a>person 资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

有关来自邮件、联系人和社交网络的人员的信息聚合。用户可以是本地联系人、来自社交网络的联系人、组织的目录以及来自最近通信 (（如电子邮件和 Skype) ）的人员。

## <a name="methods"></a>方法

| 方法 | 返回类型 | 说明 |
|:---------------|:--------|:----------|
|[List people](../api/user-list-people.md) | **person** |获取按与[用户](../resources/user.md)的相关性排序的人员对象集合。|

## <a name="properties"></a>属性

| 属性 | 类型 | 说明 |
|:---------------|:--------|:----------|
|birthday|字符串|人员的生日。|
|companyName|字符串|人员的公司名称。|
|department|字符串|人员的部门。|
|displayName|string|人员的显示名称。|
|emailAddresses|[rankedEmailAddress](rankedemailaddress.md) 集合|人员的电子邮件地址。|
|givenName|字符串|人员的名字。|
|id|string|人员的唯一标识符。只读。|
|isFavorite|boolean|如果用户已将此人员标记为常用联系人，则为 `true`。|
|mailboxType|字符串|由个人的电子邮件地址表示的邮箱类型。|
|officeLocation|字符串|人员的办公室位置。|
|personNotes|字符串|用户对此人员所做的自由格式备注。|
|personType|字符串|人员类型，例如通讯组列表。|
|phones|[phone](phone.md) collection|人员的电话号码。|
|postalAddresses|[location](location.md) collection|人员的地址。|
|profession|字符串|人员的职业。|
|源|[personDataSource](persondatasource.md) 集合|用户数据来自的源，例如目录或 Outlook 联系人。|
|surname|字符串|人员的姓氏。|
|title|string|人员的职务。|
|userPrincipalName|string|人员的用户主体名称 (UPN)。UPN 是人员基于 Internet 标准 [RFC 822](https://www.ietf.org/rfc/rfc0822.txt) 的 Internet 式登录名。按照惯例，此名称应映射到人员的电子邮件名称。常规格式为：别名@域。|
|websites|[website](website.md) collection|人员的网站。|
|yomiCompany|字符串|人员所在公司的注音日文名称。|

## <a name="relationships"></a>关系

无

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.person"
}-->

```json
{
  "birthday": "string",
  "companyName": "string",
  "department": "string",
  "displayName": "string",
  "emailAddresses": [{"@odata.type": "microsoft.graph.rankedEmailAddress"}],
  "givenName": "string",
  "id": "string (identifier)",
  "isFavorite": true,
  "mailboxType": "string",
  "officeLocation": "string",
  "personNotes": "string",
  "personType": "string",
  "phones": [{"@odata.type": "microsoft.graph.phone"}],
  "postalAddresses": [{"@odata.type": "microsoft.graph.location"}],
  "profession": "string",
  "sources": [{"@odata.type": "microsoft.graph.personDataSource"}],
  "surname": "string",
  "title": "string",
  "userPrincipalName": "string",
  "websites": [{"@odata.type": "microsoft.graph.website"}],
  "yomiCompany": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "person resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


