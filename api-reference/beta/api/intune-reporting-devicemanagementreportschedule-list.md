---
title: 列出 deviceManagementReportSchedules
description: 列出 deviceManagementReportSchedule 对象的属性和关系。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: e8e0f34e30c9ab23ad949a453252c11264d9ffd9
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2019
ms.locfileid: "37537175"
---
# <a name="list-devicemanagementreportschedules"></a><span data-ttu-id="937ac-103">列出 deviceManagementReportSchedules</span><span class="sxs-lookup"><span data-stu-id="937ac-103">List deviceManagementReportSchedules</span></span>

> <span data-ttu-id="937ac-104">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="937ac-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="937ac-105">**注意：** 适用于 Intune 的 Microsoft Graph API 需要租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="937ac-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="937ac-106">列出[deviceManagementReportSchedule](../resources/intune-reporting-devicemanagementreportschedule.md)对象的属性和关系。</span><span class="sxs-lookup"><span data-stu-id="937ac-106">List properties and relationships of the [deviceManagementReportSchedule](../resources/intune-reporting-devicemanagementreportschedule.md) objects.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="937ac-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="937ac-107">Prerequisites</span></span>
<span data-ttu-id="937ac-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="937ac-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="937ac-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="937ac-110">Permission type</span></span>|<span data-ttu-id="937ac-111">权限（从最高特权到最低特权）</span><span class="sxs-lookup"><span data-stu-id="937ac-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="937ac-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="937ac-112">Delegated (work or school account)</span></span>|<span data-ttu-id="937ac-113">Devicemanagementconfiguration.readwrite.all、Devicemanagementconfiguration.readwrite.all、Devicemanagementapps.readwrite.all、all、Devicemanagementapps.readwrite.all、all、Devicemanagementmanageddevices.readwrite.all、all、、all、Devicemanagementmanageddevices.readwrite.all</span><span class="sxs-lookup"><span data-stu-id="937ac-113">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All, DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All, DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="937ac-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="937ac-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="937ac-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="937ac-115">Not supported.</span></span>|
|<span data-ttu-id="937ac-116">应用程序</span><span class="sxs-lookup"><span data-stu-id="937ac-116">Application</span></span>|<span data-ttu-id="937ac-117">Devicemanagementconfiguration.readwrite.all、Devicemanagementconfiguration.readwrite.all、Devicemanagementapps.readwrite.all、all、Devicemanagementapps.readwrite.all、all、Devicemanagementmanageddevices.readwrite.all、all、、all、Devicemanagementmanageddevices.readwrite.all</span><span class="sxs-lookup"><span data-stu-id="937ac-117">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All, DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All, DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="937ac-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="937ac-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/reports/reportSchedules
```

## <a name="request-headers"></a><span data-ttu-id="937ac-119">请求标头</span><span class="sxs-lookup"><span data-stu-id="937ac-119">Request headers</span></span>
|<span data-ttu-id="937ac-120">标头</span><span class="sxs-lookup"><span data-stu-id="937ac-120">Header</span></span>|<span data-ttu-id="937ac-121">值</span><span class="sxs-lookup"><span data-stu-id="937ac-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="937ac-122">授权</span><span class="sxs-lookup"><span data-stu-id="937ac-122">Authorization</span></span>|<span data-ttu-id="937ac-123">Bearer &lt;token&gt;。必需。</span><span class="sxs-lookup"><span data-stu-id="937ac-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="937ac-124">接受</span><span class="sxs-lookup"><span data-stu-id="937ac-124">Accept</span></span>|<span data-ttu-id="937ac-125">application/json</span><span class="sxs-lookup"><span data-stu-id="937ac-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="937ac-126">请求正文</span><span class="sxs-lookup"><span data-stu-id="937ac-126">Request body</span></span>
<span data-ttu-id="937ac-127">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="937ac-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="937ac-128">响应</span><span class="sxs-lookup"><span data-stu-id="937ac-128">Response</span></span>
<span data-ttu-id="937ac-129">如果成功，此方法在响应`200 OK`正文中返回响应代码和[deviceManagementReportSchedule](../resources/intune-reporting-devicemanagementreportschedule.md)对象集合。</span><span class="sxs-lookup"><span data-stu-id="937ac-129">If successful, this method returns a `200 OK` response code and a collection of [deviceManagementReportSchedule](../resources/intune-reporting-devicemanagementreportschedule.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="937ac-130">示例</span><span class="sxs-lookup"><span data-stu-id="937ac-130">Example</span></span>

### <a name="request"></a><span data-ttu-id="937ac-131">请求</span><span class="sxs-lookup"><span data-stu-id="937ac-131">Request</span></span>
<span data-ttu-id="937ac-132">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="937ac-132">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/reports/reportSchedules
```

### <a name="response"></a><span data-ttu-id="937ac-133">响应</span><span class="sxs-lookup"><span data-stu-id="937ac-133">Response</span></span>
<span data-ttu-id="937ac-p102">下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="937ac-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 701

{
  "value": [
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
  ]
}
```





