---
title: updateDefinitionValues 操作
description: 尚未记录
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 35700ade5c9589a943a8560268179cb1d10ab95e
ms.sourcegitcommit: 5b1fad41067629d0e9f87746328664bb248f754f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/09/2019
ms.locfileid: "38087073"
---
# <a name="updatedefinitionvalues-action"></a><span data-ttu-id="7d05e-103">updateDefinitionValues 操作</span><span class="sxs-lookup"><span data-stu-id="7d05e-103">updateDefinitionValues action</span></span>

> <span data-ttu-id="7d05e-104">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="7d05e-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="7d05e-105">**注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="7d05e-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="7d05e-106">尚未记录</span><span class="sxs-lookup"><span data-stu-id="7d05e-106">Not yet documented</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7d05e-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="7d05e-107">Prerequisites</span></span>
<span data-ttu-id="7d05e-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="7d05e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7d05e-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="7d05e-110">Permission type</span></span>|<span data-ttu-id="7d05e-111">权限（从最高特权到最低特权）</span><span class="sxs-lookup"><span data-stu-id="7d05e-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7d05e-112">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="7d05e-112">Delegated (work or school account)</span></span>|<span data-ttu-id="7d05e-113">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7d05e-113">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="7d05e-114">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="7d05e-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7d05e-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="7d05e-115">Not supported.</span></span>|
|<span data-ttu-id="7d05e-116">应用程序</span><span class="sxs-lookup"><span data-stu-id="7d05e-116">Application</span></span>|<span data-ttu-id="7d05e-117">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7d05e-117">DeviceManagementServiceConfig.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="7d05e-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="7d05e-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/groupPolicyConfigurations/{groupPolicyConfigurationId}/updateDefinitionValues
```

## <a name="request-headers"></a><span data-ttu-id="7d05e-119">请求标头</span><span class="sxs-lookup"><span data-stu-id="7d05e-119">Request headers</span></span>
|<span data-ttu-id="7d05e-120">标头</span><span class="sxs-lookup"><span data-stu-id="7d05e-120">Header</span></span>|<span data-ttu-id="7d05e-121">值</span><span class="sxs-lookup"><span data-stu-id="7d05e-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7d05e-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="7d05e-122">Authorization</span></span>|<span data-ttu-id="7d05e-123">Bearer &lt;token&gt;。必需。</span><span class="sxs-lookup"><span data-stu-id="7d05e-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7d05e-124">接受</span><span class="sxs-lookup"><span data-stu-id="7d05e-124">Accept</span></span>|<span data-ttu-id="7d05e-125">application/json</span><span class="sxs-lookup"><span data-stu-id="7d05e-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7d05e-126">请求正文</span><span class="sxs-lookup"><span data-stu-id="7d05e-126">Request body</span></span>
<span data-ttu-id="7d05e-127">在请求正文中，提供参数的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="7d05e-127">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="7d05e-128">下表显示了可用于此操作的参数。</span><span class="sxs-lookup"><span data-stu-id="7d05e-128">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="7d05e-129">属性</span><span class="sxs-lookup"><span data-stu-id="7d05e-129">Property</span></span>|<span data-ttu-id="7d05e-130">类型</span><span class="sxs-lookup"><span data-stu-id="7d05e-130">Type</span></span>|<span data-ttu-id="7d05e-131">描述</span><span class="sxs-lookup"><span data-stu-id="7d05e-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7d05e-132">添加内容</span><span class="sxs-lookup"><span data-stu-id="7d05e-132">added</span></span>|<span data-ttu-id="7d05e-133">[groupPolicyDefinitionValue](../resources/intune-grouppolicy-grouppolicydefinitionvalue.md)集合</span><span class="sxs-lookup"><span data-stu-id="7d05e-133">[groupPolicyDefinitionValue](../resources/intune-grouppolicy-grouppolicydefinitionvalue.md) collection</span></span>|<span data-ttu-id="7d05e-134">尚未记录</span><span class="sxs-lookup"><span data-stu-id="7d05e-134">Not yet documented</span></span>|
|<span data-ttu-id="7d05e-135">updated</span><span class="sxs-lookup"><span data-stu-id="7d05e-135">updated</span></span>|<span data-ttu-id="7d05e-136">[groupPolicyDefinitionValue](../resources/intune-grouppolicy-grouppolicydefinitionvalue.md)集合</span><span class="sxs-lookup"><span data-stu-id="7d05e-136">[groupPolicyDefinitionValue](../resources/intune-grouppolicy-grouppolicydefinitionvalue.md) collection</span></span>|<span data-ttu-id="7d05e-137">尚未记录</span><span class="sxs-lookup"><span data-stu-id="7d05e-137">Not yet documented</span></span>|
|<span data-ttu-id="7d05e-138">deletedIds</span><span class="sxs-lookup"><span data-stu-id="7d05e-138">deletedIds</span></span>|<span data-ttu-id="7d05e-139">String collection</span><span class="sxs-lookup"><span data-stu-id="7d05e-139">String collection</span></span>|<span data-ttu-id="7d05e-140">尚未记录</span><span class="sxs-lookup"><span data-stu-id="7d05e-140">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="7d05e-141">响应</span><span class="sxs-lookup"><span data-stu-id="7d05e-141">Response</span></span>
<span data-ttu-id="7d05e-142">如果成功，此操作返回 `204 No Content` 响应代码。</span><span class="sxs-lookup"><span data-stu-id="7d05e-142">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="7d05e-143">示例</span><span class="sxs-lookup"><span data-stu-id="7d05e-143">Example</span></span>

### <a name="request"></a><span data-ttu-id="7d05e-144">请求</span><span class="sxs-lookup"><span data-stu-id="7d05e-144">Request</span></span>
<span data-ttu-id="7d05e-145">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="7d05e-145">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/groupPolicyConfigurations/{groupPolicyConfigurationId}/updateDefinitionValues

Content-type: application/json
Content-length: 759

{
  "added": [
    {
      "@odata.type": "#microsoft.graph.groupPolicyDefinitionValue",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "enabled": true,
      "configurationType": "preference",
      "id": "50428918-8918-5042-1889-425018894250",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00"
    }
  ],
  "updated": [
    {
      "@odata.type": "#microsoft.graph.groupPolicyDefinitionValue",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "enabled": true,
      "configurationType": "preference",
      "id": "50428918-8918-5042-1889-425018894250",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00"
    }
  ],
  "deletedIds": [
    "Deleted Ids value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="7d05e-146">响应</span><span class="sxs-lookup"><span data-stu-id="7d05e-146">Response</span></span>
<span data-ttu-id="7d05e-p102">下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="7d05e-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```





