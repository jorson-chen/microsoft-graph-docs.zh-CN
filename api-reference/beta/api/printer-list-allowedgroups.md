---
title: 列出 allowedGroups
description: 检索已授予访问权限的组列表，以将打印作业提交到关联的打印机。
author: braedenp-msft
localization_priority: Normal
ms.prod: universal-print
doc_type: apiPageType
ms.openlocfilehash: 845a8e9a379b72067117ad4f157964f926f89a60
ms.sourcegitcommit: 7baf4847486885edf08ead533c76503cd31a98a4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/21/2020
ms.locfileid: "42895690"
---
# <a name="list-allowedgroups"></a><span data-ttu-id="8fc46-103">列出 allowedGroups</span><span class="sxs-lookup"><span data-stu-id="8fc46-103">List allowedGroups</span></span>

<span data-ttu-id="8fc46-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="8fc46-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="8fc46-105">检索已授予访问权限的组列表，以将打印作业提交到关联的[打印机](../resources/printer.md)。</span><span class="sxs-lookup"><span data-stu-id="8fc46-105">Retrieve a list of groups that have been granted access to submit print jobs to the associated [printer](../resources/printer.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="8fc46-106">权限</span><span class="sxs-lookup"><span data-stu-id="8fc46-106">Permissions</span></span>
<span data-ttu-id="8fc46-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="8fc46-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

<span data-ttu-id="8fc46-109">除了以下权限之外，用户的租户还必须具有活动的通用打印订阅。</span><span class="sxs-lookup"><span data-stu-id="8fc46-109">In addition to the following permissions, the user's tenant must have an active Universal Print subscription.</span></span>

|<span data-ttu-id="8fc46-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="8fc46-110">Permission type</span></span> | <span data-ttu-id="8fc46-111">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="8fc46-111">Permissions (from least to most privileged)</span></span> |
|:---------------|:--------------------------------------------|
|<span data-ttu-id="8fc46-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="8fc46-112">Delegated (work or school account)</span></span>| <span data-ttu-id="8fc46-113">已阅读的用户。所有</span><span class="sxs-lookup"><span data-stu-id="8fc46-113">Users.Read.All</span></span> |
|<span data-ttu-id="8fc46-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="8fc46-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8fc46-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="8fc46-115">Not Supported.</span></span>|
|<span data-ttu-id="8fc46-116">应用程序</span><span class="sxs-lookup"><span data-stu-id="8fc46-116">Application</span></span>|<span data-ttu-id="8fc46-117">不支持。</span><span class="sxs-lookup"><span data-stu-id="8fc46-117">Not Supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8fc46-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="8fc46-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /print/printers/{id}/allowedGroups
```

## <a name="request-headers"></a><span data-ttu-id="8fc46-119">请求标头</span><span class="sxs-lookup"><span data-stu-id="8fc46-119">Request headers</span></span>
| <span data-ttu-id="8fc46-120">名称</span><span class="sxs-lookup"><span data-stu-id="8fc46-120">Name</span></span>      |<span data-ttu-id="8fc46-121">说明</span><span class="sxs-lookup"><span data-stu-id="8fc46-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="8fc46-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="8fc46-122">Authorization</span></span> | <span data-ttu-id="8fc46-p102">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="8fc46-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="8fc46-125">请求正文</span><span class="sxs-lookup"><span data-stu-id="8fc46-125">Request body</span></span>
<span data-ttu-id="8fc46-126">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="8fc46-126">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="8fc46-127">响应</span><span class="sxs-lookup"><span data-stu-id="8fc46-127">Response</span></span>
<span data-ttu-id="8fc46-128">如果成功，此方法在响应`200 OK`正文中返回响应代码和[identity](../resources/identity.md)对象集合。</span><span class="sxs-lookup"><span data-stu-id="8fc46-128">If successful, this method returns a `200 OK` response code and a collection of [identity](../resources/identity.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="8fc46-129">示例</span><span class="sxs-lookup"><span data-stu-id="8fc46-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="8fc46-130">请求</span><span class="sxs-lookup"><span data-stu-id="8fc46-130">Request</span></span>
<span data-ttu-id="8fc46-131">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="8fc46-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_allowedGroups"
}-->
```http
GET https://graph.microsoft.com/beta/print/printers/{id}/allowedGroups
```
##### <a name="response"></a><span data-ttu-id="8fc46-132">响应</span><span class="sxs-lookup"><span data-stu-id="8fc46-132">Response</span></span>
<span data-ttu-id="8fc46-133">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="8fc46-133">The following is an example of the response.</span></span>
><span data-ttu-id="8fc46-p103">**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。所有属性都将通过实际调用返回。</span><span class="sxs-lookup"><span data-stu-id="8fc46-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.identity",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 233

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.printIdentity)",
  "value": [
    {
      "id": "016b5565-3bbf-4067-b9ff-4d68167eb1a6",
      "displayName": "GroupName"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List allowedGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->