---
title: 列出 groupPolicyMigrationReports
description: 列出 groupPolicyMigrationReport 对象的属性和关系。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: a732f338c929fb941a4f92dacf555cef23a8e6af
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2019
ms.locfileid: "37535784"
---
# <a name="list-grouppolicymigrationreports"></a><span data-ttu-id="6d702-103">列出 groupPolicyMigrationReports</span><span class="sxs-lookup"><span data-stu-id="6d702-103">List groupPolicyMigrationReports</span></span>

> <span data-ttu-id="6d702-104">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="6d702-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="6d702-105">**注意：** 适用于 Intune 的 Microsoft Graph API 需要租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="6d702-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="6d702-106">列出[groupPolicyMigrationReport](../resources/intune-gpanalyticsservice-grouppolicymigrationreport.md)对象的属性和关系。</span><span class="sxs-lookup"><span data-stu-id="6d702-106">List properties and relationships of the [groupPolicyMigrationReport](../resources/intune-gpanalyticsservice-grouppolicymigrationreport.md) objects.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6d702-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="6d702-107">Prerequisites</span></span>
<span data-ttu-id="6d702-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="6d702-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6d702-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="6d702-110">Permission type</span></span>|<span data-ttu-id="6d702-111">权限（从最高特权到最低特权）</span><span class="sxs-lookup"><span data-stu-id="6d702-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6d702-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="6d702-112">Delegated (work or school account)</span></span>|<span data-ttu-id="6d702-113">DeviceManagementConfiguration.ReadWrite.All、DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="6d702-113">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="6d702-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="6d702-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6d702-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="6d702-115">Not supported.</span></span>|
|<span data-ttu-id="6d702-116">应用程序</span><span class="sxs-lookup"><span data-stu-id="6d702-116">Application</span></span>|<span data-ttu-id="6d702-117">DeviceManagementConfiguration.ReadWrite.All、DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="6d702-117">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="6d702-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="6d702-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/groupPolicyMigrationReports
```

## <a name="request-headers"></a><span data-ttu-id="6d702-119">请求标头</span><span class="sxs-lookup"><span data-stu-id="6d702-119">Request headers</span></span>
|<span data-ttu-id="6d702-120">标头</span><span class="sxs-lookup"><span data-stu-id="6d702-120">Header</span></span>|<span data-ttu-id="6d702-121">值</span><span class="sxs-lookup"><span data-stu-id="6d702-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6d702-122">授权</span><span class="sxs-lookup"><span data-stu-id="6d702-122">Authorization</span></span>|<span data-ttu-id="6d702-123">Bearer &lt;token&gt;。必需。</span><span class="sxs-lookup"><span data-stu-id="6d702-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6d702-124">接受</span><span class="sxs-lookup"><span data-stu-id="6d702-124">Accept</span></span>|<span data-ttu-id="6d702-125">application/json</span><span class="sxs-lookup"><span data-stu-id="6d702-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6d702-126">请求正文</span><span class="sxs-lookup"><span data-stu-id="6d702-126">Request body</span></span>
<span data-ttu-id="6d702-127">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="6d702-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6d702-128">响应</span><span class="sxs-lookup"><span data-stu-id="6d702-128">Response</span></span>
<span data-ttu-id="6d702-129">如果成功，此方法在响应`200 OK`正文中返回响应代码和[groupPolicyMigrationReport](../resources/intune-gpanalyticsservice-grouppolicymigrationreport.md)对象集合。</span><span class="sxs-lookup"><span data-stu-id="6d702-129">If successful, this method returns a `200 OK` response code and a collection of [groupPolicyMigrationReport](../resources/intune-gpanalyticsservice-grouppolicymigrationreport.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6d702-130">示例</span><span class="sxs-lookup"><span data-stu-id="6d702-130">Example</span></span>

### <a name="request"></a><span data-ttu-id="6d702-131">请求</span><span class="sxs-lookup"><span data-stu-id="6d702-131">Request</span></span>
<span data-ttu-id="6d702-132">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="6d702-132">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/groupPolicyMigrationReports
```

### <a name="response"></a><span data-ttu-id="6d702-133">响应</span><span class="sxs-lookup"><span data-stu-id="6d702-133">Response</span></span>
<span data-ttu-id="6d702-p102">下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="6d702-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 805

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.groupPolicyMigrationReport",
      "id": "60663fa8-3fa8-6066-a83f-6660a83f6660",
      "groupPolicyObjectId": "ca1c97af-97af-ca1c-af97-1ccaaf971cca",
      "displayName": "Display Name value",
      "ouDistinguishedName": "Ou Distinguished Name value",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "groupPolicyCreatedDateTime": "2016-12-31T23:58:14.0676812-08:00",
      "groupPolicyLastModifiedDateTime": "2017-01-01T00:02:51.2241017-08:00",
      "migrationReadiness": "partial",
      "targetedInActiveDirectory": true,
      "totalSettingsCount": 2,
      "supportedSettingsCount": 6,
      "supportedSettingsPercent": 8
    }
  ]
}
```





