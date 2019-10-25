---
title: 更新 deviceManagementReports
description: 更新 deviceManagementReports 对象的属性。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 034f8a6c67da7a00f1e23ad86d2849a2e38de8bb
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2019
ms.locfileid: "37537203"
---
# <a name="update-devicemanagementreports"></a><span data-ttu-id="c1671-103">更新 deviceManagementReports</span><span class="sxs-lookup"><span data-stu-id="c1671-103">Update deviceManagementReports</span></span>

> <span data-ttu-id="c1671-104">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="c1671-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="c1671-105">**注意：** 适用于 Intune 的 Microsoft Graph API 需要租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="c1671-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="c1671-106">更新[deviceManagementReports](../resources/intune-reporting-devicemanagementreports.md)对象的属性。</span><span class="sxs-lookup"><span data-stu-id="c1671-106">Update the properties of a [deviceManagementReports](../resources/intune-reporting-devicemanagementreports.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c1671-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="c1671-107">Prerequisites</span></span>
<span data-ttu-id="c1671-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="c1671-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c1671-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="c1671-110">Permission type</span></span>|<span data-ttu-id="c1671-111">权限（从最高特权到最低特权）</span><span class="sxs-lookup"><span data-stu-id="c1671-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c1671-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="c1671-112">Delegated (work or school account)</span></span>|<span data-ttu-id="c1671-113">Devicemanagementconfiguration.readwrite.all，Devicemanagementapps.readwrite.all，all，Devicemanagementmanageddevices.readwrite.all，All</span><span class="sxs-lookup"><span data-stu-id="c1671-113">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementApps.ReadWrite.All, DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="c1671-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="c1671-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c1671-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="c1671-115">Not supported.</span></span>|
|<span data-ttu-id="c1671-116">应用程序</span><span class="sxs-lookup"><span data-stu-id="c1671-116">Application</span></span>|<span data-ttu-id="c1671-117">Devicemanagementconfiguration.readwrite.all，Devicemanagementapps.readwrite.all，all，Devicemanagementmanageddevices.readwrite.all，All</span><span class="sxs-lookup"><span data-stu-id="c1671-117">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementApps.ReadWrite.All, DeviceManagementManagedDevices.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="c1671-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="c1671-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/reports
```

## <a name="request-headers"></a><span data-ttu-id="c1671-119">请求标头</span><span class="sxs-lookup"><span data-stu-id="c1671-119">Request headers</span></span>
|<span data-ttu-id="c1671-120">标头</span><span class="sxs-lookup"><span data-stu-id="c1671-120">Header</span></span>|<span data-ttu-id="c1671-121">值</span><span class="sxs-lookup"><span data-stu-id="c1671-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c1671-122">授权</span><span class="sxs-lookup"><span data-stu-id="c1671-122">Authorization</span></span>|<span data-ttu-id="c1671-123">Bearer &lt;token&gt;。必需。</span><span class="sxs-lookup"><span data-stu-id="c1671-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c1671-124">接受</span><span class="sxs-lookup"><span data-stu-id="c1671-124">Accept</span></span>|<span data-ttu-id="c1671-125">application/json</span><span class="sxs-lookup"><span data-stu-id="c1671-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c1671-126">请求正文</span><span class="sxs-lookup"><span data-stu-id="c1671-126">Request body</span></span>
<span data-ttu-id="c1671-127">在请求正文中，提供[deviceManagementReports](../resources/intune-reporting-devicemanagementreports.md)对象的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="c1671-127">In the request body, supply a JSON representation for the [deviceManagementReports](../resources/intune-reporting-devicemanagementreports.md) object.</span></span>

<span data-ttu-id="c1671-128">下表显示创建[deviceManagementReports](../resources/intune-reporting-devicemanagementreports.md)时所需的属性。</span><span class="sxs-lookup"><span data-stu-id="c1671-128">The following table shows the properties that are required when you create the [deviceManagementReports](../resources/intune-reporting-devicemanagementreports.md).</span></span>

|<span data-ttu-id="c1671-129">属性</span><span class="sxs-lookup"><span data-stu-id="c1671-129">Property</span></span>|<span data-ttu-id="c1671-130">类型</span><span class="sxs-lookup"><span data-stu-id="c1671-130">Type</span></span>|<span data-ttu-id="c1671-131">说明</span><span class="sxs-lookup"><span data-stu-id="c1671-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c1671-132">id</span><span class="sxs-lookup"><span data-stu-id="c1671-132">id</span></span>|<span data-ttu-id="c1671-133">字符串</span><span class="sxs-lookup"><span data-stu-id="c1671-133">String</span></span>|<span data-ttu-id="c1671-134">此实体的唯一标识符</span><span class="sxs-lookup"><span data-stu-id="c1671-134">Unique identifier for this entity</span></span>|



## <a name="response"></a><span data-ttu-id="c1671-135">响应</span><span class="sxs-lookup"><span data-stu-id="c1671-135">Response</span></span>
<span data-ttu-id="c1671-136">如果成功，此方法在响应`200 OK`正文中返回响应代码和更新的[deviceManagementReports](../resources/intune-reporting-devicemanagementreports.md)对象。</span><span class="sxs-lookup"><span data-stu-id="c1671-136">If successful, this method returns a `200 OK` response code and an updated [deviceManagementReports](../resources/intune-reporting-devicemanagementreports.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c1671-137">示例</span><span class="sxs-lookup"><span data-stu-id="c1671-137">Example</span></span>

### <a name="request"></a><span data-ttu-id="c1671-138">请求</span><span class="sxs-lookup"><span data-stu-id="c1671-138">Request</span></span>
<span data-ttu-id="c1671-139">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="c1671-139">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/reports
Content-type: application/json
Content-length: 65

{
  "@odata.type": "#microsoft.graph.deviceManagementReports"
}
```

### <a name="response"></a><span data-ttu-id="c1671-140">响应</span><span class="sxs-lookup"><span data-stu-id="c1671-140">Response</span></span>
<span data-ttu-id="c1671-p102">下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="c1671-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 114

{
  "@odata.type": "#microsoft.graph.deviceManagementReports",
  "id": "d6a697d3-97d3-d6a6-d397-a6d6d397a6d6"
}
```





