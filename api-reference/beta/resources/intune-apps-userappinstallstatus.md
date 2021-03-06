---
title: userAppInstallStatus 资源类型
description: 包含用户的安装状态的属性。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 6ff97ad83ee8b25194b784d0dcdaafc68bfb7fc0
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49200033"
---
# <a name="userappinstallstatus-resource-type"></a>userAppInstallStatus 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

包含用户的安装状态的属性。

## <a name="methods"></a>方法
|方法|返回类型|说明|
|:---|:---|:---|
|[列出 userAppInstallStatuses](../api/intune-apps-userappinstallstatus-list.md)|[userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) 集合|列出 [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) 对象的属性和关系。|
|[获取 userAppInstallStatus](../api/intune-apps-userappinstallstatus-get.md)|[userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md)|读取 [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) 对象的属性和关系。|
|[创建 userAppInstallStatus](../api/intune-apps-userappinstallstatus-create.md)|[userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md)|创建新的 [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) 对象。|
|[删除 userAppInstallStatus](../api/intune-apps-userappinstallstatus-delete.md)|无|删除 [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md)。|
|[更新 userAppInstallStatus](../api/intune-apps-userappinstallstatus-update.md)|[userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md)|更新 [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) 对象的属性。|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|id|String|实体的键。|
|userName|String|用户名。|
|userPrincipalName|String|用户主体名称。|
|installedDeviceCount|Int32|已安装设备的计数。|
|failedDeviceCount|Int32|已失败设备的计数。|
|notInstalledDeviceCount|Int32|Not installed device count。|

## <a name="relationships"></a>关系
|关系|类型|说明|
|:---|:---|:---|
|应用|[mobileApp](../resources/intune-shared-mobileapp.md)|指向移动应用程序的导航链接。|
|deviceStatuses|[mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) 集合|设备上的应用程序的安装状态。|

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.userAppInstallStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.userAppInstallStatus",
  "id": "String (identifier)",
  "userName": "String",
  "userPrincipalName": "String",
  "installedDeviceCount": 1024,
  "failedDeviceCount": 1024,
  "notInstalledDeviceCount": 1024
}
```




