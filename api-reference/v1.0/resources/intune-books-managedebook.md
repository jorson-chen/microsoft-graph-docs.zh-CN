---
title: managedEBook 资源类型
description: 包含托管电子书基属性的抽象类。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 9ee5bb486346e315ae00b0e54f44a9fd9b7613c7
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48088669"
---
# <a name="managedebook-resource-type"></a>managedEBook 资源类型

命名空间：microsoft.graph

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

包含托管电子书基属性的抽象类。

## <a name="methods"></a>方法
|方法|返回类型|说明|
|:---|:---|:---|
|[List managedEBooks](../api/intune-books-managedebook-list.md)|[managedEBook](../resources/intune-books-managedebook.md) 集合|列出 [managedEBook](../resources/intune-books-managedebook.md) 对象的属性和关系。|
|[Get managedEBook](../api/intune-books-managedebook-get.md)|[managedEBook](../resources/intune-books-managedebook.md)|读取 [managedEBook](../resources/intune-books-managedebook.md) 对象的属性和关系。|
|[assign 操作](../api/intune-books-managedebook-assign.md)|无|尚未记录|

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|id|String|实体的键。|
|displayName|String|电子书的名称。|
|description|String|说明。|
|publisher|String|发布者。|
|publishedDateTime|DateTimeOffset|电子书的发布日期和时间。|
|largeCover|[mimeContent](../resources/intune-shared-mimecontent.md)|书籍封面。|
|createdDateTime|DateTimeOffset|电子书文件的创建日期和时间。|
|lastModifiedDateTime|DateTimeOffset|上次修改电子书的日期和时间。|
|informationUrl|String|详细信息 Url。|
|privacyInformationUrl|String|隐私声明 Url。|

## <a name="relationships"></a>关系
|关系|类型|说明|
|:---|:---|:---|
|assignments|[managedEBookAssignment](../resources/intune-books-managedebookassignment.md) 集合|此电子书的分配列表。|
|installSummary|[eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md)|移动应用安装摘要。|
|deviceStates|[deviceInstallState](../resources/intune-books-deviceinstallstate.md) 集合|此电子书的安装状态列表。|
|userStateSummary|[userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md) 集合|此电子书的安装状态列表。|

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedEBook"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedEBook",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "publisher": "String",
  "publishedDateTime": "String (timestamp)",
  "largeCover": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "String",
    "value": "binary"
  },
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "informationUrl": "String",
  "privacyInformationUrl": "String"
}
```









