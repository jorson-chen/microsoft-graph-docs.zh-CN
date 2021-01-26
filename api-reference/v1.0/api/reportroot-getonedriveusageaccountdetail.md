---
title: 'reportRoot: getOneDriveUsageAccountDetail'
description: 获取帐户的 OneDrive 使用情况的详细信息。
localization_priority: Normal
ms.prod: reports
author: sarahwxy
doc_type: apiPageType
ms.openlocfilehash: 5ed5a3bb06a80d7af6505e6042e566da2f511dd6
ms.sourcegitcommit: 479b366f3265b666fdc024b0f90b8d29764bb4b2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/26/2021
ms.locfileid: "49981219"
---
# <a name="reportroot-getonedriveusageaccountdetail"></a><span data-ttu-id="564c3-103">reportRoot: getOneDriveUsageAccountDetail</span><span class="sxs-lookup"><span data-stu-id="564c3-103">reportRoot: getOneDriveUsageAccountDetail</span></span>

<span data-ttu-id="564c3-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="564c3-104">Namespace: microsoft.graph</span></span>

<span data-ttu-id="564c3-105">获取帐户的 OneDrive 使用情况的详细信息。</span><span class="sxs-lookup"><span data-stu-id="564c3-105">Get details about OneDrive usage by account.</span></span>

