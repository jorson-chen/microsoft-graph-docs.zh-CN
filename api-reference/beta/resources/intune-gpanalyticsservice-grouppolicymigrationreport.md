---
title: groupPolicyMigrationReport 资源类型
description: 组策略迁移报告。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 1b9a44157f05b62be6916a01347c6a2441ea83cf
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49298769"
---
# <a name="grouppolicymigrationreport-resource-type"></a>groupPolicyMigrationReport 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

组策略迁移报告。

## <a name="methods"></a>Methods
|方法|返回类型|Description|
|:---|:---|:---|
|[列出 groupPolicyMigrationReports](../api/intune-gpanalyticsservice-grouppolicymigrationreport-list.md)|[groupPolicyMigrationReport](../resources/intune-gpanalyticsservice-grouppolicymigrationreport.md) 集合|列出 [groupPolicyMigrationReport](../resources/intune-gpanalyticsservice-grouppolicymigrationreport.md) 对象的属性和关系。|
|[获取 groupPolicyMigrationReport](../api/intune-gpanalyticsservice-grouppolicymigrationreport-get.md)|[groupPolicyMigrationReport](../resources/intune-gpanalyticsservice-grouppolicymigrationreport.md)|读取 [groupPolicyMigrationReport](../resources/intune-gpanalyticsservice-grouppolicymigrationreport.md) 对象的属性和关系。|
|[创建 groupPolicyMigrationReport](../api/intune-gpanalyticsservice-grouppolicymigrationreport-create.md)|[groupPolicyMigrationReport](../resources/intune-gpanalyticsservice-grouppolicymigrationreport.md)|创建新的 [groupPolicyMigrationReport](../resources/intune-gpanalyticsservice-grouppolicymigrationreport.md) 对象。|
|[删除 groupPolicyMigrationReport](../api/intune-gpanalyticsservice-grouppolicymigrationreport-delete.md)|无|删除 [groupPolicyMigrationReport](../resources/intune-gpanalyticsservice-grouppolicymigrationreport.md)。|
|[更新 groupPolicyMigrationReport](../api/intune-gpanalyticsservice-grouppolicymigrationreport-update.md)|[groupPolicyMigrationReport](../resources/intune-gpanalyticsservice-grouppolicymigrationreport.md)|更新 [groupPolicyMigrationReport](../resources/intune-gpanalyticsservice-grouppolicymigrationreport.md) 对象的属性。|
|[createMigrationReport 操作](../api/intune-gpanalyticsservice-grouppolicymigrationreport-createmigrationreport.md)|String|尚未记录|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|id|字符串|尚未记录|
|groupPolicyObjectId|Guid|GPO Xml 内容中的组策略对象 GUID|
|displayName|字符串|来自 GPO Xml 内容的组策略对象的名称|
|ouDistinguishedName|字符串|OU 的可分辨名称。|
|createdDateTime|DateTimeOffset|GroupPolicyMigrationReport 的创建日期和时间。|
|lastModifiedDateTime|DateTimeOffset|上次修改 GroupPolicyMigrationReport 的日期和时间。|
|groupPolicyCreatedDateTime|DateTimeOffset|GroupPolicyMigrationReport 的创建日期和时间。|
|groupPolicyLastModifiedDateTime|DateTimeOffset|上次修改 GroupPolicyMigrationReport 的日期和时间。|
|migrationReadiness|[groupPolicyMigrationReadiness](../resources/intune-gpanalyticsservice-grouppolicymigrationreadiness.md)|相关联的组策略对象文件的 Intune 覆盖范围。 可取值为：`none`、`partial`、`complete`、`error`、`notApplicable`。|
|targetedInActiveDirectory|Boolean|来自 GPO Xml 内容的 AD 属性中的目标|
|totalSettingsCount|Int32|GPO 文件中的组策略设置总数。|
|supportedSettingsCount|Int32|Intune 支持的组策略设置的数量。|
|supportedSettingsPercent|Int32|Intune 支持的组策略设置的百分比。|

## <a name="relationships"></a>关系
|关系|类型|Description|
|:---|:---|:---|
|groupPolicySettingMappings|[groupPolicySettingMapping](../resources/intune-gpanalyticsservice-grouppolicysettingmapping.md) 集合|MDM/Intune 映射的组策略设置列表。|
|unsupportedGroupPolicyExtensions|[unsupportedGroupPolicyExtension](../resources/intune-gpanalyticsservice-unsupportedgrouppolicyextension.md) 集合|组策略对象中不受支持的组策略扩展的列表。|

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.groupPolicyMigrationReport"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.groupPolicyMigrationReport",
  "id": "String (identifier)",
  "groupPolicyObjectId": "Guid",
  "displayName": "String",
  "ouDistinguishedName": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "groupPolicyCreatedDateTime": "String (timestamp)",
  "groupPolicyLastModifiedDateTime": "String (timestamp)",
  "migrationReadiness": "String",
  "targetedInActiveDirectory": true,
  "totalSettingsCount": 1024,
  "supportedSettingsCount": 1024,
  "supportedSettingsPercent": 1024
}
```




