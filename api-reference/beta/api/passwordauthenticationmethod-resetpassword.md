---
title: 'passwordAuthenticationMethod: resetPassword'
description: 重置用户密码
localization_priority: Normal
author: mmcla
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: 9dabb63709b42f7eaa9c3791e9e91300f5063469
ms.sourcegitcommit: 5575e6607817ba23ceb0b01e2f5fc81e58bdcd1f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/22/2020
ms.locfileid: "43806002"
---
# <a name="passwordauthenticationmethod-resetpassword"></a><span data-ttu-id="28006-103">passwordAuthenticationMethod: resetPassword</span><span class="sxs-lookup"><span data-stu-id="28006-103">passwordAuthenticationMethod: resetPassword</span></span>

<span data-ttu-id="28006-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="28006-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="28006-105">启动与[密码身份验证方法](../resources/passwordauthenticationmethod.md)对象关联的密码的重置。</span><span class="sxs-lookup"><span data-stu-id="28006-105">Initiate a reset for the password associated with a [password authentication method](../resources/passwordauthenticationmethod.md) object.</span></span> <span data-ttu-id="28006-106">这只能由具有相应权限的管理员执行，并且无法在用户自己的帐户上执行。</span><span class="sxs-lookup"><span data-stu-id="28006-106">This can only be done by an administrator with appropriate permissions and cannot be performed on a user's own account.</span></span>

<span data-ttu-id="28006-107">此流将新密码写入 Azure Active Directory，并将其推送到本地 Active Directory （如果使用密码写回进行配置）。</span><span class="sxs-lookup"><span data-stu-id="28006-107">This flow writes the new password to Azure Active Directory and pushes it to on-premises Active Directory if configured using password writeback.</span></span> <span data-ttu-id="28006-108">管理员既可以提供新密码，也可以让系统生成一个新密码。</span><span class="sxs-lookup"><span data-stu-id="28006-108">The admin can either provide a new password or have the system generate one.</span></span> <span data-ttu-id="28006-109">系统会提示用户在下一次登录时更改其密码。</span><span class="sxs-lookup"><span data-stu-id="28006-109">The user is prompted to change their password on their next sign in.</span></span>

<span data-ttu-id="28006-110">此重置是一个长时间运行的操作，并将返回`Location`标头中的一个链接，在此情况下，呼叫者可以定期检查重置的状态。</span><span class="sxs-lookup"><span data-stu-id="28006-110">This reset is a long-running operation and will return a link in the `Location` header where the caller can periodically check for the status of the reset.</span></span>

## <a name="permissions"></a><span data-ttu-id="28006-111">Permissions</span><span class="sxs-lookup"><span data-stu-id="28006-111">Permissions</span></span>

<span data-ttu-id="28006-p103">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="28006-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="28006-114">权限类型</span><span class="sxs-lookup"><span data-stu-id="28006-114">Permission type</span></span>                        | <span data-ttu-id="28006-115">作用于自助的权限（从最高特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="28006-115">Permissions acting on self (from least to most privileged)</span></span> | <span data-ttu-id="28006-116">对其他用户的权限（从最低到最高特权）</span><span class="sxs-lookup"><span data-stu-id="28006-116">Permissions acting on others (from least to most privileged)</span></span>|
|:---------------------------------------|:-------------------------|:-----------------|
| <span data-ttu-id="28006-117">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="28006-117">Delegated (work or school account)</span></span>     | <span data-ttu-id="28006-118">UserAuthenticationMethod，UserAuthenticationMethod。</span><span class="sxs-lookup"><span data-stu-id="28006-118">UserAuthenticationMethod.ReadWrite, UserAuthenticationMethod.ReadWrite.All</span></span> | <span data-ttu-id="28006-119">UserAuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="28006-119">UserAuthenticationMethod.ReadWrite.All</span></span> |
| <span data-ttu-id="28006-120">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="28006-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="28006-121">不支持。</span><span class="sxs-lookup"><span data-stu-id="28006-121">Not supported.</span></span> | <span data-ttu-id="28006-122">不支持。</span><span class="sxs-lookup"><span data-stu-id="28006-122">Not supported.</span></span> |
| <span data-ttu-id="28006-123">应用程序</span><span class="sxs-lookup"><span data-stu-id="28006-123">Application</span></span>                            | <span data-ttu-id="28006-124">不支持。</span><span class="sxs-lookup"><span data-stu-id="28006-124">Not supported.</span></span> | <span data-ttu-id="28006-125">不支持。</span><span class="sxs-lookup"><span data-stu-id="28006-125">Not supported.</span></span> |

<span data-ttu-id="28006-126">对于在其他用户上执行管理的委派方案，管理员需要[以下角色之一](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles)：</span><span class="sxs-lookup"><span data-stu-id="28006-126">For delegated scenarios where an admin is acting on another user, the admin needs [one of the following roles](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles):</span></span>

