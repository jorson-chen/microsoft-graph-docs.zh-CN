---
title: iosNotificationSettings 资源类型
description: 说明通知设置的项。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 0e3dc929e96869475d4376c344bf08ff17ae7edd
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48074984"
---
# <a name="iosnotificationsettings-resource-type"></a>iosNotificationSettings 资源类型

命名空间：microsoft.graph

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

说明通知设置的项。

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|bundleID|String|要向其应用这些通知设置的应用的捆绑 ID。|
|appName|String|要与 bundleID 关联的应用程序名称。|
|发布者|String|要与 bundleID 关联的发布者。|
|enabled|布尔值|指示是否允许此应用使用通知。|
|showInNotificationCenter|布尔值|指示是否可以在通知中心中显示通知。|
|showOnLockScreen|布尔值|指示是否可以在锁定屏幕上显示通知。|
|alertType|[iosNotificationAlertType](../resources/intune-deviceconfig-iosnotificationalerttype.md)|指示此应用的通知的警报类型。 可取值为：`deviceDefault`、`banner`、`modal`、`none`。|
|badgesEnabled|布尔值|指示是否允许此应用使用徽章。|
|soundsEnabled|布尔值|指示是否允许此应用使用声音。|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosNotificationSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosNotificationSettings",
  "bundleID": "String",
  "appName": "String",
  "publisher": "String",
  "enabled": true,
  "showInNotificationCenter": true,
  "showOnLockScreen": true,
  "alertType": "String",
  "badgesEnabled": true,
  "soundsEnabled": true
}
```









