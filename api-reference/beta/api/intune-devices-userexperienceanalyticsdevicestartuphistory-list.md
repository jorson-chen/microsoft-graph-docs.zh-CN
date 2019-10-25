---
title: 列出 userExperienceAnalyticsDeviceStartupHistories
description: 列出 userExperienceAnalyticsDeviceStartupHistory 对象的属性和关系。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 3a84fc72dc80058b0e11468d7ac2ab201cde5a98
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2019
ms.locfileid: "37529156"
---
# <a name="list-userexperienceanalyticsdevicestartuphistories"></a><span data-ttu-id="519e3-103">列出 userExperienceAnalyticsDeviceStartupHistories</span><span class="sxs-lookup"><span data-stu-id="519e3-103">List userExperienceAnalyticsDeviceStartupHistories</span></span>

> <span data-ttu-id="519e3-104">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="519e3-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="519e3-105">**注意：** 适用于 Intune 的 Microsoft Graph API 需要租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="519e3-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="519e3-106">列出[userExperienceAnalyticsDeviceStartupHistory](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md)对象的属性和关系。</span><span class="sxs-lookup"><span data-stu-id="519e3-106">List properties and relationships of the [userExperienceAnalyticsDeviceStartupHistory](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md) objects.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="519e3-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="519e3-107">Prerequisites</span></span>
<span data-ttu-id="519e3-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="519e3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="519e3-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="519e3-110">Permission type</span></span>|<span data-ttu-id="519e3-111">权限（从最高特权到最低特权）</span><span class="sxs-lookup"><span data-stu-id="519e3-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="519e3-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="519e3-112">Delegated (work or school account)</span></span>|<span data-ttu-id="519e3-113">DeviceManagementManagedDevices.ReadWrite.All、DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="519e3-113">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="519e3-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="519e3-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="519e3-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="519e3-115">Not supported.</span></span>|
|<span data-ttu-id="519e3-116">应用程序</span><span class="sxs-lookup"><span data-stu-id="519e3-116">Application</span></span>|<span data-ttu-id="519e3-117">DeviceManagementManagedDevices.ReadWrite.All、DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="519e3-117">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="519e3-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="519e3-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/userExperienceAnalyticsDeviceStartupHistory
```

## <a name="request-headers"></a><span data-ttu-id="519e3-119">请求标头</span><span class="sxs-lookup"><span data-stu-id="519e3-119">Request headers</span></span>
|<span data-ttu-id="519e3-120">标头</span><span class="sxs-lookup"><span data-stu-id="519e3-120">Header</span></span>|<span data-ttu-id="519e3-121">值</span><span class="sxs-lookup"><span data-stu-id="519e3-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="519e3-122">授权</span><span class="sxs-lookup"><span data-stu-id="519e3-122">Authorization</span></span>|<span data-ttu-id="519e3-123">Bearer &lt;token&gt;。必需。</span><span class="sxs-lookup"><span data-stu-id="519e3-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="519e3-124">接受</span><span class="sxs-lookup"><span data-stu-id="519e3-124">Accept</span></span>|<span data-ttu-id="519e3-125">application/json</span><span class="sxs-lookup"><span data-stu-id="519e3-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="519e3-126">请求正文</span><span class="sxs-lookup"><span data-stu-id="519e3-126">Request body</span></span>
<span data-ttu-id="519e3-127">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="519e3-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="519e3-128">响应</span><span class="sxs-lookup"><span data-stu-id="519e3-128">Response</span></span>
<span data-ttu-id="519e3-129">如果成功，此方法在响应`200 OK`正文中返回响应代码和[userExperienceAnalyticsDeviceStartupHistory](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md)对象集合。</span><span class="sxs-lookup"><span data-stu-id="519e3-129">If successful, this method returns a `200 OK` response code and a collection of [userExperienceAnalyticsDeviceStartupHistory](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="519e3-130">示例</span><span class="sxs-lookup"><span data-stu-id="519e3-130">Example</span></span>

### <a name="request"></a><span data-ttu-id="519e3-131">请求</span><span class="sxs-lookup"><span data-stu-id="519e3-131">Request</span></span>
<span data-ttu-id="519e3-132">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="519e3-132">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/userExperienceAnalyticsDeviceStartupHistory
```

### <a name="response"></a><span data-ttu-id="519e3-133">响应</span><span class="sxs-lookup"><span data-stu-id="519e3-133">Response</span></span>
<span data-ttu-id="519e3-p102">下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="519e3-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 537

{
  "value": [
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
  ]
}
```





