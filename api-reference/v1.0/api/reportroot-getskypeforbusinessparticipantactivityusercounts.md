---
title: 'reportRoot: getSkypeForBusinessParticipantActivityUserCounts'
description: 获取使用情况趋势，即组织中用户参与的会议会话的唯一用户数和类型。 会议会话类型包括 IM、音频/视频、应用共享、Web 和第三方拨入/拨出。
localization_priority: Normal
ms.prod: reports
author: sarahwxy
doc_type: apiPageType
ms.openlocfilehash: 43d38c61f97a74dfb4091b0f45e1f40b7d7550e8
ms.sourcegitcommit: 479b366f3265b666fdc024b0f90b8d29764bb4b2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/26/2021
ms.locfileid: "49983452"
---
# <a name="reportroot-getskypeforbusinessparticipantactivityusercounts"></a><span data-ttu-id="f9267-104">reportRoot: getSkypeForBusinessParticipantActivityUserCounts</span><span class="sxs-lookup"><span data-stu-id="f9267-104">reportRoot: getSkypeForBusinessParticipantActivityUserCounts</span></span>

<span data-ttu-id="f9267-105">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="f9267-105">Namespace: microsoft.graph</span></span>

<span data-ttu-id="f9267-106">获取使用情况趋势，即组织中用户参与的会议会话的唯一用户数和类型。</span><span class="sxs-lookup"><span data-stu-id="f9267-106">Get usage trends on the number of unique users and type of conference sessions that users from your organization participated in.</span></span> <span data-ttu-id="f9267-107">会议会话类型包括 IM、音频/视频、应用共享、Web 和第三方拨入/拨出。</span><span class="sxs-lookup"><span data-stu-id="f9267-107">Types of conference sessions include IM, audio/video, application sharing, web, and dial-in/out - 3rd party.</span></span>

