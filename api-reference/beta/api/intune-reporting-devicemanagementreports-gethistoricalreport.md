---
title: getHistoricalReport 操作
description: 尚未记录
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 9fc8d182c1b5860017f3b91e47693c0b566ff9e2
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2019
ms.locfileid: "37537224"
---
# <a name="gethistoricalreport-action"></a><span data-ttu-id="04840-103">getHistoricalReport 操作</span><span class="sxs-lookup"><span data-stu-id="04840-103">getHistoricalReport action</span></span>

> <span data-ttu-id="04840-104">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="04840-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="04840-105">**注意：** 适用于 Intune 的 Microsoft Graph API 需要租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="04840-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="04840-106">尚未记录</span><span class="sxs-lookup"><span data-stu-id="04840-106">Not yet documented</span></span>

## <a name="prerequisites"></a><span data-ttu-id="04840-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="04840-107">Prerequisites</span></span>
<span data-ttu-id="04840-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="04840-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="04840-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="04840-110">Permission type</span></span>|<span data-ttu-id="04840-111">权限（从最高特权到最低特权）</span><span class="sxs-lookup"><span data-stu-id="04840-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="04840-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="04840-112">Delegated (work or school account)</span></span>|<span data-ttu-id="04840-113">Devicemanagementconfiguration.readwrite.all、Devicemanagementconfiguration.readwrite.all、Devicemanagementapps.readwrite.all、all、Devicemanagementapps.readwrite.all、all、Devicemanagementmanageddevices.readwrite.all、all、、all、Devicemanagementmanageddevices.readwrite.all</span><span class="sxs-lookup"><span data-stu-id="04840-113">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All, DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All, DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="04840-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="04840-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="04840-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="04840-115">Not supported.</span></span>|
|<span data-ttu-id="04840-116">应用程序</span><span class="sxs-lookup"><span data-stu-id="04840-116">Application</span></span>|<span data-ttu-id="04840-117">Devicemanagementconfiguration.readwrite.all、Devicemanagementconfiguration.readwrite.all、Devicemanagementapps.readwrite.all、all、Devicemanagementapps.readwrite.all、all、Devicemanagementmanageddevices.readwrite.all、all、、all、Devicemanagementmanageddevices.readwrite.all</span><span class="sxs-lookup"><span data-stu-id="04840-117">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All, DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All, DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="04840-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="04840-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/reports/getHistoricalReport
```

## <a name="request-headers"></a><span data-ttu-id="04840-119">请求标头</span><span class="sxs-lookup"><span data-stu-id="04840-119">Request headers</span></span>
|<span data-ttu-id="04840-120">标头</span><span class="sxs-lookup"><span data-stu-id="04840-120">Header</span></span>|<span data-ttu-id="04840-121">值</span><span class="sxs-lookup"><span data-stu-id="04840-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="04840-122">授权</span><span class="sxs-lookup"><span data-stu-id="04840-122">Authorization</span></span>|<span data-ttu-id="04840-123">Bearer &lt;token&gt;。必需。</span><span class="sxs-lookup"><span data-stu-id="04840-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="04840-124">接受</span><span class="sxs-lookup"><span data-stu-id="04840-124">Accept</span></span>|<span data-ttu-id="04840-125">application/json</span><span class="sxs-lookup"><span data-stu-id="04840-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="04840-126">请求正文</span><span class="sxs-lookup"><span data-stu-id="04840-126">Request body</span></span>
<span data-ttu-id="04840-127">在请求正文中，提供参数的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="04840-127">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="04840-128">下表显示了可用于此操作的参数。</span><span class="sxs-lookup"><span data-stu-id="04840-128">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="04840-129">属性</span><span class="sxs-lookup"><span data-stu-id="04840-129">Property</span></span>|<span data-ttu-id="04840-130">类型</span><span class="sxs-lookup"><span data-stu-id="04840-130">Type</span></span>|<span data-ttu-id="04840-131">说明</span><span class="sxs-lookup"><span data-stu-id="04840-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="04840-132">name</span><span class="sxs-lookup"><span data-stu-id="04840-132">name</span></span>|<span data-ttu-id="04840-133">字符串</span><span class="sxs-lookup"><span data-stu-id="04840-133">String</span></span>|<span data-ttu-id="04840-134">尚未记录</span><span class="sxs-lookup"><span data-stu-id="04840-134">Not yet documented</span></span>|
|<span data-ttu-id="04840-135">select</span><span class="sxs-lookup"><span data-stu-id="04840-135">select</span></span>|<span data-ttu-id="04840-136">String collection</span><span class="sxs-lookup"><span data-stu-id="04840-136">String collection</span></span>|<span data-ttu-id="04840-137">尚未记录</span><span class="sxs-lookup"><span data-stu-id="04840-137">Not yet documented</span></span>|
|<span data-ttu-id="04840-138">search</span><span class="sxs-lookup"><span data-stu-id="04840-138">search</span></span>|<span data-ttu-id="04840-139">String</span><span class="sxs-lookup"><span data-stu-id="04840-139">String</span></span>|<span data-ttu-id="04840-140">尚未记录</span><span class="sxs-lookup"><span data-stu-id="04840-140">Not yet documented</span></span>|
|<span data-ttu-id="04840-141">groupBy</span><span class="sxs-lookup"><span data-stu-id="04840-141">groupBy</span></span>|<span data-ttu-id="04840-142">String collection</span><span class="sxs-lookup"><span data-stu-id="04840-142">String collection</span></span>|<span data-ttu-id="04840-143">尚未记录</span><span class="sxs-lookup"><span data-stu-id="04840-143">Not yet documented</span></span>|
|<span data-ttu-id="04840-144">By</span><span class="sxs-lookup"><span data-stu-id="04840-144">orderBy</span></span>|<span data-ttu-id="04840-145">String collection</span><span class="sxs-lookup"><span data-stu-id="04840-145">String collection</span></span>|<span data-ttu-id="04840-146">尚未记录</span><span class="sxs-lookup"><span data-stu-id="04840-146">Not yet documented</span></span>|
|<span data-ttu-id="04840-147">skip</span><span class="sxs-lookup"><span data-stu-id="04840-147">skip</span></span>|<span data-ttu-id="04840-148">Int32</span><span class="sxs-lookup"><span data-stu-id="04840-148">Int32</span></span>|<span data-ttu-id="04840-149">尚未记录</span><span class="sxs-lookup"><span data-stu-id="04840-149">Not yet documented</span></span>|
|<span data-ttu-id="04840-150">top</span><span class="sxs-lookup"><span data-stu-id="04840-150">top</span></span>|<span data-ttu-id="04840-151">Int32</span><span class="sxs-lookup"><span data-stu-id="04840-151">Int32</span></span>|<span data-ttu-id="04840-152">尚未记录</span><span class="sxs-lookup"><span data-stu-id="04840-152">Not yet documented</span></span>|
|<span data-ttu-id="04840-153">filter</span><span class="sxs-lookup"><span data-stu-id="04840-153">filter</span></span>|<span data-ttu-id="04840-154">String</span><span class="sxs-lookup"><span data-stu-id="04840-154">String</span></span>|<span data-ttu-id="04840-155">尚未记录</span><span class="sxs-lookup"><span data-stu-id="04840-155">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="04840-156">响应</span><span class="sxs-lookup"><span data-stu-id="04840-156">Response</span></span>
<span data-ttu-id="04840-157">如果成功，此操作会在`200 OK`响应正文中返回响应代码和 Stream。</span><span class="sxs-lookup"><span data-stu-id="04840-157">If successful, this action returns a `200 OK` response code and a Stream in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="04840-158">示例</span><span class="sxs-lookup"><span data-stu-id="04840-158">Example</span></span>

### <a name="request"></a><span data-ttu-id="04840-159">请求</span><span class="sxs-lookup"><span data-stu-id="04840-159">Request</span></span>
<span data-ttu-id="04840-160">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="04840-160">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/reports/getHistoricalReport

Content-type: application/json
Content-length: 242

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
  "filter": "Filter value"
}
```

### <a name="response"></a><span data-ttu-id="04840-161">响应</span><span class="sxs-lookup"><span data-stu-id="04840-161">Response</span></span>
<span data-ttu-id="04840-p102">下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="04840-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 54

{
  "value": "<Unknown Primitive Type Edm.Stream>"
}
```





