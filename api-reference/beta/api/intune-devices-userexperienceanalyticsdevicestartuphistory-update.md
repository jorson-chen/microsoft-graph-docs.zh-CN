---
title: 更新 userExperienceAnalyticsDeviceStartupHistory
description: 更新 userExperienceAnalyticsDeviceStartupHistory 对象的属性。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: acf87e008b7e8837da1bd003f183a23c2307d08a
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2019
ms.locfileid: "37529142"
---
# <a name="update-userexperienceanalyticsdevicestartuphistory"></a><span data-ttu-id="8476d-103">更新 userExperienceAnalyticsDeviceStartupHistory</span><span class="sxs-lookup"><span data-stu-id="8476d-103">Update userExperienceAnalyticsDeviceStartupHistory</span></span>

> <span data-ttu-id="8476d-104">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="8476d-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="8476d-105">**注意：** 适用于 Intune 的 Microsoft Graph API 需要租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="8476d-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="8476d-106">更新[userExperienceAnalyticsDeviceStartupHistory](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md)对象的属性。</span><span class="sxs-lookup"><span data-stu-id="8476d-106">Update the properties of a [userExperienceAnalyticsDeviceStartupHistory](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8476d-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="8476d-107">Prerequisites</span></span>
<span data-ttu-id="8476d-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="8476d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8476d-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="8476d-110">Permission type</span></span>|<span data-ttu-id="8476d-111">权限（从最高特权到最低特权）</span><span class="sxs-lookup"><span data-stu-id="8476d-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8476d-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="8476d-112">Delegated (work or school account)</span></span>|<span data-ttu-id="8476d-113">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8476d-113">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="8476d-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="8476d-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8476d-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="8476d-115">Not supported.</span></span>|
|<span data-ttu-id="8476d-116">应用程序</span><span class="sxs-lookup"><span data-stu-id="8476d-116">Application</span></span>|<span data-ttu-id="8476d-117">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8476d-117">DeviceManagementManagedDevices.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="8476d-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="8476d-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/userExperienceAnalyticsDeviceStartupHistory/{userExperienceAnalyticsDeviceStartupHistoryId}
```

## <a name="request-headers"></a><span data-ttu-id="8476d-119">请求标头</span><span class="sxs-lookup"><span data-stu-id="8476d-119">Request headers</span></span>
|<span data-ttu-id="8476d-120">标头</span><span class="sxs-lookup"><span data-stu-id="8476d-120">Header</span></span>|<span data-ttu-id="8476d-121">值</span><span class="sxs-lookup"><span data-stu-id="8476d-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8476d-122">授权</span><span class="sxs-lookup"><span data-stu-id="8476d-122">Authorization</span></span>|<span data-ttu-id="8476d-123">Bearer &lt;token&gt;。必需。</span><span class="sxs-lookup"><span data-stu-id="8476d-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8476d-124">接受</span><span class="sxs-lookup"><span data-stu-id="8476d-124">Accept</span></span>|<span data-ttu-id="8476d-125">application/json</span><span class="sxs-lookup"><span data-stu-id="8476d-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8476d-126">请求正文</span><span class="sxs-lookup"><span data-stu-id="8476d-126">Request body</span></span>
<span data-ttu-id="8476d-127">在请求正文中，提供[userExperienceAnalyticsDeviceStartupHistory](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md)对象的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="8476d-127">In the request body, supply a JSON representation for the [userExperienceAnalyticsDeviceStartupHistory](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md) object.</span></span>

<span data-ttu-id="8476d-128">下表显示创建[userExperienceAnalyticsDeviceStartupHistory](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md)时所需的属性。</span><span class="sxs-lookup"><span data-stu-id="8476d-128">The following table shows the properties that are required when you create the [userExperienceAnalyticsDeviceStartupHistory](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md).</span></span>

|<span data-ttu-id="8476d-129">属性</span><span class="sxs-lookup"><span data-stu-id="8476d-129">Property</span></span>|<span data-ttu-id="8476d-130">类型</span><span class="sxs-lookup"><span data-stu-id="8476d-130">Type</span></span>|<span data-ttu-id="8476d-131">说明</span><span class="sxs-lookup"><span data-stu-id="8476d-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8476d-132">id</span><span class="sxs-lookup"><span data-stu-id="8476d-132">id</span></span>|<span data-ttu-id="8476d-133">字符串</span><span class="sxs-lookup"><span data-stu-id="8476d-133">String</span></span>|<span data-ttu-id="8476d-134">User experience analytics 设备启动历史记录的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="8476d-134">The unique identifier of the user experience analytics device startup history.</span></span>|
|<span data-ttu-id="8476d-135">deviceId</span><span class="sxs-lookup"><span data-stu-id="8476d-135">deviceId</span></span>|<span data-ttu-id="8476d-136">String</span><span class="sxs-lookup"><span data-stu-id="8476d-136">String</span></span>|<span data-ttu-id="8476d-137">User experience analytics 设备 id。</span><span class="sxs-lookup"><span data-stu-id="8476d-137">The user experience analytics device id.</span></span>|
|<span data-ttu-id="8476d-138">startTime</span><span class="sxs-lookup"><span data-stu-id="8476d-138">startTime</span></span>|<span data-ttu-id="8476d-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8476d-139">DateTimeOffset</span></span>|<span data-ttu-id="8476d-140">用户体验分析设备启动开始时间。</span><span class="sxs-lookup"><span data-stu-id="8476d-140">The user experience analytics device boot start time.</span></span>|
|<span data-ttu-id="8476d-141">coreBootTimeInMs</span><span class="sxs-lookup"><span data-stu-id="8476d-141">coreBootTimeInMs</span></span>|<span data-ttu-id="8476d-142">Int32</span><span class="sxs-lookup"><span data-stu-id="8476d-142">Int32</span></span>|<span data-ttu-id="8476d-143">User experience analytics device core boot time （以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="8476d-143">The user experience analytics device core boot time in milliseconds.</span></span>|
|<span data-ttu-id="8476d-144">groupPolicyBootTimeInMs</span><span class="sxs-lookup"><span data-stu-id="8476d-144">groupPolicyBootTimeInMs</span></span>|<span data-ttu-id="8476d-145">Int32</span><span class="sxs-lookup"><span data-stu-id="8476d-145">Int32</span></span>|<span data-ttu-id="8476d-146">User experience analytics Device group policy boot time （以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="8476d-146">The User experience analytics Device group policy boot time in milliseconds.</span></span>|
|<span data-ttu-id="8476d-147">featureUpdateBootTimeInMs</span><span class="sxs-lookup"><span data-stu-id="8476d-147">featureUpdateBootTimeInMs</span></span>|<span data-ttu-id="8476d-148">Int32</span><span class="sxs-lookup"><span data-stu-id="8476d-148">Int32</span></span>|<span data-ttu-id="8476d-149">User experience analytics 设备功能更新时间（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="8476d-149">The user experience analytics device feature update time in milliseconds.</span></span>|
|<span data-ttu-id="8476d-150">totalBootTimeInMs</span><span class="sxs-lookup"><span data-stu-id="8476d-150">totalBootTimeInMs</span></span>|<span data-ttu-id="8476d-151">Int32</span><span class="sxs-lookup"><span data-stu-id="8476d-151">Int32</span></span>|<span data-ttu-id="8476d-152">User experience analytics 设备总启动时间（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="8476d-152">The user experience analytics device total boot time in milliseconds.</span></span>|
|<span data-ttu-id="8476d-153">groupPolicyLoginTimeInMs</span><span class="sxs-lookup"><span data-stu-id="8476d-153">groupPolicyLoginTimeInMs</span></span>|<span data-ttu-id="8476d-154">Int32</span><span class="sxs-lookup"><span data-stu-id="8476d-154">Int32</span></span>|<span data-ttu-id="8476d-155">User experience analytics 设备组策略登录时间（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="8476d-155">The User experience analytics Device group policy login time in milliseconds.</span></span>|
|<span data-ttu-id="8476d-156">coreLoginTimeInMs</span><span class="sxs-lookup"><span data-stu-id="8476d-156">coreLoginTimeInMs</span></span>|<span data-ttu-id="8476d-157">Int32</span><span class="sxs-lookup"><span data-stu-id="8476d-157">Int32</span></span>|<span data-ttu-id="8476d-158">User experience analytics device core login time （以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="8476d-158">The user experience analytics device core login time in milliseconds.</span></span>|
|<span data-ttu-id="8476d-159">totalLoginTimeInMs</span><span class="sxs-lookup"><span data-stu-id="8476d-159">totalLoginTimeInMs</span></span>|<span data-ttu-id="8476d-160">Int32</span><span class="sxs-lookup"><span data-stu-id="8476d-160">Int32</span></span>|<span data-ttu-id="8476d-161">User experience analytics 设备总登录时间（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="8476d-161">The user experience analytics device total login time in milliseconds.</span></span>|
|<span data-ttu-id="8476d-162">isFirstLogin</span><span class="sxs-lookup"><span data-stu-id="8476d-162">isFirstLogin</span></span>|<span data-ttu-id="8476d-163">Boolean</span><span class="sxs-lookup"><span data-stu-id="8476d-163">Boolean</span></span>|<span data-ttu-id="8476d-164">User experience analytics 设备第一次登录。</span><span class="sxs-lookup"><span data-stu-id="8476d-164">The user experience analytics device first login.</span></span>|



## <a name="response"></a><span data-ttu-id="8476d-165">响应</span><span class="sxs-lookup"><span data-stu-id="8476d-165">Response</span></span>
<span data-ttu-id="8476d-166">如果成功，此方法在响应`200 OK`正文中返回响应代码和更新的[userExperienceAnalyticsDeviceStartupHistory](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md)对象。</span><span class="sxs-lookup"><span data-stu-id="8476d-166">If successful, this method returns a `200 OK` response code and an updated [userExperienceAnalyticsDeviceStartupHistory](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8476d-167">示例</span><span class="sxs-lookup"><span data-stu-id="8476d-167">Example</span></span>

### <a name="request"></a><span data-ttu-id="8476d-168">请求</span><span class="sxs-lookup"><span data-stu-id="8476d-168">Request</span></span>
<span data-ttu-id="8476d-169">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="8476d-169">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/userExperienceAnalyticsDeviceStartupHistory/{userExperienceAnalyticsDeviceStartupHistoryId}
Content-type: application/json
Content-length: 407

{
  "@odata.type": "#microsoft.graph.userExperienceAnalyticsDeviceStartupHistory",
  "deviceId": "Device Id value",
  "startTime": "2017-01-01T00:03:29.2730865-08:00",
  "coreBootTimeInMs": 0,
  "groupPolicyBootTimeInMs": 7,
  "featureUpdateBootTimeInMs": 9,
  "totalBootTimeInMs": 1,
  "groupPolicyLoginTimeInMs": 8,
  "coreLoginTimeInMs": 1,
  "totalLoginTimeInMs": 2,
  "isFirstLogin": true
}
```

### <a name="response"></a><span data-ttu-id="8476d-170">响应</span><span class="sxs-lookup"><span data-stu-id="8476d-170">Response</span></span>
<span data-ttu-id="8476d-p102">下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="8476d-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 456

{
  "@odata.type": "#microsoft.graph.userExperienceAnalyticsDeviceStartupHistory",
  "id": "13357123-7123-1335-2371-351323713513",
  "deviceId": "Device Id value",
  "startTime": "2017-01-01T00:03:29.2730865-08:00",
  "coreBootTimeInMs": 0,
  "groupPolicyBootTimeInMs": 7,
  "featureUpdateBootTimeInMs": 9,
  "totalBootTimeInMs": 1,
  "groupPolicyLoginTimeInMs": 8,
  "coreLoginTimeInMs": 1,
  "totalLoginTimeInMs": 2,
  "isFirstLogin": true
}
```





