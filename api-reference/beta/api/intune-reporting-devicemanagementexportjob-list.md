---
title: 列出 deviceManagementExportJobs
description: 列出 deviceManagementExportJob 对象的属性和关系。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: e738277d9a7647132400196afea9c34a7c51805e
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2019
ms.locfileid: "37538306"
---
# <a name="list-devicemanagementexportjobs"></a><span data-ttu-id="bb002-103">列出 deviceManagementExportJobs</span><span class="sxs-lookup"><span data-stu-id="bb002-103">List deviceManagementExportJobs</span></span>

> <span data-ttu-id="bb002-104">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="bb002-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="bb002-105">**注意：** 适用于 Intune 的 Microsoft Graph API 需要租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="bb002-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="bb002-106">列出[deviceManagementExportJob](../resources/intune-reporting-devicemanagementexportjob.md)对象的属性和关系。</span><span class="sxs-lookup"><span data-stu-id="bb002-106">List properties and relationships of the [deviceManagementExportJob](../resources/intune-reporting-devicemanagementexportjob.md) objects.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bb002-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="bb002-107">Prerequisites</span></span>
<span data-ttu-id="bb002-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="bb002-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bb002-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="bb002-110">Permission type</span></span>|<span data-ttu-id="bb002-111">权限（从最高特权到最低特权）</span><span class="sxs-lookup"><span data-stu-id="bb002-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bb002-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="bb002-112">Delegated (work or school account)</span></span>|<span data-ttu-id="bb002-113">Devicemanagementconfiguration.readwrite.all、Devicemanagementconfiguration.readwrite.all、Devicemanagementapps.readwrite.all、all、Devicemanagementapps.readwrite.all、all、Devicemanagementmanageddevices.readwrite.all、all、、all、Devicemanagementmanageddevices.readwrite.all</span><span class="sxs-lookup"><span data-stu-id="bb002-113">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All, DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All, DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="bb002-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="bb002-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bb002-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="bb002-115">Not supported.</span></span>|
|<span data-ttu-id="bb002-116">应用程序</span><span class="sxs-lookup"><span data-stu-id="bb002-116">Application</span></span>|<span data-ttu-id="bb002-117">Devicemanagementconfiguration.readwrite.all、Devicemanagementconfiguration.readwrite.all、Devicemanagementapps.readwrite.all、all、Devicemanagementapps.readwrite.all、all、Devicemanagementmanageddevices.readwrite.all、all、、all、Devicemanagementmanageddevices.readwrite.all</span><span class="sxs-lookup"><span data-stu-id="bb002-117">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All, DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All, DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="bb002-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="bb002-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/reports/exportJobs
```

## <a name="request-headers"></a><span data-ttu-id="bb002-119">请求标头</span><span class="sxs-lookup"><span data-stu-id="bb002-119">Request headers</span></span>
|<span data-ttu-id="bb002-120">标头</span><span class="sxs-lookup"><span data-stu-id="bb002-120">Header</span></span>|<span data-ttu-id="bb002-121">值</span><span class="sxs-lookup"><span data-stu-id="bb002-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bb002-122">授权</span><span class="sxs-lookup"><span data-stu-id="bb002-122">Authorization</span></span>|<span data-ttu-id="bb002-123">Bearer &lt;token&gt;。必需。</span><span class="sxs-lookup"><span data-stu-id="bb002-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bb002-124">接受</span><span class="sxs-lookup"><span data-stu-id="bb002-124">Accept</span></span>|<span data-ttu-id="bb002-125">application/json</span><span class="sxs-lookup"><span data-stu-id="bb002-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bb002-126">请求正文</span><span class="sxs-lookup"><span data-stu-id="bb002-126">Request body</span></span>
<span data-ttu-id="bb002-127">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="bb002-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bb002-128">响应</span><span class="sxs-lookup"><span data-stu-id="bb002-128">Response</span></span>
<span data-ttu-id="bb002-129">如果成功，此方法在响应`200 OK`正文中返回响应代码和[deviceManagementExportJob](../resources/intune-reporting-devicemanagementexportjob.md)对象集合。</span><span class="sxs-lookup"><span data-stu-id="bb002-129">If successful, this method returns a `200 OK` response code and a collection of [deviceManagementExportJob](../resources/intune-reporting-devicemanagementexportjob.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bb002-130">示例</span><span class="sxs-lookup"><span data-stu-id="bb002-130">Example</span></span>

### <a name="request"></a><span data-ttu-id="bb002-131">请求</span><span class="sxs-lookup"><span data-stu-id="bb002-131">Request</span></span>
<span data-ttu-id="bb002-132">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="bb002-132">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/reports/exportJobs
```

### <a name="response"></a><span data-ttu-id="bb002-133">响应</span><span class="sxs-lookup"><span data-stu-id="bb002-133">Response</span></span>
<span data-ttu-id="bb002-p102">下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="bb002-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 594

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceManagementExportJob",
      "id": "9ddfb995-b995-9ddf-95b9-df9d95b9df9d",
      "reportName": "Report Name value",
      "filter": "Filter value",
      "select": [
        "Select value"
      ],
      "orderBy": [
        "Order By value"
      ],
      "format": "pdf",
      "snapshotId": "Snapshot Id value",
      "status": "notStarted",
      "url": "Url value",
      "requestDateTime": "2017-01-01T00:03:07.1589002-08:00",
      "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00"
    }
  ]
}
```





