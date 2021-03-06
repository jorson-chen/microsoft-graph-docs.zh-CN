---
title: outOfBoxExperienceSettings 资源类型
description: "\"开箱即用体验\" 设置"
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: dc5b5e69fa0b7bdeb8f4db515ccd163fefc1b34a
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49256356"
---
# <a name="outofboxexperiencesettings-resource-type"></a>outOfBoxExperienceSettings 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

"开箱即用体验" 设置

## <a name="properties"></a>属性
|属性|类型|描述|
|:---|:---|:---|
|hidePrivacySettings|Boolean|向用户显示或隐藏隐私设置|
|hideEULA|Boolean|向用户显示或隐藏 EULA|
|userType|[windowsUserType](../resources/intune-enrollment-windowsusertype.md)|用户类型。 可取值为：`administrator`、`standard`。|
|deviceUsageType|[windowsDeviceUsageType](../resources/intune-enrollment-windowsdeviceusagetype.md)|AAD 联接身份验证类型。 可取值为：`singleUser`、`shared`。|
|skipKeyboardSelectionPage|Boolean|如果设置了语言和区域，则选择 "设置"，然后跳过 "键盘选择" 页面|
|hideEscapeLink|Boolean|如果设置为 true，则用户无法在公司登录时使用不同帐户重新开始|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.outOfBoxExperienceSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.outOfBoxExperienceSettings",
  "hidePrivacySettings": true,
  "hideEULA": true,
  "userType": "String",
  "deviceUsageType": "String",
  "skipKeyboardSelectionPage": true,
  "hideEscapeLink": true
}
```




