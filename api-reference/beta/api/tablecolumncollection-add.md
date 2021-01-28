---
title: 'TableColumnCollection: add'
description: 向表中添加新列。
author: lumine2008
localization_priority: Normal
ms.prod: excel
doc_type: apiPageType
ms.openlocfilehash: c560b6f3d326555e514b9bd73f2aef08a665606e
ms.sourcegitcommit: 9a03b719d1316729dd022bf4d268894e91515475
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2021
ms.locfileid: "50034308"
---
# <a name="tablecolumncollection-add"></a><span data-ttu-id="1460a-103">TableColumnCollection: add</span><span class="sxs-lookup"><span data-stu-id="1460a-103">TableColumnCollection: add</span></span>

<span data-ttu-id="1460a-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="1460a-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="1460a-105">向表中添加新列。</span><span class="sxs-lookup"><span data-stu-id="1460a-105">Adds a new column to the table.</span></span>
## <a name="permissions"></a><span data-ttu-id="1460a-106">Permissions</span><span class="sxs-lookup"><span data-stu-id="1460a-106">Permissions</span></span>
<span data-ttu-id="1460a-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="1460a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1460a-109">权限类型</span><span class="sxs-lookup"><span data-stu-id="1460a-109">Permission type</span></span>      | <span data-ttu-id="1460a-110">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="1460a-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1460a-111">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="1460a-111">Delegated (work or school account)</span></span> | <span data-ttu-id="1460a-112">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1460a-112">Files.ReadWrite</span></span>    |
|<span data-ttu-id="1460a-113">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="1460a-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1460a-114">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1460a-114">Files.ReadWrite</span></span>    |
|<span data-ttu-id="1460a-115">应用程序</span><span class="sxs-lookup"><span data-stu-id="1460a-115">Application</span></span> | <span data-ttu-id="1460a-116">不支持。</span><span class="sxs-lookup"><span data-stu-id="1460a-116">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="1460a-117">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="1460a-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/columns/add
POST /workbook/worksheets/{id|name}/tables/{id|name}/columns/add

```
## <a name="request-headers"></a><span data-ttu-id="1460a-118">请求标头</span><span class="sxs-lookup"><span data-stu-id="1460a-118">Request headers</span></span>
| <span data-ttu-id="1460a-119">名称</span><span class="sxs-lookup"><span data-stu-id="1460a-119">Name</span></span>       | <span data-ttu-id="1460a-120">说明</span><span class="sxs-lookup"><span data-stu-id="1460a-120">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="1460a-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="1460a-121">Authorization</span></span>  | <span data-ttu-id="1460a-p102">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="1460a-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="1460a-124">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="1460a-124">Workbook-Session-Id</span></span>  | <span data-ttu-id="1460a-p103">确定是否保留更改的工作簿会话 ID。可选。</span><span class="sxs-lookup"><span data-stu-id="1460a-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="1460a-127">请求正文</span><span class="sxs-lookup"><span data-stu-id="1460a-127">Request body</span></span>
<span data-ttu-id="1460a-128">在请求正文中，提供具有以下参数的 JSON 对象。</span><span class="sxs-lookup"><span data-stu-id="1460a-128">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="1460a-129">参数</span><span class="sxs-lookup"><span data-stu-id="1460a-129">Parameter</span></span>    | <span data-ttu-id="1460a-130">类型</span><span class="sxs-lookup"><span data-stu-id="1460a-130">Type</span></span>   |<span data-ttu-id="1460a-131">说明</span><span class="sxs-lookup"><span data-stu-id="1460a-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1460a-132">index</span><span class="sxs-lookup"><span data-stu-id="1460a-132">index</span></span>|<span data-ttu-id="1460a-133">number</span><span class="sxs-lookup"><span data-stu-id="1460a-133">number</span></span>|<span data-ttu-id="1460a-p104">指定新列的相对位置。之前位于此位置的列向右移动。索引值应等于或小于最后一列的索引值，因此不能用于在表末尾附加列。从零开始编制索引。</span><span class="sxs-lookup"><span data-stu-id="1460a-p104">Specifies the relative position of the new column. The previous column at this position is shifted to the right. The index value should be equal to or less than the last column's index value, so it cannot be used to append a column at the end of the table. Zero-indexed.</span></span>|
|<span data-ttu-id="1460a-138">值</span><span class="sxs-lookup"><span data-stu-id="1460a-138">values</span></span>|<span data-ttu-id="1460a-139"> (布尔值、字符串或) 数</span><span class="sxs-lookup"><span data-stu-id="1460a-139">(boolean or string or number) collection</span></span>|<span data-ttu-id="1460a-p105">可选。未设置格式的表列值的二维数组。</span><span class="sxs-lookup"><span data-stu-id="1460a-p105">Optional. A 2-dimensional array of unformatted values of the table column.</span></span>|

## <a name="response"></a><span data-ttu-id="1460a-142">响应</span><span class="sxs-lookup"><span data-stu-id="1460a-142">Response</span></span>

<span data-ttu-id="1460a-143">如果成功，此方法在响应正文中返回响应代码和 `200 OK` [workbookTableColumn](../resources/workbooktablecolumn.md) 对象。</span><span class="sxs-lookup"><span data-stu-id="1460a-143">If successful, this method returns `200 OK` response code and [workbookTableColumn](../resources/workbooktablecolumn.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1460a-144">示例</span><span class="sxs-lookup"><span data-stu-id="1460a-144">Example</span></span>
<span data-ttu-id="1460a-145">下面是一个如何调用此 API 的示例。</span><span class="sxs-lookup"><span data-stu-id="1460a-145">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="1460a-146">请求</span><span class="sxs-lookup"><span data-stu-id="1460a-146">Request</span></span>
<span data-ttu-id="1460a-147">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="1460a-147">Here is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="1460a-148">HTTP</span><span class="sxs-lookup"><span data-stu-id="1460a-148">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "tablecolumncollection_add"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/columns/add
Content-type: application/json
Content-length: 51

{
  "index": {
  },
  "values": [
    {
    }
  ]
}
```
# <a name="c"></a>[<span data-ttu-id="1460a-149">C#</span><span class="sxs-lookup"><span data-stu-id="1460a-149">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/tablecolumncollection-add-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="1460a-150">JavaScript</span><span class="sxs-lookup"><span data-stu-id="1460a-150">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/tablecolumncollection-add-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="1460a-151">Objective-C</span><span class="sxs-lookup"><span data-stu-id="1460a-151">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/tablecolumncollection-add-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[<span data-ttu-id="1460a-152">Java</span><span class="sxs-lookup"><span data-stu-id="1460a-152">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/tablecolumncollection-add-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a><span data-ttu-id="1460a-153">响应</span><span class="sxs-lookup"><span data-stu-id="1460a-153">Response</span></span>
<span data-ttu-id="1460a-p106">下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="1460a-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookTableColumn"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 81

{
  "id": "99",
  "name": "name-value",
  "index": 99,
  "values": "values-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "TableColumnCollection: add",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->


