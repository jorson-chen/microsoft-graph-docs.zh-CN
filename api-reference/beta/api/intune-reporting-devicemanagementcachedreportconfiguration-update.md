---
title: 更新 deviceManagementCachedReportConfiguration
description: 更新 deviceManagementCachedReportConfiguration 对象的属性。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 2308fc686358f28c3ffb3c7aff523207a7e46d8b
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2019
ms.locfileid: "37537287"
---
# <a name="update-devicemanagementcachedreportconfiguration"></a><span data-ttu-id="3c604-103">更新 deviceManagementCachedReportConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c604-103">Update deviceManagementCachedReportConfiguration</span></span>

> <span data-ttu-id="3c604-104">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="3c604-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="3c604-105">**注意：** 适用于 Intune 的 Microsoft Graph API 需要租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="3c604-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="3c604-106">更新[deviceManagementCachedReportConfiguration](../resources/intune-reporting-devicemanagementcachedreportconfiguration.md)对象的属性。</span><span class="sxs-lookup"><span data-stu-id="3c604-106">Update the properties of a [deviceManagementCachedReportConfiguration](../resources/intune-reporting-devicemanagementcachedreportconfiguration.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3c604-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="3c604-107">Prerequisites</span></span>
<span data-ttu-id="3c604-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="3c604-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3c604-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="3c604-110">Permission type</span></span>|<span data-ttu-id="3c604-111">权限（从最高特权到最低特权）</span><span class="sxs-lookup"><span data-stu-id="3c604-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3c604-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="3c604-112">Delegated (work or school account)</span></span>|<span data-ttu-id="3c604-113">Devicemanagementconfiguration.readwrite.all，Devicemanagementapps.readwrite.all，all，Devicemanagementmanageddevices.readwrite.all，All</span><span class="sxs-lookup"><span data-stu-id="3c604-113">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementApps.ReadWrite.All, DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="3c604-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="3c604-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3c604-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="3c604-115">Not supported.</span></span>|
|<span data-ttu-id="3c604-116">应用程序</span><span class="sxs-lookup"><span data-stu-id="3c604-116">Application</span></span>|<span data-ttu-id="3c604-117">Devicemanagementconfiguration.readwrite.all，Devicemanagementapps.readwrite.all，all，Devicemanagementmanageddevices.readwrite.all，All</span><span class="sxs-lookup"><span data-stu-id="3c604-117">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementApps.ReadWrite.All, DeviceManagementManagedDevices.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="3c604-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="3c604-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/reports/cachedReportConfigurations/{deviceManagementCachedReportConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="3c604-119">请求标头</span><span class="sxs-lookup"><span data-stu-id="3c604-119">Request headers</span></span>
|<span data-ttu-id="3c604-120">标头</span><span class="sxs-lookup"><span data-stu-id="3c604-120">Header</span></span>|<span data-ttu-id="3c604-121">值</span><span class="sxs-lookup"><span data-stu-id="3c604-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3c604-122">授权</span><span class="sxs-lookup"><span data-stu-id="3c604-122">Authorization</span></span>|<span data-ttu-id="3c604-123">Bearer &lt;token&gt;。必需。</span><span class="sxs-lookup"><span data-stu-id="3c604-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3c604-124">接受</span><span class="sxs-lookup"><span data-stu-id="3c604-124">Accept</span></span>|<span data-ttu-id="3c604-125">application/json</span><span class="sxs-lookup"><span data-stu-id="3c604-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3c604-126">请求正文</span><span class="sxs-lookup"><span data-stu-id="3c604-126">Request body</span></span>
<span data-ttu-id="3c604-127">在请求正文中，提供[deviceManagementCachedReportConfiguration](../resources/intune-reporting-devicemanagementcachedreportconfiguration.md)对象的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="3c604-127">In the request body, supply a JSON representation for the [deviceManagementCachedReportConfiguration](../resources/intune-reporting-devicemanagementcachedreportconfiguration.md) object.</span></span>

<span data-ttu-id="3c604-128">下表显示创建[deviceManagementCachedReportConfiguration](../resources/intune-reporting-devicemanagementcachedreportconfiguration.md)时所需的属性。</span><span class="sxs-lookup"><span data-stu-id="3c604-128">The following table shows the properties that are required when you create the [deviceManagementCachedReportConfiguration](../resources/intune-reporting-devicemanagementcachedreportconfiguration.md).</span></span>

|<span data-ttu-id="3c604-129">属性</span><span class="sxs-lookup"><span data-stu-id="3c604-129">Property</span></span>|<span data-ttu-id="3c604-130">类型</span><span class="sxs-lookup"><span data-stu-id="3c604-130">Type</span></span>|<span data-ttu-id="3c604-131">说明</span><span class="sxs-lookup"><span data-stu-id="3c604-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3c604-132">id</span><span class="sxs-lookup"><span data-stu-id="3c604-132">id</span></span>|<span data-ttu-id="3c604-133">字符串</span><span class="sxs-lookup"><span data-stu-id="3c604-133">String</span></span>|<span data-ttu-id="3c604-134">此实体的唯一标识符</span><span class="sxs-lookup"><span data-stu-id="3c604-134">Unique identifier for this entity</span></span>|
|<span data-ttu-id="3c604-135">reportName</span><span class="sxs-lookup"><span data-stu-id="3c604-135">reportName</span></span>|<span data-ttu-id="3c604-136">字符串</span><span class="sxs-lookup"><span data-stu-id="3c604-136">String</span></span>|<span data-ttu-id="3c604-137">报告的名称</span><span class="sxs-lookup"><span data-stu-id="3c604-137">Name of the report</span></span>|
|<span data-ttu-id="3c604-138">filter</span><span class="sxs-lookup"><span data-stu-id="3c604-138">filter</span></span>|<span data-ttu-id="3c604-139">字符串</span><span class="sxs-lookup"><span data-stu-id="3c604-139">String</span></span>|<span data-ttu-id="3c604-140">在创建报表时应用的筛选器。</span><span class="sxs-lookup"><span data-stu-id="3c604-140">Filters applied on report creation.</span></span>|
|<span data-ttu-id="3c604-141">select</span><span class="sxs-lookup"><span data-stu-id="3c604-141">select</span></span>|<span data-ttu-id="3c604-142">String 集合</span><span class="sxs-lookup"><span data-stu-id="3c604-142">String collection</span></span>|<span data-ttu-id="3c604-143">从报告中选择的列</span><span class="sxs-lookup"><span data-stu-id="3c604-143">Columns selected from the report</span></span>|
|<span data-ttu-id="3c604-144">By</span><span class="sxs-lookup"><span data-stu-id="3c604-144">orderBy</span></span>|<span data-ttu-id="3c604-145">String 集合</span><span class="sxs-lookup"><span data-stu-id="3c604-145">String collection</span></span>|<span data-ttu-id="3c604-146">报表中的列的排序</span><span class="sxs-lookup"><span data-stu-id="3c604-146">Ordering of columns in the report</span></span>|
|<span data-ttu-id="3c604-147">status</span><span class="sxs-lookup"><span data-stu-id="3c604-147">status</span></span>|[<span data-ttu-id="3c604-148">deviceManagementReportStatus</span><span class="sxs-lookup"><span data-stu-id="3c604-148">deviceManagementReportStatus</span></span>](../resources/intune-reporting-devicemanagementreportstatus.md)|<span data-ttu-id="3c604-149">缓存报告的状态。</span><span class="sxs-lookup"><span data-stu-id="3c604-149">Status of the cached report.</span></span> <span data-ttu-id="3c604-150">可取值为：`unknown`、`notStarted`、`inProgress`、`completed`、`failed`。</span><span class="sxs-lookup"><span data-stu-id="3c604-150">Possible values are: `unknown`, `notStarted`, `inProgress`, `completed`, `failed`.</span></span>|
|<span data-ttu-id="3c604-151">lastRefreshDateTime</span><span class="sxs-lookup"><span data-stu-id="3c604-151">lastRefreshDateTime</span></span>|<span data-ttu-id="3c604-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3c604-152">DateTimeOffset</span></span>|<span data-ttu-id="3c604-153">上次刷新缓存的报告的时间</span><span class="sxs-lookup"><span data-stu-id="3c604-153">Time that the cached report was last refreshed</span></span>|
|<span data-ttu-id="3c604-154">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="3c604-154">expirationDateTime</span></span>|<span data-ttu-id="3c604-155">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3c604-155">DateTimeOffset</span></span>|<span data-ttu-id="3c604-156">缓存的报表到期的时间</span><span class="sxs-lookup"><span data-stu-id="3c604-156">Time that the cached report expires</span></span>|



## <a name="response"></a><span data-ttu-id="3c604-157">响应</span><span class="sxs-lookup"><span data-stu-id="3c604-157">Response</span></span>
<span data-ttu-id="3c604-158">如果成功，此方法在响应`200 OK`正文中返回响应代码和更新的[deviceManagementCachedReportConfiguration](../resources/intune-reporting-devicemanagementcachedreportconfiguration.md)对象。</span><span class="sxs-lookup"><span data-stu-id="3c604-158">If successful, this method returns a `200 OK` response code and an updated [deviceManagementCachedReportConfiguration](../resources/intune-reporting-devicemanagementcachedreportconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3c604-159">示例</span><span class="sxs-lookup"><span data-stu-id="3c604-159">Example</span></span>

### <a name="request"></a><span data-ttu-id="3c604-160">请求</span><span class="sxs-lookup"><span data-stu-id="3c604-160">Request</span></span>
<span data-ttu-id="3c604-161">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="3c604-161">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/reports/cachedReportConfigurations/{deviceManagementCachedReportConfigurationId}
Content-type: application/json
Content-length: 385

{
  "@odata.type": "#microsoft.graph.deviceManagementCachedReportConfiguration",
  "reportName": "Report Name value",
  "filter": "Filter value",
  "select": [
    "Select value"
  ],
  "orderBy": [
    "Order By value"
  ],
  "status": "notStarted",
  "lastRefreshDateTime": "2016-12-31T23:58:49.97047-08:00",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00"
}
```

### <a name="response"></a><span data-ttu-id="3c604-162">响应</span><span class="sxs-lookup"><span data-stu-id="3c604-162">Response</span></span>
<span data-ttu-id="3c604-p103">下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="3c604-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 434

{
  "@odata.type": "#microsoft.graph.deviceManagementCachedReportConfiguration",
  "id": "46947722-7722-4694-2277-944622779446",
  "reportName": "Report Name value",
  "filter": "Filter value",
  "select": [
    "Select value"
  ],
  "orderBy": [
    "Order By value"
  ],
  "status": "notStarted",
  "lastRefreshDateTime": "2016-12-31T23:58:49.97047-08:00",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00"
}
```