> <span data-ttu-id="f9267-108">**注意：** 有关不同报告视图和名称的详细信息，请参阅 [Microsoft 365 报告 - Skype for Business 会议参与者活动](https://support.office.com/client/Skype-for-Business-Online-conference-participant-activity-c3c89995-65dd-4715-9e38-bb244c742c6b)。</span><span class="sxs-lookup"><span data-stu-id="f9267-108">**Note:** For details about different report views and names, see [Microsoft 365 reports - Skype for Business conference participant activity](https://support.office.com/client/Skype-for-Business-Online-conference-participant-activity-c3c89995-65dd-4715-9e38-bb244c742c6b).</span></span>

## <a name="permissions"></a><span data-ttu-id="f9267-109">Permissions</span><span class="sxs-lookup"><span data-stu-id="f9267-109">Permissions</span></span>

<span data-ttu-id="f9267-p103">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="f9267-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="f9267-112">权限类型</span><span class="sxs-lookup"><span data-stu-id="f9267-112">Permission type</span></span>                        | <span data-ttu-id="f9267-113">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="f9267-113">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="f9267-114">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="f9267-114">Delegated (work or school account)</span></span>     | <span data-ttu-id="f9267-115">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="f9267-115">Reports.Read.All</span></span>                         |
| <span data-ttu-id="f9267-116">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="f9267-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f9267-117">不支持。</span><span class="sxs-lookup"><span data-stu-id="f9267-117">Not supported.</span></span>                           |
| <span data-ttu-id="f9267-118">应用</span><span class="sxs-lookup"><span data-stu-id="f9267-118">Application</span></span>                            | <span data-ttu-id="f9267-119">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="f9267-119">Reports.Read.All</span></span>                         |

<span data-ttu-id="f9267-120">**注意**：若要获得委派权限以允许应用代表用户读取服务使用情况报告，租户管理员必须事先为用户分配适当的 Azure AD 受限管理员角色。</span><span class="sxs-lookup"><span data-stu-id="f9267-120">**Note**: For delegated permissions to allow apps to read service usage reports on behalf of a user, the tenant administrator must have assigned the user the appropriate Azure AD limited administrator role.</span></span> <span data-ttu-id="f9267-121">有关更多详细信息，请参阅[授权 API 读取 Microsoft 365 使用情况报告](/graph/reportroot-authorization)。</span><span class="sxs-lookup"><span data-stu-id="f9267-121">For more details, see [Authorization for APIs to read Microsoft 365 usage reports](/graph/reportroot-authorization).</span></span>

## <a name="http-request"></a><span data-ttu-id="f9267-122">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="f9267-122">HTTP request</span></span>


<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSkypeForBusinessParticipantActivityUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="f9267-123">函数参数</span><span class="sxs-lookup"><span data-stu-id="f9267-123">Function parameters</span></span>

<span data-ttu-id="f9267-124">在请求 URL 中，提供以下参数的有效值。</span><span class="sxs-lookup"><span data-stu-id="f9267-124">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="f9267-125">参数</span><span class="sxs-lookup"><span data-stu-id="f9267-125">Parameter</span></span> | <span data-ttu-id="f9267-126">类型</span><span class="sxs-lookup"><span data-stu-id="f9267-126">Type</span></span>   | <span data-ttu-id="f9267-127">说明</span><span class="sxs-lookup"><span data-stu-id="f9267-127">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="f9267-128">period</span><span class="sxs-lookup"><span data-stu-id="f9267-128">period</span></span>    | <span data-ttu-id="f9267-129">string</span><span class="sxs-lookup"><span data-stu-id="f9267-129">string</span></span> | <span data-ttu-id="f9267-130">指定在多长时间内聚合报表。</span><span class="sxs-lookup"><span data-stu-id="f9267-130">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="f9267-131">受支持的 {period_value} 值为：D7、D30、D90 和 D180。</span><span class="sxs-lookup"><span data-stu-id="f9267-131">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="f9267-132">这些值采用格式 D *n*，其中 *n* 表示在多少天内聚合报表。</span><span class="sxs-lookup"><span data-stu-id="f9267-132">These values follow the format D *n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="f9267-133">必需。</span><span class="sxs-lookup"><span data-stu-id="f9267-133">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="f9267-134">请求标头</span><span class="sxs-lookup"><span data-stu-id="f9267-134">Request headers</span></span>

| <span data-ttu-id="f9267-135">名称</span><span class="sxs-lookup"><span data-stu-id="f9267-135">Name</span></span>          | <span data-ttu-id="f9267-136">说明</span><span class="sxs-lookup"><span data-stu-id="f9267-136">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="f9267-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="f9267-137">Authorization</span></span> | <span data-ttu-id="f9267-p106">持有者{令牌}。必需。</span><span class="sxs-lookup"><span data-stu-id="f9267-p106">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="f9267-140">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="f9267-140">If-None-Match</span></span> | <span data-ttu-id="f9267-141">如果包含此请求头，且提供的 eTag 与文件中的当前标记一致，返回的是 `304 Not Modified` 响应代码。</span><span class="sxs-lookup"><span data-stu-id="f9267-141">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="f9267-142">可选。</span><span class="sxs-lookup"><span data-stu-id="f9267-142">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="f9267-143">响应</span><span class="sxs-lookup"><span data-stu-id="f9267-143">Response</span></span>

<span data-ttu-id="f9267-144">如果成功，此方法返回 `302 Found` 响应，以重定向到报表的预先验证的下载 URL。</span><span class="sxs-lookup"><span data-stu-id="f9267-144">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="f9267-145">可以在响应的 `Location` 头中找到此 URL。</span><span class="sxs-lookup"><span data-stu-id="f9267-145">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="f9267-146">预先验证的下载 URL 的有效时间很短（几分钟），不需要 `Authorization` 头。</span><span class="sxs-lookup"><span data-stu-id="f9267-146">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="f9267-147">CSV 文件包含下面的列标题。</span><span class="sxs-lookup"><span data-stu-id="f9267-147">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="f9267-148">报表刷新日期</span><span class="sxs-lookup"><span data-stu-id="f9267-148">Report Refresh Date</span></span>
- <span data-ttu-id="f9267-149">报表日期</span><span class="sxs-lookup"><span data-stu-id="f9267-149">Report Date</span></span>
- <span data-ttu-id="f9267-150">报表周期</span><span class="sxs-lookup"><span data-stu-id="f9267-150">Report Period</span></span>
- <span data-ttu-id="f9267-151">IM</span><span class="sxs-lookup"><span data-stu-id="f9267-151">IM</span></span>
- <span data-ttu-id="f9267-152">音频/视频</span><span class="sxs-lookup"><span data-stu-id="f9267-152">Audio/Video</span></span>
- <span data-ttu-id="f9267-153">应用共享</span><span class="sxs-lookup"><span data-stu-id="f9267-153">App Sharing</span></span>
- <span data-ttu-id="f9267-154">Web</span><span class="sxs-lookup"><span data-stu-id="f9267-154">Web</span></span>
- <span data-ttu-id="f9267-155">第三方拨入/拨出</span><span class="sxs-lookup"><span data-stu-id="f9267-155">Dial-in/out 3rd Party</span></span>

## <a name="example"></a><span data-ttu-id="f9267-156">示例</span><span class="sxs-lookup"><span data-stu-id="f9267-156">Example</span></span>

#### <a name="request"></a><span data-ttu-id="f9267-157">请求</span><span class="sxs-lookup"><span data-stu-id="f9267-157">Request</span></span>

<span data-ttu-id="f9267-158">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="f9267-158">The following is an example of the request.</span></span>


<!--{
  "blockType": "ignored",
  "isComposable": true,
  "name": "reportroot_getskypeforbusinessparticipantactivityusercounts"
}-->

```msgraph-interactive
GET https://graph.microsoft.com/v1.0/reports/getSkypeForBusinessParticipantActivityUserCounts(period='D7')
```


#### <a name="response"></a><span data-ttu-id="f9267-159">响应</span><span class="sxs-lookup"><span data-stu-id="f9267-159">Response</span></span>

<span data-ttu-id="f9267-160">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="f9267-160">The following is an example of the response.</span></span>

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

<span data-ttu-id="f9267-161">执行 302 重定向，下载的 CSV 文件将采用以下架构。</span><span class="sxs-lookup"><span data-stu-id="f9267-161">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Report Date,Report Period,IM,Audio/Video,App Sharing,Web,Dial-in/out 3rd Party
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

