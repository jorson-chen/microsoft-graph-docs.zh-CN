---
title: 获取 deviceManagementExportJob
description: 读取 deviceManagementExportJob 对象的属性和关系。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 78506c67f4ae8f83c6165dcd475bb21e367c6375
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2019
ms.locfileid: "37537266"
---
# <a name="get-devicemanagementexportjob"></a><span data-ttu-id="ceb0d-103">获取 deviceManagementExportJob</span><span class="sxs-lookup"><span data-stu-id="ceb0d-103">Get deviceManagementExportJob</span></span>

> <span data-ttu-id="ceb0d-104">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="ceb0d-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="ceb0d-105">**注意：** 适用于 Intune 的 Microsoft Graph API 需要租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="ceb0d-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="ceb0d-106">读取[deviceManagementExportJob](../resources/intune-reporting-devicemanagementexportjob.md)对象的属性和关系。</span><span class="sxs-lookup"><span data-stu-id="ceb0d-106">Read properties and relationships of the [deviceManagementExportJob](../resources/intune-reporting-devicemanagementexportjob.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ceb0d-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="ceb0d-107">Prerequisites</span></span>
<span data-ttu-id="ceb0d-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="ceb0d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ceb0d-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="ceb0d-110">Permission type</span></span>|<span data-ttu-id="ceb0d-111">权限（从最高特权到最低特权）</span><span class="sxs-lookup"><span data-stu-id="ceb0d-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ceb0d-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="ceb0d-112">Delegated (work or school account)</span></span>|<span data-ttu-id="ceb0d-113">Devicemanagementconfiguration.readwrite.all、Devicemanagementconfiguration.readwrite.all、Devicemanagementapps.readwrite.all、all、Devicemanagementapps.readwrite.all、all、Devicemanagementmanageddevices.readwrite.all、all、、all、Devicemanagementmanageddevices.readwrite.all</span><span class="sxs-lookup"><span data-stu-id="ceb0d-113">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All, DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All, DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="ceb0d-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="ceb0d-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ceb0d-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="ceb0d-115">Not supported.</span></span>|
|<span data-ttu-id="ceb0d-116">应用程序</span><span class="sxs-lookup"><span data-stu-id="ceb0d-116">Application</span></span>|<span data-ttu-id="ceb0d-117">Devicemanagementconfiguration.readwrite.all、Devicemanagementconfiguration.readwrite.all、Devicemanagementapps.readwrite.all、all、Devicemanagementapps.readwrite.all、all、Devicemanagementmanageddevices.readwrite.all、all、、all、Devicemanagementmanageddevices.readwrite.all</span><span class="sxs-lookup"><span data-stu-id="ceb0d-117">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All, DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All, DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="ceb0d-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="ceb0d-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/reports/exportJobs/{deviceManagementExportJobId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="ceb0d-119">可选的查询参数</span><span class="sxs-lookup"><span data-stu-id="ceb0d-119">Optional query parameters</span></span>
<span data-ttu-id="ceb0d-120">此方法支持 [OData 查询参数](https://docs.microsoft.com/en-us/graph/query-parameters) 来帮助自定义响应。</span><span class="sxs-lookup"><span data-stu-id="ceb0d-120">This method supports the [OData Query Parameters](https://docs.microsoft.com/en-us/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="ceb0d-121">请求标头</span><span class="sxs-lookup"><span data-stu-id="ceb0d-121">Request headers</span></span>
|<span data-ttu-id="ceb0d-122">标头</span><span class="sxs-lookup"><span data-stu-id="ceb0d-122">Header</span></span>|<span data-ttu-id="ceb0d-123">值</span><span class="sxs-lookup"><span data-stu-id="ceb0d-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ceb0d-124">授权</span><span class="sxs-lookup"><span data-stu-id="ceb0d-124">Authorization</span></span>|<span data-ttu-id="ceb0d-125">Bearer &lt;token&gt;。必需。</span><span class="sxs-lookup"><span data-stu-id="ceb0d-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ceb0d-126">接受</span><span class="sxs-lookup"><span data-stu-id="ceb0d-126">Accept</span></span>|<span data-ttu-id="ceb0d-127">application/json</span><span class="sxs-lookup"><span data-stu-id="ceb0d-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ceb0d-128">请求正文</span><span class="sxs-lookup"><span data-stu-id="ceb0d-128">Request body</span></span>
<span data-ttu-id="ceb0d-129">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="ceb0d-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ceb0d-130">响应</span><span class="sxs-lookup"><span data-stu-id="ceb0d-130">Response</span></span>
<span data-ttu-id="ceb0d-131">如果成功，此方法在响应`200 OK`正文中返回响应代码和[deviceManagementExportJob](../resources/intune-reporting-devicemanagementexportjob.md)对象。</span><span class="sxs-lookup"><span data-stu-id="ceb0d-131">If successful, this method returns a `200 OK` response code and [deviceManagementExportJob](../resources/intune-reporting-devicemanagementexportjob.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ceb0d-132">示例</span><span class="sxs-lookup"><span data-stu-id="ceb0d-132">Example</span></span>

### <a name="request"></a><span data-ttu-id="ceb0d-133">请求</span><span class="sxs-lookup"><span data-stu-id="ceb0d-133">Request</span></span>
<span data-ttu-id="ceb0d-134">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="ceb0d-134">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/reports/exportJobs/{deviceManagementExportJobId}
```

### <a name="response"></a><span data-ttu-id="ceb0d-135">响应</span><span class="sxs-lookup"><span data-stu-id="ceb0d-135">Response</span></span>
<span data-ttu-id="ceb0d-p102">下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="ceb0d-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 548

{
  "value": {
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
}
```