> <span data-ttu-id="564c3-106">**注意：** 有关不同报表视图和名称的详细信息，请参阅 [Microsoft 365 报表 - OneDrive for Business 使用情况](https://support.office.com/client/OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680)。</span><span class="sxs-lookup"><span data-stu-id="564c3-106">**Note:** For details about different report views and names, see [Microsoft 365 reports - OneDrive for Business usage](https://support.office.com/client/OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680).</span></span>

## <a name="permissions"></a><span data-ttu-id="564c3-107">Permissions</span><span class="sxs-lookup"><span data-stu-id="564c3-107">Permissions</span></span>

<span data-ttu-id="564c3-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="564c3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="564c3-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="564c3-110">Permission type</span></span>                        | <span data-ttu-id="564c3-111">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="564c3-111">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="564c3-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="564c3-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="564c3-113">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="564c3-113">Reports.Read.All</span></span>                         |
| <span data-ttu-id="564c3-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="564c3-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="564c3-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="564c3-115">Not supported.</span></span>                           |
| <span data-ttu-id="564c3-116">应用</span><span class="sxs-lookup"><span data-stu-id="564c3-116">Application</span></span>                            | <span data-ttu-id="564c3-117">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="564c3-117">Reports.Read.All</span></span>                         |

<span data-ttu-id="564c3-118">**注意**：若要获得委派权限以允许应用代表用户读取服务使用情况报告，租户管理员必须事先为用户分配适当的 Azure AD 受限管理员角色。</span><span class="sxs-lookup"><span data-stu-id="564c3-118">**Note**: For delegated permissions to allow apps to read service usage reports on behalf of a user, the tenant administrator must have assigned the user the appropriate Azure AD limited administrator role.</span></span> <span data-ttu-id="564c3-119">有关更多详细信息，请参阅[授权 API 读取 Microsoft 365 使用情况报告](/graph/reportroot-authorization)。</span><span class="sxs-lookup"><span data-stu-id="564c3-119">For more details, see [Authorization for APIs to read Microsoft 365 usage reports](/graph/reportroot-authorization).</span></span>

## <a name="http-request"></a><span data-ttu-id="564c3-120">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="564c3-120">HTTP request</span></span>


<!-- { "blockType": "samples" } --> 

```http
GET /reports/getOneDriveUsageAccountDetail(period='{period_value}')
GET /reports/getOneDriveUsageAccountDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="564c3-121">函数参数</span><span class="sxs-lookup"><span data-stu-id="564c3-121">Function parameters</span></span>

<span data-ttu-id="564c3-122">在请求 URL 中，提供以下任一参数的有效值。</span><span class="sxs-lookup"><span data-stu-id="564c3-122">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="564c3-123">参数</span><span class="sxs-lookup"><span data-stu-id="564c3-123">Parameter</span></span> | <span data-ttu-id="564c3-124">类型</span><span class="sxs-lookup"><span data-stu-id="564c3-124">Type</span></span>   | <span data-ttu-id="564c3-125">说明</span><span class="sxs-lookup"><span data-stu-id="564c3-125">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="564c3-126">period</span><span class="sxs-lookup"><span data-stu-id="564c3-126">period</span></span>    | <span data-ttu-id="564c3-127">string</span><span class="sxs-lookup"><span data-stu-id="564c3-127">string</span></span> | <span data-ttu-id="564c3-128">指定在多长时间内聚合报表。</span><span class="sxs-lookup"><span data-stu-id="564c3-128">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="564c3-129">受支持的 {period_value} 值为：D7、D30、D90 和 D180。</span><span class="sxs-lookup"><span data-stu-id="564c3-129">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="564c3-130">这些值采用格式 D *n*，其中 *n* 表示在多少天内聚合报表。</span><span class="sxs-lookup"><span data-stu-id="564c3-130">These values follow the format D *n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="564c3-131">date</span><span class="sxs-lookup"><span data-stu-id="564c3-131">date</span></span>      | <span data-ttu-id="564c3-132">Date</span><span class="sxs-lookup"><span data-stu-id="564c3-132">Date</span></span>   | <span data-ttu-id="564c3-133">指定要查看用户在哪个日期执行的任何活动。</span><span class="sxs-lookup"><span data-stu-id="564c3-133">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="564c3-134">{date_value} 必须采用格式 YYYY-MM-DD。</span><span class="sxs-lookup"><span data-stu-id="564c3-134">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="564c3-135">因为此报表的有效期仅为过去 30 天，所以 {date_value} 应为这个范围内的日期。</span><span class="sxs-lookup"><span data-stu-id="564c3-135">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="564c3-136">**注意：** 需要在 URL 中设置 period 或 date。</span><span class="sxs-lookup"><span data-stu-id="564c3-136">**Note:** You need to set either period or date in the URL.</span></span>

## <a name="request-headers"></a><span data-ttu-id="564c3-137">请求头</span><span class="sxs-lookup"><span data-stu-id="564c3-137">Request headers</span></span>

| <span data-ttu-id="564c3-138">名称</span><span class="sxs-lookup"><span data-stu-id="564c3-138">Name</span></span>          | <span data-ttu-id="564c3-139">说明</span><span class="sxs-lookup"><span data-stu-id="564c3-139">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="564c3-140">Authorization</span><span class="sxs-lookup"><span data-stu-id="564c3-140">Authorization</span></span> | <span data-ttu-id="564c3-p105">持有者{令牌}。必需。</span><span class="sxs-lookup"><span data-stu-id="564c3-p105">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="564c3-143">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="564c3-143">If-None-Match</span></span> | <span data-ttu-id="564c3-144">如果包含此请求头，且提供的 eTag 与文件中的当前标记一致，返回的是 `304 Not Modified` 响应代码。</span><span class="sxs-lookup"><span data-stu-id="564c3-144">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="564c3-145">可选。</span><span class="sxs-lookup"><span data-stu-id="564c3-145">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="564c3-146">响应</span><span class="sxs-lookup"><span data-stu-id="564c3-146">Response</span></span>

<span data-ttu-id="564c3-147">如果成功，此方法返回 `302 Found` 响应，以重定向到报表的预先验证的下载 URL。</span><span class="sxs-lookup"><span data-stu-id="564c3-147">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="564c3-148">可以在响应的 `Location` 头中找到此 URL。</span><span class="sxs-lookup"><span data-stu-id="564c3-148">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="564c3-149">预先验证的下载 URL 的有效时间很短（几分钟），不需要 `Authorization` 头。</span><span class="sxs-lookup"><span data-stu-id="564c3-149">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="564c3-150">CSV 文件包含下面的列标题。</span><span class="sxs-lookup"><span data-stu-id="564c3-150">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="564c3-151">报表刷新日期</span><span class="sxs-lookup"><span data-stu-id="564c3-151">Report Refresh Date</span></span>
- <span data-ttu-id="564c3-152">网站 URL</span><span class="sxs-lookup"><span data-stu-id="564c3-152">Site URL</span></span>
- <span data-ttu-id="564c3-153">所有者显示名称</span><span class="sxs-lookup"><span data-stu-id="564c3-153">Owner Display Name</span></span>
- <span data-ttu-id="564c3-154">已删除</span><span class="sxs-lookup"><span data-stu-id="564c3-154">Is Deleted</span></span>
- <span data-ttu-id="564c3-155">上次活动日期</span><span class="sxs-lookup"><span data-stu-id="564c3-155">Last Activity Date</span></span>
- <span data-ttu-id="564c3-156">文件数</span><span class="sxs-lookup"><span data-stu-id="564c3-156">File Count</span></span>
- <span data-ttu-id="564c3-157">活跃文件数</span><span class="sxs-lookup"><span data-stu-id="564c3-157">Active File Count</span></span>
- <span data-ttu-id="564c3-158">已使用的存储（字节）</span><span class="sxs-lookup"><span data-stu-id="564c3-158">Storage Used (Byte)</span></span>
- <span data-ttu-id="564c3-159">已分配的存储（字节）</span><span class="sxs-lookup"><span data-stu-id="564c3-159">Storage Allocated (Byte)</span></span>
- <span data-ttu-id="564c3-160">所有者主体名称</span><span class="sxs-lookup"><span data-stu-id="564c3-160">Owner Principal Name</span></span>
- <span data-ttu-id="564c3-161">报表周期</span><span class="sxs-lookup"><span data-stu-id="564c3-161">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="564c3-162">示例</span><span class="sxs-lookup"><span data-stu-id="564c3-162">Example</span></span>

#### <a name="request"></a><span data-ttu-id="564c3-163">请求</span><span class="sxs-lookup"><span data-stu-id="564c3-163">Request</span></span>

<span data-ttu-id="564c3-164">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="564c3-164">The following is an example of the request.</span></span>


<!--{
  "blockType": "ignored",
  "isComposable": true,
  "name": "reportroot_getonedriveusageuserdetail"
}-->

```msgraph-interactive
GET https://graph.microsoft.com/v1.0/reports/getOneDriveUsageAccountDetail(period='D7')
```


#### <a name="response"></a><span data-ttu-id="564c3-165">响应</span><span class="sxs-lookup"><span data-stu-id="564c3-165">Response</span></span>

<span data-ttu-id="564c3-166">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="564c3-166">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.report"
} -->

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="564c3-167">执行 302 重定向，下载的 CSV 文件将采用以下架构。</span><span class="sxs-lookup"><span data-stu-id="564c3-167">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Site URL,Owner Display Name,Is Deleted,Last Activity Date,File Count,Active File Count,Storage Used (Byte),Storage Allocated (Byte),Owner Principal Name,Report Period
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

