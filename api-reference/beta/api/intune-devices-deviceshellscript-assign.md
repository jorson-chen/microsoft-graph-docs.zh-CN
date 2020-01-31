---
title: assign 操作
description: 尚未记录
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: c1a888271cfdd03d13101b7adaeff9295b61b44e
ms.sourcegitcommit: b12904a27b6d0e197f562aca0dac5e74cd7bd3a1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2020
ms.locfileid: "41636467"
---
# <a name="assign-action"></a><span data-ttu-id="46f46-103">分配操作</span><span class="sxs-lookup"><span data-stu-id="46f46-103">assign action</span></span>

> <span data-ttu-id="46f46-104">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="46f46-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="46f46-105">**注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="46f46-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="46f46-106">尚未记录</span><span class="sxs-lookup"><span data-stu-id="46f46-106">Not yet documented</span></span>

## <a name="prerequisites"></a><span data-ttu-id="46f46-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="46f46-107">Prerequisites</span></span>
<span data-ttu-id="46f46-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="46f46-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="46f46-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="46f46-110">Permission type</span></span>|<span data-ttu-id="46f46-111">权限（从最高特权到最低特权）</span><span class="sxs-lookup"><span data-stu-id="46f46-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="46f46-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="46f46-112">Delegated (work or school account)</span></span>|<span data-ttu-id="46f46-113">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="46f46-113">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="46f46-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="46f46-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="46f46-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="46f46-115">Not supported.</span></span>|
|<span data-ttu-id="46f46-116">应用程序</span><span class="sxs-lookup"><span data-stu-id="46f46-116">Application</span></span>|<span data-ttu-id="46f46-117">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="46f46-117">DeviceManagementManagedDevices.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="46f46-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="46f46-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceShellScripts/{deviceShellScriptId}/assign
```

## <a name="request-headers"></a><span data-ttu-id="46f46-119">请求标头</span><span class="sxs-lookup"><span data-stu-id="46f46-119">Request headers</span></span>
|<span data-ttu-id="46f46-120">标头</span><span class="sxs-lookup"><span data-stu-id="46f46-120">Header</span></span>|<span data-ttu-id="46f46-121">值</span><span class="sxs-lookup"><span data-stu-id="46f46-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="46f46-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="46f46-122">Authorization</span></span>|<span data-ttu-id="46f46-123">Bearer &lt;token&gt;。必需。</span><span class="sxs-lookup"><span data-stu-id="46f46-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="46f46-124">接受</span><span class="sxs-lookup"><span data-stu-id="46f46-124">Accept</span></span>|<span data-ttu-id="46f46-125">application/json</span><span class="sxs-lookup"><span data-stu-id="46f46-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="46f46-126">请求正文</span><span class="sxs-lookup"><span data-stu-id="46f46-126">Request body</span></span>
<span data-ttu-id="46f46-127">在请求正文中，提供参数的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="46f46-127">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="46f46-128">下表显示了可用于此操作的参数。</span><span class="sxs-lookup"><span data-stu-id="46f46-128">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="46f46-129">属性</span><span class="sxs-lookup"><span data-stu-id="46f46-129">Property</span></span>|<span data-ttu-id="46f46-130">类型</span><span class="sxs-lookup"><span data-stu-id="46f46-130">Type</span></span>|<span data-ttu-id="46f46-131">Description</span><span class="sxs-lookup"><span data-stu-id="46f46-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="46f46-132">deviceManagementScriptGroupAssignments</span><span class="sxs-lookup"><span data-stu-id="46f46-132">deviceManagementScriptGroupAssignments</span></span>|<span data-ttu-id="46f46-133">[deviceManagementScriptGroupAssignment](../resources/intune-devices-devicemanagementscriptgroupassignment.md)集合</span><span class="sxs-lookup"><span data-stu-id="46f46-133">[deviceManagementScriptGroupAssignment](../resources/intune-devices-devicemanagementscriptgroupassignment.md) collection</span></span>|<span data-ttu-id="46f46-134">尚未记录</span><span class="sxs-lookup"><span data-stu-id="46f46-134">Not yet documented</span></span>|
|<span data-ttu-id="46f46-135">deviceManagementScriptAssignments</span><span class="sxs-lookup"><span data-stu-id="46f46-135">deviceManagementScriptAssignments</span></span>|<span data-ttu-id="46f46-136">[deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)集合</span><span class="sxs-lookup"><span data-stu-id="46f46-136">[deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md) collection</span></span>|<span data-ttu-id="46f46-137">尚未记录</span><span class="sxs-lookup"><span data-stu-id="46f46-137">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="46f46-138">响应</span><span class="sxs-lookup"><span data-stu-id="46f46-138">Response</span></span>
<span data-ttu-id="46f46-139">如果成功，此操作返回 `204 No Content` 响应代码。</span><span class="sxs-lookup"><span data-stu-id="46f46-139">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="46f46-140">示例</span><span class="sxs-lookup"><span data-stu-id="46f46-140">Example</span></span>

### <a name="request"></a><span data-ttu-id="46f46-141">请求</span><span class="sxs-lookup"><span data-stu-id="46f46-141">Request</span></span>
<span data-ttu-id="46f46-142">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="46f46-142">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceShellScripts/{deviceShellScriptId}/assign

Content-type: application/json
Content-length: 550

{
  "deviceManagementScriptGroupAssignments": [
    {
      "@odata.type": "#microsoft.graph.deviceManagementScriptGroupAssignment",
      "id": "ecd2357d-357d-ecd2-7d35-d2ec7d35d2ec",
      "targetGroupId": "Target Group Id value"
    }
  ],
  "deviceManagementScriptAssignments": [
    {
      "@odata.type": "#microsoft.graph.deviceManagementScriptAssignment",
      "id": "a87a601e-601e-a87a-1e60-7aa81e607aa8",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      }
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="46f46-143">响应</span><span class="sxs-lookup"><span data-stu-id="46f46-143">Response</span></span>
<span data-ttu-id="46f46-p102">下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="46f46-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```




