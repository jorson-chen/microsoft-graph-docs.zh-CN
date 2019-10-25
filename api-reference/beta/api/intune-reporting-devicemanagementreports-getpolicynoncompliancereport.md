---
title: getPolicyNonComplianceReport 操作
description: 尚未记录
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: ac4ee5035dff7a39813ceb513b981e7cc69f3a9f
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2019
ms.locfileid: "37537217"
---
# <a name="getpolicynoncompliancereport-action"></a><span data-ttu-id="9d62b-103">getPolicyNonComplianceReport 操作</span><span class="sxs-lookup"><span data-stu-id="9d62b-103">getPolicyNonComplianceReport action</span></span>

> <span data-ttu-id="9d62b-104">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="9d62b-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="9d62b-105">**注意：** 适用于 Intune 的 Microsoft Graph API 需要租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="9d62b-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="9d62b-106">尚未记录</span><span class="sxs-lookup"><span data-stu-id="9d62b-106">Not yet documented</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9d62b-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="9d62b-107">Prerequisites</span></span>
<span data-ttu-id="9d62b-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="9d62b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9d62b-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="9d62b-110">Permission type</span></span>|<span data-ttu-id="9d62b-111">权限（从最高特权到最低特权）</span><span class="sxs-lookup"><span data-stu-id="9d62b-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9d62b-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="9d62b-112">Delegated (work or school account)</span></span>|<span data-ttu-id="9d62b-113">Devicemanagementconfiguration.readwrite.all、Devicemanagementconfiguration.readwrite.all、Devicemanagementapps.readwrite.all、all、Devicemanagementapps.readwrite.all、all、Devicemanagementmanageddevices.readwrite.all、all、、all、Devicemanagementmanageddevices.readwrite.all</span><span class="sxs-lookup"><span data-stu-id="9d62b-113">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All, DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All, DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="9d62b-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="9d62b-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9d62b-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="9d62b-115">Not supported.</span></span>|
|<span data-ttu-id="9d62b-116">应用程序</span><span class="sxs-lookup"><span data-stu-id="9d62b-116">Application</span></span>|<span data-ttu-id="9d62b-117">Devicemanagementconfiguration.readwrite.all、Devicemanagementconfiguration.readwrite.all、Devicemanagementapps.readwrite.all、all、Devicemanagementapps.readwrite.all、all、Devicemanagementmanageddevices.readwrite.all、all、、all、Devicemanagementmanageddevices.readwrite.all</span><span class="sxs-lookup"><span data-stu-id="9d62b-117">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All, DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All, DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="9d62b-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="9d62b-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/reports/getPolicyNonComplianceReport
```

## <a name="request-headers"></a><span data-ttu-id="9d62b-119">请求标头</span><span class="sxs-lookup"><span data-stu-id="9d62b-119">Request headers</span></span>
|<span data-ttu-id="9d62b-120">标头</span><span class="sxs-lookup"><span data-stu-id="9d62b-120">Header</span></span>|<span data-ttu-id="9d62b-121">值</span><span class="sxs-lookup"><span data-stu-id="9d62b-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9d62b-122">授权</span><span class="sxs-lookup"><span data-stu-id="9d62b-122">Authorization</span></span>|<span data-ttu-id="9d62b-123">Bearer &lt;token&gt;。必需。</span><span class="sxs-lookup"><span data-stu-id="9d62b-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9d62b-124">接受</span><span class="sxs-lookup"><span data-stu-id="9d62b-124">Accept</span></span>|<span data-ttu-id="9d62b-125">application/json</span><span class="sxs-lookup"><span data-stu-id="9d62b-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9d62b-126">请求正文</span><span class="sxs-lookup"><span data-stu-id="9d62b-126">Request body</span></span>
<span data-ttu-id="9d62b-127">在请求正文中，提供参数的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="9d62b-127">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="9d62b-128">下表显示了可用于此操作的参数。</span><span class="sxs-lookup"><span data-stu-id="9d62b-128">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="9d62b-129">属性</span><span class="sxs-lookup"><span data-stu-id="9d62b-129">Property</span></span>|<span data-ttu-id="9d62b-130">类型</span><span class="sxs-lookup"><span data-stu-id="9d62b-130">Type</span></span>|<span data-ttu-id="9d62b-131">说明</span><span class="sxs-lookup"><span data-stu-id="9d62b-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9d62b-132">name</span><span class="sxs-lookup"><span data-stu-id="9d62b-132">name</span></span>|<span data-ttu-id="9d62b-133">字符串</span><span class="sxs-lookup"><span data-stu-id="9d62b-133">String</span></span>|<span data-ttu-id="9d62b-134">尚未记录</span><span class="sxs-lookup"><span data-stu-id="9d62b-134">Not yet documented</span></span>|
|<span data-ttu-id="9d62b-135">select</span><span class="sxs-lookup"><span data-stu-id="9d62b-135">select</span></span>|<span data-ttu-id="9d62b-136">String collection</span><span class="sxs-lookup"><span data-stu-id="9d62b-136">String collection</span></span>|<span data-ttu-id="9d62b-137">尚未记录</span><span class="sxs-lookup"><span data-stu-id="9d62b-137">Not yet documented</span></span>|
|<span data-ttu-id="9d62b-138">search</span><span class="sxs-lookup"><span data-stu-id="9d62b-138">search</span></span>|<span data-ttu-id="9d62b-139">String</span><span class="sxs-lookup"><span data-stu-id="9d62b-139">String</span></span>|<span data-ttu-id="9d62b-140">尚未记录</span><span class="sxs-lookup"><span data-stu-id="9d62b-140">Not yet documented</span></span>|
|<span data-ttu-id="9d62b-141">groupBy</span><span class="sxs-lookup"><span data-stu-id="9d62b-141">groupBy</span></span>|<span data-ttu-id="9d62b-142">String collection</span><span class="sxs-lookup"><span data-stu-id="9d62b-142">String collection</span></span>|<span data-ttu-id="9d62b-143">尚未记录</span><span class="sxs-lookup"><span data-stu-id="9d62b-143">Not yet documented</span></span>|
|<span data-ttu-id="9d62b-144">By</span><span class="sxs-lookup"><span data-stu-id="9d62b-144">orderBy</span></span>|<span data-ttu-id="9d62b-145">String collection</span><span class="sxs-lookup"><span data-stu-id="9d62b-145">String collection</span></span>|<span data-ttu-id="9d62b-146">尚未记录</span><span class="sxs-lookup"><span data-stu-id="9d62b-146">Not yet documented</span></span>|
|<span data-ttu-id="9d62b-147">skip</span><span class="sxs-lookup"><span data-stu-id="9d62b-147">skip</span></span>|<span data-ttu-id="9d62b-148">Int32</span><span class="sxs-lookup"><span data-stu-id="9d62b-148">Int32</span></span>|<span data-ttu-id="9d62b-149">尚未记录</span><span class="sxs-lookup"><span data-stu-id="9d62b-149">Not yet documented</span></span>|
|<span data-ttu-id="9d62b-150">top</span><span class="sxs-lookup"><span data-stu-id="9d62b-150">top</span></span>|<span data-ttu-id="9d62b-151">Int32</span><span class="sxs-lookup"><span data-stu-id="9d62b-151">Int32</span></span>|<span data-ttu-id="9d62b-152">尚未记录</span><span class="sxs-lookup"><span data-stu-id="9d62b-152">Not yet documented</span></span>|
|<span data-ttu-id="9d62b-153">sessionId</span><span class="sxs-lookup"><span data-stu-id="9d62b-153">sessionId</span></span>|<span data-ttu-id="9d62b-154">String</span><span class="sxs-lookup"><span data-stu-id="9d62b-154">String</span></span>|<span data-ttu-id="9d62b-155">尚未记录</span><span class="sxs-lookup"><span data-stu-id="9d62b-155">Not yet documented</span></span>|
|<span data-ttu-id="9d62b-156">filter</span><span class="sxs-lookup"><span data-stu-id="9d62b-156">filter</span></span>|<span data-ttu-id="9d62b-157">String</span><span class="sxs-lookup"><span data-stu-id="9d62b-157">String</span></span>|<span data-ttu-id="9d62b-158">尚未记录</span><span class="sxs-lookup"><span data-stu-id="9d62b-158">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="9d62b-159">响应</span><span class="sxs-lookup"><span data-stu-id="9d62b-159">Response</span></span>
<span data-ttu-id="9d62b-160">如果成功，此操作会在`200 OK`响应正文中返回响应代码和 Stream。</span><span class="sxs-lookup"><span data-stu-id="9d62b-160">If successful, this action returns a `200 OK` response code and a Stream in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9d62b-161">示例</span><span class="sxs-lookup"><span data-stu-id="9d62b-161">Example</span></span>

### <a name="request"></a><span data-ttu-id="9d62b-162">请求</span><span class="sxs-lookup"><span data-stu-id="9d62b-162">Request</span></span>
<span data-ttu-id="9d62b-163">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="9d62b-163">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/reports/getPolicyNonComplianceReport

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

### <a name="response"></a><span data-ttu-id="9d62b-164">响应</span><span class="sxs-lookup"><span data-stu-id="9d62b-164">Response</span></span>
<span data-ttu-id="9d62b-p102">下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="9d62b-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 54

{
  "value": "<Unknown Primitive Type Edm.Stream>"
}
```





