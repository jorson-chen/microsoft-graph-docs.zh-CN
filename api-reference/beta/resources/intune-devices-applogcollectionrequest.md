---
title: appLogCollectionRequest 资源类型
description: AppLogCollectionRequest 实体。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 9c3c3c1f07a6fa0cd5d9ea4ad764e67753f840e9
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49267885"
---
# <a name="applogcollectionrequest-resource-type"></a>appLogCollectionRequest 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

AppLogCollectionRequest 实体。

## <a name="methods"></a>方法
|方法|返回类型|说明|
|:---|:---|:---|
|[列出 appLogCollectionRequests](../api/intune-devices-applogcollectionrequest-list.md)|[appLogCollectionRequest](../resources/intune-devices-applogcollectionrequest.md) 集合|列出 [appLogCollectionRequest](../resources/intune-devices-applogcollectionrequest.md) 对象的属性和关系。|
|[获取 appLogCollectionRequest](../api/intune-devices-applogcollectionrequest-get.md)|[appLogCollectionRequest](../resources/intune-devices-applogcollectionrequest.md)|读取 [appLogCollectionRequest](../resources/intune-devices-applogcollectionrequest.md) 对象的属性和关系。|
|[创建 appLogCollectionRequest](../api/intune-devices-applogcollectionrequest-create.md)|[appLogCollectionRequest](../resources/intune-devices-applogcollectionrequest.md)|创建新的 [appLogCollectionRequest](../resources/intune-devices-applogcollectionrequest.md) 对象。|
|[删除 appLogCollectionRequest](../api/intune-devices-applogcollectionrequest-delete.md)|无|删除 [appLogCollectionRequest](../resources/intune-devices-applogcollectionrequest.md)。|
|[更新 appLogCollectionRequest](../api/intune-devices-applogcollectionrequest-update.md)|[appLogCollectionRequest](../resources/intune-devices-applogcollectionrequest.md)|更新 [appLogCollectionRequest](../resources/intune-devices-applogcollectionrequest.md) 对象的属性。|
|[createDownloadUrl 操作](../api/intune-devices-applogcollectionrequest-createdownloadurl.md)|[appLogCollectionDownloadDetails](../resources/intune-devices-applogcollectiondownloaddetails.md)|尚未记录|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|id|字符串|唯一标识符。 这是 userId_DeviceId_AppId id。|
|status|[appLogUploadState](../resources/intune-devices-apploguploadstate.md)|日志上载状态。 可取值为：`pending`、`completed`、`failed`。|
|errorMessage|字符串|在上载过程中出现的错误消息|
|customLogFolders|String 集合|日志文件夹的列表。 |
|completedDateTime|DateTimeOffset|上传日志请求到达终端状态的时间|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.appLogCollectionRequest"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.appLogCollectionRequest",
  "id": "String (identifier)",
  "status": "String",
  "errorMessage": "String",
  "customLogFolders": [
    "String"
  ],
  "completedDateTime": "String (timestamp)"
}
```




