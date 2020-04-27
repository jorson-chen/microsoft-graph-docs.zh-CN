---
title: getPolicyNonComplianceSummaryReport 操作
description: 尚未记录
author: dougeby
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: be6870986a4d98d0170d8b7c31b9f2af7afce567
ms.sourcegitcommit: bbcf074f0be9d5e02f84c290122850cc5968fb1f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2020
ms.locfileid: "43391709"
---
# <a name="getpolicynoncompliancesummaryreport-action"></a><span data-ttu-id="38073-103">getPolicyNonComplianceSummaryReport 操作</span><span class="sxs-lookup"><span data-stu-id="38073-103">getPolicyNonComplianceSummaryReport action</span></span>

<span data-ttu-id="38073-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="38073-104">Namespace: microsoft.graph</span></span>

> <span data-ttu-id="38073-105">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="38073-105">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="38073-106">**注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="38073-106">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="38073-107">尚未记录</span><span class="sxs-lookup"><span data-stu-id="38073-107">Not yet documented</span></span>

## <a name="prerequisites"></a><span data-ttu-id="38073-108">先决条件</span><span class="sxs-lookup"><span data-stu-id="38073-108">Prerequisites</span></span>
<span data-ttu-id="38073-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="38073-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="38073-111">权限类型</span><span class="sxs-lookup"><span data-stu-id="38073-111">Permission type</span></span>|<span data-ttu-id="38073-112">权限（从最高特权到最低特权）</span><span class="sxs-lookup"><span data-stu-id="38073-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="38073-113">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="38073-113">Delegated (work or school account)</span></span>|<span data-ttu-id="38073-114">Devicemanagementconfiguration.readwrite.all、Devicemanagementconfiguration.readwrite.all、Devicemanagementapps.readwrite.all、all、Devicemanagementapps.readwrite.all、all、devicemanagementmanageddevices.readwrite.all、all、devicemanagementmanageddevices.readwrite.all、all 和 Read. all。 All</span><span class="sxs-lookup"><span data-stu-id="38073-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All, DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All, DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="38073-115">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="38073-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="38073-116">不支持。</span><span class="sxs-lookup"><span data-stu-id="38073-116">Not supported.</span></span>|
|<span data-ttu-id="38073-117">应用程序</span><span class="sxs-lookup"><span data-stu-id="38073-117">Application</span></span>|<span data-ttu-id="38073-118">Devicemanagementconfiguration.readwrite.all、Devicemanagementconfiguration.readwrite.all、Devicemanagementapps.readwrite.all、all、Devicemanagementapps.readwrite.all、all、devicemanagementmanageddevices.readwrite.all、all、devicemanagementmanageddevices.readwrite.all、all 和 Read. all。 All</span><span class="sxs-lookup"><span data-stu-id="38073-118">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All, DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All, DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="38073-119">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="38073-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/reports/getPolicyNonComplianceSummaryReport
```

## <a name="request-headers"></a><span data-ttu-id="38073-120">请求标头</span><span class="sxs-lookup"><span data-stu-id="38073-120">Request headers</span></span>
|<span data-ttu-id="38073-121">标头</span><span class="sxs-lookup"><span data-stu-id="38073-121">Header</span></span>|<span data-ttu-id="38073-122">值</span><span class="sxs-lookup"><span data-stu-id="38073-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="38073-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="38073-123">Authorization</span></span>|<span data-ttu-id="38073-124">Bearer &lt;token&gt;。必需。</span><span class="sxs-lookup"><span data-stu-id="38073-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="38073-125">接受</span><span class="sxs-lookup"><span data-stu-id="38073-125">Accept</span></span>|<span data-ttu-id="38073-126">application/json</span><span class="sxs-lookup"><span data-stu-id="38073-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="38073-127">请求正文</span><span class="sxs-lookup"><span data-stu-id="38073-127">Request body</span></span>
<span data-ttu-id="38073-128">在请求正文中，提供参数的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="38073-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="38073-129">下表显示了可用于此操作的参数。</span><span class="sxs-lookup"><span data-stu-id="38073-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="38073-130">属性</span><span class="sxs-lookup"><span data-stu-id="38073-130">Property</span></span>|<span data-ttu-id="38073-131">类型</span><span class="sxs-lookup"><span data-stu-id="38073-131">Type</span></span>|<span data-ttu-id="38073-132">说明</span><span class="sxs-lookup"><span data-stu-id="38073-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="38073-133">name</span><span class="sxs-lookup"><span data-stu-id="38073-133">name</span></span>|<span data-ttu-id="38073-134">字符串</span><span class="sxs-lookup"><span data-stu-id="38073-134">String</span></span>|<span data-ttu-id="38073-135">尚未记录</span><span class="sxs-lookup"><span data-stu-id="38073-135">Not yet documented</span></span>|
|<span data-ttu-id="38073-136">select</span><span class="sxs-lookup"><span data-stu-id="38073-136">select</span></span>|<span data-ttu-id="38073-137">String collection</span><span class="sxs-lookup"><span data-stu-id="38073-137">String collection</span></span>|<span data-ttu-id="38073-138">尚未记录</span><span class="sxs-lookup"><span data-stu-id="38073-138">Not yet documented</span></span>|
|<span data-ttu-id="38073-139">search</span><span class="sxs-lookup"><span data-stu-id="38073-139">search</span></span>|<span data-ttu-id="38073-140">String</span><span class="sxs-lookup"><span data-stu-id="38073-140">String</span></span>|<span data-ttu-id="38073-141">尚未记录</span><span class="sxs-lookup"><span data-stu-id="38073-141">Not yet documented</span></span>|
|<span data-ttu-id="38073-142">groupBy</span><span class="sxs-lookup"><span data-stu-id="38073-142">groupBy</span></span>|<span data-ttu-id="38073-143">String collection</span><span class="sxs-lookup"><span data-stu-id="38073-143">String collection</span></span>|<span data-ttu-id="38073-144">尚未记录</span><span class="sxs-lookup"><span data-stu-id="38073-144">Not yet documented</span></span>|
|<span data-ttu-id="38073-145">By</span><span class="sxs-lookup"><span data-stu-id="38073-145">orderBy</span></span>|<span data-ttu-id="38073-146">String collection</span><span class="sxs-lookup"><span data-stu-id="38073-146">String collection</span></span>|<span data-ttu-id="38073-147">尚未记录</span><span class="sxs-lookup"><span data-stu-id="38073-147">Not yet documented</span></span>|
|<span data-ttu-id="38073-148">skip</span><span class="sxs-lookup"><span data-stu-id="38073-148">skip</span></span>|<span data-ttu-id="38073-149">Int32</span><span class="sxs-lookup"><span data-stu-id="38073-149">Int32</span></span>|<span data-ttu-id="38073-150">尚未记录</span><span class="sxs-lookup"><span data-stu-id="38073-150">Not yet documented</span></span>|
|<span data-ttu-id="38073-151">top</span><span class="sxs-lookup"><span data-stu-id="38073-151">top</span></span>|<span data-ttu-id="38073-152">Int32</span><span class="sxs-lookup"><span data-stu-id="38073-152">Int32</span></span>|<span data-ttu-id="38073-153">尚未记录</span><span class="sxs-lookup"><span data-stu-id="38073-153">Not yet documented</span></span>|
|<span data-ttu-id="38073-154">sessionId</span><span class="sxs-lookup"><span data-stu-id="38073-154">sessionId</span></span>|<span data-ttu-id="38073-155">String</span><span class="sxs-lookup"><span data-stu-id="38073-155">String</span></span>|<span data-ttu-id="38073-156">尚未记录</span><span class="sxs-lookup"><span data-stu-id="38073-156">Not yet documented</span></span>|
|<span data-ttu-id="38073-157">filter</span><span class="sxs-lookup"><span data-stu-id="38073-157">filter</span></span>|<span data-ttu-id="38073-158">String</span><span class="sxs-lookup"><span data-stu-id="38073-158">String</span></span>|<span data-ttu-id="38073-159">尚未记录</span><span class="sxs-lookup"><span data-stu-id="38073-159">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="38073-160">响应</span><span class="sxs-lookup"><span data-stu-id="38073-160">Response</span></span>
<span data-ttu-id="38073-161">如果成功，此操作会在`200 OK`响应正文中返回响应代码和 Stream。</span><span class="sxs-lookup"><span data-stu-id="38073-161">If successful, this action returns a `200 OK` response code and a Stream in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="38073-162">示例</span><span class="sxs-lookup"><span data-stu-id="38073-162">Example</span></span>

### <a name="request"></a><span data-ttu-id="38073-163">请求</span><span class="sxs-lookup"><span data-stu-id="38073-163">Request</span></span>
<span data-ttu-id="38073-164">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="38073-164">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/reports/getPolicyNonComplianceSummaryReport

Content-type: application/json
Content-length: 278

{
  "name": "Name value",
  "select": [
    "Select value"
  ],
  "search": "Search value",
  "groupBy": [
    "Group By value"
  ],
  "orderBy": [
    "Order By value"
  ],
  "skip": 4,
  "top": 3,
  "sessionId": "Session Id value",
  "filter": "Filter value"
}
```

### <a name="response"></a><span data-ttu-id="38073-165">响应</span><span class="sxs-lookup"><span data-stu-id="38073-165">Response</span></span>
<span data-ttu-id="38073-p102">下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="38073-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 54

{
  "value": "<Unknown Primitive Type Edm.Stream>"
}
```


