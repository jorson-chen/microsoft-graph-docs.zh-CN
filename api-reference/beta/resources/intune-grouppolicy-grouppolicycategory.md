---
title: groupPolicyCategory 资源类型
description: Category 实体存储组策略定义的类别
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: d7c1f2bc44093342ee227c30eece551f10197ae3
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49267241"
---
# <a name="grouppolicycategory-resource-type"></a>groupPolicyCategory 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

Category 实体存储组策略定义的类别

## <a name="methods"></a>方法
|方法|返回类型|说明|
|:---|:---|:---|
|[获取 groupPolicyCategory](../api/intune-grouppolicy-grouppolicycategory-get.md)|[groupPolicyCategory](../resources/intune-grouppolicy-grouppolicycategory.md)|读取 [groupPolicyCategory](../resources/intune-grouppolicy-grouppolicycategory.md) 对象的属性和关系。|
|[更新 groupPolicyCategory](../api/intune-grouppolicy-grouppolicycategory-update.md)|[groupPolicyCategory](../resources/intune-grouppolicy-grouppolicycategory.md)|更新 [groupPolicyCategory](../resources/intune-grouppolicy-grouppolicycategory.md) 对象的属性。|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|displayName|字符串|类别的显示名称的字符串 id|
|isRoot|Boolean|定义类别是否为根类别|
|id|字符串|实体的键。|
|lastModifiedDateTime|DateTimeOffset|上次修改实体的日期和时间。|

## <a name="relationships"></a>关系
|关系|类型|说明|
|:---|:---|:---|
|父级|[groupPolicyCategory](../resources/intune-grouppolicy-grouppolicycategory.md)|父类别|
|children|[groupPolicyCategory](../resources/intune-grouppolicy-grouppolicycategory.md) 集合|子类别|
|限定|[groupPolicyDefinition](../resources/intune-grouppolicy-grouppolicydefinition.md) 集合|类别的直接 GroupPolicyDefinition 子类别|
|definitionFile|[groupPolicyDefinitionFile](../resources/intune-grouppolicy-grouppolicydefinitionfile.md)|类别所属的定义文件的 id|

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.groupPolicyCategory"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.groupPolicyCategory",
  "displayName": "String",
  "isRoot": true,
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)"
}
```




