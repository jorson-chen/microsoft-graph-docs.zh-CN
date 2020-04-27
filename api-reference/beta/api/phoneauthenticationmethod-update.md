---
title: 更新 phoneAuthenticationMethod
description: 更新与 phoneAuthenticationMethod 对象关联的电话号码。
localization_priority: Normal
author: mmcla
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: 6be00410dfc32e13faf7d686c93fbeb3bd160096
ms.sourcegitcommit: 5575e6607817ba23ceb0b01e2f5fc81e58bdcd1f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/22/2020
ms.locfileid: "43805838"
---
# <a name="update-phoneauthenticationmethod"></a><span data-ttu-id="ad291-103">更新 phoneAuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="ad291-103">Update phoneAuthenticationMethod</span></span>

<span data-ttu-id="ad291-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="ad291-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="ad291-105">更新与[电话身份验证方法](../resources/phoneauthenticationmethod.md)关联的电话号码。</span><span class="sxs-lookup"><span data-stu-id="ad291-105">Update the phone number associated with a [phone authentication method](../resources/phoneauthenticationmethod.md).</span></span>

<span data-ttu-id="ad291-106">无法更改电话类型。</span><span class="sxs-lookup"><span data-stu-id="ad291-106">You can't change a phone's type.</span></span> <span data-ttu-id="ad291-107">若要更改电话类型，请添加所需类型的新号码，然后使用原始类型删除该对象。</span><span class="sxs-lookup"><span data-stu-id="ad291-107">To change a phone's type, add a new number of the desired type and then delete the object with the original type.</span></span>

<span data-ttu-id="ad291-108">如果用户通过策略启用，以使用 SMS 登录，并且更改了`mobile`号码，则系统将尝试注册该号码以在该系统中使用。</span><span class="sxs-lookup"><span data-stu-id="ad291-108">If a user is enabled by policy to use SMS to sign in and the `mobile` number is changed, the system will attempt to register the number for use in that system.</span></span>

## <a name="permissions"></a><span data-ttu-id="ad291-109">Permissions</span><span class="sxs-lookup"><span data-stu-id="ad291-109">Permissions</span></span>

<span data-ttu-id="ad291-p102">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="ad291-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="ad291-112">权限类型</span><span class="sxs-lookup"><span data-stu-id="ad291-112">Permission type</span></span>                        | <span data-ttu-id="ad291-113">作用于自助的权限（从最高特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="ad291-113">Permissions acting on self (from least to most privileged)</span></span> | <span data-ttu-id="ad291-114">对其他用户的权限（从最低到最高特权）</span><span class="sxs-lookup"><span data-stu-id="ad291-114">Permissions acting on others (from least to most privileged)</span></span>|
|:---------------------------------------|:-------------------------|:-----------------|
| <span data-ttu-id="ad291-115">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="ad291-115">Delegated (work or school account)</span></span>     | <span data-ttu-id="ad291-116">UserAuthenticationMethod，UserAuthenticationMethod。</span><span class="sxs-lookup"><span data-stu-id="ad291-116">UserAuthenticationMethod.ReadWrite, UserAuthenticationMethod.ReadWrite.All</span></span> | <span data-ttu-id="ad291-117">UserAuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="ad291-117">UserAuthenticationMethod.ReadWrite.All</span></span> |
| <span data-ttu-id="ad291-118">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="ad291-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ad291-119">不支持。</span><span class="sxs-lookup"><span data-stu-id="ad291-119">Not supported.</span></span> | <span data-ttu-id="ad291-120">不支持。</span><span class="sxs-lookup"><span data-stu-id="ad291-120">Not supported.</span></span> |
| <span data-ttu-id="ad291-121">应用程序</span><span class="sxs-lookup"><span data-stu-id="ad291-121">Application</span></span>                            | <span data-ttu-id="ad291-122">不支持。</span><span class="sxs-lookup"><span data-stu-id="ad291-122">Not supported.</span></span> | <span data-ttu-id="ad291-123">不支持。</span><span class="sxs-lookup"><span data-stu-id="ad291-123">Not supported.</span></span> |

<span data-ttu-id="ad291-124">对于在其他用户上执行管理的委派方案，管理员需要[以下角色之一](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles)：</span><span class="sxs-lookup"><span data-stu-id="ad291-124">For delegated scenarios where an admin is acting on another user, the admin needs [one of the following roles](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles):</span></span>

* <span data-ttu-id="ad291-125">全局管理员</span><span class="sxs-lookup"><span data-stu-id="ad291-125">Global admin</span></span>
* <span data-ttu-id="ad291-126">特权身份验证管理员</span><span class="sxs-lookup"><span data-stu-id="ad291-126">Privileged authentication admin</span></span>
* <span data-ttu-id="ad291-127">身份验证管理员</span><span class="sxs-lookup"><span data-stu-id="ad291-127">Authentication admin</span></span>

