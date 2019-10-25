---
title: summarizeDeviceRegressionPerformance 函数
description: 尚未记录
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 9a0f1a17ae6d44b48c2c8d8367858dac4046a1bc
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2019
ms.locfileid: "37529114"
---
# <a name="summarizedeviceregressionperformance-function"></a><span data-ttu-id="5ae51-103">summarizeDeviceRegressionPerformance 函数</span><span class="sxs-lookup"><span data-stu-id="5ae51-103">summarizeDeviceRegressionPerformance function</span></span>

> <span data-ttu-id="5ae51-104">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="5ae51-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="5ae51-105">**注意：** 适用于 Intune 的 Microsoft Graph API 需要租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="5ae51-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="5ae51-106">尚未记录</span><span class="sxs-lookup"><span data-stu-id="5ae51-106">Not yet documented</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5ae51-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="5ae51-107">Prerequisites</span></span>
<span data-ttu-id="5ae51-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="5ae51-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5ae51-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="5ae51-110">Permission type</span></span>|<span data-ttu-id="5ae51-111">权限（从最高特权到最低特权）</span><span class="sxs-lookup"><span data-stu-id="5ae51-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5ae51-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="5ae51-112">Delegated (work or school account)</span></span>|<span data-ttu-id="5ae51-113">DeviceManagementManagedDevices.ReadWrite.All、DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="5ae51-113">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="5ae51-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="5ae51-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5ae51-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="5ae51-115">Not supported.</span></span>|
|<span data-ttu-id="5ae51-116">应用程序</span><span class="sxs-lookup"><span data-stu-id="5ae51-116">Application</span></span>|<span data-ttu-id="5ae51-117">DeviceManagementManagedDevices.ReadWrite.All、DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="5ae51-117">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="5ae51-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="5ae51-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/userExperienceAnalyticsRegressionSummary/summarizeDeviceRegressionPerformance
```

## <a name="request-headers"></a><span data-ttu-id="5ae51-119">请求标头</span><span class="sxs-lookup"><span data-stu-id="5ae51-119">Request headers</span></span>
|<span data-ttu-id="5ae51-120">标头</span><span class="sxs-lookup"><span data-stu-id="5ae51-120">Header</span></span>|<span data-ttu-id="5ae51-121">值</span><span class="sxs-lookup"><span data-stu-id="5ae51-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5ae51-122">授权</span><span class="sxs-lookup"><span data-stu-id="5ae51-122">Authorization</span></span>|<span data-ttu-id="5ae51-123">Bearer &lt;token&gt;。必需。</span><span class="sxs-lookup"><span data-stu-id="5ae51-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5ae51-124">接受</span><span class="sxs-lookup"><span data-stu-id="5ae51-124">Accept</span></span>|<span data-ttu-id="5ae51-125">application/json</span><span class="sxs-lookup"><span data-stu-id="5ae51-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5ae51-126">请求正文</span><span class="sxs-lookup"><span data-stu-id="5ae51-126">Request body</span></span>
<span data-ttu-id="5ae51-127">在请求 URL 中，提供以下查询参数（含值）。</span><span class="sxs-lookup"><span data-stu-id="5ae51-127">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="5ae51-128">下表显示了可用于此函数的参数。</span><span class="sxs-lookup"><span data-stu-id="5ae51-128">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="5ae51-129">属性</span><span class="sxs-lookup"><span data-stu-id="5ae51-129">Property</span></span>|<span data-ttu-id="5ae51-130">类型</span><span class="sxs-lookup"><span data-stu-id="5ae51-130">Type</span></span>|<span data-ttu-id="5ae51-131">说明</span><span class="sxs-lookup"><span data-stu-id="5ae51-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5ae51-132">summarizeBy</span><span class="sxs-lookup"><span data-stu-id="5ae51-132">summarizeBy</span></span>|[<span data-ttu-id="5ae51-133">userExperienceAnalyticsSummarizedBy</span><span class="sxs-lookup"><span data-stu-id="5ae51-133">userExperienceAnalyticsSummarizedBy</span></span>](../resources/intune-devices-userexperienceanalyticssummarizedby.md)|<span data-ttu-id="5ae51-134">尚未记录</span><span class="sxs-lookup"><span data-stu-id="5ae51-134">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="5ae51-135">响应</span><span class="sxs-lookup"><span data-stu-id="5ae51-135">Response</span></span>
<span data-ttu-id="5ae51-136">如果成功，此函数会在`200 OK`响应正文中返回响应代码和[userExperienceAnalyticsRegressionSummary](../resources/intune-devices-userexperienceanalyticsregressionsummary.md) 。</span><span class="sxs-lookup"><span data-stu-id="5ae51-136">If successful, this function returns a `200 OK` response code and a [userExperienceAnalyticsRegressionSummary](../resources/intune-devices-userexperienceanalyticsregressionsummary.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5ae51-137">示例</span><span class="sxs-lookup"><span data-stu-id="5ae51-137">Example</span></span>

### <a name="request"></a><span data-ttu-id="5ae51-138">请求</span><span class="sxs-lookup"><span data-stu-id="5ae51-138">Request</span></span>
<span data-ttu-id="5ae51-139">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="5ae51-139">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/userExperienceAnalyticsRegressionSummary/summarizeDeviceRegressionPerformance(summarizeBy='parameterValue')
```

### <a name="response"></a><span data-ttu-id="5ae51-140">响应</span><span class="sxs-lookup"><span data-stu-id="5ae51-140">Response</span></span>
<span data-ttu-id="5ae51-p103">下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="5ae51-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 154

{
  "value": {
    "@odata.type": "#microsoft.graph.userExperienceAnalyticsRegressionSummary",
    "id": "41683327-3327-4168-2733-684127336841"
  }
}
```





