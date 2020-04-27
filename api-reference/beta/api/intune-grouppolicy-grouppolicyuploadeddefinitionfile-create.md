---
title: 创建 groupPolicyUploadedDefinitionFile
description: 创建新的 groupPolicyUploadedDefinitionFile 对象。
author: dougeby
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 828464d5a0e620a713eac7187b6a8883ea7a2648
ms.sourcegitcommit: bbcf074f0be9d5e02f84c290122850cc5968fb1f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2020
ms.locfileid: "43388648"
---
# <a name="create-grouppolicyuploadeddefinitionfile"></a><span data-ttu-id="abdb8-103">创建 groupPolicyUploadedDefinitionFile</span><span class="sxs-lookup"><span data-stu-id="abdb8-103">Create groupPolicyUploadedDefinitionFile</span></span>

<span data-ttu-id="abdb8-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="abdb8-104">Namespace: microsoft.graph</span></span>

> <span data-ttu-id="abdb8-105">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="abdb8-105">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="abdb8-106">**注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="abdb8-106">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="abdb8-107">创建新的[groupPolicyUploadedDefinitionFile](../resources/intune-grouppolicy-grouppolicyuploadeddefinitionfile.md)对象。</span><span class="sxs-lookup"><span data-stu-id="abdb8-107">Create a new [groupPolicyUploadedDefinitionFile](../resources/intune-grouppolicy-grouppolicyuploadeddefinitionfile.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="abdb8-108">先决条件</span><span class="sxs-lookup"><span data-stu-id="abdb8-108">Prerequisites</span></span>
<span data-ttu-id="abdb8-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="abdb8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="abdb8-111">权限类型</span><span class="sxs-lookup"><span data-stu-id="abdb8-111">Permission type</span></span>|<span data-ttu-id="abdb8-112">权限（从最高特权到最低特权）</span><span class="sxs-lookup"><span data-stu-id="abdb8-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="abdb8-113">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="abdb8-113">Delegated (work or school account)</span></span>|<span data-ttu-id="abdb8-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="abdb8-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="abdb8-115">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="abdb8-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="abdb8-116">不支持。</span><span class="sxs-lookup"><span data-stu-id="abdb8-116">Not supported.</span></span>|
|<span data-ttu-id="abdb8-117">应用程序</span><span class="sxs-lookup"><span data-stu-id="abdb8-117">Application</span></span>|<span data-ttu-id="abdb8-118">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="abdb8-118">DeviceManagementConfiguration.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="abdb8-119">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="abdb8-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/groupPolicyUploadedDefinitionFiles
```

## <a name="request-headers"></a><span data-ttu-id="abdb8-120">请求标头</span><span class="sxs-lookup"><span data-stu-id="abdb8-120">Request headers</span></span>
|<span data-ttu-id="abdb8-121">标头</span><span class="sxs-lookup"><span data-stu-id="abdb8-121">Header</span></span>|<span data-ttu-id="abdb8-122">值</span><span class="sxs-lookup"><span data-stu-id="abdb8-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="abdb8-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="abdb8-123">Authorization</span></span>|<span data-ttu-id="abdb8-124">Bearer &lt;token&gt;。必需。</span><span class="sxs-lookup"><span data-stu-id="abdb8-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="abdb8-125">接受</span><span class="sxs-lookup"><span data-stu-id="abdb8-125">Accept</span></span>|<span data-ttu-id="abdb8-126">application/json</span><span class="sxs-lookup"><span data-stu-id="abdb8-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="abdb8-127">请求正文</span><span class="sxs-lookup"><span data-stu-id="abdb8-127">Request body</span></span>
<span data-ttu-id="abdb8-128">在请求正文中，提供 groupPolicyUploadedDefinitionFile 对象的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="abdb8-128">In the request body, supply a JSON representation for the groupPolicyUploadedDefinitionFile object.</span></span>

<span data-ttu-id="abdb8-129">下表显示创建 groupPolicyUploadedDefinitionFile 时所需的属性。</span><span class="sxs-lookup"><span data-stu-id="abdb8-129">The following table shows the properties that are required when you create the groupPolicyUploadedDefinitionFile.</span></span>

|<span data-ttu-id="abdb8-130">属性</span><span class="sxs-lookup"><span data-stu-id="abdb8-130">Property</span></span>|<span data-ttu-id="abdb8-131">类型</span><span class="sxs-lookup"><span data-stu-id="abdb8-131">Type</span></span>|<span data-ttu-id="abdb8-132">说明</span><span class="sxs-lookup"><span data-stu-id="abdb8-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="abdb8-133">displayName</span><span class="sxs-lookup"><span data-stu-id="abdb8-133">displayName</span></span>|<span data-ttu-id="abdb8-134">字符串</span><span class="sxs-lookup"><span data-stu-id="abdb8-134">String</span></span>|<span data-ttu-id="abdb8-135">ADMX 文件的本地化友好名称。</span><span class="sxs-lookup"><span data-stu-id="abdb8-135">The localized friendly name of the ADMX file.</span></span> <span data-ttu-id="abdb8-136">继承自[groupPolicyDefinitionFile](../resources/intune-grouppolicy-grouppolicydefinitionfile.md)</span><span class="sxs-lookup"><span data-stu-id="abdb8-136">Inherited from [groupPolicyDefinitionFile](../resources/intune-grouppolicy-grouppolicydefinitionfile.md)</span></span>|
|<span data-ttu-id="abdb8-137">description</span><span class="sxs-lookup"><span data-stu-id="abdb8-137">description</span></span>|<span data-ttu-id="abdb8-138">String</span><span class="sxs-lookup"><span data-stu-id="abdb8-138">String</span></span>|<span data-ttu-id="abdb8-139">ADMX 文件中策略设置的本地化说明。</span><span class="sxs-lookup"><span data-stu-id="abdb8-139">The localized description of the policy settings in the ADMX file.</span></span> <span data-ttu-id="abdb8-140">默认值为空白。</span><span class="sxs-lookup"><span data-stu-id="abdb8-140">The default value is empty.</span></span> <span data-ttu-id="abdb8-141">继承自[groupPolicyDefinitionFile](../resources/intune-grouppolicy-grouppolicydefinitionfile.md)</span><span class="sxs-lookup"><span data-stu-id="abdb8-141">Inherited from [groupPolicyDefinitionFile](../resources/intune-grouppolicy-grouppolicydefinitionfile.md)</span></span>|
|<span data-ttu-id="abdb8-142">languageCodes</span><span class="sxs-lookup"><span data-stu-id="abdb8-142">languageCodes</span></span>|<span data-ttu-id="abdb8-143">String 集合</span><span class="sxs-lookup"><span data-stu-id="abdb8-143">String collection</span></span>|<span data-ttu-id="abdb8-144">ADMX 文件的受支持的语言代码。</span><span class="sxs-lookup"><span data-stu-id="abdb8-144">The supported language codes for the ADMX file.</span></span> <span data-ttu-id="abdb8-145">继承自[groupPolicyDefinitionFile](../resources/intune-grouppolicy-grouppolicydefinitionfile.md)</span><span class="sxs-lookup"><span data-stu-id="abdb8-145">Inherited from [groupPolicyDefinitionFile](../resources/intune-grouppolicy-grouppolicydefinitionfile.md)</span></span>|
|<span data-ttu-id="abdb8-146">targetPrefix</span><span class="sxs-lookup"><span data-stu-id="abdb8-146">targetPrefix</span></span>|<span data-ttu-id="abdb8-147">字符串</span><span class="sxs-lookup"><span data-stu-id="abdb8-147">String</span></span>|<span data-ttu-id="abdb8-148">指定在 ADMX 文件中引用命名空间的逻辑名称。</span><span class="sxs-lookup"><span data-stu-id="abdb8-148">Specifies the logical name that refers to the namespace within the ADMX file.</span></span> <span data-ttu-id="abdb8-149">继承自[groupPolicyDefinitionFile](../resources/intune-grouppolicy-grouppolicydefinitionfile.md)</span><span class="sxs-lookup"><span data-stu-id="abdb8-149">Inherited from [groupPolicyDefinitionFile](../resources/intune-grouppolicy-grouppolicydefinitionfile.md)</span></span>|
|<span data-ttu-id="abdb8-150">targetNamespace</span><span class="sxs-lookup"><span data-stu-id="abdb8-150">targetNamespace</span></span>|<span data-ttu-id="abdb8-151">字符串</span><span class="sxs-lookup"><span data-stu-id="abdb8-151">String</span></span>|<span data-ttu-id="abdb8-152">指定用于标识 ADMX 文件中的命名空间的 URI。</span><span class="sxs-lookup"><span data-stu-id="abdb8-152">Specifies the URI used to identify the namespace within the ADMX file.</span></span> <span data-ttu-id="abdb8-153">继承自[groupPolicyDefinitionFile](../resources/intune-grouppolicy-grouppolicydefinitionfile.md)</span><span class="sxs-lookup"><span data-stu-id="abdb8-153">Inherited from [groupPolicyDefinitionFile](../resources/intune-grouppolicy-grouppolicydefinitionfile.md)</span></span>|
|<span data-ttu-id="abdb8-154">policyType</span><span class="sxs-lookup"><span data-stu-id="abdb8-154">policyType</span></span>|[<span data-ttu-id="abdb8-155">groupPolicyType</span><span class="sxs-lookup"><span data-stu-id="abdb8-155">groupPolicyType</span></span>](../resources/intune-grouppolicy-grouppolicytype.md)|<span data-ttu-id="abdb8-156">指定组策略的类型。</span><span class="sxs-lookup"><span data-stu-id="abdb8-156">Specifies the type of group policy.</span></span> <span data-ttu-id="abdb8-157">继承自[groupPolicyDefinitionFile](../resources/intune-grouppolicy-grouppolicydefinitionfile.md)。</span><span class="sxs-lookup"><span data-stu-id="abdb8-157">Inherited from [groupPolicyDefinitionFile](../resources/intune-grouppolicy-grouppolicydefinitionfile.md).</span></span> <span data-ttu-id="abdb8-158">可取值为：`admxBacked`、`admxIngested`。</span><span class="sxs-lookup"><span data-stu-id="abdb8-158">Possible values are: `admxBacked`, `admxIngested`.</span></span>|
|<span data-ttu-id="abdb8-159">a01</span><span class="sxs-lookup"><span data-stu-id="abdb8-159">revision</span></span>|<span data-ttu-id="abdb8-160">字符串</span><span class="sxs-lookup"><span data-stu-id="abdb8-160">String</span></span>|<span data-ttu-id="abdb8-161">与文件关联的修订版本。</span><span class="sxs-lookup"><span data-stu-id="abdb8-161">The revision version associated with the file.</span></span> <span data-ttu-id="abdb8-162">继承自[groupPolicyDefinitionFile](../resources/intune-grouppolicy-grouppolicydefinitionfile.md)</span><span class="sxs-lookup"><span data-stu-id="abdb8-162">Inherited from [groupPolicyDefinitionFile](../resources/intune-grouppolicy-grouppolicydefinitionfile.md)</span></span>|
|<span data-ttu-id="abdb8-163">id</span><span class="sxs-lookup"><span data-stu-id="abdb8-163">id</span></span>|<span data-ttu-id="abdb8-164">字符串</span><span class="sxs-lookup"><span data-stu-id="abdb8-164">String</span></span>|<span data-ttu-id="abdb8-165">实体的键。</span><span class="sxs-lookup"><span data-stu-id="abdb8-165">Key of the entity.</span></span> <span data-ttu-id="abdb8-166">继承自[groupPolicyDefinitionFile](../resources/intune-grouppolicy-grouppolicydefinitionfile.md)</span><span class="sxs-lookup"><span data-stu-id="abdb8-166">Inherited from [groupPolicyDefinitionFile](../resources/intune-grouppolicy-grouppolicydefinitionfile.md)</span></span>|
|<span data-ttu-id="abdb8-167">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="abdb8-167">lastModifiedDateTime</span></span>|<span data-ttu-id="abdb8-168">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="abdb8-168">DateTimeOffset</span></span>|<span data-ttu-id="abdb8-169">上次修改实体的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="abdb8-169">The date and time the entity was last modified.</span></span> <span data-ttu-id="abdb8-170">继承自[groupPolicyDefinitionFile](../resources/intune-grouppolicy-grouppolicydefinitionfile.md)</span><span class="sxs-lookup"><span data-stu-id="abdb8-170">Inherited from [groupPolicyDefinitionFile](../resources/intune-grouppolicy-grouppolicydefinitionfile.md)</span></span>|
|<span data-ttu-id="abdb8-171">fileName</span><span class="sxs-lookup"><span data-stu-id="abdb8-171">fileName</span></span>|<span data-ttu-id="abdb8-172">String</span><span class="sxs-lookup"><span data-stu-id="abdb8-172">String</span></span>|<span data-ttu-id="abdb8-173">上传的 ADML 文件的文件名。</span><span class="sxs-lookup"><span data-stu-id="abdb8-173">The file name of the uploaded ADML file.</span></span>|
|<span data-ttu-id="abdb8-174">状态</span><span class="sxs-lookup"><span data-stu-id="abdb8-174">status</span></span>|[<span data-ttu-id="abdb8-175">groupPolicyUploadedDefinitionFileStatus</span><span class="sxs-lookup"><span data-stu-id="abdb8-175">groupPolicyUploadedDefinitionFileStatus</span></span>](../resources/intune-grouppolicy-grouppolicyuploadeddefinitionfilestatus.md)|<span data-ttu-id="abdb8-176">已上载的 ADMX 文件的上载状态。</span><span class="sxs-lookup"><span data-stu-id="abdb8-176">The upload status of the uploaded ADMX file.</span></span> <span data-ttu-id="abdb8-177">可取值为：`none`、`uploadInProgress`、`available`、`assigned`、`removalInProgress`、`uploadFailed` 或 `removalFailed`。</span><span class="sxs-lookup"><span data-stu-id="abdb8-177">Possible values are: `none`, `uploadInProgress`, `available`, `assigned`, `removalInProgress`, `uploadFailed`, `removalFailed`.</span></span>|
|<span data-ttu-id="abdb8-178">content</span><span class="sxs-lookup"><span data-stu-id="abdb8-178">content</span></span>|<span data-ttu-id="abdb8-179">Binary</span><span class="sxs-lookup"><span data-stu-id="abdb8-179">Binary</span></span>|<span data-ttu-id="abdb8-180">已上载的 ADMX 文件的内容。</span><span class="sxs-lookup"><span data-stu-id="abdb8-180">The contents of the uploaded ADMX file.</span></span>|
|<span data-ttu-id="abdb8-181">uploadDateTime</span><span class="sxs-lookup"><span data-stu-id="abdb8-181">uploadDateTime</span></span>|<span data-ttu-id="abdb8-182">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="abdb8-182">DateTimeOffset</span></span>|<span data-ttu-id="abdb8-183">上载的 ADMX 文件的上载时间。</span><span class="sxs-lookup"><span data-stu-id="abdb8-183">The uploaded time of the uploaded ADMX file.</span></span>|
|<span data-ttu-id="abdb8-184">defaultLanguageCode</span><span class="sxs-lookup"><span data-stu-id="abdb8-184">defaultLanguageCode</span></span>|<span data-ttu-id="abdb8-185">字符串</span><span class="sxs-lookup"><span data-stu-id="abdb8-185">String</span></span>|<span data-ttu-id="abdb8-186">上载的 ADMX 文件的默认语言。</span><span class="sxs-lookup"><span data-stu-id="abdb8-186">The default language of the uploaded ADMX file.</span></span>|
|<span data-ttu-id="abdb8-187">groupPolicyUploadedLanguageFiles</span><span class="sxs-lookup"><span data-stu-id="abdb8-187">groupPolicyUploadedLanguageFiles</span></span>|<span data-ttu-id="abdb8-188">[groupPolicyUploadedLanguageFile](../resources/intune-grouppolicy-grouppolicyuploadedlanguagefile.md)集合</span><span class="sxs-lookup"><span data-stu-id="abdb8-188">[groupPolicyUploadedLanguageFile](../resources/intune-grouppolicy-grouppolicyuploadedlanguagefile.md) collection</span></span>|<span data-ttu-id="abdb8-189">与上载的 ADMX 文件关联的 ADML 文件的列表。</span><span class="sxs-lookup"><span data-stu-id="abdb8-189">The list of ADML files associated with the uploaded ADMX file.</span></span>|



## <a name="response"></a><span data-ttu-id="abdb8-190">响应</span><span class="sxs-lookup"><span data-stu-id="abdb8-190">Response</span></span>
<span data-ttu-id="abdb8-191">如果成功，此方法在响应`201 Created`正文中返回响应代码和[groupPolicyUploadedDefinitionFile](../resources/intune-grouppolicy-grouppolicyuploadeddefinitionfile.md)对象。</span><span class="sxs-lookup"><span data-stu-id="abdb8-191">If successful, this method returns a `201 Created` response code and a [groupPolicyUploadedDefinitionFile](../resources/intune-grouppolicy-grouppolicyuploadeddefinitionfile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="abdb8-192">示例</span><span class="sxs-lookup"><span data-stu-id="abdb8-192">Example</span></span>

### <a name="request"></a><span data-ttu-id="abdb8-193">请求</span><span class="sxs-lookup"><span data-stu-id="abdb8-193">Request</span></span>
<span data-ttu-id="abdb8-194">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="abdb8-194">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/groupPolicyUploadedDefinitionFiles
Content-type: application/json
Content-length: 922

{
  "@odata.type": "#microsoft.graph.groupPolicyUploadedDefinitionFile",
  "displayName": "Display Name value",
  "description": "Description value",
  "languageCodes": [
    "Language Codes value"
  ],
  "targetPrefix": "Target Prefix value",
  "targetNamespace": "Target Namespace value",
  "policyType": "admxIngested",
  "revision": "Revision value",
  "fileName": "File Name value",
  "status": "uploadInProgress",
  "content": "Y29udGVudA==",
  "uploadDateTime": "2016-12-31T23:58:46.5747426-08:00",
  "defaultLanguageCode": "Default Language Code value",
  "groupPolicyUploadedLanguageFiles": [
    {
      "@odata.type": "microsoft.graph.groupPolicyUploadedLanguageFile",
      "fileName": "File Name value",
      "languageCode": "Language Code value",
      "content": "Y29udGVudA==",
      "id": "Id value",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00"
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="abdb8-195">响应</span><span class="sxs-lookup"><span data-stu-id="abdb8-195">Response</span></span>
<span data-ttu-id="abdb8-p112">下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="abdb8-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1035

{
  "@odata.type": "#microsoft.graph.groupPolicyUploadedDefinitionFile",
  "displayName": "Display Name value",
  "description": "Description value",
  "languageCodes": [
    "Language Codes value"
  ],
  "targetPrefix": "Target Prefix value",
  "targetNamespace": "Target Namespace value",
  "policyType": "admxIngested",
  "revision": "Revision value",
  "id": "0ce1a8cf-a8cf-0ce1-cfa8-e10ccfa8e10c",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "fileName": "File Name value",
  "status": "uploadInProgress",
  "content": "Y29udGVudA==",
  "uploadDateTime": "2016-12-31T23:58:46.5747426-08:00",
  "defaultLanguageCode": "Default Language Code value",
  "groupPolicyUploadedLanguageFiles": [
    {
      "@odata.type": "microsoft.graph.groupPolicyUploadedLanguageFile",
      "fileName": "File Name value",
      "languageCode": "Language Code value",
      "content": "Y29udGVudA==",
      "id": "Id value",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00"
    }
  ]
}
```


