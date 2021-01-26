---
title: 'reportRoot: getYammerDeviceUsageUserCounts'
description: 按设备类型获取每日用户数。
localization_priority: Normal
ms.prod: reports
author: sarahwxy
doc_type: apiPageType
ms.openlocfilehash: ec139af8abeff34d9a44bf37612455abbb1441bf
ms.sourcegitcommit: 479b366f3265b666fdc024b0f90b8d29764bb4b2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/26/2021
ms.locfileid: "49983347"
---
# <a name="reportroot-getyammerdeviceusageusercounts"></a><span data-ttu-id="22c9f-103">reportRoot: getYammerDeviceUsageUserCounts</span><span class="sxs-lookup"><span data-stu-id="22c9f-103">reportRoot: getYammerDeviceUsageUserCounts</span></span>

<span data-ttu-id="22c9f-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="22c9f-104">Namespace: microsoft.graph</span></span>

<span data-ttu-id="22c9f-105">按设备类型获取每日用户数。</span><span class="sxs-lookup"><span data-stu-id="22c9f-105">Get the number of daily users by device type.</span></span>

> <span data-ttu-id="22c9f-106">**注意：** 有关不同报表视图和名称的详细信息，请参阅 [Microsoft 365 报表 - Yammer 设备使用情况](https://support.office.com/client/Yammer-device-usage-b793ffdd-effa-43d0-849a-b1ca2e899f38)。</span><span class="sxs-lookup"><span data-stu-id="22c9f-106">**Note:** For details about different report views and names, see [Microsoft 365 reports - Yammer device usage](https://support.office.com/client/Yammer-device-usage-b793ffdd-effa-43d0-849a-b1ca2e899f38).</span></span>

## <a name="permissions"></a><span data-ttu-id="22c9f-107">Permissions</span><span class="sxs-lookup"><span data-stu-id="22c9f-107">Permissions</span></span>

<span data-ttu-id="22c9f-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="22c9f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="22c9f-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="22c9f-110">Permission type</span></span>                        | <span data-ttu-id="22c9f-111">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="22c9f-111">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="22c9f-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="22c9f-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="22c9f-113">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="22c9f-113">Reports.Read.All</span></span>                         |
| <span data-ttu-id="22c9f-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="22c9f-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="22c9f-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="22c9f-115">Not supported.</span></span>                           |
| <span data-ttu-id="22c9f-116">应用</span><span class="sxs-lookup"><span data-stu-id="22c9f-116">Application</span></span>                            | <span data-ttu-id="22c9f-117">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="22c9f-117">Reports.Read.All</span></span>                         |

<span data-ttu-id="22c9f-118">**注意**：若要获得委派权限以允许应用代表用户读取服务使用情况报告，租户管理员必须事先为用户分配适当的 Azure AD 受限管理员角色。</span><span class="sxs-lookup"><span data-stu-id="22c9f-118">**Note**: For delegated permissions to allow apps to read service usage reports on behalf of a user, the tenant administrator must have assigned the user the appropriate Azure AD limited administrator role.</span></span> <span data-ttu-id="22c9f-119">有关更多详细信息，请参阅[授权 API 读取 Microsoft 365 使用情况报告](/graph/reportroot-authorization)。</span><span class="sxs-lookup"><span data-stu-id="22c9f-119">For more details, see [Authorization for APIs to read Microsoft 365 usage reports](/graph/reportroot-authorization).</span></span>

## <a name="http-request"></a><span data-ttu-id="22c9f-120">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="22c9f-120">HTTP request</span></span>


<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getYammerDeviceUsageUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="22c9f-121">函数参数</span><span class="sxs-lookup"><span data-stu-id="22c9f-121">Function parameters</span></span>

<span data-ttu-id="22c9f-122">在请求 URL 中，提供以下参数的有效值。</span><span class="sxs-lookup"><span data-stu-id="22c9f-122">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="22c9f-123">参数</span><span class="sxs-lookup"><span data-stu-id="22c9f-123">Parameter</span></span> | <span data-ttu-id="22c9f-124">类型</span><span class="sxs-lookup"><span data-stu-id="22c9f-124">Type</span></span>   | <span data-ttu-id="22c9f-125">说明</span><span class="sxs-lookup"><span data-stu-id="22c9f-125">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="22c9f-126">period</span><span class="sxs-lookup"><span data-stu-id="22c9f-126">period</span></span>    | <span data-ttu-id="22c9f-127">string</span><span class="sxs-lookup"><span data-stu-id="22c9f-127">string</span></span> | <span data-ttu-id="22c9f-128">指定在多长时间内聚合报表。</span><span class="sxs-lookup"><span data-stu-id="22c9f-128">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="22c9f-129">受支持的 {period_value} 值为：D7、D30、D90 和 D180。</span><span class="sxs-lookup"><span data-stu-id="22c9f-129">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="22c9f-130">这些值采用格式 D *n*，其中 *n* 表示在多少天内聚合报表。</span><span class="sxs-lookup"><span data-stu-id="22c9f-130">These values follow the format D *n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="22c9f-131">必需。</span><span class="sxs-lookup"><span data-stu-id="22c9f-131">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="22c9f-132">请求标头</span><span class="sxs-lookup"><span data-stu-id="22c9f-132">Request headers</span></span>

| <span data-ttu-id="22c9f-133">名称</span><span class="sxs-lookup"><span data-stu-id="22c9f-133">Name</span></span>          | <span data-ttu-id="22c9f-134">说明</span><span class="sxs-lookup"><span data-stu-id="22c9f-134">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="22c9f-135">Authorization</span><span class="sxs-lookup"><span data-stu-id="22c9f-135">Authorization</span></span> | <span data-ttu-id="22c9f-p104">持有者{令牌}。必需。</span><span class="sxs-lookup"><span data-stu-id="22c9f-p104">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="22c9f-138">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="22c9f-138">If-None-Match</span></span> | <span data-ttu-id="22c9f-139">如果包含此请求头，且提供的 eTag 与文件中的当前标记一致，返回的是 `304 Not Modified` 响应代码。</span><span class="sxs-lookup"><span data-stu-id="22c9f-139">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="22c9f-140">可选。</span><span class="sxs-lookup"><span data-stu-id="22c9f-140">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="22c9f-141">响应</span><span class="sxs-lookup"><span data-stu-id="22c9f-141">Response</span></span>

<span data-ttu-id="22c9f-142">如果成功，此方法返回 `302 Found` 响应，以重定向到报表的预先验证的下载 URL。</span><span class="sxs-lookup"><span data-stu-id="22c9f-142">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="22c9f-143">可以在响应的 `Location` 头中找到此 URL。</span><span class="sxs-lookup"><span data-stu-id="22c9f-143">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="22c9f-144">预先验证的下载 URL 的有效时间很短（几分钟），不需要 `Authorization` 头。</span><span class="sxs-lookup"><span data-stu-id="22c9f-144">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="22c9f-145">CSV 文件包含下面的列标题。</span><span class="sxs-lookup"><span data-stu-id="22c9f-145">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="22c9f-146">报表刷新日期</span><span class="sxs-lookup"><span data-stu-id="22c9f-146">Report Refresh Date</span></span>
- <span data-ttu-id="22c9f-147">Web</span><span class="sxs-lookup"><span data-stu-id="22c9f-147">Web</span></span>
- <span data-ttu-id="22c9f-148">Windows 手机</span><span class="sxs-lookup"><span data-stu-id="22c9f-148">Windows Phone</span></span>
- <span data-ttu-id="22c9f-149">Android 手机</span><span class="sxs-lookup"><span data-stu-id="22c9f-149">Android Phone</span></span>
- <span data-ttu-id="22c9f-150">iPhone</span><span class="sxs-lookup"><span data-stu-id="22c9f-150">iPhone</span></span>
- <span data-ttu-id="22c9f-151">iPad</span><span class="sxs-lookup"><span data-stu-id="22c9f-151">iPad</span></span>
- <span data-ttu-id="22c9f-152">其他</span><span class="sxs-lookup"><span data-stu-id="22c9f-152">Other</span></span>
- <span data-ttu-id="22c9f-153">报表日期</span><span class="sxs-lookup"><span data-stu-id="22c9f-153">Report Date</span></span>
- <span data-ttu-id="22c9f-154">报表周期</span><span class="sxs-lookup"><span data-stu-id="22c9f-154">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="22c9f-155">示例</span><span class="sxs-lookup"><span data-stu-id="22c9f-155">Example</span></span>

#### <a name="request"></a><span data-ttu-id="22c9f-156">请求</span><span class="sxs-lookup"><span data-stu-id="22c9f-156">Request</span></span>

<span data-ttu-id="22c9f-157">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="22c9f-157">The following is an example of the request.</span></span>


<!--{
  "blockType": "ignored",
  "isComposable": true,
  "name": "reportroot_getyammerdeviceusageusercounts"
}-->

```msgraph-interactive
GET https://graph.microsoft.com/v1.0/reports/getYammerDeviceUsageUserCounts(period='D7')
```


#### <a name="response"></a><span data-ttu-id="22c9f-158">响应</span><span class="sxs-lookup"><span data-stu-id="22c9f-158">Response</span></span>

<span data-ttu-id="22c9f-159">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="22c9f-159">The following is an example of the response.</span></span>

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

<span data-ttu-id="22c9f-160">执行 302 重定向，下载的 CSV 文件将采用以下架构。</span><span class="sxs-lookup"><span data-stu-id="22c9f-160">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Web,Windows Phone,Android Phone,iPhone,iPad,Other,Report Date,Report Period
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

