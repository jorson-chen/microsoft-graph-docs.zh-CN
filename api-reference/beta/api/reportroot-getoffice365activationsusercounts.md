---
title: 'reportRoot: getOffice365ActivationsUserCounts'
description: 获取已启用的用户数，以及已激活桌面或设备或共享计算机上的 Office 订阅的用户数。
localization_priority: Normal
ms.prod: reports
author: sarahwxy
doc_type: apiPageType
ms.openlocfilehash: a93a4207285d84dc9a9d748d85e43908aff2d13d
ms.sourcegitcommit: 479b366f3265b666fdc024b0f90b8d29764bb4b2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/26/2021
ms.locfileid: "49983725"
---
# <a name="reportroot-getoffice365activationsusercounts"></a><span data-ttu-id="970c8-103">reportRoot: getOffice365ActivationsUserCounts</span><span class="sxs-lookup"><span data-stu-id="970c8-103">reportRoot: getOffice365ActivationsUserCounts</span></span>

<span data-ttu-id="970c8-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="970c8-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="970c8-105">获取已启用的用户数，以及已激活桌面或设备或共享计算机上的 Office 订阅的用户数。</span><span class="sxs-lookup"><span data-stu-id="970c8-105">Get the count of users that are enabled and those that have activated the Office subscription on desktop or devices or shared computers.</span></span>

