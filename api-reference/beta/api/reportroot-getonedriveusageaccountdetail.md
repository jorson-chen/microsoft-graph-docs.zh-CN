---
title: 'reportRoot: getOneDriveUsageAccountDetail'
description: 获取帐户的 OneDrive 使用情况的详细信息。
localization_priority: Normal
ms.prod: reports
author: sarahwxy
doc_type: apiPageType
ms.openlocfilehash: 7da7b20c4f2fcf2a8f99fc75d07c6244ac1b2ad8
ms.sourcegitcommit: 479b366f3265b666fdc024b0f90b8d29764bb4b2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/26/2021
ms.locfileid: "49981240"
---
# <a name="reportroot-getonedriveusageaccountdetail"></a><span data-ttu-id="5d965-103">reportRoot: getOneDriveUsageAccountDetail</span><span class="sxs-lookup"><span data-stu-id="5d965-103">reportRoot: getOneDriveUsageAccountDetail</span></span>

<span data-ttu-id="5d965-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="5d965-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="5d965-105">获取帐户的 OneDrive 使用情况的详细信息。</span><span class="sxs-lookup"><span data-stu-id="5d965-105">Get details about OneDrive usage by account.</span></span>

> <span data-ttu-id="5d965-106">**注意：** 有关不同报表视图和名称的详细信息，请参阅 [Microsoft 365 报表 - OneDrive for Business 使用情况](https://support.office.com/client/OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680)。</span><span class="sxs-lookup"><span data-stu-id="5d965-106">**Note:** For details about different report views and names, see [Microsoft 365 reports - OneDrive for Business usage](https://support.office.com/client/OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680).</span></span>

## <a name="permissions"></a><span data-ttu-id="5d965-107">Permissions</span><span class="sxs-lookup"><span data-stu-id="5d965-107">Permissions</span></span>

<span data-ttu-id="5d965-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="5d965-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="5d965-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="5d965-110">Permission type</span></span>                        | <span data-ttu-id="5d965-111">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="5d965-111">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="5d965-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="5d965-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="5d965-113">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="5d965-113">Reports.Read.All</span></span>                         |
| <span data-ttu-id="5d965-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="5d965-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5d965-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="5d965-115">Not supported.</span></span>                           |
| <span data-ttu-id="5d965-116">应用</span><span class="sxs-lookup"><span data-stu-id="5d965-116">Application</span></span>                            | <span data-ttu-id="5d965-117">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="5d965-117">Reports.Read.All</span></span>                         |

<span data-ttu-id="5d965-118">**注意**：若要获得委派权限以允许应用代表用户读取服务使用情况报告，租户管理员必须事先为用户分配适当的 Azure AD 受限管理员角色。</span><span class="sxs-lookup"><span data-stu-id="5d965-118">**Note**: For delegated permissions to allow apps to read service usage reports on behalf of a user, the tenant administrator must have assigned the user the appropriate Azure AD limited administrator role.</span></span> <span data-ttu-id="5d965-119">有关更多详细信息，请参阅[授权 API 读取 Microsoft 365 使用情况报告](/graph/reportroot-authorization)。</span><span class="sxs-lookup"><span data-stu-id="5d965-119">For more details, see [Authorization for APIs to read Microsoft 365 usage reports](/graph/reportroot-authorization).</span></span>

## <a name="http-request"></a><span data-ttu-id="5d965-120">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="5d965-120">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOneDriveUsageAccountDetail(period='{period_value}')
GET /reports/getOneDriveUsageAccountDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="5d965-121">函数参数</span><span class="sxs-lookup"><span data-stu-id="5d965-121">Function parameters</span></span>

<span data-ttu-id="5d965-122">在请求 URL 中，提供以下任一参数的有效值。</span><span class="sxs-lookup"><span data-stu-id="5d965-122">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="5d965-123">参数</span><span class="sxs-lookup"><span data-stu-id="5d965-123">Parameter</span></span> | <span data-ttu-id="5d965-124">类型</span><span class="sxs-lookup"><span data-stu-id="5d965-124">Type</span></span>   | <span data-ttu-id="5d965-125">说明</span><span class="sxs-lookup"><span data-stu-id="5d965-125">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="5d965-126">period</span><span class="sxs-lookup"><span data-stu-id="5d965-126">period</span></span>    | <span data-ttu-id="5d965-127">string</span><span class="sxs-lookup"><span data-stu-id="5d965-127">string</span></span> | <span data-ttu-id="5d965-128">指定在多长时间内聚合报表。</span><span class="sxs-lookup"><span data-stu-id="5d965-128">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="5d965-129">受支持的 {period_value} 值为：D7、D30、D90 和 D180。</span><span class="sxs-lookup"><span data-stu-id="5d965-129">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="5d965-130">这些值采用格式 D *n*，其中 *n* 表示在多少天内聚合报表。</span><span class="sxs-lookup"><span data-stu-id="5d965-130">These values follow the format D *n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="5d965-131">date</span><span class="sxs-lookup"><span data-stu-id="5d965-131">date</span></span>      | <span data-ttu-id="5d965-132">Date</span><span class="sxs-lookup"><span data-stu-id="5d965-132">Date</span></span>   | <span data-ttu-id="5d965-133">指定要查看用户在哪个日期执行的任何活动。</span><span class="sxs-lookup"><span data-stu-id="5d965-133">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="5d965-134">{date_value} 必须采用格式 YYYY-MM-DD。</span><span class="sxs-lookup"><span data-stu-id="5d965-134">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="5d965-135">因为此报表的有效期仅为过去 30 天，所以 {date_value} 应为这个范围内的日期。</span><span class="sxs-lookup"><span data-stu-id="5d965-135">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="5d965-136">**注意：** 需要在 URL 中设置 period 或 date。</span><span class="sxs-lookup"><span data-stu-id="5d965-136">**Note:** You need to set either period or date in the URL.</span></span>

<span data-ttu-id="5d965-137">此方法支持使用 `$format`、`$top` 和 `$skipToken` [OData 查询参数](/graph/query-parameters)自定义响应。</span><span class="sxs-lookup"><span data-stu-id="5d965-137">This method supports the `$format`, `$top`, and `$skipToken` [OData query parameters](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="5d965-138">默认输出类型为 text/csv。</span><span class="sxs-lookup"><span data-stu-id="5d965-138">The default output type is text/csv.</span></span> <span data-ttu-id="5d965-139">但是，如果要指定输出类型，可以使用设置为 text/csv 或 application/json 的 OData $format查询参数。</span><span class="sxs-lookup"><span data-stu-id="5d965-139">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="5d965-140">请求标头</span><span class="sxs-lookup"><span data-stu-id="5d965-140">Request headers</span></span>

| <span data-ttu-id="5d965-141">名称</span><span class="sxs-lookup"><span data-stu-id="5d965-141">Name</span></span>          | <span data-ttu-id="5d965-142">说明</span><span class="sxs-lookup"><span data-stu-id="5d965-142">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="5d965-143">Authorization</span><span class="sxs-lookup"><span data-stu-id="5d965-143">Authorization</span></span> | <span data-ttu-id="5d965-p106">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="5d965-p106">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="5d965-146">响应</span><span class="sxs-lookup"><span data-stu-id="5d965-146">Response</span></span>

### <a name="csv"></a><span data-ttu-id="5d965-147">CSV</span><span class="sxs-lookup"><span data-stu-id="5d965-147">CSV</span></span>

<span data-ttu-id="5d965-148">如果成功，此方法返回 `302 Found` 响应，以重定向到报表的预先验证的下载 URL。</span><span class="sxs-lookup"><span data-stu-id="5d965-148">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="5d965-149">可以在响应的 `Location` 头中找到此 URL。</span><span class="sxs-lookup"><span data-stu-id="5d965-149">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="5d965-150">预先验证的下载 URL 的有效时间很短（几分钟），不需要 `Authorization` 头。</span><span class="sxs-lookup"><span data-stu-id="5d965-150">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="5d965-151">CSV 文件包含下面的列标题。</span><span class="sxs-lookup"><span data-stu-id="5d965-151">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="5d965-152">报表刷新日期</span><span class="sxs-lookup"><span data-stu-id="5d965-152">Report Refresh Date</span></span>
- <span data-ttu-id="5d965-153">网站 URL</span><span class="sxs-lookup"><span data-stu-id="5d965-153">Site URL</span></span>
- <span data-ttu-id="5d965-154">所有者显示名称</span><span class="sxs-lookup"><span data-stu-id="5d965-154">Owner Display Name</span></span>
- <span data-ttu-id="5d965-155">已删除</span><span class="sxs-lookup"><span data-stu-id="5d965-155">Is Deleted</span></span>
- <span data-ttu-id="5d965-156">上次活动日期</span><span class="sxs-lookup"><span data-stu-id="5d965-156">Last Activity Date</span></span>
- <span data-ttu-id="5d965-157">文件数</span><span class="sxs-lookup"><span data-stu-id="5d965-157">File Count</span></span>
- <span data-ttu-id="5d965-158">活跃文件数</span><span class="sxs-lookup"><span data-stu-id="5d965-158">Active File Count</span></span>
- <span data-ttu-id="5d965-159">已使用的存储（字节）</span><span class="sxs-lookup"><span data-stu-id="5d965-159">Storage Used (Byte)</span></span>
- <span data-ttu-id="5d965-160">已分配的存储（字节）</span><span class="sxs-lookup"><span data-stu-id="5d965-160">Storage Allocated (Byte)</span></span>
- <span data-ttu-id="5d965-161">所有者主体名称</span><span class="sxs-lookup"><span data-stu-id="5d965-161">Owner Principal Name</span></span>
- <span data-ttu-id="5d965-162">报表周期</span><span class="sxs-lookup"><span data-stu-id="5d965-162">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="5d965-163">JSON</span><span class="sxs-lookup"><span data-stu-id="5d965-163">JSON</span></span>

<span data-ttu-id="5d965-164">如果成功，此方法在响应正文中返回响应代码和 `200 OK` **[oneDriveUsageAccountDetail](../resources/onedriveusageaccountdetail.md)** 对象。</span><span class="sxs-lookup"><span data-stu-id="5d965-164">If successful, this method returns a `200 OK` response code and a **[oneDriveUsageAccountDetail](../resources/onedriveusageaccountdetail.md)** object in the response body.</span></span>

<span data-ttu-id="5d965-165">此请求的默认页面大小为 200 个项目。</span><span class="sxs-lookup"><span data-stu-id="5d965-165">The default page size for this request is 200 items.</span></span>

## <a name="example"></a><span data-ttu-id="5d965-166">示例</span><span class="sxs-lookup"><span data-stu-id="5d965-166">Example</span></span>

<span data-ttu-id="5d965-167">下面是一个输出 CSV 的示例。</span><span class="sxs-lookup"><span data-stu-id="5d965-167">The following is an example that outputs CSV.</span></span>

### <a name="csv"></a><span data-ttu-id="5d965-168">CSV</span><span class="sxs-lookup"><span data-stu-id="5d965-168">CSV</span></span>

#### <a name="request"></a><span data-ttu-id="5d965-169">请求</span><span class="sxs-lookup"><span data-stu-id="5d965-169">Request</span></span>

<span data-ttu-id="5d965-170">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="5d965-170">The following is an example of the request.</span></span>


<!-- {
  "blockType": "ignored",
  "name": "reportroot_getonedriveusageaccountdetail_csv"
}-->

```msgraph-interactive
GET https://graph.microsoft.com/beta/reports/getOneDriveUsageAccountDetail(period='D7')?$format=text/csv
```


#### <a name="response"></a><span data-ttu-id="5d965-171">响应</span><span class="sxs-lookup"><span data-stu-id="5d965-171">Response</span></span>

<span data-ttu-id="5d965-172">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="5d965-172">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="5d965-173">执行 302 重定向，下载的 CSV 文件将采用以下架构。</span><span class="sxs-lookup"><span data-stu-id="5d965-173">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Site URL,Owner Display Name,Is Deleted,Last Activity Date,File Count,Active File Count,Storage Used (Byte),Storage Allocated (Byte),Owner Principal Name,Report Period
```

### <a name="json"></a><span data-ttu-id="5d965-174">JSON</span><span class="sxs-lookup"><span data-stu-id="5d965-174">JSON</span></span>

<span data-ttu-id="5d965-175">下面是返回 JSON 的示例。</span><span class="sxs-lookup"><span data-stu-id="5d965-175">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="5d965-176">请求</span><span class="sxs-lookup"><span data-stu-id="5d965-176">Request</span></span>

<span data-ttu-id="5d965-177">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="5d965-177">The following is an example of the request.</span></span>


<!-- {
  "blockType": "ignored",
  "name": "reportroot_getonedriveusageaccountdetail_json"
}-->

```msgraph-interactive
GET https://graph.microsoft.com/beta/reports/getOneDriveUsageAccountDetail(period='D7')?$format=application/json
```


#### <a name="response"></a><span data-ttu-id="5d965-178">响应</span><span class="sxs-lookup"><span data-stu-id="5d965-178">Response</span></span>

<span data-ttu-id="5d965-179">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="5d965-179">The following is an example of the response.</span></span>

> <span data-ttu-id="5d965-p108">**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。所有属性都将通过实际调用返回。</span><span class="sxs-lookup"><span data-stu-id="5d965-p108">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.oneDriveUsageAccountDetail"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 400

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.oneDriveUsageAccountDetail)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "siteUrl": "siteUrl-value", 
      "ownerDisplayName": "ownerDisplayName-value", 
      "ownerPrincipalName": "ownerPrincipalName-value", 
      "isDeleted": false, 
      "lastActivityDate": "2017-09-01", 
      "fileCount": 9, 
      "activeFileCount": 5, 
      "storageUsedInBytes": 12190375, 
      "storageAllocatedInBytes": 549755813880, 
      "reportPeriod": "7"
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


