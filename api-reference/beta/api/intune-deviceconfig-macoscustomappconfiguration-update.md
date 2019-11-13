---
title: 更新 macOSCustomAppConfiguration
description: 更新 macOSCustomAppConfiguration 对象的属性。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 97f42012f093c0dfa33fc67cb12bea8e2dabba18
ms.sourcegitcommit: 5b1fad41067629d0e9f87746328664bb248f754f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/09/2019
ms.locfileid: "38084277"
---
# <a name="update-macoscustomappconfiguration"></a><span data-ttu-id="0da26-103">更新 macOSCustomAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="0da26-103">Update macOSCustomAppConfiguration</span></span>

> <span data-ttu-id="0da26-104">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="0da26-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="0da26-105">**注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="0da26-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="0da26-106">更新[macOSCustomAppConfiguration](../resources/intune-deviceconfig-macoscustomappconfiguration.md)对象的属性。</span><span class="sxs-lookup"><span data-stu-id="0da26-106">Update the properties of a [macOSCustomAppConfiguration](../resources/intune-deviceconfig-macoscustomappconfiguration.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0da26-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="0da26-107">Prerequisites</span></span>
<span data-ttu-id="0da26-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="0da26-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0da26-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="0da26-110">Permission type</span></span>|<span data-ttu-id="0da26-111">权限（从最高特权到最低特权）</span><span class="sxs-lookup"><span data-stu-id="0da26-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0da26-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="0da26-112">Delegated (work or school account)</span></span>|<span data-ttu-id="0da26-113">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0da26-113">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="0da26-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="0da26-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0da26-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="0da26-115">Not supported.</span></span>|
|<span data-ttu-id="0da26-116">应用程序</span><span class="sxs-lookup"><span data-stu-id="0da26-116">Application</span></span>|<span data-ttu-id="0da26-117">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0da26-117">DeviceManagementConfiguration.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="0da26-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="0da26-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="0da26-119">请求标头</span><span class="sxs-lookup"><span data-stu-id="0da26-119">Request headers</span></span>
|<span data-ttu-id="0da26-120">标头</span><span class="sxs-lookup"><span data-stu-id="0da26-120">Header</span></span>|<span data-ttu-id="0da26-121">值</span><span class="sxs-lookup"><span data-stu-id="0da26-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0da26-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="0da26-122">Authorization</span></span>|<span data-ttu-id="0da26-123">Bearer &lt;token&gt;。必需。</span><span class="sxs-lookup"><span data-stu-id="0da26-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0da26-124">接受</span><span class="sxs-lookup"><span data-stu-id="0da26-124">Accept</span></span>|<span data-ttu-id="0da26-125">application/json</span><span class="sxs-lookup"><span data-stu-id="0da26-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0da26-126">请求正文</span><span class="sxs-lookup"><span data-stu-id="0da26-126">Request body</span></span>
<span data-ttu-id="0da26-127">在请求正文中，提供[macOSCustomAppConfiguration](../resources/intune-deviceconfig-macoscustomappconfiguration.md)对象的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="0da26-127">In the request body, supply a JSON representation for the [macOSCustomAppConfiguration](../resources/intune-deviceconfig-macoscustomappconfiguration.md) object.</span></span>

<span data-ttu-id="0da26-128">下表显示创建[macOSCustomAppConfiguration](../resources/intune-deviceconfig-macoscustomappconfiguration.md)时所需的属性。</span><span class="sxs-lookup"><span data-stu-id="0da26-128">The following table shows the properties that are required when you create the [macOSCustomAppConfiguration](../resources/intune-deviceconfig-macoscustomappconfiguration.md).</span></span>

|<span data-ttu-id="0da26-129">属性</span><span class="sxs-lookup"><span data-stu-id="0da26-129">Property</span></span>|<span data-ttu-id="0da26-130">类型</span><span class="sxs-lookup"><span data-stu-id="0da26-130">Type</span></span>|<span data-ttu-id="0da26-131">描述</span><span class="sxs-lookup"><span data-stu-id="0da26-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0da26-132">id</span><span class="sxs-lookup"><span data-stu-id="0da26-132">id</span></span>|<span data-ttu-id="0da26-133">字符串</span><span class="sxs-lookup"><span data-stu-id="0da26-133">String</span></span>|<span data-ttu-id="0da26-134">实体的键。</span><span class="sxs-lookup"><span data-stu-id="0da26-134">Key of the entity.</span></span> <span data-ttu-id="0da26-135">继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0da26-135">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0da26-136">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="0da26-136">lastModifiedDateTime</span></span>|<span data-ttu-id="0da26-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0da26-137">DateTimeOffset</span></span>|<span data-ttu-id="0da26-138">上次修改对象的日期/时间。</span><span class="sxs-lookup"><span data-stu-id="0da26-138">DateTime the object was last modified.</span></span> <span data-ttu-id="0da26-139">继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0da26-139">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0da26-140">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="0da26-140">roleScopeTagIds</span></span>|<span data-ttu-id="0da26-141">String collection</span><span class="sxs-lookup"><span data-stu-id="0da26-141">String collection</span></span>|<span data-ttu-id="0da26-142">此实体实例的范围标记列表。</span><span class="sxs-lookup"><span data-stu-id="0da26-142">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="0da26-143">继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0da26-143">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0da26-144">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="0da26-144">supportsScopeTags</span></span>|<span data-ttu-id="0da26-145">Boolean</span><span class="sxs-lookup"><span data-stu-id="0da26-145">Boolean</span></span>|<span data-ttu-id="0da26-146">指示基础设备配置是否支持作用域标记的分配。</span><span class="sxs-lookup"><span data-stu-id="0da26-146">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="0da26-147">如果此值为 false，则不允许分配给 ScopeTags 属性，并且实体将对作用域用户不可见。</span><span class="sxs-lookup"><span data-stu-id="0da26-147">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="0da26-148">这适用于在 Silverlight 中创建的旧版策略，可以通过在 Azure 门户中删除并重新创建策略来解决此事件。</span><span class="sxs-lookup"><span data-stu-id="0da26-148">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="0da26-149">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="0da26-149">This property is read-only.</span></span> <span data-ttu-id="0da26-150">继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0da26-150">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0da26-151">deviceManagementApplicabilityRuleOsEdition</span><span class="sxs-lookup"><span data-stu-id="0da26-151">deviceManagementApplicabilityRuleOsEdition</span></span>|[<span data-ttu-id="0da26-152">deviceManagementApplicabilityRuleOsEdition</span><span class="sxs-lookup"><span data-stu-id="0da26-152">deviceManagementApplicabilityRuleOsEdition</span></span>](../resources/intune-deviceconfig-devicemanagementapplicabilityruleosedition.md)|<span data-ttu-id="0da26-153">适用于此策略的操作系统版本。</span><span class="sxs-lookup"><span data-stu-id="0da26-153">The OS edition applicability for this Policy.</span></span> <span data-ttu-id="0da26-154">继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0da26-154">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0da26-155">deviceManagementApplicabilityRuleOsVersion</span><span class="sxs-lookup"><span data-stu-id="0da26-155">deviceManagementApplicabilityRuleOsVersion</span></span>|[<span data-ttu-id="0da26-156">deviceManagementApplicabilityRuleOsVersion</span><span class="sxs-lookup"><span data-stu-id="0da26-156">deviceManagementApplicabilityRuleOsVersion</span></span>](../resources/intune-deviceconfig-devicemanagementapplicabilityruleosversion.md)|<span data-ttu-id="0da26-157">此策略的操作系统版本适用性规则。</span><span class="sxs-lookup"><span data-stu-id="0da26-157">The OS version applicability rule for this Policy.</span></span> <span data-ttu-id="0da26-158">继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0da26-158">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0da26-159">deviceManagementApplicabilityRuleDeviceMode</span><span class="sxs-lookup"><span data-stu-id="0da26-159">deviceManagementApplicabilityRuleDeviceMode</span></span>|[<span data-ttu-id="0da26-160">deviceManagementApplicabilityRuleDeviceMode</span><span class="sxs-lookup"><span data-stu-id="0da26-160">deviceManagementApplicabilityRuleDeviceMode</span></span>](../resources/intune-deviceconfig-devicemanagementapplicabilityruledevicemode.md)|<span data-ttu-id="0da26-161">此策略的设备模式适用性规则。</span><span class="sxs-lookup"><span data-stu-id="0da26-161">The device mode applicability rule for this Policy.</span></span> <span data-ttu-id="0da26-162">继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0da26-162">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0da26-163">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="0da26-163">createdDateTime</span></span>|<span data-ttu-id="0da26-164">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0da26-164">DateTimeOffset</span></span>|<span data-ttu-id="0da26-165">创建对象的日期/时间。</span><span class="sxs-lookup"><span data-stu-id="0da26-165">DateTime the object was created.</span></span> <span data-ttu-id="0da26-166">继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0da26-166">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0da26-167">说明</span><span class="sxs-lookup"><span data-stu-id="0da26-167">description</span></span>|<span data-ttu-id="0da26-168">String</span><span class="sxs-lookup"><span data-stu-id="0da26-168">String</span></span>|<span data-ttu-id="0da26-169">管理员提供的设备配置的说明。</span><span class="sxs-lookup"><span data-stu-id="0da26-169">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="0da26-170">继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0da26-170">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0da26-171">displayName</span><span class="sxs-lookup"><span data-stu-id="0da26-171">displayName</span></span>|<span data-ttu-id="0da26-172">String</span><span class="sxs-lookup"><span data-stu-id="0da26-172">String</span></span>|<span data-ttu-id="0da26-173">管理员提供的设备配置的名称。</span><span class="sxs-lookup"><span data-stu-id="0da26-173">Admin provided name of the device configuration.</span></span> <span data-ttu-id="0da26-174">继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0da26-174">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0da26-175">version</span><span class="sxs-lookup"><span data-stu-id="0da26-175">version</span></span>|<span data-ttu-id="0da26-176">Int32</span><span class="sxs-lookup"><span data-stu-id="0da26-176">Int32</span></span>|<span data-ttu-id="0da26-177">设备配置的版本。</span><span class="sxs-lookup"><span data-stu-id="0da26-177">Version of the device configuration.</span></span> <span data-ttu-id="0da26-178">继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0da26-178">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0da26-179">bundleId</span><span class="sxs-lookup"><span data-stu-id="0da26-179">bundleId</span></span>|<span data-ttu-id="0da26-180">String</span><span class="sxs-lookup"><span data-stu-id="0da26-180">String</span></span>|<span data-ttu-id="0da26-181">目标的捆绑包 id。</span><span class="sxs-lookup"><span data-stu-id="0da26-181">Bundle id for targeting.</span></span>|
|<span data-ttu-id="0da26-182">fileName</span><span class="sxs-lookup"><span data-stu-id="0da26-182">fileName</span></span>|<span data-ttu-id="0da26-183">String</span><span class="sxs-lookup"><span data-stu-id="0da26-183">String</span></span>|<span data-ttu-id="0da26-184">配置文件名（\* plist</span><span class="sxs-lookup"><span data-stu-id="0da26-184">Configuration file name (\*.plist</span></span> | <span data-ttu-id="0da26-185">\*.xml)。</span><span class="sxs-lookup"><span data-stu-id="0da26-185">\*.xml).</span></span>|
|<span data-ttu-id="0da26-186">configurationXml</span><span class="sxs-lookup"><span data-stu-id="0da26-186">configurationXml</span></span>|<span data-ttu-id="0da26-187">Binary</span><span class="sxs-lookup"><span data-stu-id="0da26-187">Binary</span></span>|<span data-ttu-id="0da26-188">配置 xml。</span><span class="sxs-lookup"><span data-stu-id="0da26-188">Configuration xml.</span></span> <span data-ttu-id="0da26-189">（UTF8 编码的字节数组）</span><span class="sxs-lookup"><span data-stu-id="0da26-189">(UTF8 encoded byte array)</span></span>|



