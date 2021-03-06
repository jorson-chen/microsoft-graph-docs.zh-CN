---
title: 创建 educationAssignmentResource
description: odata。键入以指示要创建的资源的类型。 请注意，必须首先将基于文件的资源上载到工作分配 **resourceFolder**。
localization_priority: Normal
author: dipakboyed
ms.prod: education
doc_type: apiPageType
ms.openlocfilehash: 1e432d4521ffe871de75be4ae8764953d99a3abc
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48002553"
---
# <a name="create-educationassignmentresource"></a>创建 educationAssignmentResource

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

创建 [工作分配资源](../resources/educationassignmentresource.md)。 资源本身有一个 @odata。若要指示正在创建的资源的类型，请键入。 请注意，必须首先将基于文件的资源上载到工作分配 **resourceFolder**。

## <a name="permissions"></a>权限
要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。

|权限类型      | 权限（从最低特权到最高特权）              |
|:--------------------|:---------------------------------------------------------|
|委派（工作或学校帐户） |  EduAssignments、ReadWriteBasic、EduAssignments  |
|委派（个人 Microsoft 帐户） |  不支持。  |
|应用程序 | 不支持。  | 

## <a name="http-request"></a>HTTP 请求
<!-- { "blockType": "ignored" } -->
```http
POST /education/classes/{id}/assignments/{id}/resources
```
## <a name="request-headers"></a>请求标头
| 标头       | 值 |
|:---------------|:--------|
| Authorization  | Bearer {token}。必需。  |
| Content-Type  | application/json  |

## <a name="request-body"></a>请求正文
在请求正文中，提供 [educationAssignmentResource](../resources/educationassignmentresource.md) 对象的 JSON 表示形式。


## <a name="response"></a>响应
如果成功，此方法 `201 Created` 在响应正文中返回响应代码和 [educationAssignmentResource](../resources/educationassignmentresource.md) 对象。

## <a name="example"></a>示例
##### <a name="request"></a>请求
下面展示了示例请求。
<!-- {
  "blockType": "ignored",
  "name": "create_educationassignmentresource_from_educationassignment"
}-->
```http
POST https://graph.microsoft.com/beta/education/classes/11021/assignments/19002/resources
Content-type: application/json
Content-length: 212

{
  "distributeForStudentWork": "false",
  "resource": {
    "displayName": "Bing",
    "link": "https://www.bing.com",
    "@odata.type": "#microsoft.education.assignments.api.educationLinkResource"
  }
}

```
在请求正文中，提供 [educationAssignmentResource](../resources/educationassignmentresource.md) 对象的 JSON 表示形式。
##### <a name="response"></a>响应
下面介绍响应示例。 

>**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。 将从实际调用中返回所有属性。


<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationAssignmentResource"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 229

{
  "id": "122333",
  "distributeForStudentWork": false,
  "resource": {
    "displayName": "Bing",
    "link": "https://www.bing.com",
    "@odata.type": "#microsoft.education.assignments.api.educationLinkResource"
  }
}

```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Create educationAssignmentResource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


