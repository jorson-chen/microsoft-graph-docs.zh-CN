---
title: 'reportRoot: getOneDriveUsageStorage'
description: 获取 OneDrive for Business 使用的存储空间趋势。
localization_priority: Normal
ms.prod: reports
author: sarahwxy
doc_type: apiPageType
ms.openlocfilehash: 6508024d0f8dd9e9e56874c0c760acf8fe1b9fe4
ms.sourcegitcommit: 479b366f3265b666fdc024b0f90b8d29764bb4b2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/26/2021
ms.locfileid: "49982682"
---
# <a name="reportroot-getonedriveusagestorage"></a><span data-ttu-id="c9e05-103">reportRoot: getOneDriveUsageStorage</span><span class="sxs-lookup"><span data-stu-id="c9e05-103">reportRoot: getOneDriveUsageStorage</span></span>

<span data-ttu-id="c9e05-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="c9e05-104">Namespace: microsoft.graph</span></span>

<span data-ttu-id="c9e05-105">获取 OneDrive for Business 使用的存储空间趋势。</span><span class="sxs-lookup"><span data-stu-id="c9e05-105">Get the trend on the amount of storage you are using in OneDrive for Business.</span></span>

> <span data-ttu-id="c9e05-106">**注意：** 有关不同报表视图和名称的详细信息，请参阅 [Microsoft 365 报表 - OneDrive for Business 使用情况](https://support.office.com/client/OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680)。</span><span class="sxs-lookup"><span data-stu-id="c9e05-106">**Note:** For details about different report views and names, see [Microsoft 365 reports - OneDrive for Business usage](https://support.office.com/client/OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680).</span></span>

## <a name="permissions"></a><span data-ttu-id="c9e05-107">Permissions</span><span class="sxs-lookup"><span data-stu-id="c9e05-107">Permissions</span></span>

<span data-ttu-id="c9e05-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="c9e05-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="c9e05-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="c9e05-110">Permission type</span></span>                        | <span data-ttu-id="c9e05-111">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="c9e05-111">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="c9e05-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="c9e05-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="c9e05-113">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="c9e05-113">Reports.Read.All</span></span>                         |
| <span data-ttu-id="c9e05-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="c9e05-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c9e05-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="c9e05-115">Not supported.</span></span>                           |
| <span data-ttu-id="c9e05-116">应用</span><span class="sxs-lookup"><span data-stu-id="c9e05-116">Application</span></span>                            | <span data-ttu-id="c9e05-117">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="c9e05-117">Reports.Read.All</span></span>                         |

<span data-ttu-id="c9e05-118">**注意**：若要获得委派权限以允许应用代表用户读取服务使用情况报告，租户管理员必须事先为用户分配适当的 Azure AD 受限管理员角色。</span><span class="sxs-lookup"><span data-stu-id="c9e05-118">**Note**: For delegated permissions to allow apps to read service usage reports on behalf of a user, the tenant administrator must have assigned the user the appropriate Azure AD limited administrator role.</span></span> <span data-ttu-id="c9e05-119">有关更多详细信息，请参阅[授权 API 读取 Microsoft 365 使用情况报告](/graph/reportroot-authorization)。</span><span class="sxs-lookup"><span data-stu-id="c9e05-119">For more details, see [Authorization for APIs to read Microsoft 365 usage reports](/graph/reportroot-authorization).</span></span>

## <a name="http-request"></a><span data-ttu-id="c9e05-120">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="c9e05-120">HTTP request</span></span>


<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOneDriveUsageStorage(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="c9e05-121">函数参数</span><span class="sxs-lookup"><span data-stu-id="c9e05-121">Function parameters</span></span>

<span data-ttu-id="c9e05-122">在请求 URL 中，提供以下参数的有效值。</span><span class="sxs-lookup"><span data-stu-id="c9e05-122">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="c9e05-123">参数</span><span class="sxs-lookup"><span data-stu-id="c9e05-123">Parameter</span></span> | <span data-ttu-id="c9e05-124">类型</span><span class="sxs-lookup"><span data-stu-id="c9e05-124">Type</span></span>   | <span data-ttu-id="c9e05-125">说明</span><span class="sxs-lookup"><span data-stu-id="c9e05-125">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="c9e05-126">period</span><span class="sxs-lookup"><span data-stu-id="c9e05-126">period</span></span>    | <span data-ttu-id="c9e05-127">string</span><span class="sxs-lookup"><span data-stu-id="c9e05-127">string</span></span> | <span data-ttu-id="c9e05-128">指定在多长时间内聚合报表。</span><span class="sxs-lookup"><span data-stu-id="c9e05-128">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="c9e05-129">受支持的 {period_value} 值为：D7、D30、D90 和 D180。</span><span class="sxs-lookup"><span data-stu-id="c9e05-129">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="c9e05-130">这些值采用格式 D *n*，其中 *n* 表示在多少天内聚合报表。</span><span class="sxs-lookup"><span data-stu-id="c9e05-130">These values follow the format D *n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="c9e05-131">必需。</span><span class="sxs-lookup"><span data-stu-id="c9e05-131">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="c9e05-132">请求标头</span><span class="sxs-lookup"><span data-stu-id="c9e05-132">Request headers</span></span>

| <span data-ttu-id="c9e05-133">名称</span><span class="sxs-lookup"><span data-stu-id="c9e05-133">Name</span></span>          | <span data-ttu-id="c9e05-134">说明</span><span class="sxs-lookup"><span data-stu-id="c9e05-134">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="c9e05-135">Authorization</span><span class="sxs-lookup"><span data-stu-id="c9e05-135">Authorization</span></span> | <span data-ttu-id="c9e05-p104">持有者{令牌}。必需。</span><span class="sxs-lookup"><span data-stu-id="c9e05-p104">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="c9e05-138">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="c9e05-138">If-None-Match</span></span> | <span data-ttu-id="c9e05-139">如果包含此请求头，且提供的 eTag 与文件中的当前标记一致，返回的是 `304 Not Modified` 响应代码。</span><span class="sxs-lookup"><span data-stu-id="c9e05-139">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="c9e05-140">可选。</span><span class="sxs-lookup"><span data-stu-id="c9e05-140">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="c9e05-141">响应</span><span class="sxs-lookup"><span data-stu-id="c9e05-141">Response</span></span>

<span data-ttu-id="c9e05-142">如果成功，此方法返回 `302 Found` 响应，以重定向到报表的预先验证的下载 URL。</span><span class="sxs-lookup"><span data-stu-id="c9e05-142">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="c9e05-143">可以在响应的 `Location` 头中找到此 URL。</span><span class="sxs-lookup"><span data-stu-id="c9e05-143">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="c9e05-144">预先验证的下载 URL 的有效时间很短（几分钟），不需要 `Authorization` 头。</span><span class="sxs-lookup"><span data-stu-id="c9e05-144">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="c9e05-145">CSV 文件包含下面的列标题。</span><span class="sxs-lookup"><span data-stu-id="c9e05-145">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="c9e05-146">报表刷新日期</span><span class="sxs-lookup"><span data-stu-id="c9e05-146">Report Refresh Date</span></span>
- <span data-ttu-id="c9e05-147">网站类型</span><span class="sxs-lookup"><span data-stu-id="c9e05-147">Site Type</span></span>
- <span data-ttu-id="c9e05-148">已使用的存储（字节）</span><span class="sxs-lookup"><span data-stu-id="c9e05-148">Storage Used (Byte)</span></span>
- <span data-ttu-id="c9e05-149">报表日期</span><span class="sxs-lookup"><span data-stu-id="c9e05-149">Report Date</span></span>
- <span data-ttu-id="c9e05-150">报表周期</span><span class="sxs-lookup"><span data-stu-id="c9e05-150">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="c9e05-151">示例</span><span class="sxs-lookup"><span data-stu-id="c9e05-151">Example</span></span>

#### <a name="request"></a><span data-ttu-id="c9e05-152">请求</span><span class="sxs-lookup"><span data-stu-id="c9e05-152">Request</span></span>

<span data-ttu-id="c9e05-153">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="c9e05-153">The following is an example of the request.</span></span>


<!--{
  "blockType": "ignored",
  "isComposable": true,
  "name": "reportroot_getonedriveusagestorage"
}-->

```msgraph-interactive
GET https://graph.microsoft.com/v1.0/reports/getOneDriveUsageStorage(period='D7')
```


#### <a name="response"></a><span data-ttu-id="c9e05-154">响应</span><span class="sxs-lookup"><span data-stu-id="c9e05-154">Response</span></span>

<span data-ttu-id="c9e05-155">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="c9e05-155">The following is an example of the response.</span></span>

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

<span data-ttu-id="c9e05-156">执行 302 重定向，下载的 CSV 文件将采用以下架构。</span><span class="sxs-lookup"><span data-stu-id="c9e05-156">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Site Type,Storage Used (Byte),Report Date,Report Period
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