## <a name="http-request"></a><span data-ttu-id="ad291-128">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="ad291-128">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PUT /me/authentication/phoneMethods/{id}
PUT /users/{id}/authentication/phoneMethods/{id}
```

## <a name="request-headers"></a><span data-ttu-id="ad291-129">请求标头</span><span class="sxs-lookup"><span data-stu-id="ad291-129">Request headers</span></span>

| <span data-ttu-id="ad291-130">名称</span><span class="sxs-lookup"><span data-stu-id="ad291-130">Name</span></span>       | <span data-ttu-id="ad291-131">说明</span><span class="sxs-lookup"><span data-stu-id="ad291-131">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="ad291-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="ad291-132">Authorization</span></span> | <span data-ttu-id="ad291-p103">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="ad291-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="ad291-135">Content-type</span><span class="sxs-lookup"><span data-stu-id="ad291-135">Content-type</span></span>  | <span data-ttu-id="ad291-p104">application/json. Required.</span><span class="sxs-lookup"><span data-stu-id="ad291-p104">application/json. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ad291-138">请求正文</span><span class="sxs-lookup"><span data-stu-id="ad291-138">Request body</span></span>

<span data-ttu-id="ad291-139">在请求正文中，提供应更新的相关字段的值。</span><span class="sxs-lookup"><span data-stu-id="ad291-139">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="ad291-140">将根据其他属性值的更改重新计算未包含在请求正文中的现有属性。</span><span class="sxs-lookup"><span data-stu-id="ad291-140">Existing properties that are not included in the request body will be recalculated based on changes to other property values.</span></span>

| <span data-ttu-id="ad291-141">属性</span><span class="sxs-lookup"><span data-stu-id="ad291-141">Property</span></span>     | <span data-ttu-id="ad291-142">类型</span><span class="sxs-lookup"><span data-stu-id="ad291-142">Type</span></span>        | <span data-ttu-id="ad291-143">说明</span><span class="sxs-lookup"><span data-stu-id="ad291-143">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="ad291-144">phoneNumber</span><span class="sxs-lookup"><span data-stu-id="ad291-144">phoneNumber</span></span>|<span data-ttu-id="ad291-145">String</span><span class="sxs-lookup"><span data-stu-id="ad291-145">String</span></span>|<span data-ttu-id="ad291-146">将电话号码设为文本或呼叫以进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="ad291-146">The phone number to text or call for authentication.</span></span> <span data-ttu-id="ad291-147">\<电话号码使用 "+ 国家/地区代码\> \<号码\>x\<分机\>" 格式，扩展名为可选。</span><span class="sxs-lookup"><span data-stu-id="ad291-147">Phone numbers use the format "+\<country code\> \<number\>x\<extension\>", with extension optional.</span></span> <span data-ttu-id="ad291-148">例如，+ 1 5555551234 或 + 1 5555551234x123 是有效的。</span><span class="sxs-lookup"><span data-stu-id="ad291-148">For example, +1 5555551234 or +1 5555551234x123 are valid.</span></span> <span data-ttu-id="ad291-149">如果创建/更新时编号不符合要求的格式，则会拒绝编号。</span><span class="sxs-lookup"><span data-stu-id="ad291-149">Numbers are rejected when creating/updating if they do not match the required format.</span></span>|
|<span data-ttu-id="ad291-150">phoneType</span><span class="sxs-lookup"><span data-stu-id="ad291-150">phoneType</span></span>|<span data-ttu-id="ad291-151">string</span><span class="sxs-lookup"><span data-stu-id="ad291-151">string</span></span>| <span data-ttu-id="ad291-152">可能的值包括`mobile`： `alternateMobile`、或`office`。</span><span class="sxs-lookup"><span data-stu-id="ad291-152">Possible values are: `mobile`, `alternateMobile`, or `office`.</span></span>|

## <a name="response"></a><span data-ttu-id="ad291-153">响应</span><span class="sxs-lookup"><span data-stu-id="ad291-153">Response</span></span>

<span data-ttu-id="ad291-154">如果成功，此方法在响应`200 OK`正文中返回响应代码和更新的[phoneAuthenticationMethod](../resources/phoneauthenticationmethod.md)对象。</span><span class="sxs-lookup"><span data-stu-id="ad291-154">If successful, this method returns a `200 OK` response code and an updated [phoneAuthenticationMethod](../resources/phoneauthenticationmethod.md) object in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="ad291-155">示例</span><span class="sxs-lookup"><span data-stu-id="ad291-155">Examples</span></span>

### <a name="request"></a><span data-ttu-id="ad291-156">请求</span><span class="sxs-lookup"><span data-stu-id="ad291-156">Request</span></span>

<span data-ttu-id="ad291-157">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="ad291-157">The following is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="ad291-158">HTTP</span><span class="sxs-lookup"><span data-stu-id="ad291-158">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "update_phoneauthenticationmethod"
}-->

```http
PUT https://graph.microsoft.com/beta/me/authentication/phoneMethods/3179e48a-750b-4051-897c-87b9720928f7
Content-type: application/json

{
  "phoneNumber": "+1 2065555554",
  "phoneType": "mobile",
}
```
# <a name="c"></a>[<span data-ttu-id="ad291-159">C#</span><span class="sxs-lookup"><span data-stu-id="ad291-159">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/update-phoneauthenticationmethod-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="ad291-160">JavaScript</span><span class="sxs-lookup"><span data-stu-id="ad291-160">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/update-phoneauthenticationmethod-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="ad291-161">Objective-C</span><span class="sxs-lookup"><span data-stu-id="ad291-161">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/update-phoneauthenticationmethod-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


### <a name="response"></a><span data-ttu-id="ad291-162">响应</span><span class="sxs-lookup"><span data-stu-id="ad291-162">Response</span></span>

<span data-ttu-id="ad291-163">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="ad291-163">The following is an example of the response.</span></span>

> <span data-ttu-id="ad291-p107">**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。所有属性都将通过实际调用返回。</span><span class="sxs-lookup"><span data-stu-id="ad291-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.phoneAuthenticationMethod"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "phoneNumber": "+1 2065555554",
  "phoneType": "mobile",
  "smsSignInState": "ready",
  "id": "3179e48a-750b-4051-897c-87b9720928f7"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update phoneauthenticationmethod",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->