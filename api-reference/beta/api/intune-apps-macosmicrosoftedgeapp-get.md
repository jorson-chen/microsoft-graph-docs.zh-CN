---
title: 获取 macOSMicrosoftEdgeApp
description: 读取 macOSMicrosoftEdgeApp 对象的属性和关系。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 23205c161655273762ed559e849b4c4f157d5970
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2019
ms.locfileid: "37535329"
---
# <a name="get-macosmicrosoftedgeapp"></a><span data-ttu-id="4fe74-103">获取 macOSMicrosoftEdgeApp</span><span class="sxs-lookup"><span data-stu-id="4fe74-103">Get macOSMicrosoftEdgeApp</span></span>

> <span data-ttu-id="4fe74-104">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="4fe74-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="4fe74-105">**注意：** 适用于 Intune 的 Microsoft Graph API 需要租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="4fe74-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="4fe74-106">读取[macOSMicrosoftEdgeApp](../resources/intune-apps-macosmicrosoftedgeapp.md)对象的属性和关系。</span><span class="sxs-lookup"><span data-stu-id="4fe74-106">Read properties and relationships of the [macOSMicrosoftEdgeApp](../resources/intune-apps-macosmicrosoftedgeapp.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4fe74-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="4fe74-107">Prerequisites</span></span>
<span data-ttu-id="4fe74-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="4fe74-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4fe74-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="4fe74-110">Permission type</span></span>|<span data-ttu-id="4fe74-111">权限（从最高特权到最低特权）</span><span class="sxs-lookup"><span data-stu-id="4fe74-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4fe74-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="4fe74-112">Delegated (work or school account)</span></span>|<span data-ttu-id="4fe74-113">DeviceManagementApps.ReadWrite.All、DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="4fe74-113">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="4fe74-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="4fe74-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4fe74-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="4fe74-115">Not supported.</span></span>|
|<span data-ttu-id="4fe74-116">应用程序</span><span class="sxs-lookup"><span data-stu-id="4fe74-116">Application</span></span>|<span data-ttu-id="4fe74-117">DeviceManagementApps.ReadWrite.All、DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="4fe74-117">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="4fe74-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="4fe74-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps/{mobileAppId}
GET /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
GET /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="optional-query-parameters"></a><span data-ttu-id="4fe74-119">可选的查询参数</span><span class="sxs-lookup"><span data-stu-id="4fe74-119">Optional query parameters</span></span>
<span data-ttu-id="4fe74-120">此方法支持 [OData 查询参数](https://docs.microsoft.com/en-us/graph/query-parameters) 来帮助自定义响应。</span><span class="sxs-lookup"><span data-stu-id="4fe74-120">This method supports the [OData Query Parameters](https://docs.microsoft.com/en-us/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="4fe74-121">请求标头</span><span class="sxs-lookup"><span data-stu-id="4fe74-121">Request headers</span></span>
|<span data-ttu-id="4fe74-122">标头</span><span class="sxs-lookup"><span data-stu-id="4fe74-122">Header</span></span>|<span data-ttu-id="4fe74-123">值</span><span class="sxs-lookup"><span data-stu-id="4fe74-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4fe74-124">授权</span><span class="sxs-lookup"><span data-stu-id="4fe74-124">Authorization</span></span>|<span data-ttu-id="4fe74-125">Bearer &lt;token&gt;。必需。</span><span class="sxs-lookup"><span data-stu-id="4fe74-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4fe74-126">接受</span><span class="sxs-lookup"><span data-stu-id="4fe74-126">Accept</span></span>|<span data-ttu-id="4fe74-127">application/json</span><span class="sxs-lookup"><span data-stu-id="4fe74-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4fe74-128">请求正文</span><span class="sxs-lookup"><span data-stu-id="4fe74-128">Request body</span></span>
<span data-ttu-id="4fe74-129">请勿提供此方法的请求正文。</span><span class="sxs-lookup"><span data-stu-id="4fe74-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4fe74-130">响应</span><span class="sxs-lookup"><span data-stu-id="4fe74-130">Response</span></span>
<span data-ttu-id="4fe74-131">如果成功，此方法在响应`200 OK`正文中返回响应代码和[macOSMicrosoftEdgeApp](../resources/intune-apps-macosmicrosoftedgeapp.md)对象。</span><span class="sxs-lookup"><span data-stu-id="4fe74-131">If successful, this method returns a `200 OK` response code and [macOSMicrosoftEdgeApp](../resources/intune-apps-macosmicrosoftedgeapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4fe74-132">示例</span><span class="sxs-lookup"><span data-stu-id="4fe74-132">Example</span></span>

### <a name="request"></a><span data-ttu-id="4fe74-133">请求</span><span class="sxs-lookup"><span data-stu-id="4fe74-133">Request</span></span>
<span data-ttu-id="4fe74-134">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="4fe74-134">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}
```

### <a name="response"></a><span data-ttu-id="4fe74-135">响应</span><span class="sxs-lookup"><span data-stu-id="4fe74-135">Response</span></span>
<span data-ttu-id="4fe74-p102">下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="4fe74-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 961

{
  "value": {
    "@odata.type": "#microsoft.graph.macOSMicrosoftEdgeApp",
    "id": "c964092a-092a-c964-2a09-64c92a0964c9",
    "displayName": "Display Name value",
    "description": "Description value",
    "publisher": "Publisher value",
    "largeIcon": {
      "@odata.type": "microsoft.graph.mimeContent",
      "type": "Type value",
      "value": "dmFsdWU="
    },
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "isFeatured": true,
    "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
    "informationUrl": "https://example.com/informationUrl/",
    "owner": "Owner value",
    "developer": "Developer value",
    "notes": "Notes value",
    "uploadState": 11,
    "publishingState": "processing",
    "isAssigned": true,
    "roleScopeTagIds": [
      "Role Scope Tag Ids value"
    ],
    "dependentAppCount": 1
  }
}
```





