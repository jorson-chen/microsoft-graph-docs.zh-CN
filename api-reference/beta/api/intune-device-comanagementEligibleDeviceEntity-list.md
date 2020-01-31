---
title: 列出 comanagementEligibleDeviceEntity
description: 列出 comanagementEligibleDeviceEntity 对象的属性和关系。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 39d7a92c5914107cdd5ecfebb9b4b7948bc8b8b0
ms.sourcegitcommit: b12904a27b6d0e197f562aca0dac5e74cd7bd3a1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2020
ms.locfileid: "41636089"
---
# <a name="list-comanagementeligibledeviceentity"></a><span data-ttu-id="90f92-103">列出 comanagementEligibleDeviceEntity</span><span class="sxs-lookup"><span data-stu-id="90f92-103">List comanagementEligibleDeviceEntity</span></span>

> <span data-ttu-id="90f92-104">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="90f92-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="90f92-105">**注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="90f92-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="90f92-106">列出 comanagementEligibleDeviceEntity 对象的属性和关系。</span><span class="sxs-lookup"><span data-stu-id="90f92-106">List properties and relationships of the comanagementEligibleDeviceEntity objects.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="90f92-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="90f92-107">Prerequisites</span></span>
<span data-ttu-id="90f92-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="90f92-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="90f92-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="90f92-110">Permission type</span></span>|<span data-ttu-id="90f92-111">权限（从最高特权到最低特权）</span><span class="sxs-lookup"><span data-stu-id="90f92-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="90f92-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="90f92-112">Delegated (work or school account)</span></span>|<span data-ttu-id="90f92-113">DeviceManagementManagedDevices.ReadWrite.All、DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="90f92-113">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="90f92-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="90f92-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="90f92-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="90f92-115">Not supported.</span></span>|
|<span data-ttu-id="90f92-116">应用程序</span><span class="sxs-lookup"><span data-stu-id="90f92-116">Application</span></span>|<span data-ttu-id="90f92-117">DeviceManagementManagedDevices.ReadWrite.All、DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="90f92-117">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="90f92-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="90f92-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/comanagementEligibleReports
```

## <a name="request-headers"></a><span data-ttu-id="90f92-119">请求标头</span><span class="sxs-lookup"><span data-stu-id="90f92-119">Request headers</span></span>
|<span data-ttu-id="90f92-120">标头</span><span class="sxs-lookup"><span data-stu-id="90f92-120">Header</span></span>|<span data-ttu-id="90f92-121">值</span><span class="sxs-lookup"><span data-stu-id="90f92-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="90f92-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="90f92-122">Authorization</span></span>|<span data-ttu-id="90f92-123">Bearer &lt;token&gt;。必需。</span><span class="sxs-lookup"><span data-stu-id="90f92-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="90f92-124">接受</span><span class="sxs-lookup"><span data-stu-id="90f92-124">Accept</span></span>|<span data-ttu-id="90f92-125">application/json</span><span class="sxs-lookup"><span data-stu-id="90f92-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="90f92-126">请求正文</span><span class="sxs-lookup"><span data-stu-id="90f92-126">Request body</span></span>
<span data-ttu-id="90f92-127">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="90f92-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="90f92-128">响应</span><span class="sxs-lookup"><span data-stu-id="90f92-128">Response</span></span>
<span data-ttu-id="90f92-129">如果成功，此方法在响应`200 OK`正文中返回响应代码和 comanagementEligibleDeviceEntity 对象集合。</span><span class="sxs-lookup"><span data-stu-id="90f92-129">If successful, this method returns a `200 OK` response code and a collection of comanagementEligibleDeviceEntity objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="90f92-130">示例</span><span class="sxs-lookup"><span data-stu-id="90f92-130">Example</span></span>

### <a name="request"></a><span data-ttu-id="90f92-131">请求</span><span class="sxs-lookup"><span data-stu-id="90f92-131">Request</span></span>
<span data-ttu-id="90f92-132">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="90f92-132">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/comanagementEligibleReports
```

### <a name="response"></a><span data-ttu-id="90f92-133">响应</span><span class="sxs-lookup"><span data-stu-id="90f92-133">Response</span></span>
<span data-ttu-id="90f92-p102">下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="90f92-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1303

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.comanagementEligibleDeviceEntity",
      "id": "659554f2-54f2-6595-f254-9565f2549565",
      "deviceId": "Device Id value",
      "deviceName": "Device Name value",
      "deviceType": "Device Type value",
      "clientRegistrationStatus": "Client Registration Status value",
      "ownerType": "Owner Type value",
      "managementAgents": "Management Agent value",
      "managementState": "Management State value",
      "referenceId": "Reference Id value",
      "mdmStatus": "MDM Status value",
      "osVersion": "OS Version value",
      "serialNumber": "Serial Number value",
      "manufacturer": "Manufacture value",
      "model": "Model value",
      "osDescription": "OS Description value",
      "entitySource": 1024,
      "userId": "User Id value",
      "upn": "UPN value",
      "userEmail": "User Email value",
      "userName": "User name value",
      "coManageEligibleStatus": "CO Manage Eligible Status value"
    }
  ]
}
```


