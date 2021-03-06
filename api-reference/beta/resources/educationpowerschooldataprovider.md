---
title: educationPowerSchoolDataProvider 资源
description: 用于在将 PowerSchool 用作输入源时设置学校数据同步配置文件。
author: mmast-msft
localization_priority: Normal
ms.prod: education
doc_type: resourcePageType
ms.openlocfilehash: 664b7c9c3ad255e502583fca6be332043e712a46
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "47979614"
---
# <a name="educationpowerschooldataprovider-resource"></a>educationPowerSchoolDataProvider 资源

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

用于在将 [PowerSchool](https://www.powerschool.com/solutions/student-information-system-sis/) 用作输入源时设置学校数据同步配置文件。

派生自 [educationSynchronizationDataProvider](educationsynchronizationdataprovider.md)。

## <a name="properties"></a>属性

| 属性                       | 类型                                     | 说明                                                                            |
| :----------------------------- | :--------------------------------------- | :------------------------------------------------------------------------------------- |
| allowTeachersInMultipleSchools | Boolean                                  | 指示源是否具有单个学生或教师的多个标识符。 |
| clientId                       | 字符串                                   | 用于连接到 PowerSchool 的客户端 ID。                                          |
| clientSecret                   | 字符串                                   | 用于对与 PowerSchool 实例的连接进行身份验证的客户端密码。          |
| connectionUrl                  | String                                   | 指向 PowerSchool 实例的连接 URL。                                        |
| schoolsIds                     | String collection                        | 要同步的学校列表。                                                           |
| schoolYear                     | String                                   | 要同步的学校年。                                                               |
| 操作                 | [educationSynchronizationCustomizations] | 要应用于同步配置文件的可选自定义项。                   |

[educationsynchronizationconnectionsettings]: educationsynchronizationconnectionsettings.md
[educationsynchronizationcustomizations]: educationsynchronizationcustomizations.md

## <a name="json-representation"></a>JSON 表示形式

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationPowerSchoolDataProvider"
}-->

```json
{
  "@odata.type": "microsoft.graph.educationPowerSchoolDataProvider",
  "connectionUrl": "String",
  "clientId": "String",
  "clientSecret": "String",
  "schoolsIds": ["String"],
  "schoolYear": "String",
  "allowTeachersInMultipleSchools": "Boolean",
  "customizations": {
    "@odata.type": "microsoft.graph.educationSynchronizationCustomizations"
  }
}
```