> <span data-ttu-id="970c8-106">**注意：** 有关不同报表视图和名称的详细信息，请参阅 [Microsoft 365 报表 -](https://support.office.com/client/Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60)Microsoft Office激活。</span><span class="sxs-lookup"><span data-stu-id="970c8-106">**Note:** For details about different report views and names, see [Microsoft 365 reports - Microsoft Office activations](https://support.office.com/client/Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60).</span></span>

## <a name="permissions"></a><span data-ttu-id="970c8-107">Permissions</span><span class="sxs-lookup"><span data-stu-id="970c8-107">Permissions</span></span>

<span data-ttu-id="970c8-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="970c8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="970c8-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="970c8-110">Permission type</span></span>                        | <span data-ttu-id="970c8-111">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="970c8-111">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="970c8-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="970c8-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="970c8-113">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="970c8-113">Reports.Read.All</span></span>                         |
| <span data-ttu-id="970c8-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="970c8-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="970c8-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="970c8-115">Not supported.</span></span>                           |
| <span data-ttu-id="970c8-116">应用</span><span class="sxs-lookup"><span data-stu-id="970c8-116">Application</span></span>                            | <span data-ttu-id="970c8-117">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="970c8-117">Reports.Read.All</span></span>                         |

<span data-ttu-id="970c8-118">**注意**：若要获得委派权限以允许应用代表用户读取服务使用情况报告，租户管理员必须事先为用户分配适当的 Azure AD 受限管理员角色。</span><span class="sxs-lookup"><span data-stu-id="970c8-118">**Note**: For delegated permissions to allow apps to read service usage reports on behalf of a user, the tenant administrator must have assigned the user the appropriate Azure AD limited administrator role.</span></span> <span data-ttu-id="970c8-119">有关更多详细信息，请参阅[授权 API 读取 Microsoft 365 使用情况报告](/graph/reportroot-authorization)。</span><span class="sxs-lookup"><span data-stu-id="970c8-119">For more details, see [Authorization for APIs to read Microsoft 365 usage reports](/graph/reportroot-authorization).</span></span>

## <a name="http-request"></a><span data-ttu-id="970c8-120">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="970c8-120">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOffice365ActivationsUserCounts
```

## <a name="query-parameters"></a><span data-ttu-id="970c8-121">查询参数</span><span class="sxs-lookup"><span data-stu-id="970c8-121">Query parameters</span></span>

<span data-ttu-id="970c8-122">此方法支持使用 `$format` [OData 查询参数](/graph/query-parameters)自定义响应。</span><span class="sxs-lookup"><span data-stu-id="970c8-122">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="970c8-123">默认输出类型为 text/csv。</span><span class="sxs-lookup"><span data-stu-id="970c8-123">The default output type is text/csv.</span></span> <span data-ttu-id="970c8-124">但是，如果要指定输出类型，可以使用设置为 text/csv 或 application/json 的 OData $format查询参数。</span><span class="sxs-lookup"><span data-stu-id="970c8-124">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="970c8-125">请求标头</span><span class="sxs-lookup"><span data-stu-id="970c8-125">Request headers</span></span>

| <span data-ttu-id="970c8-126">名称</span><span class="sxs-lookup"><span data-stu-id="970c8-126">Name</span></span>          | <span data-ttu-id="970c8-127">说明</span><span class="sxs-lookup"><span data-stu-id="970c8-127">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="970c8-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="970c8-128">Authorization</span></span> | <span data-ttu-id="970c8-p104">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="970c8-p104">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="970c8-131">响应</span><span class="sxs-lookup"><span data-stu-id="970c8-131">Response</span></span>

### <a name="csv"></a><span data-ttu-id="970c8-132">CSV</span><span class="sxs-lookup"><span data-stu-id="970c8-132">CSV</span></span>

<span data-ttu-id="970c8-133">如果成功，此方法返回 `302 Found` 响应，以重定向到报表的预先验证的下载 URL。</span><span class="sxs-lookup"><span data-stu-id="970c8-133">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="970c8-134">可以在响应的 `Location` 头中找到此 URL。</span><span class="sxs-lookup"><span data-stu-id="970c8-134">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="970c8-135">预先验证的下载 URL 的有效时间很短（几分钟），不需要 `Authorization` 头。</span><span class="sxs-lookup"><span data-stu-id="970c8-135">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="970c8-136">CSV 文件包含下面的列标题。</span><span class="sxs-lookup"><span data-stu-id="970c8-136">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="970c8-137">报表刷新日期</span><span class="sxs-lookup"><span data-stu-id="970c8-137">Report Refresh Date</span></span>
- <span data-ttu-id="970c8-138">产品类型</span><span class="sxs-lookup"><span data-stu-id="970c8-138">Product Type</span></span>
- <span data-ttu-id="970c8-139">已分配</span><span class="sxs-lookup"><span data-stu-id="970c8-139">Assigned</span></span>
- <span data-ttu-id="970c8-140">已激活</span><span class="sxs-lookup"><span data-stu-id="970c8-140">Activated</span></span>
- <span data-ttu-id="970c8-141">共享计算机激活</span><span class="sxs-lookup"><span data-stu-id="970c8-141">Shared Computer Activation</span></span>

### <a name="json"></a><span data-ttu-id="970c8-142">JSON</span><span class="sxs-lookup"><span data-stu-id="970c8-142">JSON</span></span>

<span data-ttu-id="970c8-143">如果成功，此方法在响应正文中返回响应代码和 `200 OK` **[office365ActivationsUserCounts](../resources/office365activationsusercounts.md)** 对象。</span><span class="sxs-lookup"><span data-stu-id="970c8-143">If successful, this method returns a `200 OK` response code and an **[office365ActivationsUserCounts](../resources/office365activationsusercounts.md)** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="970c8-144">示例</span><span class="sxs-lookup"><span data-stu-id="970c8-144">Example</span></span>

### <a name="csv"></a><span data-ttu-id="970c8-145">CSV</span><span class="sxs-lookup"><span data-stu-id="970c8-145">CSV</span></span>

<span data-ttu-id="970c8-146">下面是一个输出 CSV 的示例。</span><span class="sxs-lookup"><span data-stu-id="970c8-146">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="970c8-147">请求</span><span class="sxs-lookup"><span data-stu-id="970c8-147">Request</span></span>

<span data-ttu-id="970c8-148">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="970c8-148">The following is an example of the request.</span></span>


<!-- {
  "blockType": "ignored",
  "name": "reportroot_getoffice365activationsusercounts_csv"
}-->

```msgraph-interactive
GET https://graph.microsoft.com/beta/reports/getOffice365ActivationsUserCounts?$format=text/csv
```


#### <a name="response"></a><span data-ttu-id="970c8-149">响应</span><span class="sxs-lookup"><span data-stu-id="970c8-149">Response</span></span>

<span data-ttu-id="970c8-150">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="970c8-150">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="970c8-151">执行 302 重定向，下载的 CSV 文件将采用以下架构。</span><span class="sxs-lookup"><span data-stu-id="970c8-151">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Product Type,Assigned,Activated,Shared Computer Activation
```

### <a name="json"></a><span data-ttu-id="970c8-152">JSON</span><span class="sxs-lookup"><span data-stu-id="970c8-152">JSON</span></span>

<span data-ttu-id="970c8-153">下面是返回 JSON 的示例。</span><span class="sxs-lookup"><span data-stu-id="970c8-153">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="970c8-154">请求</span><span class="sxs-lookup"><span data-stu-id="970c8-154">Request</span></span>

<span data-ttu-id="970c8-155">下面为请求示例。</span><span class="sxs-lookup"><span data-stu-id="970c8-155">The following example shows the request.</span></span>


<!-- {
  "blockType": "ignored",
  "name": "reportroot_getoffice365activationsusercounts_json"
}-->

```msgraph-interactive
GET https://graph.microsoft.com/beta/reports/getOffice365ActivationsUserCounts?$format=application/json
```


#### <a name="response"></a><span data-ttu-id="970c8-156">响应</span><span class="sxs-lookup"><span data-stu-id="970c8-156">Response</span></span>

<span data-ttu-id="970c8-157">以下示例显示了相应的响应。</span><span class="sxs-lookup"><span data-stu-id="970c8-157">The following example shows the response.</span></span>

> <span data-ttu-id="970c8-p106">**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。所有属性都将通过实际调用返回。</span><span class="sxs-lookup"><span data-stu-id="970c8-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.office365ActivationsUserCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 233

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.office365ActivationsUserCounts)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "productType": "Microsoft 365 Apps for enterprise", 
      "assigned": 2679, 
      "activated": 1710,
      "sharedComputerActivation": 1024
    }
  ]
}
```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79 
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Example",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->


