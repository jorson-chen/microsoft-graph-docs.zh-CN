---
title: 更新 deviceManagementReportSchedule
description: 更新 deviceManagementReportSchedule 对象的属性。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: f46c8881e1b936f224bd6a4f5c493f0fd69bb997
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2019
ms.locfileid: "37537168"
---
# <a name="update-devicemanagementreportschedule"></a><span data-ttu-id="2dd16-103">更新 deviceManagementReportSchedule</span><span class="sxs-lookup"><span data-stu-id="2dd16-103">Update deviceManagementReportSchedule</span></span>

> <span data-ttu-id="2dd16-104">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="2dd16-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="2dd16-105">**注意：** 适用于 Intune 的 Microsoft Graph API 需要租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="2dd16-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="2dd16-106">更新[deviceManagementReportSchedule](../resources/intune-reporting-devicemanagementreportschedule.md)对象的属性。</span><span class="sxs-lookup"><span data-stu-id="2dd16-106">Update the properties of a [deviceManagementReportSchedule](../resources/intune-reporting-devicemanagementreportschedule.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2dd16-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="2dd16-107">Prerequisites</span></span>
<span data-ttu-id="2dd16-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="2dd16-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2dd16-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="2dd16-110">Permission type</span></span>|<span data-ttu-id="2dd16-111">权限（从最高特权到最低特权）</span><span class="sxs-lookup"><span data-stu-id="2dd16-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2dd16-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="2dd16-112">Delegated (work or school account)</span></span>|<span data-ttu-id="2dd16-113">Devicemanagementconfiguration.readwrite.all，Devicemanagementapps.readwrite.all，all，Devicemanagementmanageddevices.readwrite.all，All</span><span class="sxs-lookup"><span data-stu-id="2dd16-113">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementApps.ReadWrite.All, DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="2dd16-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="2dd16-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2dd16-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="2dd16-115">Not supported.</span></span>|
|<span data-ttu-id="2dd16-116">应用程序</span><span class="sxs-lookup"><span data-stu-id="2dd16-116">Application</span></span>|<span data-ttu-id="2dd16-117">Devicemanagementconfiguration.readwrite.all，Devicemanagementapps.readwrite.all，all，Devicemanagementmanageddevices.readwrite.all，All</span><span class="sxs-lookup"><span data-stu-id="2dd16-117">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementApps.ReadWrite.All, DeviceManagementManagedDevices.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="2dd16-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="2dd16-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/reports/reportSchedules/{deviceManagementReportScheduleId}
```

## <a name="request-headers"></a><span data-ttu-id="2dd16-119">请求标头</span><span class="sxs-lookup"><span data-stu-id="2dd16-119">Request headers</span></span>
|<span data-ttu-id="2dd16-120">标头</span><span class="sxs-lookup"><span data-stu-id="2dd16-120">Header</span></span>|<span data-ttu-id="2dd16-121">值</span><span class="sxs-lookup"><span data-stu-id="2dd16-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2dd16-122">授权</span><span class="sxs-lookup"><span data-stu-id="2dd16-122">Authorization</span></span>|<span data-ttu-id="2dd16-123">Bearer &lt;token&gt;。必需。</span><span class="sxs-lookup"><span data-stu-id="2dd16-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2dd16-124">接受</span><span class="sxs-lookup"><span data-stu-id="2dd16-124">Accept</span></span>|<span data-ttu-id="2dd16-125">application/json</span><span class="sxs-lookup"><span data-stu-id="2dd16-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2dd16-126">请求正文</span><span class="sxs-lookup"><span data-stu-id="2dd16-126">Request body</span></span>
<span data-ttu-id="2dd16-127">在请求正文中，提供[deviceManagementReportSchedule](../resources/intune-reporting-devicemanagementreportschedule.md)对象的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="2dd16-127">In the request body, supply a JSON representation for the [deviceManagementReportSchedule](../resources/intune-reporting-devicemanagementreportschedule.md) object.</span></span>

<span data-ttu-id="2dd16-128">下表显示创建[deviceManagementReportSchedule](../resources/intune-reporting-devicemanagementreportschedule.md)时所需的属性。</span><span class="sxs-lookup"><span data-stu-id="2dd16-128">The following table shows the properties that are required when you create the [deviceManagementReportSchedule](../resources/intune-reporting-devicemanagementreportschedule.md).</span></span>

|<span data-ttu-id="2dd16-129">属性</span><span class="sxs-lookup"><span data-stu-id="2dd16-129">Property</span></span>|<span data-ttu-id="2dd16-130">类型</span><span class="sxs-lookup"><span data-stu-id="2dd16-130">Type</span></span>|<span data-ttu-id="2dd16-131">说明</span><span class="sxs-lookup"><span data-stu-id="2dd16-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2dd16-132">id</span><span class="sxs-lookup"><span data-stu-id="2dd16-132">id</span></span>|<span data-ttu-id="2dd16-133">字符串</span><span class="sxs-lookup"><span data-stu-id="2dd16-133">String</span></span>|<span data-ttu-id="2dd16-134">此实体的唯一标识符</span><span class="sxs-lookup"><span data-stu-id="2dd16-134">Unique identifier for this entity</span></span>|
|<span data-ttu-id="2dd16-135">reportScheduleName</span><span class="sxs-lookup"><span data-stu-id="2dd16-135">reportScheduleName</span></span>|<span data-ttu-id="2dd16-136">字符串</span><span class="sxs-lookup"><span data-stu-id="2dd16-136">String</span></span>|<span data-ttu-id="2dd16-137">计划的名称</span><span class="sxs-lookup"><span data-stu-id="2dd16-137">Name of the schedule</span></span>|
|<span data-ttu-id="2dd16-138">subject</span><span class="sxs-lookup"><span data-stu-id="2dd16-138">subject</span></span>|<span data-ttu-id="2dd16-139">String</span><span class="sxs-lookup"><span data-stu-id="2dd16-139">String</span></span>|<span data-ttu-id="2dd16-140">已传递的计划报告的主题</span><span class="sxs-lookup"><span data-stu-id="2dd16-140">Subject of the scheduled reports that are delivered</span></span>|
|<span data-ttu-id="2dd16-141">电子邮件</span><span class="sxs-lookup"><span data-stu-id="2dd16-141">emails</span></span>|<span data-ttu-id="2dd16-142">String 集合</span><span class="sxs-lookup"><span data-stu-id="2dd16-142">String collection</span></span>|<span data-ttu-id="2dd16-143">计划报告传递到的电子邮件</span><span class="sxs-lookup"><span data-stu-id="2dd16-143">Emails to which the scheduled reports are delivered</span></span>|
|<span data-ttu-id="2dd16-144">recurrence</span><span class="sxs-lookup"><span data-stu-id="2dd16-144">recurrence</span></span>|[<span data-ttu-id="2dd16-145">deviceManagementScheduledReportRecurrence</span><span class="sxs-lookup"><span data-stu-id="2dd16-145">deviceManagementScheduledReportRecurrence</span></span>](../resources/intune-reporting-devicemanagementscheduledreportrecurrence.md)|<span data-ttu-id="2dd16-146">计划报告传递的频率。</span><span class="sxs-lookup"><span data-stu-id="2dd16-146">Frequency of scheduled report delivery.</span></span> <span data-ttu-id="2dd16-147">可取值为：`none`、`daily`、`weekly`、`monthly`。</span><span class="sxs-lookup"><span data-stu-id="2dd16-147">Possible values are: `none`, `daily`, `weekly`, `monthly`.</span></span>|
|<span data-ttu-id="2dd16-148">startDateTime</span><span class="sxs-lookup"><span data-stu-id="2dd16-148">startDateTime</span></span>|<span data-ttu-id="2dd16-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2dd16-149">DateTimeOffset</span></span>|<span data-ttu-id="2dd16-150">计划报告的开始交付时间</span><span class="sxs-lookup"><span data-stu-id="2dd16-150">Time that the delivery of the scheduled reports starts</span></span>|
|<span data-ttu-id="2dd16-151">endDateTime</span><span class="sxs-lookup"><span data-stu-id="2dd16-151">endDateTime</span></span>|<span data-ttu-id="2dd16-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2dd16-152">DateTimeOffset</span></span>|<span data-ttu-id="2dd16-153">计划报告的结束传递时间</span><span class="sxs-lookup"><span data-stu-id="2dd16-153">Time that the delivery of the scheduled reports ends</span></span>|
|<span data-ttu-id="2dd16-154">userId</span><span class="sxs-lookup"><span data-stu-id="2dd16-154">userId</span></span>|<span data-ttu-id="2dd16-155">String</span><span class="sxs-lookup"><span data-stu-id="2dd16-155">String</span></span>|<span data-ttu-id="2dd16-156">创建报表的用户的 Id</span><span class="sxs-lookup"><span data-stu-id="2dd16-156">The Id of the User who created the report</span></span>|
|<span data-ttu-id="2dd16-157">reportName</span><span class="sxs-lookup"><span data-stu-id="2dd16-157">reportName</span></span>|<span data-ttu-id="2dd16-158">字符串</span><span class="sxs-lookup"><span data-stu-id="2dd16-158">String</span></span>|<span data-ttu-id="2dd16-159">报告的名称</span><span class="sxs-lookup"><span data-stu-id="2dd16-159">Name of the report</span></span>|
|<span data-ttu-id="2dd16-160">filter</span><span class="sxs-lookup"><span data-stu-id="2dd16-160">filter</span></span>|<span data-ttu-id="2dd16-161">字符串</span><span class="sxs-lookup"><span data-stu-id="2dd16-161">String</span></span>|<span data-ttu-id="2dd16-162">在报表上应用的筛选器</span><span class="sxs-lookup"><span data-stu-id="2dd16-162">Filters applied on the report</span></span>|
|<span data-ttu-id="2dd16-163">select</span><span class="sxs-lookup"><span data-stu-id="2dd16-163">select</span></span>|<span data-ttu-id="2dd16-164">String 集合</span><span class="sxs-lookup"><span data-stu-id="2dd16-164">String collection</span></span>|<span data-ttu-id="2dd16-165">从报告中选择的列</span><span class="sxs-lookup"><span data-stu-id="2dd16-165">Columns selected from the report</span></span>|
|<span data-ttu-id="2dd16-166">By</span><span class="sxs-lookup"><span data-stu-id="2dd16-166">orderBy</span></span>|<span data-ttu-id="2dd16-167">String 集合</span><span class="sxs-lookup"><span data-stu-id="2dd16-167">String collection</span></span>|<span data-ttu-id="2dd16-168">报表中的列的排序</span><span class="sxs-lookup"><span data-stu-id="2dd16-168">Ordering of columns in the report</span></span>|
|<span data-ttu-id="2dd16-169">format</span><span class="sxs-lookup"><span data-stu-id="2dd16-169">format</span></span>|[<span data-ttu-id="2dd16-170">deviceManagementReportFileFormat</span><span class="sxs-lookup"><span data-stu-id="2dd16-170">deviceManagementReportFileFormat</span></span>](../resources/intune-reporting-devicemanagementreportfileformat.md)|<span data-ttu-id="2dd16-171">计划报告的格式。</span><span class="sxs-lookup"><span data-stu-id="2dd16-171">Format of the scheduled report.</span></span> <span data-ttu-id="2dd16-172">可取值为：`csv`、`pdf`。</span><span class="sxs-lookup"><span data-stu-id="2dd16-172">Possible values are: `csv`, `pdf`.</span></span>|



## <a name="response"></a><span data-ttu-id="2dd16-173">响应</span><span class="sxs-lookup"><span data-stu-id="2dd16-173">Response</span></span>
<span data-ttu-id="2dd16-174">如果成功，此方法在响应`200 OK`正文中返回响应代码和更新的[deviceManagementReportSchedule](../resources/intune-reporting-devicemanagementreportschedule.md)对象。</span><span class="sxs-lookup"><span data-stu-id="2dd16-174">If successful, this method returns a `200 OK` response code and an updated [deviceManagementReportSchedule](../resources/intune-reporting-devicemanagementreportschedule.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2dd16-175">示例</span><span class="sxs-lookup"><span data-stu-id="2dd16-175">Example</span></span>

### <a name="request"></a><span data-ttu-id="2dd16-176">请求</span><span class="sxs-lookup"><span data-stu-id="2dd16-176">Request</span></span>
<span data-ttu-id="2dd16-177">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="2dd16-177">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/reports/reportSchedules/{deviceManagementReportScheduleId}
Content-type: application/json
Content-length: 539

{
  "@odata.type": "#microsoft.graph.deviceManagementReportSchedule",
  "reportScheduleName": "Report Schedule Name value",
  "subject": "Subject value",
  "emails": [
    "Emails value"
  ],
  "recurrence": "daily",
  "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
  "endDateTime": "2017-01-01T00:03:30.9241974-08:00",
  "userId": "User Id value",
  "reportName": "Report Name value",
  "filter": "Filter value",
  "select": [
    "Select value"
  ],
  "orderBy": [
    "Order By value"
  ],
  "format": "pdf"
}
```

### <a name="response"></a><span data-ttu-id="2dd16-178">响应</span><span class="sxs-lookup"><span data-stu-id="2dd16-178">Response</span></span>
<span data-ttu-id="2dd16-p104">下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="2dd16-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 588

{
  "@odata.type": "#microsoft.graph.deviceManagementReportSchedule",
  "id": "00bb9785-9785-00bb-8597-bb008597bb00",
  "reportScheduleName": "Report Schedule Name value",
  "subject": "Subject value",
  "emails": [
    "Emails value"
  ],
  "recurrence": "daily",
  "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
  "endDateTime": "2017-01-01T00:03:30.9241974-08:00",
  "userId": "User Id value",
  "reportName": "Report Name value",
  "filter": "Filter value",
  "select": [
    "Select value"
  ],
  "orderBy": [
    "Order By value"
  ],
  "format": "pdf"
}
```





