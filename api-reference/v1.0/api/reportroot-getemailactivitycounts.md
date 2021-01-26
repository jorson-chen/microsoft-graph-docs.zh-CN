---
title: 'reportRoot: getEmailActivityCounts'
description: 可便于了解组织中的电子邮件活动趋势（如已发送、已阅读和已接收的电子邮件数）。
localization_priority: Normal
ms.prod: reports
author: sarahwxy
doc_type: apiPageType
ms.openlocfilehash: 00072b3010caf2948bb85356eaab12a2973ce0ac
ms.sourcegitcommit: 479b366f3265b666fdc024b0f90b8d29764bb4b2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/26/2021
ms.locfileid: "49982143"
---
# <a name="reportroot-getemailactivitycounts"></a><span data-ttu-id="49840-103">reportRoot: getEmailActivityCounts</span><span class="sxs-lookup"><span data-stu-id="49840-103">reportRoot: getEmailActivityCounts</span></span>

<span data-ttu-id="49840-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="49840-104">Namespace: microsoft.graph</span></span>

<span data-ttu-id="49840-105">可便于了解组织中的电子邮件活动趋势（如已发送、已阅读和已接收的电子邮件数）。</span><span class="sxs-lookup"><span data-stu-id="49840-105">Enables you to understand the trends of email activity (like how many were sent, read, and received) in your organization.</span></span>

