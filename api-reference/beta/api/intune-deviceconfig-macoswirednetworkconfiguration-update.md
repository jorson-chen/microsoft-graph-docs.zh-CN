---
title: 更新 macOSWiredNetworkConfiguration
description: 更新 macOSWiredNetworkConfiguration 对象的属性。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 787348435f34381a56965d7a752fae5fd7222a55
ms.sourcegitcommit: 5b1fad41067629d0e9f87746328664bb248f754f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/09/2019
ms.locfileid: "38084200"
---
# <a name="update-macoswirednetworkconfiguration"></a><span data-ttu-id="ce2d5-103">更新 macOSWiredNetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce2d5-103">Update macOSWiredNetworkConfiguration</span></span>

> <span data-ttu-id="ce2d5-104">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="ce2d5-105">**注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="ce2d5-106">更新[macOSWiredNetworkConfiguration](../resources/intune-deviceconfig-macoswirednetworkconfiguration.md)对象的属性。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-106">Update the properties of a [macOSWiredNetworkConfiguration](../resources/intune-deviceconfig-macoswirednetworkconfiguration.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ce2d5-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="ce2d5-107">Prerequisites</span></span>
<span data-ttu-id="ce2d5-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ce2d5-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="ce2d5-110">Permission type</span></span>|<span data-ttu-id="ce2d5-111">权限（从最高特权到最低特权）</span><span class="sxs-lookup"><span data-stu-id="ce2d5-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ce2d5-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="ce2d5-112">Delegated (work or school account)</span></span>|<span data-ttu-id="ce2d5-113">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ce2d5-113">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="ce2d5-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="ce2d5-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ce2d5-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-115">Not supported.</span></span>|
|<span data-ttu-id="ce2d5-116">应用程序</span><span class="sxs-lookup"><span data-stu-id="ce2d5-116">Application</span></span>|<span data-ttu-id="ce2d5-117">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ce2d5-117">DeviceManagementConfiguration.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="ce2d5-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="ce2d5-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="ce2d5-119">请求标头</span><span class="sxs-lookup"><span data-stu-id="ce2d5-119">Request headers</span></span>
|<span data-ttu-id="ce2d5-120">标头</span><span class="sxs-lookup"><span data-stu-id="ce2d5-120">Header</span></span>|<span data-ttu-id="ce2d5-121">值</span><span class="sxs-lookup"><span data-stu-id="ce2d5-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ce2d5-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="ce2d5-122">Authorization</span></span>|<span data-ttu-id="ce2d5-123">Bearer &lt;token&gt;。必需。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ce2d5-124">接受</span><span class="sxs-lookup"><span data-stu-id="ce2d5-124">Accept</span></span>|<span data-ttu-id="ce2d5-125">application/json</span><span class="sxs-lookup"><span data-stu-id="ce2d5-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ce2d5-126">请求正文</span><span class="sxs-lookup"><span data-stu-id="ce2d5-126">Request body</span></span>
<span data-ttu-id="ce2d5-127">在请求正文中，提供[macOSWiredNetworkConfiguration](../resources/intune-deviceconfig-macoswirednetworkconfiguration.md)对象的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-127">In the request body, supply a JSON representation for the [macOSWiredNetworkConfiguration](../resources/intune-deviceconfig-macoswirednetworkconfiguration.md) object.</span></span>

<span data-ttu-id="ce2d5-128">下表显示创建[macOSWiredNetworkConfiguration](../resources/intune-deviceconfig-macoswirednetworkconfiguration.md)时所需的属性。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-128">The following table shows the properties that are required when you create the [macOSWiredNetworkConfiguration](../resources/intune-deviceconfig-macoswirednetworkconfiguration.md).</span></span>

