---
title: dataSharingConsent 资源类型
description: 数据共享同意信息。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 11cdcc0bf083e88da6e1e1c1dd149fce50a05d18
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49293176"
---
# <a name="datasharingconsent-resource-type"></a>dataSharingConsent 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

数据共享同意信息。

## <a name="methods"></a>Methods
|方法|返回类型|Description|
|:---|:---|:---|
|[列出 dataSharingConsents](../api/intune-devices-datasharingconsent-list.md)|[dataSharingConsent](../resources/intune-devices-datasharingconsent.md) 集合|列出 [dataSharingConsent](../resources/intune-devices-datasharingconsent.md) 对象的属性和关系。|
|[获取 dataSharingConsent](../api/intune-devices-datasharingconsent-get.md)|[dataSharingConsent](../resources/intune-devices-datasharingconsent.md)|读取 [dataSharingConsent](../resources/intune-devices-datasharingconsent.md) 对象的属性和关系。|
|[创建 dataSharingConsent](../api/intune-devices-datasharingconsent-create.md)|[dataSharingConsent](../resources/intune-devices-datasharingconsent.md)|创建新的 [dataSharingConsent](../resources/intune-devices-datasharingconsent.md) 对象。|
|[删除 dataSharingConsent](../api/intune-devices-datasharingconsent-delete.md)|无|删除 [dataSharingConsent](../resources/intune-devices-datasharingconsent.md)。|
|[更新 dataSharingConsent](../api/intune-devices-datasharingconsent-update.md)|[dataSharingConsent](../resources/intune-devices-datasharingconsent.md)|更新 [dataSharingConsent](../resources/intune-devices-datasharingconsent.md) 对象的属性。|
|[consentToDataSharing 操作](../api/intune-devices-datasharingconsent-consenttodatasharing.md)|[dataSharingConsent](../resources/intune-devices-datasharingconsent.md)|尚未记录|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|id|字符串|数据共享同意 Id|
|serviceDisplayName|字符串|服务工作流的显示名称|
|termsUrl|字符串|数据共享同意的 TermsUrl|
|granted|Boolean|"数据共享同意" 的 "已授予" 状态|
|grantDateTime|DateTimeOffset|授予此帐户的时间许可|
|grantedByUpn|字符串|授予此帐户同意的用户的 Upn|
|grantedByUserId|字符串|授予此帐户同意的用户的用户 Id|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.dataSharingConsent"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.dataSharingConsent",
  "id": "String (identifier)",
  "serviceDisplayName": "String",
  "termsUrl": "String",
  "granted": true,
  "grantDateTime": "String (timestamp)",
  "grantedByUpn": "String",
  "grantedByUserId": "String"
}
```




