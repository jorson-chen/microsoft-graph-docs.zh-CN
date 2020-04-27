---
title: updateLanguageFiles 操作
description: 尚未记录
author: dougeby
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 631a147bf095930f12b729ae0ab79e01f1bffa91
ms.sourcegitcommit: bbcf074f0be9d5e02f84c290122850cc5968fb1f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2020
ms.locfileid: "43440888"
---
# <a name="updatelanguagefiles-action"></a><span data-ttu-id="7431f-103">updateLanguageFiles 操作</span><span class="sxs-lookup"><span data-stu-id="7431f-103">updateLanguageFiles action</span></span>

<span data-ttu-id="7431f-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="7431f-104">Namespace: microsoft.graph</span></span>

> <span data-ttu-id="7431f-105">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="7431f-105">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="7431f-106">**注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="7431f-106">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="7431f-107">尚未记录</span><span class="sxs-lookup"><span data-stu-id="7431f-107">Not yet documented</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7431f-108">先决条件</span><span class="sxs-lookup"><span data-stu-id="7431f-108">Prerequisites</span></span>
<span data-ttu-id="7431f-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="7431f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7431f-111">权限类型</span><span class="sxs-lookup"><span data-stu-id="7431f-111">Permission type</span></span>|<span data-ttu-id="7431f-112">权限（从最高特权到最低特权）</span><span class="sxs-lookup"><span data-stu-id="7431f-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7431f-113">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="7431f-113">Delegated (work or school account)</span></span>|<span data-ttu-id="7431f-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7431f-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="7431f-115">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="7431f-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7431f-116">不支持。</span><span class="sxs-lookup"><span data-stu-id="7431f-116">Not supported.</span></span>|
|<span data-ttu-id="7431f-117">应用程序</span><span class="sxs-lookup"><span data-stu-id="7431f-117">Application</span></span>|<span data-ttu-id="7431f-118">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7431f-118">DeviceManagementConfiguration.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="7431f-119">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="7431f-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/groupPolicyUploadedDefinitionFiles/{groupPolicyUploadedDefinitionFileId}/updateLanguageFiles
```

## <a name="request-headers"></a><span data-ttu-id="7431f-120">请求标头</span><span class="sxs-lookup"><span data-stu-id="7431f-120">Request headers</span></span>
|<span data-ttu-id="7431f-121">标头</span><span class="sxs-lookup"><span data-stu-id="7431f-121">Header</span></span>|<span data-ttu-id="7431f-122">值</span><span class="sxs-lookup"><span data-stu-id="7431f-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7431f-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="7431f-123">Authorization</span></span>|<span data-ttu-id="7431f-124">Bearer &lt;token&gt;。必需。</span><span class="sxs-lookup"><span data-stu-id="7431f-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7431f-125">接受</span><span class="sxs-lookup"><span data-stu-id="7431f-125">Accept</span></span>|<span data-ttu-id="7431f-126">application/json</span><span class="sxs-lookup"><span data-stu-id="7431f-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7431f-127">请求正文</span><span class="sxs-lookup"><span data-stu-id="7431f-127">Request body</span></span>
<span data-ttu-id="7431f-128">在请求正文中，提供参数的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="7431f-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="7431f-129">下表显示了可用于此操作的参数。</span><span class="sxs-lookup"><span data-stu-id="7431f-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="7431f-130">属性</span><span class="sxs-lookup"><span data-stu-id="7431f-130">Property</span></span>|<span data-ttu-id="7431f-131">类型</span><span class="sxs-lookup"><span data-stu-id="7431f-131">Type</span></span>|<span data-ttu-id="7431f-132">说明</span><span class="sxs-lookup"><span data-stu-id="7431f-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7431f-133">groupPolicyUploadedLanguageFiles</span><span class="sxs-lookup"><span data-stu-id="7431f-133">groupPolicyUploadedLanguageFiles</span></span>|<span data-ttu-id="7431f-134">[groupPolicyUploadedLanguageFile](../resources/intune-grouppolicy-grouppolicyuploadedlanguagefile.md)集合</span><span class="sxs-lookup"><span data-stu-id="7431f-134">[groupPolicyUploadedLanguageFile](../resources/intune-grouppolicy-grouppolicyuploadedlanguagefile.md) collection</span></span>|<span data-ttu-id="7431f-135">尚未记录</span><span class="sxs-lookup"><span data-stu-id="7431f-135">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="7431f-136">响应</span><span class="sxs-lookup"><span data-stu-id="7431f-136">Response</span></span>
<span data-ttu-id="7431f-137">如果成功，此操作返回 `204 No Content` 响应代码。</span><span class="sxs-lookup"><span data-stu-id="7431f-137">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="7431f-138">示例</span><span class="sxs-lookup"><span data-stu-id="7431f-138">Example</span></span>

### <a name="request"></a><span data-ttu-id="7431f-139">请求</span><span class="sxs-lookup"><span data-stu-id="7431f-139">Request</span></span>
<span data-ttu-id="7431f-140">下面是一个请求示例。</span><span class="sxs-lookup"><span data-stu-id="7431f-140">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/groupPolicyUploadedDefinitionFiles/{groupPolicyUploadedDefinitionFileId}/updateLanguageFiles

Content-type: application/json
Content-length: 347

{
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

### <a name="response"></a><span data-ttu-id="7431f-141">响应</span><span class="sxs-lookup"><span data-stu-id="7431f-141">Response</span></span>
<span data-ttu-id="7431f-p102">下面是一个响应示例。注意：为了简单起见，可能会将此处所示的响应对象截断。将从实际调用中返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="7431f-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```


