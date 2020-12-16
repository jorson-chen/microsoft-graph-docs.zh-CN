---
title: printJob： abort
description: 中止打印作业。
author: nilakhan
localization_priority: Normal
ms.prod: universal-print
doc_type: apiPageType
ms.openlocfilehash: 8fe447b11a8198af41bf9e69e98a7ea64231dec8
ms.sourcegitcommit: 75428fc7535662f34e965c6b69fef3a53fdaf1cb
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/16/2020
ms.locfileid: "49691051"
---
# <a name="printjob-abort"></a><span data-ttu-id="6b0fd-103">printJob： abort</span><span class="sxs-lookup"><span data-stu-id="6b0fd-103">printJob: abort</span></span>

<span data-ttu-id="6b0fd-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="6b0fd-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="6b0fd-105">中止打印作业。</span><span class="sxs-lookup"><span data-stu-id="6b0fd-105">Abort a print job.</span></span> <span data-ttu-id="6b0fd-106">只有使用应用程序权限的应用程序才能中止打印作业。</span><span class="sxs-lookup"><span data-stu-id="6b0fd-106">Only applications using application permissions can abort a print job.</span></span>

## <a name="permissions"></a><span data-ttu-id="6b0fd-107">权限</span><span class="sxs-lookup"><span data-stu-id="6b0fd-107">Permissions</span></span>
<span data-ttu-id="6b0fd-p102">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="6b0fd-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

<span data-ttu-id="6b0fd-110">除了以下权限之外，应用的租户还必须具有活动的通用打印订阅，并且具有授予 [获取](printer-get.md) 打印机访问权限的权限。</span><span class="sxs-lookup"><span data-stu-id="6b0fd-110">In addition to the following permissions, the app's tenant must have an active Universal Print subscription and have a permission that grants [Get printer](printer-get.md) access.</span></span>

|<span data-ttu-id="6b0fd-111">权限类型</span><span class="sxs-lookup"><span data-stu-id="6b0fd-111">Permission type</span></span> | <span data-ttu-id="6b0fd-112">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="6b0fd-112">Permissions (from least to most privileged)</span></span> |
|:---------------|:--------------------------------------------|
|<span data-ttu-id="6b0fd-113">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="6b0fd-113">Delegated (work or school account)</span></span>| <span data-ttu-id="6b0fd-114">不支持</span><span class="sxs-lookup"><span data-stu-id="6b0fd-114">Not Supported</span></span> |
|<span data-ttu-id="6b0fd-115">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="6b0fd-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6b0fd-116">不支持。</span><span class="sxs-lookup"><span data-stu-id="6b0fd-116">Not Supported.</span></span>|
|<span data-ttu-id="6b0fd-117">应用程序</span><span class="sxs-lookup"><span data-stu-id="6b0fd-117">Application</span></span>| <span data-ttu-id="6b0fd-118">PrintJob.ReadWriteBasic.All、PrintJob.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6b0fd-118">PrintJob.ReadWriteBasic.All, PrintJob.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="6b0fd-119">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="6b0fd-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /print/printers/{id}/jobs/{id}/abort
```
## <a name="request-headers"></a><span data-ttu-id="6b0fd-120">请求标头</span><span class="sxs-lookup"><span data-stu-id="6b0fd-120">Request headers</span></span>
| <span data-ttu-id="6b0fd-121">名称</span><span class="sxs-lookup"><span data-stu-id="6b0fd-121">Name</span></span>          | <span data-ttu-id="6b0fd-122">说明</span><span class="sxs-lookup"><span data-stu-id="6b0fd-122">Description</span></span>   |
|:--------------|:--------------|
| <span data-ttu-id="6b0fd-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="6b0fd-123">Authorization</span></span> | <span data-ttu-id="6b0fd-p103">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="6b0fd-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6b0fd-126">请求正文</span><span class="sxs-lookup"><span data-stu-id="6b0fd-126">Request body</span></span>
<span data-ttu-id="6b0fd-127">在请求正文中，可以选择提供作业中止的原因。</span><span class="sxs-lookup"><span data-stu-id="6b0fd-127">In the request body, you can optionally provide the reason why the job is being aborted.</span></span>

| <span data-ttu-id="6b0fd-128">属性</span><span class="sxs-lookup"><span data-stu-id="6b0fd-128">Property</span></span>     | <span data-ttu-id="6b0fd-129">类型</span><span class="sxs-lookup"><span data-stu-id="6b0fd-129">Type</span></span>        | <span data-ttu-id="6b0fd-130">说明</span><span class="sxs-lookup"><span data-stu-id="6b0fd-130">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="6b0fd-131">reason</span><span class="sxs-lookup"><span data-stu-id="6b0fd-131">reason</span></span>|<span data-ttu-id="6b0fd-132">String</span><span class="sxs-lookup"><span data-stu-id="6b0fd-132">String</span></span>|<span data-ttu-id="6b0fd-133">作业中止的原因。</span><span class="sxs-lookup"><span data-stu-id="6b0fd-133">Reason why job is being aborted.</span></span>|

## <a name="response"></a><span data-ttu-id="6b0fd-134">响应</span><span class="sxs-lookup"><span data-stu-id="6b0fd-134">Response</span></span>
<span data-ttu-id="6b0fd-p104">如果成功，此方法返回 `204 No Content` 响应代码。它不在响应正文中返回任何内容。</span><span class="sxs-lookup"><span data-stu-id="6b0fd-p104">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6b0fd-137">示例</span><span class="sxs-lookup"><span data-stu-id="6b0fd-137">Example</span></span>
<span data-ttu-id="6b0fd-138">以下示例演示如何调用此 API。</span><span class="sxs-lookup"><span data-stu-id="6b0fd-138">The following example shows how to call this API.</span></span>
### <a name="request"></a><span data-ttu-id="6b0fd-139">请求</span><span class="sxs-lookup"><span data-stu-id="6b0fd-139">Request</span></span>
<span data-ttu-id="6b0fd-140">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="6b0fd-140">The following is an example of the request.</span></span>


# <a name="http"></a>[<span data-ttu-id="6b0fd-141">HTTP</span><span class="sxs-lookup"><span data-stu-id="6b0fd-141">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "printjob-abort"
}-->
```http
POST https://graph.microsoft.com/beta/print/printers/{id}/jobs/{id}/abort
```
# <a name="c"></a>[<span data-ttu-id="6b0fd-142">C#</span><span class="sxs-lookup"><span data-stu-id="6b0fd-142">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/printjob-abort-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="6b0fd-143">JavaScript</span><span class="sxs-lookup"><span data-stu-id="6b0fd-143">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/printjob-abort-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="6b0fd-144">Objective-C</span><span class="sxs-lookup"><span data-stu-id="6b0fd-144">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/printjob-abort-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[<span data-ttu-id="6b0fd-145">Java</span><span class="sxs-lookup"><span data-stu-id="6b0fd-145">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/printjob-abort-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


### <a name="response"></a><span data-ttu-id="6b0fd-146">响应</span><span class="sxs-lookup"><span data-stu-id="6b0fd-146">Response</span></span>
<span data-ttu-id="6b0fd-147">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="6b0fd-147">The following is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "printJob: abort",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
