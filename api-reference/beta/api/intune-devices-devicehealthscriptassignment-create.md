---
title: 创建 deviceHealthScriptAssignment
description: 创建新的 deviceHealthScriptAssignment 对象。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: e088f2802c68f0d07cc44529e42a70b4f5936ee2
ms.sourcegitcommit: 5b1fad41067629d0e9f87746328664bb248f754f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/09/2019
ms.locfileid: "38087599"
---
# <a name="create-devicehealthscriptassignment"></a><span data-ttu-id="c8a28-103">创建 deviceHealthScriptAssignment</span><span class="sxs-lookup"><span data-stu-id="c8a28-103">Create deviceHealthScriptAssignment</span></span>

> <span data-ttu-id="c8a28-104">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="c8a28-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="c8a28-105">**注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="c8a28-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="c8a28-106">创建新的[deviceHealthScriptAssignment](../resources/intune-devices-devicehealthscriptassignment.md)对象。</span><span class="sxs-lookup"><span data-stu-id="c8a28-106">Create a new [deviceHealthScriptAssignment](../resources/intune-devices-devicehealthscriptassignment.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c8a28-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="c8a28-107">Prerequisites</span></span>
<span data-ttu-id="c8a28-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="c8a28-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c8a28-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="c8a28-110">Permission type</span></span>|<span data-ttu-id="c8a28-111">权限（从最高特权到最低特权）</span><span class="sxs-lookup"><span data-stu-id="c8a28-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c8a28-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="c8a28-112">Delegated (work or school account)</span></span>|<span data-ttu-id="c8a28-113">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c8a28-113">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="c8a28-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="c8a28-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c8a28-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="c8a28-115">Not supported.</span></span>|
|<span data-ttu-id="c8a28-116">应用程序</span><span class="sxs-lookup"><span data-stu-id="c8a28-116">Application</span></span>|<span data-ttu-id="c8a28-117">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c8a28-117">DeviceManagementManagedDevices.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="c8a28-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="c8a28-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceHealthScripts/{deviceHealthScriptId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="c8a28-119">请求标头</span><span class="sxs-lookup"><span data-stu-id="c8a28-119">Request headers</span></span>
|<span data-ttu-id="c8a28-120">标头</span><span class="sxs-lookup"><span data-stu-id="c8a28-120">Header</span></span>|<span data-ttu-id="c8a28-121">值</span><span class="sxs-lookup"><span data-stu-id="c8a28-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c8a28-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="c8a28-122">Authorization</span></span>|<span data-ttu-id="c8a28-123">Bearer &lt;token&gt;。必需。</span><span class="sxs-lookup"><span data-stu-id="c8a28-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c8a28-124">接受</span><span class="sxs-lookup"><span data-stu-id="c8a28-124">Accept</span></span>|<span data-ttu-id="c8a28-125">application/json</span><span class="sxs-lookup"><span data-stu-id="c8a28-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c8a28-126">请求正文</span><span class="sxs-lookup"><span data-stu-id="c8a28-126">Request body</span></span>
<span data-ttu-id="c8a28-127">在请求正文中，提供 deviceHealthScriptAssignment 对象的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="c8a28-127">In the request body, supply a JSON representation for the deviceHealthScriptAssignment object.</span></span>

<span data-ttu-id="c8a28-128">下表显示创建 deviceHealthScriptAssignment 时所需的属性。</span><span class="sxs-lookup"><span data-stu-id="c8a28-128">The following table shows the properties that are required when you create the deviceHealthScriptAssignment.</span></span>

|<span data-ttu-id="c8a28-129">属性</span><span class="sxs-lookup"><span data-stu-id="c8a28-129">Property</span></span>|<span data-ttu-id="c8a28-130">类型</span><span class="sxs-lookup"><span data-stu-id="c8a28-130">Type</span></span>|<span data-ttu-id="c8a28-131">说明</span><span class="sxs-lookup"><span data-stu-id="c8a28-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c8a28-132">id</span><span class="sxs-lookup"><span data-stu-id="c8a28-132">id</span></span>|<span data-ttu-id="c8a28-133">String</span><span class="sxs-lookup"><span data-stu-id="c8a28-133">String</span></span>|<span data-ttu-id="c8a28-134">设备运行状况脚本分配实体的键。</span><span class="sxs-lookup"><span data-stu-id="c8a28-134">Key of the device health script assignment entity.</span></span> <span data-ttu-id="c8a28-135">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="c8a28-135">This property is read-only.</span></span>|
|<span data-ttu-id="c8a28-136">target</span><span class="sxs-lookup"><span data-stu-id="c8a28-136">target</span></span>|[<span data-ttu-id="c8a28-137">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="c8a28-137">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="c8a28-138">将脚本设定为的 Azure Active Directory 组</span><span class="sxs-lookup"><span data-stu-id="c8a28-138">The Azure Active Directory group we are targeting the script to</span></span>|
|<span data-ttu-id="c8a28-139">runRemediationScript</span><span class="sxs-lookup"><span data-stu-id="c8a28-139">runRemediationScript</span></span>|<span data-ttu-id="c8a28-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="c8a28-140">Boolean</span></span>|<span data-ttu-id="c8a28-141">确定是只运行检测脚本还是运行两个检测脚本和修正脚本</span><span class="sxs-lookup"><span data-stu-id="c8a28-141">Determine whether we want to run detection script only or run both detection script and remediation script</span></span>|
|<span data-ttu-id="c8a28-142">runSchedule</span><span class="sxs-lookup"><span data-stu-id="c8a28-142">runSchedule</span></span>|[<span data-ttu-id="c8a28-143">runSchedule</span><span class="sxs-lookup"><span data-stu-id="c8a28-143">runSchedule</span></span>](../resources/intune-devices-runschedule.md)|<span data-ttu-id="c8a28-144">目标组的脚本运行计划</span><span class="sxs-lookup"><span data-stu-id="c8a28-144">Script run schedule for the target group</span></span>|



## <a name="response"></a><span data-ttu-id="c8a28-145">响应</span><span class="sxs-lookup"><span data-stu-id="c8a28-145">Response</span></span>
<span data-ttu-id="c8a28-146">如果成功，此方法在响应`201 Created`正文中返回响应代码和[deviceHealthScriptAssignment](../resources/intune-devices-devicehealthscriptassignment.md)对象。</span><span class="sxs-lookup"><span data-stu-id="c8a28-146">If successful, this method returns a `201 Created` response code and a [deviceHealthScriptAssignment](../resources/intune-devices-devicehealthscriptassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c8a28-147">示例</span><span class="sxs-lookup"><span data-stu-id="c8a28-147">Example</span></span>

### <a name="request"></a><span data-ttu-id="c8a28-148">请求</span><span class="sxs-lookup"><span data-stu-id="c8a28-148">Request</span></span>
<span data-ttu-id="c8a28-149">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="c8a28-149">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceHealthScripts/{deviceHealthScriptId}/assignments
Content-type: application/json
Content-length: 277

{
  "@odata.type": "#microsoft.graph.deviceHealthScriptAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "runRemediationScript": true,
  "runSchedule": {
    "@odata.type": "microsoft.graph.runSchedule"
  }
}
```

### <a name="response"></a><span data-ttu-id="c8a28-150">响应</span><span class="sxs-lookup"><span data-stu-id="c8a28-150">Response</span></span>
<span data-ttu-id="c8a28-p103">下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="c8a28-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 326

{
  "@odata.type": "#microsoft.graph.deviceHealthScriptAssignment",
  "id": "c08c4eb1-4eb1-c08c-b14e-8cc0b14e8cc0",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "runRemediationScript": true,
  "runSchedule": {
    "@odata.type": "microsoft.graph.runSchedule"
  }
}
```





