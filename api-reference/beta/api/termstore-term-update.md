---
title: 更新术语
description: 更新术语对象的属性。
author: mohitpcad
localization_priority: Normal
ms.prod: Sharepoint
doc_type: apiPageType
ms.openlocfilehash: 1168407425b0ef8faff213fd807f9499317e0f7b
ms.sourcegitcommit: eacd2a6e46c19dd3cd8519592b1668fabe14d85d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "49874380"
---
# <a name="update-term"></a><span data-ttu-id="c7a1f-103">更新术语</span><span class="sxs-lookup"><span data-stu-id="c7a1f-103">Update term</span></span>
<span data-ttu-id="c7a1f-104">命名空间：microsoft.graph.termStore</span><span class="sxs-lookup"><span data-stu-id="c7a1f-104">Namespace: microsoft.graph.termStore</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="c7a1f-105">更新 [术语对象的属性](../resources/termstore-term.md) 。</span><span class="sxs-lookup"><span data-stu-id="c7a1f-105">Update the properties of a [term](../resources/termstore-term.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="c7a1f-106">权限</span><span class="sxs-lookup"><span data-stu-id="c7a1f-106">Permissions</span></span>
<span data-ttu-id="c7a1f-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="c7a1f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c7a1f-109">权限类型</span><span class="sxs-lookup"><span data-stu-id="c7a1f-109">Permission type</span></span>|<span data-ttu-id="c7a1f-110">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="c7a1f-110">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c7a1f-111">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="c7a1f-111">Delegated (work or school account)</span></span> | <span data-ttu-id="c7a1f-112">TermStore.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c7a1f-112">TermStore.ReadWrite.All</span></span> |
|<span data-ttu-id="c7a1f-113">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="c7a1f-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c7a1f-114">不支持。</span><span class="sxs-lookup"><span data-stu-id="c7a1f-114">Not supported.</span></span>    |
|<span data-ttu-id="c7a1f-115">应用程序</span><span class="sxs-lookup"><span data-stu-id="c7a1f-115">Application</span></span> | <span data-ttu-id="c7a1f-116">不支持。</span><span class="sxs-lookup"><span data-stu-id="c7a1f-116">Not supported.</span></span> |


## <a name="http-request"></a><span data-ttu-id="c7a1f-117">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="c7a1f-117">HTTP request</span></span>

<!-- {
  "blockType": "ignored"
}-->

``` http
PATCH /termStore/sets/{setId}/terms/{termId}
```

## <a name="request-headers"></a><span data-ttu-id="c7a1f-118">请求标头</span><span class="sxs-lookup"><span data-stu-id="c7a1f-118">Request headers</span></span>
|<span data-ttu-id="c7a1f-119">名称</span><span class="sxs-lookup"><span data-stu-id="c7a1f-119">Name</span></span>|<span data-ttu-id="c7a1f-120">说明</span><span class="sxs-lookup"><span data-stu-id="c7a1f-120">Description</span></span>|
|:---|:---|
|<span data-ttu-id="c7a1f-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="c7a1f-121">Authorization</span></span>|<span data-ttu-id="c7a1f-p102">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="c7a1f-p102">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="c7a1f-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c7a1f-124">Content-Type</span></span>|<span data-ttu-id="c7a1f-p103">application/json. Required.</span><span class="sxs-lookup"><span data-stu-id="c7a1f-p103">application/json. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="c7a1f-127">请求正文</span><span class="sxs-lookup"><span data-stu-id="c7a1f-127">Request body</span></span>
<span data-ttu-id="c7a1f-128">在请求正文中，提供术语对象的 JSON [表示](../resources/termstore-term.md) 形式。</span><span class="sxs-lookup"><span data-stu-id="c7a1f-128">In the request body, supply a JSON representation of the [term](../resources/termstore-term.md) object.</span></span>

<span data-ttu-id="c7a1f-129">下表显示了可以更新术语 [的属性](../resources/termstore-term.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a1f-129">The following table shows the properties that can be updated for a [term](../resources/termstore-term.md).</span></span>

|<span data-ttu-id="c7a1f-130">属性</span><span class="sxs-lookup"><span data-stu-id="c7a1f-130">Property</span></span>|<span data-ttu-id="c7a1f-131">类型</span><span class="sxs-lookup"><span data-stu-id="c7a1f-131">Type</span></span>|<span data-ttu-id="c7a1f-132">Description</span><span class="sxs-lookup"><span data-stu-id="c7a1f-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c7a1f-133">labels</span><span class="sxs-lookup"><span data-stu-id="c7a1f-133">labels</span></span>|<span data-ttu-id="c7a1f-134">[microsoft.graph.termStore.localizedLabel](../resources/termstore-localizedlabel.md) 集合</span><span class="sxs-lookup"><span data-stu-id="c7a1f-134">[microsoft.graph.termStore.localizedLabel](../resources/termstore-localizedlabel.md) collection</span></span>|<span data-ttu-id="c7a1f-135">术语的标签</span><span class="sxs-lookup"><span data-stu-id="c7a1f-135">labels of a term</span></span>|
|<span data-ttu-id="c7a1f-136">说明</span><span class="sxs-lookup"><span data-stu-id="c7a1f-136">descriptions</span></span>|<span data-ttu-id="c7a1f-137">[microsoft.graph.termStore.localizedDescription](../resources/termstore-localizeddescription.md) 集合</span><span class="sxs-lookup"><span data-stu-id="c7a1f-137">[microsoft.graph.termStore.localizedDescription](../resources/termstore-localizeddescription.md) collection</span></span>|<span data-ttu-id="c7a1f-138">有关术语的说明</span><span class="sxs-lookup"><span data-stu-id="c7a1f-138">description about the term</span></span>|
|<span data-ttu-id="c7a1f-139">properties</span><span class="sxs-lookup"><span data-stu-id="c7a1f-139">properties</span></span>|<span data-ttu-id="c7a1f-140">[microsoft.graph.keyValue](../resources/keyvalue.md) 集合</span><span class="sxs-lookup"><span data-stu-id="c7a1f-140">[microsoft.graph.keyValue](../resources/keyvalue.md) collection</span></span>|<span data-ttu-id="c7a1f-141">与术语关联的属性</span><span class="sxs-lookup"><span data-stu-id="c7a1f-141">properties associated with the term</span></span>|



## <a name="response"></a><span data-ttu-id="c7a1f-142">响应</span><span class="sxs-lookup"><span data-stu-id="c7a1f-142">Response</span></span>

<span data-ttu-id="c7a1f-143">如果成功，此方法在响应 `200 OK` 正文中返回响应代码和更新[](../resources/termstore-term.md)的术语对象。</span><span class="sxs-lookup"><span data-stu-id="c7a1f-143">If successful, this method returns a `200 OK` response code and an updated [term](../resources/termstore-term.md) object in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="c7a1f-144">示例</span><span class="sxs-lookup"><span data-stu-id="c7a1f-144">Examples</span></span>

### <a name="request"></a><span data-ttu-id="c7a1f-145">请求</span><span class="sxs-lookup"><span data-stu-id="c7a1f-145">Request</span></span>

# <a name="http"></a>[<span data-ttu-id="c7a1f-146">HTTP</span><span class="sxs-lookup"><span data-stu-id="c7a1f-146">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "update_term"
} -->

``` http
PATCH https://graph.microsoft.com/beta/termStore/sets/{setId}/terms/{termId}
Content-Type: application/json
Content-length: 366

{
  "labels" : [
      {
          "name" : "changedLabel",
          "languageTag" : "en-US",
          "isDefault" : true
      }
  ]
}
```
# <a name="c"></a>[<span data-ttu-id="c7a1f-147">C#</span><span class="sxs-lookup"><span data-stu-id="c7a1f-147">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/update-term-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="c7a1f-148">JavaScript</span><span class="sxs-lookup"><span data-stu-id="c7a1f-148">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/update-term-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="c7a1f-149">Objective-C</span><span class="sxs-lookup"><span data-stu-id="c7a1f-149">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/update-term-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[<span data-ttu-id="c7a1f-150">Java</span><span class="sxs-lookup"><span data-stu-id="c7a1f-150">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/update-term-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---



### <a name="response"></a><span data-ttu-id="c7a1f-151">响应</span><span class="sxs-lookup"><span data-stu-id="c7a1f-151">Response</span></span>
<span data-ttu-id="c7a1f-152">**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。</span><span class="sxs-lookup"><span data-stu-id="c7a1f-152">**Note:** The response object shown here might be shortened for readability.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.termStore.term"
}-->

``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "id": "81be9856-9856-81be-5698-be815698be81",
  "labels" : [
      {
          "name" : "changedLabel",
          "languageTag" : "en-US",
          "isDefault" : true
      }
  ]
}
```

[microsoft.graph.termStore.term]: ../resources/termstore-term.md

<!--
{
  "type": "#page.annotation",
  "description": "Get term entity in termStore",
  "keywords": "term,termStore",
  "section": "documentation",
  "tocPath": "termStore/Update term",
  "suppressions": [
  ]
}
-->


