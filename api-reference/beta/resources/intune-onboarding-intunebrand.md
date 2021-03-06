---
title: intuneBrand 资源类型
description: intuneBrand 包含在自定义公司门户应用程序以及最终用户 Web 门户的外观时使用的数据。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: d97ecb5a0cb55ca717da3ceb6870d71c70df199a
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49266527"
---
# <a name="intunebrand-resource-type"></a>intuneBrand 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

intuneBrand 包含在自定义公司门户应用程序以及最终用户网页版门户的外观时使用的数据。

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|displayName|字符串|向最终用户显示的公司/组织名称。|
|themeColor|[rgbColor](../resources/intune-shared-rgbcolor.md)|公司门户应用程序和 Web 门户中使用的主要主题颜色。|
|showLogo|布尔值|表示是否显示管理员提供的徽标图像的布尔值。|
|lightBackgroundLogo|[mimeContent](../resources/intune-shared-mimecontent.md)|在公司门户应用中显示的徽标图像，徽标后有浅色背景。|
|darkBackgroundLogo|[mimeContent](../resources/intune-shared-mimecontent.md)|在公司门户应用中显示的徽标图像，徽标后有深色背景。|
|showNameNextToLogo|布尔值|表示是否要在徽标图像旁显示管理员提供的显示名称的布尔值。|
|landingPageCustomizedImage|[mimeContent](../resources/intune-shared-mimecontent.md)|在公司门户应用登录页中显示的自定义图像|
|showDisplayNameNextToLogo|布尔值|表示是否要在徽标图像旁显示管理员提供的显示名称的布尔值。|
|roleScopeTagIds|String 集合|分配给默认品牌配置文件的作用域标记列表|
|contactITName|String|负责 IT 支持的员工/组织名称。|
|contactITPhoneNumber|String|负责 IT 支持的员工/组织的电话号码。|
|contactITEmailAddress|String|负责 IT 支持的员工/组织的电子邮件地址。|
|contactITNotes|String|负责 IT 支持的员工/组织的文本注释。|
|onlineSupportSiteUrl|String|指向公司/组织 IT 支持人员网站的 URL。|
|onlineSupportSiteName|String|显示公司/组织 IT 支持人员网站的名称。|
|privacyUrl|String|指向公司/组织隐私策略的 URL。|
|customPrivacyMessage|字符串|用于解释组织无法在托管设备上看到或执行的操作的自定义隐私邮件。|
|customCantSeePrivacyMessage|字符串|用于解释组织无法在托管设备上看到或执行的操作的自定义隐私邮件。|
|customCanSeePrivacyMessage|字符串|自定义隐私邮件，用于解释组织可以在托管设备上看到和执行的操作。|
|isRemoveDeviceDisabled|Boolean|一个 Boolean 类型的值，该值表示 adminsistrator 是否已在企业拥有的设备上禁用了 "删除设备" 操作。|
|isFactoryResetDisabled|Boolean|一个 Boolean 类型的值，该值表示 adminsistrator 是否已在企业拥有的设备上禁用了 "Factory 重置" 操作。|
|companyPortalBlockedActions|[companyPortalBlockedAction](../resources/intune-shared-companyportalblockedaction.md) 集合|按平台和设备所有权类型对公司门户的阻止操作的集合。|
|showAzureADEnterpriseApps|Boolean|指示是否将在公司门户中显示 AzureAD 企业应用程序的布尔值|
|showOfficeWebApps|Boolean|指示 Office WebApps 是否将显示在公司门户中的布尔值|
|sendDeviceOwnershipChangePushNotification|Boolean|一个 Boolean 类型的值，该值指示当用户的设备所有权类型从个人更改为公司时是否向用户发送推送通知|
|enrollmentAvailability|[enrollmentAvailabilityOptions](../resources/intune-shared-enrollmentavailabilityoptions.md)|向最终用户显示的自定义设备注册流。 可取值为：`availableWithPrompts`、`availableWithoutPrompts`、`unavailable`。|
|disableClientTelemetry|Boolean|适用于从所有客户端发送到 Intune 服务的遥测。 如果禁用此设置，则会关闭客户端中的所有主动故障排除和问题警告，并且遥测设置将显示为非活动或对设备用户隐藏。|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.intuneBrand"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.intuneBrand",
  "displayName": "String",
  "themeColor": {
    "@odata.type": "microsoft.graph.rgbColor",
    "r": 1024,
    "g": 1024,
    "b": 1024
  },
  "showLogo": true,
  "lightBackgroundLogo": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "String",
    "value": "binary"
  },
  "darkBackgroundLogo": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "String",
    "value": "binary"
  },
  "showNameNextToLogo": true,
  "landingPageCustomizedImage": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "String",
    "value": "binary"
  },
  "showDisplayNameNextToLogo": true,
  "roleScopeTagIds": [
    "String"
  ],
  "contactITName": "String",
  "contactITPhoneNumber": "String",
  "contactITEmailAddress": "String",
  "contactITNotes": "String",
  "onlineSupportSiteUrl": "String",
  "onlineSupportSiteName": "String",
  "privacyUrl": "String",
  "customPrivacyMessage": "String",
  "customCantSeePrivacyMessage": "String",
  "customCanSeePrivacyMessage": "String",
  "isRemoveDeviceDisabled": true,
  "isFactoryResetDisabled": true,
  "companyPortalBlockedActions": [
    {
      "@odata.type": "microsoft.graph.companyPortalBlockedAction",
      "platform": "String",
      "ownerType": "String",
      "action": "String"
    }
  ],
  "showAzureADEnterpriseApps": true,
  "showOfficeWebApps": true,
  "sendDeviceOwnershipChangePushNotification": true,
  "enrollmentAvailability": "String",
  "disableClientTelemetry": true
}
```