|<span data-ttu-id="ce2d5-129">属性</span><span class="sxs-lookup"><span data-stu-id="ce2d5-129">Property</span></span>|<span data-ttu-id="ce2d5-130">类型</span><span class="sxs-lookup"><span data-stu-id="ce2d5-130">Type</span></span>|<span data-ttu-id="ce2d5-131">描述</span><span class="sxs-lookup"><span data-stu-id="ce2d5-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ce2d5-132">id</span><span class="sxs-lookup"><span data-stu-id="ce2d5-132">id</span></span>|<span data-ttu-id="ce2d5-133">字符串</span><span class="sxs-lookup"><span data-stu-id="ce2d5-133">String</span></span>|<span data-ttu-id="ce2d5-134">实体的键。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-134">Key of the entity.</span></span> <span data-ttu-id="ce2d5-135">继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ce2d5-135">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ce2d5-136">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="ce2d5-136">lastModifiedDateTime</span></span>|<span data-ttu-id="ce2d5-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ce2d5-137">DateTimeOffset</span></span>|<span data-ttu-id="ce2d5-138">上次修改对象的日期/时间。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-138">DateTime the object was last modified.</span></span> <span data-ttu-id="ce2d5-139">继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ce2d5-139">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ce2d5-140">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="ce2d5-140">roleScopeTagIds</span></span>|<span data-ttu-id="ce2d5-141">String collection</span><span class="sxs-lookup"><span data-stu-id="ce2d5-141">String collection</span></span>|<span data-ttu-id="ce2d5-142">此实体实例的范围标记列表。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-142">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="ce2d5-143">继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ce2d5-143">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ce2d5-144">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="ce2d5-144">supportsScopeTags</span></span>|<span data-ttu-id="ce2d5-145">Boolean</span><span class="sxs-lookup"><span data-stu-id="ce2d5-145">Boolean</span></span>|<span data-ttu-id="ce2d5-146">指示基础设备配置是否支持作用域标记的分配。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-146">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="ce2d5-147">如果此值为 false，则不允许分配给 ScopeTags 属性，并且实体将对作用域用户不可见。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-147">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="ce2d5-148">这适用于在 Silverlight 中创建的旧版策略，可以通过在 Azure 门户中删除并重新创建策略来解决此事件。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-148">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="ce2d5-149">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-149">This property is read-only.</span></span> <span data-ttu-id="ce2d5-150">继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ce2d5-150">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ce2d5-151">deviceManagementApplicabilityRuleOsEdition</span><span class="sxs-lookup"><span data-stu-id="ce2d5-151">deviceManagementApplicabilityRuleOsEdition</span></span>|[<span data-ttu-id="ce2d5-152">deviceManagementApplicabilityRuleOsEdition</span><span class="sxs-lookup"><span data-stu-id="ce2d5-152">deviceManagementApplicabilityRuleOsEdition</span></span>](../resources/intune-deviceconfig-devicemanagementapplicabilityruleosedition.md)|<span data-ttu-id="ce2d5-153">适用于此策略的操作系统版本。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-153">The OS edition applicability for this Policy.</span></span> <span data-ttu-id="ce2d5-154">继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ce2d5-154">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ce2d5-155">deviceManagementApplicabilityRuleOsVersion</span><span class="sxs-lookup"><span data-stu-id="ce2d5-155">deviceManagementApplicabilityRuleOsVersion</span></span>|[<span data-ttu-id="ce2d5-156">deviceManagementApplicabilityRuleOsVersion</span><span class="sxs-lookup"><span data-stu-id="ce2d5-156">deviceManagementApplicabilityRuleOsVersion</span></span>](../resources/intune-deviceconfig-devicemanagementapplicabilityruleosversion.md)|<span data-ttu-id="ce2d5-157">此策略的操作系统版本适用性规则。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-157">The OS version applicability rule for this Policy.</span></span> <span data-ttu-id="ce2d5-158">继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ce2d5-158">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ce2d5-159">deviceManagementApplicabilityRuleDeviceMode</span><span class="sxs-lookup"><span data-stu-id="ce2d5-159">deviceManagementApplicabilityRuleDeviceMode</span></span>|[<span data-ttu-id="ce2d5-160">deviceManagementApplicabilityRuleDeviceMode</span><span class="sxs-lookup"><span data-stu-id="ce2d5-160">deviceManagementApplicabilityRuleDeviceMode</span></span>](../resources/intune-deviceconfig-devicemanagementapplicabilityruledevicemode.md)|<span data-ttu-id="ce2d5-161">此策略的设备模式适用性规则。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-161">The device mode applicability rule for this Policy.</span></span> <span data-ttu-id="ce2d5-162">继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ce2d5-162">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ce2d5-163">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="ce2d5-163">createdDateTime</span></span>|<span data-ttu-id="ce2d5-164">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ce2d5-164">DateTimeOffset</span></span>|<span data-ttu-id="ce2d5-165">创建对象的日期/时间。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-165">DateTime the object was created.</span></span> <span data-ttu-id="ce2d5-166">继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ce2d5-166">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ce2d5-167">说明</span><span class="sxs-lookup"><span data-stu-id="ce2d5-167">description</span></span>|<span data-ttu-id="ce2d5-168">String</span><span class="sxs-lookup"><span data-stu-id="ce2d5-168">String</span></span>|<span data-ttu-id="ce2d5-169">管理员提供的设备配置的说明。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-169">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="ce2d5-170">继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ce2d5-170">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ce2d5-171">displayName</span><span class="sxs-lookup"><span data-stu-id="ce2d5-171">displayName</span></span>|<span data-ttu-id="ce2d5-172">String</span><span class="sxs-lookup"><span data-stu-id="ce2d5-172">String</span></span>|<span data-ttu-id="ce2d5-173">管理员提供的设备配置的名称。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-173">Admin provided name of the device configuration.</span></span> <span data-ttu-id="ce2d5-174">继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ce2d5-174">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ce2d5-175">version</span><span class="sxs-lookup"><span data-stu-id="ce2d5-175">version</span></span>|<span data-ttu-id="ce2d5-176">Int32</span><span class="sxs-lookup"><span data-stu-id="ce2d5-176">Int32</span></span>|<span data-ttu-id="ce2d5-177">设备配置的版本。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-177">Version of the device configuration.</span></span> <span data-ttu-id="ce2d5-178">继承自 [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ce2d5-178">Inherited from [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ce2d5-179">networkName</span><span class="sxs-lookup"><span data-stu-id="ce2d5-179">networkName</span></span>|<span data-ttu-id="ce2d5-180">String</span><span class="sxs-lookup"><span data-stu-id="ce2d5-180">String</span></span>|<span data-ttu-id="ce2d5-181">网络名称</span><span class="sxs-lookup"><span data-stu-id="ce2d5-181">Network Name</span></span>|
|<span data-ttu-id="ce2d5-182">networkInterface</span><span class="sxs-lookup"><span data-stu-id="ce2d5-182">networkInterface</span></span>|[<span data-ttu-id="ce2d5-183">wiredNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ce2d5-183">wiredNetworkInterface</span></span>](../resources/intune-deviceconfig-wirednetworkinterface.md)|<span data-ttu-id="ce2d5-184">网络接口。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-184">Network interface.</span></span> <span data-ttu-id="ce2d5-185">可取值为：`anyEthernet`、`firstActiveEthernet`、`secondActiveEthernet`、`thirdActiveEthernet`、`firstEthernet`、`secondEthernet` 或 `thirdEthernet`。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-185">Possible values are: `anyEthernet`, `firstActiveEthernet`, `secondActiveEthernet`, `thirdActiveEthernet`, `firstEthernet`, `secondEthernet`, `thirdEthernet`.</span></span>|
|<span data-ttu-id="ce2d5-186">eapType</span><span class="sxs-lookup"><span data-stu-id="ce2d5-186">eapType</span></span>|[<span data-ttu-id="ce2d5-187">eapType</span><span class="sxs-lookup"><span data-stu-id="ce2d5-187">eapType</span></span>](../resources/intune-deviceconfig-eaptype.md)|<span data-ttu-id="ce2d5-188">可扩展的身份验证协议（EAP）。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-188">Extensible Authentication Protocol (EAP).</span></span> <span data-ttu-id="ce2d5-189">指示有线网络上的 EAP 协议集的类型。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-189">Indicates the type of EAP protocol set on the wired network.</span></span> <span data-ttu-id="ce2d5-190">可取值为：`eapTls`、`leap`、`eapSim`、`eapTtls`、`peap`、`eapFast`。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-190">Possible values are: `eapTls`, `leap`, `eapSim`, `eapTtls`, `peap`, `eapFast`.</span></span>|
|<span data-ttu-id="ce2d5-191">eapFastConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce2d5-191">eapFastConfiguration</span></span>|[<span data-ttu-id="ce2d5-192">eapFastConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce2d5-192">eapFastConfiguration</span></span>](../resources/intune-deviceconfig-eapfastconfiguration.md)|<span data-ttu-id="ce2d5-193">EAP-FAST 配置选项，当 EAP-FAST 是所选的 EAP 类型时。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-193">EAP-FAST Configuration Option when EAP-FAST is the selected EAP Type.</span></span> <span data-ttu-id="ce2d5-194">可取值为：`noProtectedAccessCredential`、`useProtectedAccessCredential`、`useProtectedAccessCredentialAndProvision`、`useProtectedAccessCredentialAndProvisionAnonymously`。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-194">Possible values are: `noProtectedAccessCredential`, `useProtectedAccessCredential`, `useProtectedAccessCredentialAndProvision`, `useProtectedAccessCredentialAndProvisionAnonymously`.</span></span>|
|<span data-ttu-id="ce2d5-195">trustedServerCertificateNames</span><span class="sxs-lookup"><span data-stu-id="ce2d5-195">trustedServerCertificateNames</span></span>|<span data-ttu-id="ce2d5-196">String collection</span><span class="sxs-lookup"><span data-stu-id="ce2d5-196">String collection</span></span>|<span data-ttu-id="ce2d5-197">将 EAP 类型配置为 EAP-TLS/TTLS/FAST 或 PEAP 时受信任的服务器证书名称。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-197">Trusted server certificate names when EAP Type is configured to EAP-TLS/TTLS/FAST or PEAP.</span></span> <span data-ttu-id="ce2d5-198">这是由受信任的证书颁发机构（CA）颁发的证书中使用的公用名称。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-198">This is the common name used in the certificates issued by your trusted certificate authority (CA).</span></span> <span data-ttu-id="ce2d5-199">如果您提供此信息，您可以绕过在最终用户设备连接到此有线网络时显示的 "动态信任" 对话框。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-199">If you provide this information, you can bypass the dynamic trust dialog that is displayed on end users devices when they connect to this wired network.</span></span>|
|<span data-ttu-id="ce2d5-200">authenticationMethod</span><span class="sxs-lookup"><span data-stu-id="ce2d5-200">authenticationMethod</span></span>|[<span data-ttu-id="ce2d5-201">wiFiAuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="ce2d5-201">wiFiAuthenticationMethod</span></span>](../resources/intune-deviceconfig-wifiauthenticationmethod.md)|<span data-ttu-id="ce2d5-202">EAP 类型配置为 PEAP 或 EAP-TTLS 时的身份验证方法。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-202">Authentication Method when EAP Type is configured to PEAP or EAP-TTLS.</span></span> <span data-ttu-id="ce2d5-203">可取值为：`certificate`、`usernameAndPassword`、`derivedCredential`。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-203">Possible values are: `certificate`, `usernameAndPassword`, `derivedCredential`.</span></span>|
|<span data-ttu-id="ce2d5-204">nonEapAuthenticationMethodForEapTtls</span><span class="sxs-lookup"><span data-stu-id="ce2d5-204">nonEapAuthenticationMethodForEapTtls</span></span>|[<span data-ttu-id="ce2d5-205">nonEapAuthenticationMethodForEapTtlsType</span><span class="sxs-lookup"><span data-stu-id="ce2d5-205">nonEapAuthenticationMethodForEapTtlsType</span></span>](../resources/intune-deviceconfig-noneapauthenticationmethodforeapttlstype.md)|<span data-ttu-id="ce2d5-206">EAP 类型为 EAP 时，用于身份验证的非 EAP 方法（内部标识）-TTLS 和 Authenticationmethod 为用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-206">Non-EAP Method for Authentication (Inner Identity) when EAP Type is EAP-TTLS and Authenticationmethod is Username and Password.</span></span> <span data-ttu-id="ce2d5-207">可取值为：`unencryptedPassword`、`challengeHandshakeAuthenticationProtocol`、`microsoftChap`、`microsoftChapVersionTwo`。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-207">Possible values are: `unencryptedPassword`, `challengeHandshakeAuthenticationProtocol`, `microsoftChap`, `microsoftChapVersionTwo`.</span></span>|
|<span data-ttu-id="ce2d5-208">enableOuterIdentityPrivacy</span><span class="sxs-lookup"><span data-stu-id="ce2d5-208">enableOuterIdentityPrivacy</span></span>|<span data-ttu-id="ce2d5-209">String</span><span class="sxs-lookup"><span data-stu-id="ce2d5-209">String</span></span>|<span data-ttu-id="ce2d5-210">将 EAP 类型配置为 EAP-TTLS、EAP-FAST 或 PEAP 时启用标识隐私（外部标识）。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-210">Enable identity privacy (Outer Identity) when EAP Type is configured to EAP-TTLS, EAP-FAST or PEAP.</span></span> <span data-ttu-id="ce2d5-211">此属性使用您输入的文本屏蔽用户名。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-211">This property masks usernames with the text you enter.</span></span> <span data-ttu-id="ce2d5-212">例如，如果使用 "匿名"，则使用其真实用户名通过此有线网络进行身份验证的每个用户都会显示为 "匿名"。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-212">For example, if you use 'anonymous', each user that authenticates with this wired network using their real username is displayed as 'anonymous'.</span></span>|



## <a name="response"></a><span data-ttu-id="ce2d5-213">响应</span><span class="sxs-lookup"><span data-stu-id="ce2d5-213">Response</span></span>
<span data-ttu-id="ce2d5-214">如果成功，此方法在响应`200 OK`正文中返回响应代码和更新的[macOSWiredNetworkConfiguration](../resources/intune-deviceconfig-macoswirednetworkconfiguration.md)对象。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-214">If successful, this method returns a `200 OK` response code and an updated [macOSWiredNetworkConfiguration](../resources/intune-deviceconfig-macoswirednetworkconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ce2d5-215">示例</span><span class="sxs-lookup"><span data-stu-id="ce2d5-215">Example</span></span>

### <a name="request"></a><span data-ttu-id="ce2d5-216">请求</span><span class="sxs-lookup"><span data-stu-id="ce2d5-216">Request</span></span>
<span data-ttu-id="ce2d5-217">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-217">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 1499

{
  "@odata.type": "#microsoft.graph.macOSWiredNetworkConfiguration",
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
  "networkName": "Network Name value",
  "networkInterface": "firstActiveEthernet",
  "eapType": "leap",
  "eapFastConfiguration": "useProtectedAccessCredential",
  "trustedServerCertificateNames": [
    "Trusted Server Certificate Names value"
  ],
  "authenticationMethod": "usernameAndPassword",
  "nonEapAuthenticationMethodForEapTtls": "challengeHandshakeAuthenticationProtocol",
  "enableOuterIdentityPrivacy": "Enable Outer Identity Privacy value"
}
```

### <a name="response"></a><span data-ttu-id="ce2d5-218">响应</span><span class="sxs-lookup"><span data-stu-id="ce2d5-218">Response</span></span>
<span data-ttu-id="ce2d5-p120">下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1671

{
  "@odata.type": "#microsoft.graph.macOSWiredNetworkConfiguration",
  "id": "e5a57519-7519-e5a5-1975-a5e51975a5e5",
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
  "networkName": "Network Name value",
  "networkInterface": "firstActiveEthernet",
  "eapType": "leap",
  "eapFastConfiguration": "useProtectedAccessCredential",
  "trustedServerCertificateNames": [
    "Trusted Server Certificate Names value"
  ],
  "authenticationMethod": "usernameAndPassword",
  "nonEapAuthenticationMethodForEapTtls": "challengeHandshakeAuthenticationProtocol",
  "enableOuterIdentityPrivacy": "Enable Outer Identity Privacy value"
}
```





