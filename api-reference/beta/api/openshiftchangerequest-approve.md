---
title: openShiftChangeRequest：批准
description: 批准 openshift 请求。
localization_priority: Normal
author: akumar39
ms.prod: microsoft-teams
doc_type: apiPageType
ms.openlocfilehash: 37af35af00f6c5f0253580f5d5034cfbd8e1f3bf
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48019901"
---
# <a name="openshiftchangerequest-approve"></a>openShiftChangeRequest：批准

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

批准 [openshiftchangerequest](../resources/openshiftchangerequest.md) 对象。

## <a name="permissions"></a>权限

要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。

| 权限类型                        | 权限（从最低特权到最高特权） |
|:---------------------------------------|:--------------------------------------------|
| 委派（工作或学校帐户）     | Group.ReadWrite.All |
| 委派（个人 Microsoft 帐户） | 不支持。 |
| 应用程序                            | 不支持。 |

## <a name="http-request"></a>HTTP 请求

<!-- { "blockType": "ignored" } -->

```http
POST /teams/{id}/schedule/openShiftsChangeRequests/{openShiftChangeRequestId}/approve
```

## <a name="request-headers"></a>请求标头

| 名称          | 说明   |
|:--------------|:--------------|
| Authorization | Bearer {token}。必需。 |
| Content-type | application/json. Required. |

## <a name="request-body"></a>请求正文

在请求正文中，提供具有以下参数的 JSON 对象。

| 参数    | 类型        | 描述 |
|:-------------|:------------|:------------|
|message|String|自定义审批邮件。|

## <a name="response"></a>响应

如果成功，此方法返回 `200 OK` 响应代码。它不在响应正文中返回任何内容。

## <a name="examples"></a>示例

以下示例演示如何调用此 API。

### <a name="request"></a>请求

请求示例如下所示。
<!-- {
  "blockType": "request",
  "name": "openshiftchangerequest_approve"
}-->

```http
POST https://graph.microsoft.com/beta/teams/{id}/schedule/openShiftsChangeRequests/{openShiftChangeRequestId}/approve
Content-type: application/json

{
  "message": "message-value"
}
```

### <a name="response"></a>响应

下面展示了示例响应。
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->

```http
HTTP/1.1 200 OK
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "openShiftChangeRequest: approve",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


