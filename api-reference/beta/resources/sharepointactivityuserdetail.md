---
title: sharePointActivityUserDetail 资源类型
description: 下面是资源的 JSON 表示形式。
localization_priority: Normal
ms.prod: sharepoint
doc_type: resourcePageType
author: JeremyKelley
ms.openlocfilehash: 7394e2fab0604286e8066b64e86f413f421472cf
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "47997793"
---
# <a name="sharepointactivityuserdetail-resource-type"></a>sharePointActivityUserDetail 资源类型

命名空间：microsoft.graph

## <a name="properties"></a>属性

| 属性                  | 类型              |
| :------------------------ | :---------------- |
| reportRefreshDate         | 日期              |
| userPrincipalName         | String            |
| isDeleted                 | Boolean           |
| deletedDate               | 日期              |
| lastActivityDate          | 日期              |
| viewedOrEditedFileCount   | Int64             |
| syncedFileCount           | Int64             |
| sharedInternallyFileCount | Int64             |
| sharedExternallyFileCount | Int64             |
| visitedPageCount          | Int64             |
| assignedProducts          | String collection |
| reportPeriod              | String            |

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.sharePointActivityUserDetail"
} -->

```json
{
  "reportRefreshDate": "Date",
  "userPrincipalName": "String",
  "isDeleted": true,
  "deletedDate": "Date",
  "lastActivityDate": "Date",
  "viewedOrEditedFileCount": 1024,
  "syncedFileCount": 1024,
  "sharedInternallyFileCount": 1024,
  "sharedExternallyFileCount": 1024,
  "visitedPageCount": 1024,
  "assignedProducts": ["String"],
  "reportPeriod": "String"
}
```