## <a name="response"></a><span data-ttu-id="0da26-190">响应</span><span class="sxs-lookup"><span data-stu-id="0da26-190">Response</span></span>
<span data-ttu-id="0da26-191">如果成功，此方法在响应`200 OK`正文中返回响应代码和更新的[macOSCustomAppConfiguration](../resources/intune-deviceconfig-macoscustomappconfiguration.md)对象。</span><span class="sxs-lookup"><span data-stu-id="0da26-191">If successful, this method returns a `200 OK` response code and an updated [macOSCustomAppConfiguration](../resources/intune-deviceconfig-macoscustomappconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0da26-192">示例</span><span class="sxs-lookup"><span data-stu-id="0da26-192">Example</span></span>

### <a name="request"></a><span data-ttu-id="0da26-193">请求</span><span class="sxs-lookup"><span data-stu-id="0da26-193">Request</span></span>
<span data-ttu-id="0da26-194">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="0da26-194">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 1149

{
  "@odata.type": "#microsoft.graph.macOSCustomAppConfiguration",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "deviceManagementApplicabilityRuleOsEdition": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleOsEdition",
    "osEditionTypes": [
      "windows10EnterpriseN"
    ],
    "name": "Name value",
    "ruleType": "exclude"
  },
  "deviceManagementApplicabilityRuleOsVersion": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleOsVersion",
    "minOSVersion": "Min OSVersion value",
    "maxOSVersion": "Max OSVersion value",
    "name": "Name value",
    "ruleType": "exclude"
  },
  "deviceManagementApplicabilityRuleDeviceMode": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleDeviceMode",
    "deviceMode": "sModeConfiguration",
    "name": "Name value",
    "ruleType": "exclude"
  },
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "bundleId": "Bundle Id value",
  "fileName": "File Name value",
  "configurationXml": "Y29uZmlndXJhdGlvblhtbA=="
}
```

### <a name="response"></a><span data-ttu-id="0da26-195">响应</span><span class="sxs-lookup"><span data-stu-id="0da26-195">Response</span></span>
<span data-ttu-id="0da26-p114">下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="0da26-p114">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1321

{
  "@odata.type": "#microsoft.graph.macOSCustomAppConfiguration",
  "id": "1b8a4e02-4e02-1b8a-024e-8a1b024e8a1b",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "deviceManagementApplicabilityRuleOsEdition": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleOsEdition",
    "osEditionTypes": [
      "windows10EnterpriseN"
    ],
    "name": "Name value",
    "ruleType": "exclude"
  },
  "deviceManagementApplicabilityRuleOsVersion": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleOsVersion",
    "minOSVersion": "Min OSVersion value",
    "maxOSVersion": "Max OSVersion value",
    "name": "Name value",
    "ruleType": "exclude"
  },
  "deviceManagementApplicabilityRuleDeviceMode": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleDeviceMode",
    "deviceMode": "sModeConfiguration",
    "name": "Name value",
    "ruleType": "exclude"
  },
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "bundleId": "Bundle Id value",
  "fileName": "File Name value",
  "configurationXml": "Y29uZmlndXJhdGlvblhtbA=="
}
```





