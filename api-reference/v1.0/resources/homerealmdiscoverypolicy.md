---
title: homeRealmDiscoveryPolicy 资源类型
description: 表示用于控制联合用户的 Azure Active Directory 身份验证行为的策略。
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: de2efe618d9a7ccebf9523fc227219cf8e2fd770
ms.sourcegitcommit: 9a6ce4ddf75beead19b7c35a1949cf4d105b9b29
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/11/2020
ms.locfileid: "43229456"
---
# <a name="homerealmdiscoverypolicy-resource-type"></a><span data-ttu-id="078cf-103">homeRealmDiscoveryPolicy 资源类型</span><span class="sxs-lookup"><span data-stu-id="078cf-103">homeRealmDiscoveryPolicy resource type</span></span>

<span data-ttu-id="078cf-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="078cf-104">Namespace: microsoft.graph</span></span>



<span data-ttu-id="078cf-105">表示用于控制联盟用户的 Azure Active Directory 身份验证行为的策略，尤其适用于联合域中的自动加速和用户身份验证限制。</span><span class="sxs-lookup"><span data-stu-id="078cf-105">Represents a policy to control Azure Active Directory authentication behavior for federated users, in particular for auto-acceleration and user authentication restrictions in federated domains.</span></span> <span data-ttu-id="078cf-106">您可以为组织中的所有服务主体或组织中的特定服务主体设置 homeRealmDiscoveryPolicy。</span><span class="sxs-lookup"><span data-stu-id="078cf-106">You can set homeRealmDiscoveryPolicy for all service principals in your organization, or for specific service principals in your organization.</span></span>  <span data-ttu-id="078cf-107">有关详细方案和策略的详细信息，请参阅[使用主领域发现策略为应用程序配置 AZURE AD 登录行为](https://docs.microsoft.com/azure/active-directory/manage-apps/configure-authentication-for-federated-users-portal)。</span><span class="sxs-lookup"><span data-stu-id="078cf-107">For more scenario and policy details see [Configure Azure AD sign in behavior for an application by using a Home Realm Discovery policy](https://docs.microsoft.com/azure/active-directory/manage-apps/configure-authentication-for-federated-users-portal).</span></span>

<span data-ttu-id="078cf-108">继承自[stsPolicy](stsPolicy.md)。</span><span class="sxs-lookup"><span data-stu-id="078cf-108">Inherits from [stsPolicy](stsPolicy.md).</span></span>

## <a name="methods"></a><span data-ttu-id="078cf-109">方法</span><span class="sxs-lookup"><span data-stu-id="078cf-109">Methods</span></span>

| <span data-ttu-id="078cf-110">方法</span><span class="sxs-lookup"><span data-stu-id="078cf-110">Method</span></span>       | <span data-ttu-id="078cf-111">返回类型</span><span class="sxs-lookup"><span data-stu-id="078cf-111">Return Type</span></span> | <span data-ttu-id="078cf-112">说明</span><span class="sxs-lookup"><span data-stu-id="078cf-112">Description</span></span> |
|:-------------|:------------|:------------|
| [<span data-ttu-id="078cf-113">列出 homeRealmDiscoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="078cf-113">List homeRealmDiscoveryPolicies</span></span>](../api/homerealmdiscoverypolicy-list.md) | [<span data-ttu-id="078cf-114">homeRealmDiscoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="078cf-114">homeRealmDiscoveryPolicy</span></span>](homerealmdiscoverypolicy.md) | <span data-ttu-id="078cf-115">读取 homeRealmDiscoveryPolicies 对象的属性和关系。</span><span class="sxs-lookup"><span data-stu-id="078cf-115">Read properties and relationships of homeRealmDiscoveryPolicies objects.</span></span> |
| [<span data-ttu-id="078cf-116">创建 homeRealmDiscoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="078cf-116">Create homeRealmDiscoveryPolicy</span></span>](../api/homerealmdiscoverypolicy-post-homerealmdiscoverypolicies.md) | [<span data-ttu-id="078cf-117">homeRealmDiscoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="078cf-117">homeRealmDiscoveryPolicy</span></span>](homerealmdiscoverypolicy.md) | <span data-ttu-id="078cf-118">创建 homeRealmDiscoveryPolicy 对象。</span><span class="sxs-lookup"><span data-stu-id="078cf-118">Create a homeRealmDiscoveryPolicy object.</span></span> |
| [<span data-ttu-id="078cf-119">获取 homeRealmDiscoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="078cf-119">Get homeRealmDiscoveryPolicy</span></span>](../api/homerealmdiscoverypolicy-get.md) | [<span data-ttu-id="078cf-120">homeRealmDiscoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="078cf-120">homeRealmDiscoveryPolicy</span></span>](homerealmdiscoverypolicy.md) | <span data-ttu-id="078cf-121">读取 homeRealmDiscoveryPolicy 对象的属性和关系。</span><span class="sxs-lookup"><span data-stu-id="078cf-121">Read properties and relationships of a homeRealmDiscoveryPolicy object.</span></span> |
| [<span data-ttu-id="078cf-122">更新 homeRealmDiscoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="078cf-122">Update homeRealmDiscoveryPolicy</span></span>](../api/homerealmdiscoverypolicy-update.md) | <span data-ttu-id="078cf-123">无</span><span class="sxs-lookup"><span data-stu-id="078cf-123">None</span></span> | <span data-ttu-id="078cf-124">更新 homeRealmDiscoveryPolicy 对象。</span><span class="sxs-lookup"><span data-stu-id="078cf-124">Update a homeRealmDiscoveryPolicy object.</span></span> |
| [<span data-ttu-id="078cf-125">删除 homeRealmDiscoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="078cf-125">Delete homeRealmDiscoveryPolicy</span></span>](../api/homerealmdiscoverypolicy-delete.md) | <span data-ttu-id="078cf-126">无</span><span class="sxs-lookup"><span data-stu-id="078cf-126">None</span></span> | <span data-ttu-id="078cf-127">删除 homeRealmDiscoveryPolicy 对象。</span><span class="sxs-lookup"><span data-stu-id="078cf-127">Delete a homeRealmDiscoveryPolicy object.</span></span> |
| [<span data-ttu-id="078cf-128">列出 appliesTo</span><span class="sxs-lookup"><span data-stu-id="078cf-128">List appliesTo</span></span>](../api/homerealmdiscoverypolicy-list-appliesto.md) | <span data-ttu-id="078cf-129">[directoryObject](directoryobject.md) 集合</span><span class="sxs-lookup"><span data-stu-id="078cf-129">[directoryObject](directoryobject.md) collection</span></span> | <span data-ttu-id="078cf-130">获取已应用此策略的 directoryObjects 的列表。</span><span class="sxs-lookup"><span data-stu-id="078cf-130">Get the list of directoryObjects that this policy has been applied to.</span></span> |

## <a name="properties"></a><span data-ttu-id="078cf-131">属性</span><span class="sxs-lookup"><span data-stu-id="078cf-131">Properties</span></span>

| <span data-ttu-id="078cf-132">属性</span><span class="sxs-lookup"><span data-stu-id="078cf-132">Property</span></span>     | <span data-ttu-id="078cf-133">类型</span><span class="sxs-lookup"><span data-stu-id="078cf-133">Type</span></span>        | <span data-ttu-id="078cf-134">说明</span><span class="sxs-lookup"><span data-stu-id="078cf-134">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="078cf-135">id</span><span class="sxs-lookup"><span data-stu-id="078cf-135">id</span></span>|<span data-ttu-id="078cf-136">字符串</span><span class="sxs-lookup"><span data-stu-id="078cf-136">String</span></span>| <span data-ttu-id="078cf-137">此策略的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="078cf-137">Unique identifier for this policy.</span></span> <span data-ttu-id="078cf-138">只读。</span><span class="sxs-lookup"><span data-stu-id="078cf-138">Read-only.</span></span>|
|<span data-ttu-id="078cf-139">定义</span><span class="sxs-lookup"><span data-stu-id="078cf-139">definition</span></span>|<span data-ttu-id="078cf-140">String 集合</span><span class="sxs-lookup"><span data-stu-id="078cf-140">String collection</span></span>| <span data-ttu-id="078cf-141">一个包含 JSON 字符串的字符串集合，该字符串定义此策略的规则和设置。</span><span class="sxs-lookup"><span data-stu-id="078cf-141">A string collection containing a JSON string that defines the rules and settings for this policy.</span></span> <span data-ttu-id="078cf-142">有关此属性的 JSON 架构的更多详细信息，请参阅下文。</span><span class="sxs-lookup"><span data-stu-id="078cf-142">See below for more details about the JSON schema for this property.</span></span> <span data-ttu-id="078cf-143">必需。</span><span class="sxs-lookup"><span data-stu-id="078cf-143">Required.</span></span>|
|<span data-ttu-id="078cf-144">description</span><span class="sxs-lookup"><span data-stu-id="078cf-144">description</span></span>|<span data-ttu-id="078cf-145">String</span><span class="sxs-lookup"><span data-stu-id="078cf-145">String</span></span>| <span data-ttu-id="078cf-146">此策略的说明。</span><span class="sxs-lookup"><span data-stu-id="078cf-146">Description for this policy.</span></span>|
|<span data-ttu-id="078cf-147">displayName</span><span class="sxs-lookup"><span data-stu-id="078cf-147">displayName</span></span>|<span data-ttu-id="078cf-148">String</span><span class="sxs-lookup"><span data-stu-id="078cf-148">String</span></span>| <span data-ttu-id="078cf-149">此策略的显示名称。</span><span class="sxs-lookup"><span data-stu-id="078cf-149">Display name for this policy.</span></span> <span data-ttu-id="078cf-150">必需。</span><span class="sxs-lookup"><span data-stu-id="078cf-150">Required.</span></span>|
|<span data-ttu-id="078cf-151">isOrganizationDefault</span><span class="sxs-lookup"><span data-stu-id="078cf-151">isOrganizationDefault</span></span>|<span data-ttu-id="078cf-152">布尔</span><span class="sxs-lookup"><span data-stu-id="078cf-152">Boolean</span></span>|<span data-ttu-id="078cf-153">如果设置为 true，则激活此策略。</span><span class="sxs-lookup"><span data-stu-id="078cf-153">If set to true, activates this policy.</span></span> <span data-ttu-id="078cf-154">对于同一策略类型，可以有多个策略，但只有一个策略可以作为组织默认激活。</span><span class="sxs-lookup"><span data-stu-id="078cf-154">There can be many policies for the same policy type, but only one can be activated as the organization default.</span></span> <span data-ttu-id="078cf-155">可选，默认值为 false。</span><span class="sxs-lookup"><span data-stu-id="078cf-155">Optional, default value is false.</span></span>|


### <a name="properties-of-a-home-realm-discovery-policy-definition"></a><span data-ttu-id="078cf-156">主领域发现策略定义的属性</span><span class="sxs-lookup"><span data-stu-id="078cf-156">Properties of a home realm discovery policy definition</span></span>
<span data-ttu-id="078cf-157">下面的属性构成了表示令牌生存期策略的 JSON 对象。</span><span class="sxs-lookup"><span data-stu-id="078cf-157">The properties below form the JSON object that represents a token lifetime policy.</span></span> <span data-ttu-id="078cf-158">此 JSON 对象必须**转换为转义了引号的字符串**，以将其插入到**定义**属性中。</span><span class="sxs-lookup"><span data-stu-id="078cf-158">This JSON object must be **converted to a string with quotations escaped** to be inserted into the **definition** property.</span></span> <span data-ttu-id="078cf-159">下面以 JSON 格式显示了一个示例：</span><span class="sxs-lookup"><span data-stu-id="078cf-159">An example is shown below in JSON format:</span></span>

<!-- {
  "blockType": "ignored"
}-->
``` json
"definition": [
    "{\"HomeRealmDiscoveryPolicy\":
     {\"AccelerateToFederatedDomain\":true,
      \"PreferredDomain\":\"federated.example.edu\"}}"
  ]
```

| <span data-ttu-id="078cf-160">属性</span><span class="sxs-lookup"><span data-stu-id="078cf-160">Property</span></span>     | <span data-ttu-id="078cf-161">类型</span><span class="sxs-lookup"><span data-stu-id="078cf-161">Type</span></span>   |<span data-ttu-id="078cf-162">说明</span><span class="sxs-lookup"><span data-stu-id="078cf-162">Description</span></span>| 
|:---------------|:--------|:----------|
|<span data-ttu-id="078cf-163">AccelerateToFederatedDomain</span><span class="sxs-lookup"><span data-stu-id="078cf-163">AccelerateToFederatedDomain</span></span>|<span data-ttu-id="078cf-164">布尔</span><span class="sxs-lookup"><span data-stu-id="078cf-164">Boolean</span></span>| <span data-ttu-id="078cf-165">设置为`true`以进行自动加速（绕过主页领域发现）。</span><span class="sxs-lookup"><span data-stu-id="078cf-165">Set to `true` for auto-acceleration (bypass home realm discovery).</span></span> <span data-ttu-id="078cf-166">如果`true`在租户中只有一个经过验证和联合的域，则用户将直接转到联合身份提供程序（如 ADFS）以进行登录。</span><span class="sxs-lookup"><span data-stu-id="078cf-166">If `true` and there is only one verified and federated domain in the tenant, then users will be taken straight to the federated identity provider (such as ADFS) for sign in.</span></span> <span data-ttu-id="078cf-167">如果`true`租户中有多个已验证的域，则必须指定**PreferredDomain** 。</span><span class="sxs-lookup"><span data-stu-id="078cf-167">If `true` and there is more than one verified domain in the tenant, **PreferredDomain** must be specified.</span></span> <span data-ttu-id="078cf-168">可选。</span><span class="sxs-lookup"><span data-stu-id="078cf-168">Optional.</span></span>|
|<span data-ttu-id="078cf-169">PreferredDomain</span><span class="sxs-lookup"><span data-stu-id="078cf-169">PreferredDomain</span></span>|<span data-ttu-id="078cf-170">String</span><span class="sxs-lookup"><span data-stu-id="078cf-170">String</span></span>| <span data-ttu-id="078cf-171">指定要加速登录到的域。</span><span class="sxs-lookup"><span data-stu-id="078cf-171">Specifies a domain to accelerate sign-in to.</span></span> <span data-ttu-id="078cf-172">如果租户只有一个联合域，则可以省略它。</span><span class="sxs-lookup"><span data-stu-id="078cf-172">It can be omitted if the tenant has only one federated domain.</span></span> <span data-ttu-id="078cf-173">如果省略它，并且有多个经过验证的联合域，则此策略将不起作用。</span><span class="sxs-lookup"><span data-stu-id="078cf-173">If it is omitted, and there is more than one verified federated domain, this policy has no effect.</span></span> <span data-ttu-id="078cf-174">如果**AccelerateToFederatedDomain**为， `true`则为必需。</span><span class="sxs-lookup"><span data-stu-id="078cf-174">Required if **AccelerateToFederatedDomain** is `true`.</span></span>|
|<span data-ttu-id="078cf-175">AllowCloudPasswordValidation</span><span class="sxs-lookup"><span data-stu-id="078cf-175">AllowCloudPasswordValidation</span></span>|<span data-ttu-id="078cf-176">布尔</span><span class="sxs-lookup"><span data-stu-id="078cf-176">Boolean</span></span>| <span data-ttu-id="078cf-177">设置为`true`以允许应用程序通过直接向 Azure Active Directory 令牌终结点提供用户名/密码凭据来对联合用户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="078cf-177">Set to `true` to allow an application to authenticate a federated user by presenting username/password credentials directly to the Azure Active Directory token endpoint.</span></span> <span data-ttu-id="078cf-178">仅在启用密码哈希同步时才有效。</span><span class="sxs-lookup"><span data-stu-id="078cf-178">Only works if Password Hash Sync is enabled.</span></span> <span data-ttu-id="078cf-179">可选。</span><span class="sxs-lookup"><span data-stu-id="078cf-179">Optional.</span></span>|

## <a name="relationships"></a><span data-ttu-id="078cf-180">关系</span><span class="sxs-lookup"><span data-stu-id="078cf-180">Relationships</span></span>

| <span data-ttu-id="078cf-181">关系</span><span class="sxs-lookup"><span data-stu-id="078cf-181">Relationship</span></span> | <span data-ttu-id="078cf-182">类型</span><span class="sxs-lookup"><span data-stu-id="078cf-182">Type</span></span>        | <span data-ttu-id="078cf-183">说明</span><span class="sxs-lookup"><span data-stu-id="078cf-183">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="078cf-184">appliesTo</span><span class="sxs-lookup"><span data-stu-id="078cf-184">appliesTo</span></span>|<span data-ttu-id="078cf-185">[directoryObject](directoryobject.md) 集合</span><span class="sxs-lookup"><span data-stu-id="078cf-185">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="078cf-186">已将此策略应用于的[directoryObject](directoryObject.md)集合。</span><span class="sxs-lookup"><span data-stu-id="078cf-186">The [directoryObject](directoryObject.md) collection that this policy has been applied to.</span></span> <span data-ttu-id="078cf-187">只读。</span><span class="sxs-lookup"><span data-stu-id="078cf-187">Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="078cf-188">JSON 表示形式</span><span class="sxs-lookup"><span data-stu-id="078cf-188">JSON representation</span></span>

<span data-ttu-id="078cf-189">下面是资源的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="078cf-189">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.homeRealmDiscoveryPolicy",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "definition": ["String"],
  "description": "String",
  "displayName": "String",
  "id": "String (identifier)",
  "isOrganizationDefault": true,
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "homeRealmDiscoveryPolicy resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->