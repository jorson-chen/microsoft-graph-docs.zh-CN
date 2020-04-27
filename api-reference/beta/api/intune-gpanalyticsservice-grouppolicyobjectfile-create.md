---
title: 创建 groupPolicyObjectFile
description: 创建新的 groupPolicyObjectFile 对象。
author: dougeby
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: addb2ac25071618b01866065afac6c4389aa15cb
ms.sourcegitcommit: bbcf074f0be9d5e02f84c290122850cc5968fb1f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2020
ms.locfileid: "43454937"
---
# <a name="create-grouppolicyobjectfile"></a><span data-ttu-id="0fde8-103">创建 groupPolicyObjectFile</span><span class="sxs-lookup"><span data-stu-id="0fde8-103">Create groupPolicyObjectFile</span></span>

<span data-ttu-id="0fde8-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="0fde8-104">Namespace: microsoft.graph</span></span>

> <span data-ttu-id="0fde8-105">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="0fde8-105">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="0fde8-106">**注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="0fde8-106">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="0fde8-107">创建新的[groupPolicyObjectFile](../resources/intune-gpanalyticsservice-grouppolicyobjectfile.md)对象。</span><span class="sxs-lookup"><span data-stu-id="0fde8-107">Create a new [groupPolicyObjectFile](../resources/intune-gpanalyticsservice-grouppolicyobjectfile.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0fde8-108">先决条件</span><span class="sxs-lookup"><span data-stu-id="0fde8-108">Prerequisites</span></span>
<span data-ttu-id="0fde8-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="0fde8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0fde8-111">权限类型</span><span class="sxs-lookup"><span data-stu-id="0fde8-111">Permission type</span></span>|<span data-ttu-id="0fde8-112">权限（从最高特权到最低特权）</span><span class="sxs-lookup"><span data-stu-id="0fde8-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0fde8-113">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="0fde8-113">Delegated (work or school account)</span></span>|<span data-ttu-id="0fde8-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0fde8-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="0fde8-115">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="0fde8-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0fde8-116">不支持。</span><span class="sxs-lookup"><span data-stu-id="0fde8-116">Not supported.</span></span>|
|<span data-ttu-id="0fde8-117">应用程序</span><span class="sxs-lookup"><span data-stu-id="0fde8-117">Application</span></span>|<span data-ttu-id="0fde8-118">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0fde8-118">DeviceManagementConfiguration.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="0fde8-119">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="0fde8-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/groupPolicyObjectFiles
```

## <a name="request-headers"></a><span data-ttu-id="0fde8-120">请求标头</span><span class="sxs-lookup"><span data-stu-id="0fde8-120">Request headers</span></span>
|<span data-ttu-id="0fde8-121">标头</span><span class="sxs-lookup"><span data-stu-id="0fde8-121">Header</span></span>|<span data-ttu-id="0fde8-122">值</span><span class="sxs-lookup"><span data-stu-id="0fde8-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0fde8-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="0fde8-123">Authorization</span></span>|<span data-ttu-id="0fde8-124">Bearer &lt;token&gt;。必需。</span><span class="sxs-lookup"><span data-stu-id="0fde8-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0fde8-125">接受</span><span class="sxs-lookup"><span data-stu-id="0fde8-125">Accept</span></span>|<span data-ttu-id="0fde8-126">application/json</span><span class="sxs-lookup"><span data-stu-id="0fde8-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0fde8-127">请求正文</span><span class="sxs-lookup"><span data-stu-id="0fde8-127">Request body</span></span>
<span data-ttu-id="0fde8-128">在请求正文中，提供 groupPolicyObjectFile 对象的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="0fde8-128">In the request body, supply a JSON representation for the groupPolicyObjectFile object.</span></span>

<span data-ttu-id="0fde8-129">下表显示创建 groupPolicyObjectFile 时所需的属性。</span><span class="sxs-lookup"><span data-stu-id="0fde8-129">The following table shows the properties that are required when you create the groupPolicyObjectFile.</span></span>

|<span data-ttu-id="0fde8-130">属性</span><span class="sxs-lookup"><span data-stu-id="0fde8-130">Property</span></span>|<span data-ttu-id="0fde8-131">类型</span><span class="sxs-lookup"><span data-stu-id="0fde8-131">Type</span></span>|<span data-ttu-id="0fde8-132">说明</span><span class="sxs-lookup"><span data-stu-id="0fde8-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0fde8-133">id</span><span class="sxs-lookup"><span data-stu-id="0fde8-133">id</span></span>|<span data-ttu-id="0fde8-134">String</span><span class="sxs-lookup"><span data-stu-id="0fde8-134">String</span></span>|<span data-ttu-id="0fde8-135">尚未记录</span><span class="sxs-lookup"><span data-stu-id="0fde8-135">Not yet documented</span></span>|
|<span data-ttu-id="0fde8-136">groupPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="0fde8-136">groupPolicyObjectId</span></span>|<span data-ttu-id="0fde8-137">Guid</span><span class="sxs-lookup"><span data-stu-id="0fde8-137">Guid</span></span>|<span data-ttu-id="0fde8-138">GPO Xml 内容中的组策略对象 GUID</span><span class="sxs-lookup"><span data-stu-id="0fde8-138">The Group Policy Object GUID from GPO Xml content</span></span>|
|<span data-ttu-id="0fde8-139">ouDistinguishedName</span><span class="sxs-lookup"><span data-stu-id="0fde8-139">ouDistinguishedName</span></span>|<span data-ttu-id="0fde8-140">String</span><span class="sxs-lookup"><span data-stu-id="0fde8-140">String</span></span>|<span data-ttu-id="0fde8-141">OU 的可分辨名称。</span><span class="sxs-lookup"><span data-stu-id="0fde8-141">The distinguished name of the OU.</span></span>|
|<span data-ttu-id="0fde8-142">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="0fde8-142">createdDateTime</span></span>|<span data-ttu-id="0fde8-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0fde8-143">DateTimeOffset</span></span>|<span data-ttu-id="0fde8-144">首次上传 GroupPolicy 的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="0fde8-144">The date and time at which the GroupPolicy was first uploaded.</span></span>|
|<span data-ttu-id="0fde8-145">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="0fde8-145">lastModifiedDateTime</span></span>|<span data-ttu-id="0fde8-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0fde8-146">DateTimeOffset</span></span>|<span data-ttu-id="0fde8-147">上次修改 GroupPolicyObjectFile 的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="0fde8-147">The date and time at which the GroupPolicyObjectFile was last modified.</span></span>|
|<span data-ttu-id="0fde8-148">内容</span><span class="sxs-lookup"><span data-stu-id="0fde8-148">content</span></span>|<span data-ttu-id="0fde8-149">String</span><span class="sxs-lookup"><span data-stu-id="0fde8-149">String</span></span>|<span data-ttu-id="0fde8-150">组策略对象文件内容。</span><span class="sxs-lookup"><span data-stu-id="0fde8-150">The Group Policy Object file content.</span></span>|



## <a name="response"></a><span data-ttu-id="0fde8-151">响应</span><span class="sxs-lookup"><span data-stu-id="0fde8-151">Response</span></span>
<span data-ttu-id="0fde8-152">如果成功，此方法在响应`201 Created`正文中返回响应代码和[groupPolicyObjectFile](../resources/intune-gpanalyticsservice-grouppolicyobjectfile.md)对象。</span><span class="sxs-lookup"><span data-stu-id="0fde8-152">If successful, this method returns a `201 Created` response code and a [groupPolicyObjectFile](../resources/intune-gpanalyticsservice-grouppolicyobjectfile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0fde8-153">示例</span><span class="sxs-lookup"><span data-stu-id="0fde8-153">Example</span></span>

### <a name="request"></a><span data-ttu-id="0fde8-154">请求</span><span class="sxs-lookup"><span data-stu-id="0fde8-154">Request</span></span>
<span data-ttu-id="0fde8-155">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="0fde8-155">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/groupPolicyObjectFiles
Content-type: application/json
Content-length: 217

{
  "@odata.type": "#microsoft.graph.groupPolicyObjectFile",
  "groupPolicyObjectId": "ca1c97af-97af-ca1c-af97-1ccaaf971cca",
  "ouDistinguishedName": "Ou Distinguished Name value",
  "content": "Content value"
}
```

### <a name="response"></a><span data-ttu-id="0fde8-156">响应</span><span class="sxs-lookup"><span data-stu-id="0fde8-156">Response</span></span>
<span data-ttu-id="0fde8-p102">下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="0fde8-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 389

{
  "@odata.type": "#microsoft.graph.groupPolicyObjectFile",
  "id": "65c0499d-499d-65c0-9d49-c0659d49c065",
  "groupPolicyObjectId": "ca1c97af-97af-ca1c-af97-1ccaaf971cca",
  "ouDistinguishedName": "Ou Distinguished Name value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "content": "Content value"
}
```


