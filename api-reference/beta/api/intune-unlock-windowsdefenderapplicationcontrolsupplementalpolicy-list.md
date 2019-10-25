---
title: 列出 windowsDefenderApplicationControlSupplementalPolicies
description: 列出 windowsDefenderApplicationControlSupplementalPolicy 对象的属性和关系。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 0d932f7b46d5781b8dfaa3fadd96dc65273f6b2e
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2019
ms.locfileid: "37537669"
---
# <a name="list-windowsdefenderapplicationcontrolsupplementalpolicies"></a><span data-ttu-id="bb432-103">列出 windowsDefenderApplicationControlSupplementalPolicies</span><span class="sxs-lookup"><span data-stu-id="bb432-103">List windowsDefenderApplicationControlSupplementalPolicies</span></span>

> <span data-ttu-id="bb432-104">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="bb432-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="bb432-105">**注意：** 适用于 Intune 的 Microsoft Graph API 需要租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="bb432-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="bb432-106">列出[windowsDefenderApplicationControlSupplementalPolicy](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicy.md)对象的属性和关系。</span><span class="sxs-lookup"><span data-stu-id="bb432-106">List properties and relationships of the [windowsDefenderApplicationControlSupplementalPolicy](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicy.md) objects.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bb432-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="bb432-107">Prerequisites</span></span>
<span data-ttu-id="bb432-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="bb432-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bb432-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="bb432-110">Permission type</span></span>|<span data-ttu-id="bb432-111">权限（从最高特权到最低特权）</span><span class="sxs-lookup"><span data-stu-id="bb432-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bb432-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="bb432-112">Delegated (work or school account)</span></span>|<span data-ttu-id="bb432-113">DeviceManagementApps.ReadWrite.All、DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="bb432-113">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="bb432-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="bb432-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bb432-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="bb432-115">Not supported.</span></span>|
|<span data-ttu-id="bb432-116">应用程序</span><span class="sxs-lookup"><span data-stu-id="bb432-116">Application</span></span>|<span data-ttu-id="bb432-117">DeviceManagementApps.ReadWrite.All、DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="bb432-117">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="bb432-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="bb432-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/wdacSupplementalPolicies
```

## <a name="request-headers"></a><span data-ttu-id="bb432-119">请求标头</span><span class="sxs-lookup"><span data-stu-id="bb432-119">Request headers</span></span>
|<span data-ttu-id="bb432-120">标头</span><span class="sxs-lookup"><span data-stu-id="bb432-120">Header</span></span>|<span data-ttu-id="bb432-121">值</span><span class="sxs-lookup"><span data-stu-id="bb432-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bb432-122">授权</span><span class="sxs-lookup"><span data-stu-id="bb432-122">Authorization</span></span>|<span data-ttu-id="bb432-123">Bearer &lt;token&gt;。必需。</span><span class="sxs-lookup"><span data-stu-id="bb432-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bb432-124">接受</span><span class="sxs-lookup"><span data-stu-id="bb432-124">Accept</span></span>|<span data-ttu-id="bb432-125">application/json</span><span class="sxs-lookup"><span data-stu-id="bb432-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bb432-126">请求正文</span><span class="sxs-lookup"><span data-stu-id="bb432-126">Request body</span></span>
<span data-ttu-id="bb432-127">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="bb432-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bb432-128">响应</span><span class="sxs-lookup"><span data-stu-id="bb432-128">Response</span></span>
<span data-ttu-id="bb432-129">如果成功，此方法在响应`200 OK`正文中返回响应代码和[windowsDefenderApplicationControlSupplementalPolicy](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicy.md)对象集合。</span><span class="sxs-lookup"><span data-stu-id="bb432-129">If successful, this method returns a `200 OK` response code and a collection of [windowsDefenderApplicationControlSupplementalPolicy](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicy.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bb432-130">示例</span><span class="sxs-lookup"><span data-stu-id="bb432-130">Example</span></span>

### <a name="request"></a><span data-ttu-id="bb432-131">请求</span><span class="sxs-lookup"><span data-stu-id="bb432-131">Request</span></span>
<span data-ttu-id="bb432-132">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="bb432-132">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/wdacSupplementalPolicies
```

### <a name="response"></a><span data-ttu-id="bb432-133">响应</span><span class="sxs-lookup"><span data-stu-id="bb432-133">Response</span></span>
<span data-ttu-id="bb432-p102">下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="bb432-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 598

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsDefenderApplicationControlSupplementalPolicy",
      "id": "83d0c39e-c39e-83d0-9ec3-d0839ec3d083",
      "displayName": "Display Name value",
      "description": "Description value",
      "content": "Y29udGVudA==",
      "contentFileName": "Content File Name value",
      "version": "Version value",
      "creationDateTime": "2017-01-01T00:00:43.1365422-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "roleScopeTagIds": [
        "Role Scope Tag Ids value"
      ]
    }
  ]
}
```





