---
title: iosVppAppAssignedLicense 资源类型
description: iOS 批量采购计划许可证分配。 此类不支持创建、删除或更新。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 65bc79263b39613b8dde454ae9da5bbc149fb474
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49261200"
---
# <a name="iosvppappassignedlicense-resource-type"></a>iosVppAppAssignedLicense 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

iOS 批量采购计划许可证分配。 此类不支持创建、删除或更新。

## <a name="methods"></a>方法
|方法|返回类型|说明|
|:---|:---|:---|
|[列出 iosVppAppAssignedLicenses](../api/intune-apps-iosvppappassignedlicense-list.md)|[iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md) 集合|列出 [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md) 对象的属性和关系。|
|[获取 iosVppAppAssignedLicense](../api/intune-apps-iosvppappassignedlicense-get.md)|[iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)|读取 [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md) 对象的属性和关系。|
|[创建 iosVppAppAssignedLicense](../api/intune-apps-iosvppappassignedlicense-create.md)|[iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)|创建新的 [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md) 对象。|
|[删除 iosVppAppAssignedLicense](../api/intune-apps-iosvppappassignedlicense-delete.md)|无|删除 [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)。|
|[更新 iosVppAppAssignedLicense](../api/intune-apps-iosvppappassignedlicense-update.md)|[iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)|更新 [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md) 对象的属性。|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|id|String|实体的键。|
|userEmailAddress|String|用户电子邮件地址。|
|userId|String|用户 ID。|
|userName|String|用户名。|
|userPrincipalName|String|用户主体名称。|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosVppAppAssignedLicense"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosVppAppAssignedLicense",
  "id": "String (identifier)",
  "userEmailAddress": "String",
  "userId": "String",
  "userName": "String",
  "userPrincipalName": "String"
}
```