* <span data-ttu-id="28006-127">全局管理员</span><span class="sxs-lookup"><span data-stu-id="28006-127">Global admin</span></span>
* <span data-ttu-id="28006-128">特权身份验证管理员</span><span class="sxs-lookup"><span data-stu-id="28006-128">Privileged authentication admin</span></span>
* <span data-ttu-id="28006-129">身份验证管理员</span><span class="sxs-lookup"><span data-stu-id="28006-129">Authentication admin</span></span>

## <a name="http-request"></a><span data-ttu-id="28006-130">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="28006-130">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /users/{id}/authentication/passwordMethods/{id}/resetPassword
```

## <a name="request-headers"></a><span data-ttu-id="28006-131">请求标头</span><span class="sxs-lookup"><span data-stu-id="28006-131">Request headers</span></span>

| <span data-ttu-id="28006-132">名称</span><span class="sxs-lookup"><span data-stu-id="28006-132">Name</span></span>          | <span data-ttu-id="28006-133">说明</span><span class="sxs-lookup"><span data-stu-id="28006-133">Description</span></span>   |
|:--------------|:--------------|
| <span data-ttu-id="28006-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="28006-134">Authorization</span></span> | <span data-ttu-id="28006-p104">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="28006-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="28006-137">Content-type</span><span class="sxs-lookup"><span data-stu-id="28006-137">Content-type</span></span>  | <span data-ttu-id="28006-p105">application/json. Required.</span><span class="sxs-lookup"><span data-stu-id="28006-p105">application/json. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="28006-140">请求正文</span><span class="sxs-lookup"><span data-stu-id="28006-140">Request body</span></span>

<span data-ttu-id="28006-141">在请求正文中，提供具有以下参数的 JSON 对象。</span><span class="sxs-lookup"><span data-stu-id="28006-141">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="28006-142">参数</span><span class="sxs-lookup"><span data-stu-id="28006-142">Parameter</span></span>    | <span data-ttu-id="28006-143">类型</span><span class="sxs-lookup"><span data-stu-id="28006-143">Type</span></span>        | <span data-ttu-id="28006-144">说明</span><span class="sxs-lookup"><span data-stu-id="28006-144">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="28006-145">newPassword</span><span class="sxs-lookup"><span data-stu-id="28006-145">newPassword</span></span>|<span data-ttu-id="28006-146">字符串</span><span class="sxs-lookup"><span data-stu-id="28006-146">String</span></span>|<span data-ttu-id="28006-147">管理员输入的新密码。对于具有混合密码方案的租户是必需的。</span><span class="sxs-lookup"><span data-stu-id="28006-147">The new password entered by the admin. Required for tenants with hybrid password scenarios.</span></span> <span data-ttu-id="28006-148">如果对仅云密码省略，则系统将返回系统生成的密码。</span><span class="sxs-lookup"><span data-stu-id="28006-148">If omitted for a cloud-only password, the system returns a system-generated password.</span></span> <span data-ttu-id="28006-149">这是不带任何其他编码的 unicode 字符串。</span><span class="sxs-lookup"><span data-stu-id="28006-149">This is a unicode string with no other encoding.</span></span> <span data-ttu-id="28006-150">在接受之前，它会针对租户的禁用密码系统进行验证，并且必须遵守租户的云和/或本地密码要求。</span><span class="sxs-lookup"><span data-stu-id="28006-150">It is validated against the tenant's banned password system before acceptance, and must adhere to the tenant's cloud and/or on-premises password requirements.</span></span>|

## <a name="response"></a><span data-ttu-id="28006-151">响应</span><span class="sxs-lookup"><span data-stu-id="28006-151">Response</span></span>

<span data-ttu-id="28006-152">如果成功，此方法在`202 ACCEPTED` `Location`标头中返回响应代码和 URL。</span><span class="sxs-lookup"><span data-stu-id="28006-152">If successful, this method returns a `202 ACCEPTED` response code and a URL in the `Location` header.</span></span>

<span data-ttu-id="28006-153">如果呼叫者未提交密码，则会在响应正文中的 JSON 对象中提供 Microsoft 生成的密码。</span><span class="sxs-lookup"><span data-stu-id="28006-153">If the caller did not submit a password, a Microsoft-generated password is provided in a JSON object in the response body.</span></span>

### <a name="response-headers"></a><span data-ttu-id="28006-154">响应标头</span><span class="sxs-lookup"><span data-stu-id="28006-154">Response headers</span></span>

| <span data-ttu-id="28006-155">名称</span><span class="sxs-lookup"><span data-stu-id="28006-155">Name</span></span>        | <span data-ttu-id="28006-156">说明</span><span class="sxs-lookup"><span data-stu-id="28006-156">Description</span></span>     |
|:------------|:----------------|
|<span data-ttu-id="28006-157">Location</span><span class="sxs-lookup"><span data-stu-id="28006-157">Location</span></span>     | <span data-ttu-id="28006-158">要调用以检查操作状态的 URL。</span><span class="sxs-lookup"><span data-stu-id="28006-158">URL to call to check the status of the operation.</span></span>|
|<span data-ttu-id="28006-159">重试-after</span><span class="sxs-lookup"><span data-stu-id="28006-159">Retry-after</span></span>  | <span data-ttu-id="28006-160">以秒为单位的持续时间。</span><span class="sxs-lookup"><span data-stu-id="28006-160">Duration in seconds.</span></span>|

## <a name="examples"></a><span data-ttu-id="28006-161">示例</span><span class="sxs-lookup"><span data-stu-id="28006-161">Examples</span></span>

### <a name="example-1-user-submitted-password"></a><span data-ttu-id="28006-162">示例1：用户提交的密码</span><span class="sxs-lookup"><span data-stu-id="28006-162">Example 1: User-submitted password</span></span>

<span data-ttu-id="28006-163">下面的示例演示在调用方提交密码时如何调用此 API。</span><span class="sxs-lookup"><span data-stu-id="28006-163">The following example shows how to call this API when the caller submits a password.</span></span>

#### <a name="request"></a><span data-ttu-id="28006-164">请求</span><span class="sxs-lookup"><span data-stu-id="28006-164">Request</span></span>

<span data-ttu-id="28006-165">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="28006-165">The following is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="28006-166">HTTP</span><span class="sxs-lookup"><span data-stu-id="28006-166">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "passwordauthenticationmethod_resetpassword_adminprovided"
}-->

```http
POST https://graph.microsoft.com/beta/users/{id}/authentication/passwordMethods/{id}/resetPassword
Content-type: application/json

