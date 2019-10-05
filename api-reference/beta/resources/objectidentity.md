---
title: objectIdentity 资源类型
description: 表示用于登录到用户帐户的标识。
localization_priority: Normal
doc_type: resourcePageType
ms.prod: microsoft-identity-platform
author: davidmu1
ms.openlocfilehash: 5cfc3fd73e053d35bd084e11602a7407cdbfb0c4
ms.sourcegitcommit: 8ef30790a4d7aa94879df93773eae80b37abbfa4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/26/2019
ms.locfileid: "37204011"
---
# <a name="objectidentity-resource-type"></a>objectIdentity 资源类型

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

表示用于登录到用户帐户的标识。 标识可由 Microsoft、组织或由与用户帐户关联的社会身份提供商（如 Facebook、Google 或 Microsoft）提供。 这样一来，用户就可以使用任何相关标识登录到用户帐户。

[User](user.md)资源的**标识**属性是一个**objectIdentity**对象。

## <a name="properties"></a>属性

| 属性   | 类型 |说明|
|:---------------|:--------|:----------|
|signInType|string| 指定目录中的用户登录类型，如`emailAddress` `userName`或。 `federated` 此处， `federated`表示颁发者的用户的唯一标识符，该标识符可以采用颁发者选择的任何格式。 当登录类型设置为**** `emailAddress`或`userName`时，对 issuerAssignedId 强制执行其他验证。 此属性还可以设置为任何自定义字符串。<br><br>支持`$filter`。|
|常用|string|指定标识的颁发者，例如`facebook.com`。<br>对于本地帐户（其中**signInType**不`federated`是），此属性是本地 B2C 租户默认域名（例如`contoso.onmicrosoft.com`）。<br>对于来自其他 Azure AD 组织的外部用户，这将是联合组织的域，例如`contoso.com`。<br><br>支持`$filter`。 512字符限制。|
|issuerAssignedId|string|指定由颁发者分配给用户的唯一标识符。 **颁发者**和**issuerAssignedId**的组合在组织中必须是唯一的。 表示用户的登录名，如果将**signInType**设置为`emailAddress`或`userName` （也称为 "本地帐户"）。<br>当**signInType**设置为时： <ul><li>`emailAddress`， **issuerAssignedId**必须是有效的电子邮件地址</li><li>`userName`， **issuerAssignedId**必须是[电子邮件地址的有效本地部分](https://tools.ietf.org/html/rfc3696#section-3)</li></ul>支持`$filter`。 512字符限制。|

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.objectIdentity"
}-->

```json
{
  "signInType": "string",
  "issuer": "string",
  "issuerAssignedId": "string"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "objectIdentity resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->