> <span data-ttu-id="49840-106">**备注：** 若要了解不同报表视图和名称的详细信息，请参阅 [Microsoft 365 报表 - 邮箱活动况](https://support.office.com/client/Email-activity-1cbe2c00-ca65-4fb9-9663-1bbfa58ebe44)。</span><span class="sxs-lookup"><span data-stu-id="49840-106">**Note:** For details about different report views and names, see [Microsoft 365 reports - Email Activity](https://support.office.com/client/Email-activity-1cbe2c00-ca65-4fb9-9663-1bbfa58ebe44).</span></span>

## <a name="permissions"></a><span data-ttu-id="49840-107">权限</span><span class="sxs-lookup"><span data-stu-id="49840-107">Permissions</span></span>

<span data-ttu-id="49840-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="49840-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="49840-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="49840-110">Permission type</span></span>                        | <span data-ttu-id="49840-111">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="49840-111">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="49840-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="49840-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="49840-113">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="49840-113">Reports.Read.All</span></span>                         |
| <span data-ttu-id="49840-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="49840-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="49840-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="49840-115">Not supported.</span></span>                           |
| <span data-ttu-id="49840-116">应用</span><span class="sxs-lookup"><span data-stu-id="49840-116">Application</span></span>                            | <span data-ttu-id="49840-117">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="49840-117">Reports.Read.All</span></span>                         |

> <span data-ttu-id="49840-118">**注意**：若要获得委派权限以允许应用代表用户读取服务使用情况报告，租户管理员必须事先为用户分配适当的 Azure AD 受限管理员角色。</span><span class="sxs-lookup"><span data-stu-id="49840-118">**Note**: For delegated permissions to allow apps to read service usage reports on behalf of a user, the tenant administrator must have assigned the user the appropriate Azure AD limited administrator role.</span></span> <span data-ttu-id="49840-119">有关更多详细信息，请参阅[授权 API 读取 Microsoft 365 使用情况报告](/graph/reportroot-authorization)。</span><span class="sxs-lookup"><span data-stu-id="49840-119">For more details, see [Authorization for APIs to read Microsoft 365 usage reports](/graph/reportroot-authorization).</span></span>

## <a name="http-request"></a><span data-ttu-id="49840-120">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="49840-120">HTTP request</span></span>


<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getEmailActivityCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="49840-121">函数参数</span><span class="sxs-lookup"><span data-stu-id="49840-121">Function parameters</span></span>

<span data-ttu-id="49840-122">在请求 URL 中，提供以下参数的有效值。</span><span class="sxs-lookup"><span data-stu-id="49840-122">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="49840-123">参数</span><span class="sxs-lookup"><span data-stu-id="49840-123">Parameter</span></span> | <span data-ttu-id="49840-124">类型</span><span class="sxs-lookup"><span data-stu-id="49840-124">Type</span></span>   | <span data-ttu-id="49840-125">说明</span><span class="sxs-lookup"><span data-stu-id="49840-125">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="49840-126">period</span><span class="sxs-lookup"><span data-stu-id="49840-126">period</span></span>    | <span data-ttu-id="49840-127">string</span><span class="sxs-lookup"><span data-stu-id="49840-127">string</span></span> | <span data-ttu-id="49840-128">指定在多长时间内聚合报表。</span><span class="sxs-lookup"><span data-stu-id="49840-128">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="49840-129">受支持的 {period_value} 值为：D7、D30、D90 和 D180。</span><span class="sxs-lookup"><span data-stu-id="49840-129">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="49840-130">这些值采用格式 D *n*，其中 *n* 表示在多少天内聚合报表。</span><span class="sxs-lookup"><span data-stu-id="49840-130">These values follow the format D *n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="49840-131">必需。</span><span class="sxs-lookup"><span data-stu-id="49840-131">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="49840-132">请求标头</span><span class="sxs-lookup"><span data-stu-id="49840-132">Request headers</span></span>

| <span data-ttu-id="49840-133">名称</span><span class="sxs-lookup"><span data-stu-id="49840-133">Name</span></span>          | <span data-ttu-id="49840-134">说明</span><span class="sxs-lookup"><span data-stu-id="49840-134">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="49840-135">Authorization</span><span class="sxs-lookup"><span data-stu-id="49840-135">Authorization</span></span> | <span data-ttu-id="49840-p104">持有者{令牌}。必需。</span><span class="sxs-lookup"><span data-stu-id="49840-p104">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="49840-138">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="49840-138">If-None-Match</span></span> | <span data-ttu-id="49840-139">如果包含此请求头，且提供的 eTag 与文件中的当前标记一致，返回的是 `304 Not Modified` 响应代码。</span><span class="sxs-lookup"><span data-stu-id="49840-139">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="49840-140">可选。</span><span class="sxs-lookup"><span data-stu-id="49840-140">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="49840-141">响应</span><span class="sxs-lookup"><span data-stu-id="49840-141">Response</span></span>

<span data-ttu-id="49840-142">如果成功，此方法返回 `302 Found` 响应，以重定向到报表的预先验证的下载 URL。</span><span class="sxs-lookup"><span data-stu-id="49840-142">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="49840-143">可以在响应的 `Location` 头中找到此 URL。</span><span class="sxs-lookup"><span data-stu-id="49840-143">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="49840-144">预先验证的下载 URL 的有效时间很短（几分钟），不需要 `Authorization` 头。</span><span class="sxs-lookup"><span data-stu-id="49840-144">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="49840-145">CSV 文件包含下面的列标题。</span><span class="sxs-lookup"><span data-stu-id="49840-145">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="49840-146">报表刷新日期</span><span class="sxs-lookup"><span data-stu-id="49840-146">Report Refresh Date</span></span>
- <span data-ttu-id="49840-147">已发送</span><span class="sxs-lookup"><span data-stu-id="49840-147">Send</span></span>
- <span data-ttu-id="49840-148">已接收</span><span class="sxs-lookup"><span data-stu-id="49840-148">Receive</span></span>
- <span data-ttu-id="49840-149">已阅读</span><span class="sxs-lookup"><span data-stu-id="49840-149">Read</span></span>
- <span data-ttu-id="49840-150">报表日期</span><span class="sxs-lookup"><span data-stu-id="49840-150">Report Date</span></span>
- <span data-ttu-id="49840-151">报表周期</span><span class="sxs-lookup"><span data-stu-id="49840-151">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="49840-152">示例</span><span class="sxs-lookup"><span data-stu-id="49840-152">Example</span></span>

#### <a name="request"></a><span data-ttu-id="49840-153">请求</span><span class="sxs-lookup"><span data-stu-id="49840-153">Request</span></span>

<span data-ttu-id="49840-154">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="49840-154">The following is an example of the request.</span></span>


<!--{
  "blockType": "ignored",
  "isComposable": true,
  "name": "reportroot_getemailactivitycounts"
}-->

```msgraph-interactive
GET https://graph.microsoft.com/v1.0/reports/getEmailActivityCounts(period='D7')
```


#### <a name="response"></a><span data-ttu-id="49840-155">响应</span><span class="sxs-lookup"><span data-stu-id="49840-155">Response</span></span>

<span data-ttu-id="49840-156">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="49840-156">The following is an example of the response.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.report" } --> 

```http
HTTP/1.1 302 Found
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="49840-157">执行 302 重定向，下载的 CSV 文件将采用以下架构。</span><span class="sxs-lookup"><span data-stu-id="49840-157">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "ignored"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Send,Receive,Read,Report Date,Report Period
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