{
  "newPassword": "newPassword-value",
}
```
# <a name="c"></a>[<span data-ttu-id="28006-167">C#</span><span class="sxs-lookup"><span data-stu-id="28006-167">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/passwordauthenticationmethod-resetpassword-adminprovided-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="28006-168">JavaScript</span><span class="sxs-lookup"><span data-stu-id="28006-168">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/passwordauthenticationmethod-resetpassword-adminprovided-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="28006-169">Objective-C</span><span class="sxs-lookup"><span data-stu-id="28006-169">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/passwordauthenticationmethod-resetpassword-adminprovided-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


#### <a name="response"></a><span data-ttu-id="28006-170">响应</span><span class="sxs-lookup"><span data-stu-id="28006-170">Response</span></span>

<span data-ttu-id="28006-171">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="28006-171">The following is an example of the response.</span></span>

> <span data-ttu-id="28006-p107">**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。所有属性都将通过实际调用返回。</span><span class="sxs-lookup"><span data-stu-id="28006-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
} -->

```http
HTTP/1.1 202 ACCEPTED
Content-type: application/json
Location: https://graph.microsoft.com/beta/users/{id}/authentication/operations/{id}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "passwordAuthenticationMethod: resetPassword",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

### <a name="example-2-system-generated-password"></a><span data-ttu-id="28006-174">示例2：系统生成的密码</span><span class="sxs-lookup"><span data-stu-id="28006-174">Example 2: System-generated password</span></span>

<span data-ttu-id="28006-175">下面的示例演示当调用方不提交密码时如何调用此 API。</span><span class="sxs-lookup"><span data-stu-id="28006-175">The following example shows how to call this API when the caller does not submit a password.</span></span>

#### <a name="request"></a><span data-ttu-id="28006-176">请求</span><span class="sxs-lookup"><span data-stu-id="28006-176">Request</span></span>

<span data-ttu-id="28006-177">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="28006-177">The following is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="28006-178">HTTP</span><span class="sxs-lookup"><span data-stu-id="28006-178">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "passwordauthenticationmethod_resetpassword_systemgenerated"
}-->

```http
POST https://graph.microsoft.com/beta/users/{id}/authentication/passwordMethods/{id}/resetPassword
```
# <a name="c"></a>[<span data-ttu-id="28006-179">C#</span><span class="sxs-lookup"><span data-stu-id="28006-179">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/passwordauthenticationmethod-resetpassword-systemgenerated-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="28006-180">JavaScript</span><span class="sxs-lookup"><span data-stu-id="28006-180">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/passwordauthenticationmethod-resetpassword-systemgenerated-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="28006-181">Objective-C</span><span class="sxs-lookup"><span data-stu-id="28006-181">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/passwordauthenticationmethod-resetpassword-systemgenerated-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


#### <a name="response"></a><span data-ttu-id="28006-182">响应</span><span class="sxs-lookup"><span data-stu-id="28006-182">Response</span></span>

<span data-ttu-id="28006-183">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="28006-183">The following is an example of the response.</span></span>

> <span data-ttu-id="28006-p108">**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。所有属性都将通过实际调用返回。</span><span class="sxs-lookup"><span data-stu-id="28006-p108">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.entity"
} -->

```http
HTTP/1.1 202 ACCEPTED
Location: https://graph.microsoft.com/beta/users/{id}/authentication/operations/{id}
Content-type: application/json

{
  "password": "new system generated password"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "passwordAuthenticationMethod: resetPassword",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->