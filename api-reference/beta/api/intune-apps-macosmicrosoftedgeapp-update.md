---
title: 更新 macOSMicrosoftEdgeApp
description: 更新 macOSMicrosoftEdgeApp 对象的属性。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 55d3f64b8d20af8838a98823667e11f88dfaaf3b
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2019
ms.locfileid: "37535315"
---
# <a name="update-macosmicrosoftedgeapp"></a><span data-ttu-id="83a75-103">更新 macOSMicrosoftEdgeApp</span><span class="sxs-lookup"><span data-stu-id="83a75-103">Update macOSMicrosoftEdgeApp</span></span>

> <span data-ttu-id="83a75-104">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="83a75-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="83a75-105">**注意：** 适用于 Intune 的 Microsoft Graph API 需要租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="83a75-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="83a75-106">更新[macOSMicrosoftEdgeApp](../resources/intune-apps-macosmicrosoftedgeapp.md)对象的属性。</span><span class="sxs-lookup"><span data-stu-id="83a75-106">Update the properties of a [macOSMicrosoftEdgeApp](../resources/intune-apps-macosmicrosoftedgeapp.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="83a75-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="83a75-107">Prerequisites</span></span>
<span data-ttu-id="83a75-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="83a75-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="83a75-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="83a75-110">Permission type</span></span>|<span data-ttu-id="83a75-111">权限（从最高特权到最低特权）</span><span class="sxs-lookup"><span data-stu-id="83a75-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="83a75-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="83a75-112">Delegated (work or school account)</span></span>|<span data-ttu-id="83a75-113">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="83a75-113">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="83a75-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="83a75-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="83a75-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="83a75-115">Not supported.</span></span>|
|<span data-ttu-id="83a75-116">应用程序</span><span class="sxs-lookup"><span data-stu-id="83a75-116">Application</span></span>|<span data-ttu-id="83a75-117">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="83a75-117">DeviceManagementApps.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="83a75-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="83a75-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="request-headers"></a><span data-ttu-id="83a75-119">请求标头</span><span class="sxs-lookup"><span data-stu-id="83a75-119">Request headers</span></span>
|<span data-ttu-id="83a75-120">标头</span><span class="sxs-lookup"><span data-stu-id="83a75-120">Header</span></span>|<span data-ttu-id="83a75-121">值</span><span class="sxs-lookup"><span data-stu-id="83a75-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="83a75-122">授权</span><span class="sxs-lookup"><span data-stu-id="83a75-122">Authorization</span></span>|<span data-ttu-id="83a75-123">Bearer &lt;token&gt;。必需。</span><span class="sxs-lookup"><span data-stu-id="83a75-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="83a75-124">接受</span><span class="sxs-lookup"><span data-stu-id="83a75-124">Accept</span></span>|<span data-ttu-id="83a75-125">application/json</span><span class="sxs-lookup"><span data-stu-id="83a75-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="83a75-126">请求正文</span><span class="sxs-lookup"><span data-stu-id="83a75-126">Request body</span></span>
<span data-ttu-id="83a75-127">在请求正文中，提供[macOSMicrosoftEdgeApp](../resources/intune-apps-macosmicrosoftedgeapp.md)对象的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="83a75-127">In the request body, supply a JSON representation for the [macOSMicrosoftEdgeApp](../resources/intune-apps-macosmicrosoftedgeapp.md) object.</span></span>

<span data-ttu-id="83a75-128">下表显示创建[macOSMicrosoftEdgeApp](../resources/intune-apps-macosmicrosoftedgeapp.md)时所需的属性。</span><span class="sxs-lookup"><span data-stu-id="83a75-128">The following table shows the properties that are required when you create the [macOSMicrosoftEdgeApp](../resources/intune-apps-macosmicrosoftedgeapp.md).</span></span>

|<span data-ttu-id="83a75-129">属性</span><span class="sxs-lookup"><span data-stu-id="83a75-129">Property</span></span>|<span data-ttu-id="83a75-130">类型</span><span class="sxs-lookup"><span data-stu-id="83a75-130">Type</span></span>|<span data-ttu-id="83a75-131">说明</span><span class="sxs-lookup"><span data-stu-id="83a75-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="83a75-132">id</span><span class="sxs-lookup"><span data-stu-id="83a75-132">id</span></span>|<span data-ttu-id="83a75-133">字符串</span><span class="sxs-lookup"><span data-stu-id="83a75-133">String</span></span>|<span data-ttu-id="83a75-134">实体的键。</span><span class="sxs-lookup"><span data-stu-id="83a75-134">Key of the entity.</span></span> <span data-ttu-id="83a75-135">继承自 [mobileApp](../resources/intune-shared-mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="83a75-135">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="83a75-136">displayName</span><span class="sxs-lookup"><span data-stu-id="83a75-136">displayName</span></span>|<span data-ttu-id="83a75-137">字符串</span><span class="sxs-lookup"><span data-stu-id="83a75-137">String</span></span>|<span data-ttu-id="83a75-138">管理员提供或导入的应用标题。</span><span class="sxs-lookup"><span data-stu-id="83a75-138">The admin provided or imported title of the app.</span></span> <span data-ttu-id="83a75-139">继承自 [mobileApp](../resources/intune-shared-mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="83a75-139">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="83a75-140">说明</span><span class="sxs-lookup"><span data-stu-id="83a75-140">description</span></span>|<span data-ttu-id="83a75-141">字符串</span><span class="sxs-lookup"><span data-stu-id="83a75-141">String</span></span>|<span data-ttu-id="83a75-142">应用的说明。</span><span class="sxs-lookup"><span data-stu-id="83a75-142">The description of the app.</span></span> <span data-ttu-id="83a75-143">继承自 [mobileApp](../resources/intune-shared-mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="83a75-143">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="83a75-144">publisher</span><span class="sxs-lookup"><span data-stu-id="83a75-144">publisher</span></span>|<span data-ttu-id="83a75-145">字符串</span><span class="sxs-lookup"><span data-stu-id="83a75-145">String</span></span>|<span data-ttu-id="83a75-146">应用的发布者。</span><span class="sxs-lookup"><span data-stu-id="83a75-146">The publisher of the app.</span></span> <span data-ttu-id="83a75-147">继承自 [mobileApp](../resources/intune-shared-mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="83a75-147">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="83a75-148">largeIcon</span><span class="sxs-lookup"><span data-stu-id="83a75-148">largeIcon</span></span>|[<span data-ttu-id="83a75-149">mimeContent</span><span class="sxs-lookup"><span data-stu-id="83a75-149">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="83a75-150">要显示在应用详细信息中并用于图标上传的大图标。</span><span class="sxs-lookup"><span data-stu-id="83a75-150">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="83a75-151">继承自 [mobileApp](../resources/intune-shared-mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="83a75-151">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="83a75-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="83a75-152">createdDateTime</span></span>|<span data-ttu-id="83a75-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="83a75-153">DateTimeOffset</span></span>|<span data-ttu-id="83a75-154">创建应用的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="83a75-154">The date and time the app was created.</span></span> <span data-ttu-id="83a75-155">继承自 [mobileApp](../resources/intune-shared-mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="83a75-155">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="83a75-156">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="83a75-156">lastModifiedDateTime</span></span>|<span data-ttu-id="83a75-157">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="83a75-157">DateTimeOffset</span></span>|<span data-ttu-id="83a75-158">上次修改应用的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="83a75-158">The date and time the app was last modified.</span></span> <span data-ttu-id="83a75-159">继承自 [mobileApp](../resources/intune-shared-mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="83a75-159">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="83a75-160">isFeatured</span><span class="sxs-lookup"><span data-stu-id="83a75-160">isFeatured</span></span>|<span data-ttu-id="83a75-161">Boolean</span><span class="sxs-lookup"><span data-stu-id="83a75-161">Boolean</span></span>|<span data-ttu-id="83a75-162">指示应用是否被管理员标记为特色的值。继承自 [mobileApp](../resources/intune-shared-mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="83a75-162">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="83a75-163">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="83a75-163">privacyInformationUrl</span></span>|<span data-ttu-id="83a75-164">字符串</span><span class="sxs-lookup"><span data-stu-id="83a75-164">String</span></span>|<span data-ttu-id="83a75-165">隐私声明 URL。</span><span class="sxs-lookup"><span data-stu-id="83a75-165">The privacy statement Url.</span></span> <span data-ttu-id="83a75-166">继承自 [mobileApp](../resources/intune-shared-mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="83a75-166">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="83a75-167">informationUrl</span><span class="sxs-lookup"><span data-stu-id="83a75-167">informationUrl</span></span>|<span data-ttu-id="83a75-168">字符串</span><span class="sxs-lookup"><span data-stu-id="83a75-168">String</span></span>|<span data-ttu-id="83a75-169">详细信息 URL。</span><span class="sxs-lookup"><span data-stu-id="83a75-169">The more information Url.</span></span> <span data-ttu-id="83a75-170">继承自 [mobileApp](../resources/intune-shared-mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="83a75-170">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="83a75-171">owner</span><span class="sxs-lookup"><span data-stu-id="83a75-171">owner</span></span>|<span data-ttu-id="83a75-172">String</span><span class="sxs-lookup"><span data-stu-id="83a75-172">String</span></span>|<span data-ttu-id="83a75-173">应用的所有者。</span><span class="sxs-lookup"><span data-stu-id="83a75-173">The owner of the app.</span></span> <span data-ttu-id="83a75-174">继承自 [mobileApp](../resources/intune-shared-mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="83a75-174">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="83a75-175">developer</span><span class="sxs-lookup"><span data-stu-id="83a75-175">developer</span></span>|<span data-ttu-id="83a75-176">字符串</span><span class="sxs-lookup"><span data-stu-id="83a75-176">String</span></span>|<span data-ttu-id="83a75-177">应用的开发者。</span><span class="sxs-lookup"><span data-stu-id="83a75-177">The developer of the app.</span></span> <span data-ttu-id="83a75-178">继承自 [mobileApp](../resources/intune-shared-mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="83a75-178">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="83a75-179">notes</span><span class="sxs-lookup"><span data-stu-id="83a75-179">notes</span></span>|<span data-ttu-id="83a75-180">String</span><span class="sxs-lookup"><span data-stu-id="83a75-180">String</span></span>|<span data-ttu-id="83a75-181">应用的备注。</span><span class="sxs-lookup"><span data-stu-id="83a75-181">Notes for the app.</span></span> <span data-ttu-id="83a75-182">继承自 [mobileApp](../resources/intune-shared-mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="83a75-182">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="83a75-183">uploadState</span><span class="sxs-lookup"><span data-stu-id="83a75-183">uploadState</span></span>|<span data-ttu-id="83a75-184">Int32</span><span class="sxs-lookup"><span data-stu-id="83a75-184">Int32</span></span>|<span data-ttu-id="83a75-185">上载状态。</span><span class="sxs-lookup"><span data-stu-id="83a75-185">The upload state.</span></span> <span data-ttu-id="83a75-186">继承自 [mobileApp](../resources/intune-shared-mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="83a75-186">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="83a75-187">publishingState</span><span class="sxs-lookup"><span data-stu-id="83a75-187">publishingState</span></span>|[<span data-ttu-id="83a75-188">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="83a75-188">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="83a75-189">应用的发布状态。</span><span class="sxs-lookup"><span data-stu-id="83a75-189">The publishing state for the app.</span></span> <span data-ttu-id="83a75-190">除非应用已发布，否则无法分配应用。</span><span class="sxs-lookup"><span data-stu-id="83a75-190">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="83a75-191">继承自[mobileApp](../resources/intune-shared-mobileapp.md)。</span><span class="sxs-lookup"><span data-stu-id="83a75-191">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md).</span></span> <span data-ttu-id="83a75-192">可取值为：`notPublished`、`processing`、`published`。</span><span class="sxs-lookup"><span data-stu-id="83a75-192">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="83a75-193">isAssigned</span><span class="sxs-lookup"><span data-stu-id="83a75-193">isAssigned</span></span>|<span data-ttu-id="83a75-194">Boolean</span><span class="sxs-lookup"><span data-stu-id="83a75-194">Boolean</span></span>|<span data-ttu-id="83a75-195">指示是否至少向一个组分配了应用程序的值。</span><span class="sxs-lookup"><span data-stu-id="83a75-195">The value indicating whether the app is assigned to at least one group.</span></span> <span data-ttu-id="83a75-196">继承自 [mobileApp](../resources/intune-shared-mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="83a75-196">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="83a75-197">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="83a75-197">roleScopeTagIds</span></span>|<span data-ttu-id="83a75-198">String 集合</span><span class="sxs-lookup"><span data-stu-id="83a75-198">String collection</span></span>|<span data-ttu-id="83a75-199">此移动应用的作用域标记 id 列表。</span><span class="sxs-lookup"><span data-stu-id="83a75-199">List of scope tag ids for this mobile app.</span></span> <span data-ttu-id="83a75-200">继承自 [mobileApp](../resources/intune-shared-mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="83a75-200">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="83a75-201">dependentAppCount</span><span class="sxs-lookup"><span data-stu-id="83a75-201">dependentAppCount</span></span>|<span data-ttu-id="83a75-202">Int32</span><span class="sxs-lookup"><span data-stu-id="83a75-202">Int32</span></span>|<span data-ttu-id="83a75-203">子应用程序的依赖项总数。</span><span class="sxs-lookup"><span data-stu-id="83a75-203">The total number of dependencies the child app has.</span></span> <span data-ttu-id="83a75-204">继承自 [mobileApp](../resources/intune-shared-mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="83a75-204">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|



## <a name="response"></a><span data-ttu-id="83a75-205">响应</span><span class="sxs-lookup"><span data-stu-id="83a75-205">Response</span></span>
<span data-ttu-id="83a75-206">如果成功，此方法在响应`200 OK`正文中返回响应代码和更新的[macOSMicrosoftEdgeApp](../resources/intune-apps-macosmicrosoftedgeapp.md)对象。</span><span class="sxs-lookup"><span data-stu-id="83a75-206">If successful, this method returns a `200 OK` response code and an updated [macOSMicrosoftEdgeApp](../resources/intune-apps-macosmicrosoftedgeapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="83a75-207">示例</span><span class="sxs-lookup"><span data-stu-id="83a75-207">Example</span></span>

### <a name="request"></a><span data-ttu-id="83a75-208">请求</span><span class="sxs-lookup"><span data-stu-id="83a75-208">Request</span></span>
<span data-ttu-id="83a75-209">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="83a75-209">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 720

{
  "@odata.type": "#microsoft.graph.macOSMicrosoftEdgeApp",
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
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
```

### <a name="response"></a><span data-ttu-id="83a75-210">响应</span><span class="sxs-lookup"><span data-stu-id="83a75-210">Response</span></span>
<span data-ttu-id="83a75-p119">下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="83a75-p119">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 892

{
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
```





