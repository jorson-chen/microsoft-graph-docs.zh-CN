---
title: iosRedirectSingleSignOnExtension 资源类型
description: 表示 iOS 设备的重定向类型单一 Sign-On 扩展配置文件。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 40148b36984ae2239465410ed66d1427e1aed60a
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49280114"
---
# <a name="iosredirectsinglesignonextension-resource-type"></a>iosRedirectSingleSignOnExtension 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

表示 iOS 设备的重定向类型单一 Sign-On 扩展配置文件。


继承自 [iosSingleSignOnExtension](../resources/intune-deviceconfig-iossinglesignonextension.md)

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|extensionIdentifier|字符串|获取或设置对指定 Url 执行 SSO 的应用扩展的捆绑包 ID。|
|teamIdentifier|字符串|获取或设置为指定的 Url 执行 SSO 的应用程序扩展的团队 ID。|
|配置|[keyTypedValuePair](../resources/intune-deviceconfig-keytypedvaluepair.md) 集合|获取或设置用于配置凭据类型配置文件的类型键/值对的列表。 该集合最多可包含 500 个元素。|
|urlPrefixes|String 集合|标识提供程序的一个或多个 URL 前缀，代表其应用程序扩展执行单一登录。 Url 必须以 http://或 https://开头。 所有 URL 前缀对所有配置文件都必须是唯一的。|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosRedirectSingleSignOnExtension"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosRedirectSingleSignOnExtension",
  "extensionIdentifier": "String",
  "teamIdentifier": "String",
  "configurations": [
    {
      "@odata.type": "microsoft.graph.keyTypedValuePair",
      "key": "String"
    }
  ],
  "urlPrefixes": [
    "String"
  ]
}
```




