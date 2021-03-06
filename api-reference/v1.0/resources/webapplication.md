---
title: webApplication 资源类型
description: 指定 Web 应用程序的设置。
localization_priority: Normal
doc_type: resourcePageType
ms.prod: microsoft-identity-platform
author: sureshja
ms.openlocfilehash: aae3184a025757b910e0b19daa8a8d8057128506
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48015258"
---
# <a name="webapplication-resource-type"></a>webApplication 资源类型

命名空间：microsoft.graph

指定 Web 应用程序的设置。

## <a name="properties"></a>属性

| 属性 | 类型 | 说明 |
|:---------|:-----|:------------|
| homePageUrl | String | 应用程序的主页或登录页面。 |
| implicitGrantSettings | [implicitGrantSettings](implicitgrantsettings.md)| 指定此 web 应用程序是否可以使用 OAuth 2.0 隐式流请求令牌。 |
| logoutUrl | String | 指定 Microsoft 授权服务使用[正向通道](https://openid.net/specs/openid-connect-frontchannel-1_0.html)、[反向通道](https://openid.net/specs/openid-connect-backchannel-1_0.html)或 SAML 注销协议注销用户时所使用的 URL。 |
| redirectUris | String collection | 指定向其发送用户令牌以进行登录的 Url，或用于发送 OAuth 2.0 授权代码和访问令牌的重定向 Uri。 |

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.webApplication"
}-->

```json
{
  "homePageUrl": "String",
  "implicitGrantSettings": {"@odata.type": "microsoft.graph.implicitGrantSettings"},
  "logoutUrl": "String",
  "redirectUris": ["String"]
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "webApplication resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->

