---
title: resourceOperation 资源类型
description: 描述 resourceOperation 资源 (entity) of Microsoft Graph API (REST) ，它支持与基于角色的访问控制 (RBAC) 相关的 Intune 工作流。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 59eb8f7c9b30f466748513846b71271aa04a35d6
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49300911"
---
# <a name="resourceoperation-resource-type"></a>resourceOperation 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

描述 resourceOperation 资源 (entity) of Microsoft Graph API (REST) ，它支持与基于角色的访问控制 (RBAC) 相关的 Intune 工作流。

## <a name="methods"></a>Methods
|方法|返回类型|Description|
|:---|:---|:---|
|[List resourceOperations](../api/intune-rbac-resourceoperation-list.md)|[resourceOperation](../resources/intune-rbac-resourceoperation.md) 集合|列出 [resourceOperation](../resources/intune-rbac-resourceoperation.md) 对象的属性和关系。|
|[Get resourceOperation](../api/intune-rbac-resourceoperation-get.md)|[resourceOperation](../resources/intune-rbac-resourceoperation.md)|读取 [resourceOperation](../resources/intune-rbac-resourceoperation.md) 对象的属性和关系。|
|[Create resourceOperation](../api/intune-rbac-resourceoperation-create.md)|[resourceOperation](../resources/intune-rbac-resourceoperation.md)|创建新的 [resourceOperation](../resources/intune-rbac-resourceoperation.md) 对象。|
|[Delete resourceOperation](../api/intune-rbac-resourceoperation-delete.md)|无|删除 [resourceOperation](../resources/intune-rbac-resourceoperation.md)。|
|[Update resourceOperation](../api/intune-rbac-resourceoperation-update.md)|[resourceOperation](../resources/intune-rbac-resourceoperation.md)|更新 [resourceOperation](../resources/intune-rbac-resourceoperation.md) 对象的属性。|
|[getScopesForUser 函数](../api/intune-rbac-resourceoperation-getscopesforuser.md)|String collection|尚未记录|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|id|字符串|资源操作的键。 只读，且自动生成。|
|resource|字符串|此操作所属的资源类别。|
|resourceName|String|执行此操作的资源的名称。|
|actionName|String|此操作将执行的操作类型。 actionName 应简明，并尽可能限制在几个字以内。|
|description|字符串|资源操作的说明。 当在 Azure 门户中显示时，会在操作的鼠标悬停文本中使用说明。|
|enabledForScopeValidation|Boolean|确定是否针对按角色分配定义的作用域验证权限。|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.resourceOperation"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.resourceOperation",
  "id": "String (identifier)",
  "resource": "String",
  "resourceName": "String",
  "actionName": "String",
  "description": "String",
  "enabledForScopeValidation": true
}
```




