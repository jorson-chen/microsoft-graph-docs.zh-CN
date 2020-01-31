---
title: claimsMappingPolicy 资源类型
description: 表示可控制 Azure Active Directory （Azure AD）颁发的访问令牌的生存期的策略。
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 8fe6ca32e606829f12400a03a70c9fb783f32f77
ms.sourcegitcommit: 0536ab327c8b8bf215b726e0d4c25e8f6e8996f9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/18/2020
ms.locfileid: "41234206"
---
# <a name="claimsmappingpolicy-resource-type"></a><span data-ttu-id="e680c-103">claimsMappingPolicy 资源类型</span><span class="sxs-lookup"><span data-stu-id="e680c-103">claimsMappingPolicy resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="e680c-104">表示对颁发给特定应用程序的令牌的 WS 馈送、SAML、OAuth 2.0 和 OpenID Connect 协议的声明映射策略。</span><span class="sxs-lookup"><span data-stu-id="e680c-104">Represents the claim-mapping policies for WS-Fed, SAML, OAuth 2.0, and OpenID Connect protocols, for tokens issued to a specific application.</span></span> <span data-ttu-id="e680c-105">您可以使用声明映射策略执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="e680c-105">You can use claims-mapping policies to:</span></span>

- <span data-ttu-id="e680c-106">选择令牌中包含的声明</span><span class="sxs-lookup"><span data-stu-id="e680c-106">Select which claims are included in tokens</span></span>
- <span data-ttu-id="e680c-107">创建尚不存在的声明类型</span><span class="sxs-lookup"><span data-stu-id="e680c-107">Create claim types that do not already exist</span></span>
- <span data-ttu-id="e680c-108">选择或更改特定声明中发出的数据源</span><span class="sxs-lookup"><span data-stu-id="e680c-108">Choose or change the source of data emitted in specific claims</span></span>  

<span data-ttu-id="e680c-109">有关更多方案和配置详细信息，请参阅[如何：自定义在租户中的特定应用程序令牌中发出的声明](https://docs.microsoft.com/azure/active-directory/develop/active-directory-claims-mapping#claims-mapping-policy-properties)。</span><span class="sxs-lookup"><span data-stu-id="e680c-109">For more scenario and configuration details see [How to: Customize claims emitted in tokens for a specific app in a tenant](https://docs.microsoft.com/azure/active-directory/develop/active-directory-claims-mapping#claims-mapping-policy-properties).</span></span>

<span data-ttu-id="e680c-110">继承自[stsPolicy](stsPolicy.md)。</span><span class="sxs-lookup"><span data-stu-id="e680c-110">Inherits from [stsPolicy](stsPolicy.md).</span></span>

## <a name="methods"></a><span data-ttu-id="e680c-111">方法</span><span class="sxs-lookup"><span data-stu-id="e680c-111">Methods</span></span>

| <span data-ttu-id="e680c-112">方法</span><span class="sxs-lookup"><span data-stu-id="e680c-112">Method</span></span>       | <span data-ttu-id="e680c-113">返回类型</span><span class="sxs-lookup"><span data-stu-id="e680c-113">Return Type</span></span> | <span data-ttu-id="e680c-114">说明</span><span class="sxs-lookup"><span data-stu-id="e680c-114">Description</span></span> |
|:-------------|:------------|:------------|
| [<span data-ttu-id="e680c-115">创建 claimsMappingPolicy</span><span class="sxs-lookup"><span data-stu-id="e680c-115">Create claimsMappingPolicy</span></span>](../api/claimsmappingpolicy-post-claimsmappingpolicies.md) | [<span data-ttu-id="e680c-116">claimsMappingPolicy</span><span class="sxs-lookup"><span data-stu-id="e680c-116">claimsMappingPolicy</span></span>](claimsmappingpolicy.md) | <span data-ttu-id="e680c-117">创建 claimsMappingPolicy 对象。</span><span class="sxs-lookup"><span data-stu-id="e680c-117">Create a claimsMappingPolicy object.</span></span> |
| [<span data-ttu-id="e680c-118">获取 claimsMappingPolicy</span><span class="sxs-lookup"><span data-stu-id="e680c-118">Get claimsMappingPolicy</span></span>](../api/claimsmappingpolicy-get.md) | [<span data-ttu-id="e680c-119">claimsMappingPolicy</span><span class="sxs-lookup"><span data-stu-id="e680c-119">claimsMappingPolicy</span></span>](claimsmappingpolicy.md) | <span data-ttu-id="e680c-120">读取 claimsMappingPolicy 对象的属性和关系。</span><span class="sxs-lookup"><span data-stu-id="e680c-120">Read properties and relationships of a claimsMappingPolicy object.</span></span> |
| [<span data-ttu-id="e680c-121">列出 claimsMappingPolicies</span><span class="sxs-lookup"><span data-stu-id="e680c-121">List claimsMappingPolicies</span></span>](../api/claimsmappingpolicy-list.md) | [<span data-ttu-id="e680c-122">claimsMappingPolicy</span><span class="sxs-lookup"><span data-stu-id="e680c-122">claimsMappingPolicy</span></span>](claimsmappingpolicy.md) | <span data-ttu-id="e680c-123">读取 claimsMappingPolicies 对象的属性和关系。</span><span class="sxs-lookup"><span data-stu-id="e680c-123">Read properties and relationships of claimsMappingPolicies objects.</span></span> |
| [<span data-ttu-id="e680c-124">更新 claimsMappingPolicy</span><span class="sxs-lookup"><span data-stu-id="e680c-124">Update claimsMappingPolicy</span></span>](../api/claimsmappingpolicy-update.md) | <span data-ttu-id="e680c-125">无</span><span class="sxs-lookup"><span data-stu-id="e680c-125">None</span></span> | <span data-ttu-id="e680c-126">更新 claimsMappingPolicy 对象。</span><span class="sxs-lookup"><span data-stu-id="e680c-126">Update a claimsMappingPolicy object.</span></span> |
| [<span data-ttu-id="e680c-127">删除 claimsMappingPolicy</span><span class="sxs-lookup"><span data-stu-id="e680c-127">Delete claimsMappingPolicy</span></span>](../api/claimsmappingpolicy-delete.md) | <span data-ttu-id="e680c-128">无</span><span class="sxs-lookup"><span data-stu-id="e680c-128">None</span></span> | <span data-ttu-id="e680c-129">删除 claimsMappingPolicy 对象。</span><span class="sxs-lookup"><span data-stu-id="e680c-129">Delete a claimsMappingPolicy object.</span></span> |
| [<span data-ttu-id="e680c-130">列出 appliesTo</span><span class="sxs-lookup"><span data-stu-id="e680c-130">List appliesTo</span></span>](../api/claimsmappingpolicy-list-appliesto.md) | <span data-ttu-id="e680c-131">[directoryObject](directoryobject.md) collection</span><span class="sxs-lookup"><span data-stu-id="e680c-131">[directoryObject](directoryobject.md) collection</span></span> | <span data-ttu-id="e680c-132">获取已应用此策略的 directoryObjects 的列表。</span><span class="sxs-lookup"><span data-stu-id="e680c-132">Get the list of directoryObjects that this policy has been applied to.</span></span> |

## <a name="properties"></a><span data-ttu-id="e680c-133">属性</span><span class="sxs-lookup"><span data-stu-id="e680c-133">Properties</span></span>

| <span data-ttu-id="e680c-134">属性</span><span class="sxs-lookup"><span data-stu-id="e680c-134">Property</span></span>     | <span data-ttu-id="e680c-135">类型</span><span class="sxs-lookup"><span data-stu-id="e680c-135">Type</span></span>        | <span data-ttu-id="e680c-136">说明</span><span class="sxs-lookup"><span data-stu-id="e680c-136">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="e680c-137">id</span><span class="sxs-lookup"><span data-stu-id="e680c-137">id</span></span>|<span data-ttu-id="e680c-138">字符串</span><span class="sxs-lookup"><span data-stu-id="e680c-138">String</span></span>| <span data-ttu-id="e680c-139">此策略的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="e680c-139">Unique identifier for this policy.</span></span> <span data-ttu-id="e680c-140">只读。</span><span class="sxs-lookup"><span data-stu-id="e680c-140">Read-only.</span></span>|
|<span data-ttu-id="e680c-141">定义</span><span class="sxs-lookup"><span data-stu-id="e680c-141">definition</span></span>|<span data-ttu-id="e680c-142">String collection</span><span class="sxs-lookup"><span data-stu-id="e680c-142">String collection</span></span>| <span data-ttu-id="e680c-143">一个包含 JSON 字符串的字符串集合，该字符串定义此策略的规则和设置。</span><span class="sxs-lookup"><span data-stu-id="e680c-143">A string collection containing a JSON string that defines the rules and settings for this policy.</span></span> <span data-ttu-id="e680c-144">有关此属性的 JSON 架构的更多详细信息，请参阅下文。</span><span class="sxs-lookup"><span data-stu-id="e680c-144">See below for more details about the JSON schema for this property.</span></span> <span data-ttu-id="e680c-145">必需。</span><span class="sxs-lookup"><span data-stu-id="e680c-145">Required.</span></span>|
|<span data-ttu-id="e680c-146">description</span><span class="sxs-lookup"><span data-stu-id="e680c-146">description</span></span>|<span data-ttu-id="e680c-147">String</span><span class="sxs-lookup"><span data-stu-id="e680c-147">String</span></span>| <span data-ttu-id="e680c-148">此策略的说明。</span><span class="sxs-lookup"><span data-stu-id="e680c-148">Description for this policy.</span></span>|
|<span data-ttu-id="e680c-149">displayName</span><span class="sxs-lookup"><span data-stu-id="e680c-149">displayName</span></span>|<span data-ttu-id="e680c-150">String</span><span class="sxs-lookup"><span data-stu-id="e680c-150">String</span></span>| <span data-ttu-id="e680c-151">此策略的显示名称。</span><span class="sxs-lookup"><span data-stu-id="e680c-151">Display name for this policy.</span></span> <span data-ttu-id="e680c-152">必需。</span><span class="sxs-lookup"><span data-stu-id="e680c-152">Required.</span></span>|
|<span data-ttu-id="e680c-153">isOrganizationDefault</span><span class="sxs-lookup"><span data-stu-id="e680c-153">isOrganizationDefault</span></span>|<span data-ttu-id="e680c-154">Boolean</span><span class="sxs-lookup"><span data-stu-id="e680c-154">Boolean</span></span>|<span data-ttu-id="e680c-155">忽略此属性。</span><span class="sxs-lookup"><span data-stu-id="e680c-155">Ignore this property.</span></span> <span data-ttu-id="e680c-156">声明映射策略仅可应用于服务主体，不能为组织全局设置。</span><span class="sxs-lookup"><span data-stu-id="e680c-156">The claims-mapping policy can only be applied to service principals and can't be set globally for the organization.</span></span>|

### <a name="properties-of-a-claims-mapping-policy-definition"></a><span data-ttu-id="e680c-157">声明映射策略定义的属性</span><span class="sxs-lookup"><span data-stu-id="e680c-157">Properties of a claims-mapping policy definition</span></span>

<span data-ttu-id="e680c-158">下面的属性构成了表示声明映射策略的 JSON 对象。</span><span class="sxs-lookup"><span data-stu-id="e680c-158">The properties below form the JSON object that represents a claims-mapping policy.</span></span> <span data-ttu-id="e680c-159">此 JSON 对象必须**转换为转义了引号的字符串**，以将其插入到**定义**属性中。</span><span class="sxs-lookup"><span data-stu-id="e680c-159">This JSON object must be **converted to a string with quotations escaped** to be inserted into the **definition** property.</span></span> <span data-ttu-id="e680c-160">下面显示了几个定义示例：</span><span class="sxs-lookup"><span data-stu-id="e680c-160">A few definition examples are shown below:</span></span>

#### <a name="example-definition-to-include-the-employeeid-and-tenantcountry-as-claims-in-tokens"></a><span data-ttu-id="e680c-161">示例：将 "雇员 Id" 和 "TenantCountry" 作为声明包含在标记中的**定义**</span><span class="sxs-lookup"><span data-stu-id="e680c-161">Example: **definition** to include the EmployeeID and TenantCountry as claims in tokens</span></span>
<!-- {
  "blockType": "ignored"
}-->
``` json
{
  "definition": [
    "{\"ClaimsMappingPolicy\":{
      \"Version\":1,
      \"IncludeBasicClaimSet\":\"true\", 
      \"ClaimsSchema\": [
        {\"Source\":\"user\",\"ID\":\"employeeid\",\"SamlClaimType\":\"http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name\",\"JwtClaimType\":\"name\"},{\"Source\":\"company\",\"ID\":\"tenantcountry\",\"SamlClaimType\":\"http://schemas.xmlsoap.org/ws/2005/05/identity/claims/country\",\"JwtClaimType\":\"country\"}
        ]
      }
    }"
  ]
}
```

#### <a name="example-definition-that-uses-a-claims-transformation"></a><span data-ttu-id="e680c-162">示例：使用声明转换的**定义**</span><span class="sxs-lookup"><span data-stu-id="e680c-162">Example: **definition** that uses a claims transformation</span></span>
<!-- {
  "blockType": "ignored"
}-->
``` json
{
  "definition": [
    "{\"ClaimsMappingPolicy\":{
      \"Version\":1,
      \"IncludeBasicClaimSet\":\"true\", 
      \"ClaimsSchema\":[
        {\"Source\":\"user\",\"ID\":\"extensionattribute1\"},{\"Source\":\"transformation\",\"ID\":\"DataJoin\",\"TransformationId\":\"JoinTheData\",\"JwtClaimType\":\"JoinedData\"}
        ],
      \"ClaimsTransformation\":[
        {\"ID\":\"JoinTheData\",\"TransformationMethod\":\"Join\",\"InputClaims\":[{\"ClaimTypeReferenceId\":\"extensionattribute1\",\"TransformationClaimType\":\"string1\"}], \"InputParameters\": [{\"ID\":\"string2\",\"Value\":\"sandbox\"},{\"ID\":\"separator\",\"Value\":\".\"}],\"OutputClaims\":[{\"ClaimTypeReferenceId\":\"DataJoin\",\"TransformationClaimType\":\"outputClaim\"}]}
        ]
      }
    }"
  ]
}
```

| <span data-ttu-id="e680c-163">属性</span><span class="sxs-lookup"><span data-stu-id="e680c-163">Property</span></span>     | <span data-ttu-id="e680c-164">类型</span><span class="sxs-lookup"><span data-stu-id="e680c-164">Type</span></span>   |<span data-ttu-id="e680c-165">说明</span><span class="sxs-lookup"><span data-stu-id="e680c-165">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e680c-166">版本</span><span class="sxs-lookup"><span data-stu-id="e680c-166">Version</span></span>|<span data-ttu-id="e680c-167">整数</span><span class="sxs-lookup"><span data-stu-id="e680c-167">Integer</span></span>|<span data-ttu-id="e680c-168">将值设置为1。</span><span class="sxs-lookup"><span data-stu-id="e680c-168">Set value of 1.</span></span> <span data-ttu-id="e680c-169">必需。</span><span class="sxs-lookup"><span data-stu-id="e680c-169">Required.</span></span>|
|<span data-ttu-id="e680c-170">IncludeBasicClaimSet</span><span class="sxs-lookup"><span data-stu-id="e680c-170">IncludeBasicClaimSet</span></span>|<span data-ttu-id="e680c-171">Boolean</span><span class="sxs-lookup"><span data-stu-id="e680c-171">Boolean</span></span>|<span data-ttu-id="e680c-172">如果设置为 true，则在受策略影响的令牌中发出基本声明集中的所有声明。</span><span class="sxs-lookup"><span data-stu-id="e680c-172">If set to true, all claims in the basic claim set are emitted in tokens affected by the policy.</span></span> <span data-ttu-id="e680c-173">如果设置为 false，则基本声明集中的声明不在令牌中，除非它们单独添加到同一策略的 ClaimsSchema 属性中。</span><span class="sxs-lookup"><span data-stu-id="e680c-173">If set to false, claims in the basic claim set are not in the tokens, unless they are individually added in the ClaimsSchema property of the same policy.</span></span>|
|<span data-ttu-id="e680c-174">ClaimsSchema</span><span class="sxs-lookup"><span data-stu-id="e680c-174">ClaimsSchema</span></span>|<span data-ttu-id="e680c-175">JSON 对象</span><span class="sxs-lookup"><span data-stu-id="e680c-175">JSON object</span></span>|<span data-ttu-id="e680c-176">定义受策略影响的令牌中存在的声明，以及基本声明集和核心声明集。</span><span class="sxs-lookup"><span data-stu-id="e680c-176">Defines which claims are present in the tokens affected by the policy, in addition to the basic claim set and the core claim set.</span></span> <span data-ttu-id="e680c-177">对于在此属性中定义的每个声明架构条目，需要特定信息。</span><span class="sxs-lookup"><span data-stu-id="e680c-177">For each claim schema entry defined in this property, certain information is required.</span></span> <span data-ttu-id="e680c-178">指定数据的来源（"值" 或 "源/ID 对"），以及将数据作为（声明类型）发出的声明。</span><span class="sxs-lookup"><span data-stu-id="e680c-178">Specify where the data is coming from (Value or Source/ID pair), and which claim the data is emitted as (Claim Type).</span></span> <span data-ttu-id="e680c-179">[ClaimsSchema 定义](https://docs.microsoft.com/azure/active-directory/develop/active-directory-claims-mapping#claims-schema)中提供了更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="e680c-179">Further details are available in the [ClaimsSchema definition](https://docs.microsoft.com/azure/active-directory/develop/active-directory-claims-mapping#claims-schema).</span></span>|
|<span data-ttu-id="e680c-180">ClaimsTransformation</span><span class="sxs-lookup"><span data-stu-id="e680c-180">ClaimsTransformation</span></span>|<span data-ttu-id="e680c-181">JSON 对象</span><span class="sxs-lookup"><span data-stu-id="e680c-181">JSON object</span></span>| <span data-ttu-id="e680c-182">定义可应用于源数据的常见转换，以生成 ClaimsSchema 中指定的声明的输出数据。</span><span class="sxs-lookup"><span data-stu-id="e680c-182">Defines common transformations that can be applied to source data, to generate the output data for claims specified in the ClaimsSchema.</span></span> <span data-ttu-id="e680c-183">[ClaimsTransformation 定义](https://docs.microsoft.com/azure/active-directory/develop/active-directory-claims-mapping#claims-transformation)中提供了更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="e680c-183">Further details are available in the [ClaimsTransformation definition](https://docs.microsoft.com/azure/active-directory/develop/active-directory-claims-mapping#claims-transformation).</span></span>|


## <a name="relationships"></a><span data-ttu-id="e680c-184">关系</span><span class="sxs-lookup"><span data-stu-id="e680c-184">Relationships</span></span>

| <span data-ttu-id="e680c-185">关系</span><span class="sxs-lookup"><span data-stu-id="e680c-185">Relationship</span></span> | <span data-ttu-id="e680c-186">类型</span><span class="sxs-lookup"><span data-stu-id="e680c-186">Type</span></span>        | <span data-ttu-id="e680c-187">说明</span><span class="sxs-lookup"><span data-stu-id="e680c-187">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="e680c-188">appliesTo</span><span class="sxs-lookup"><span data-stu-id="e680c-188">appliesTo</span></span>|<span data-ttu-id="e680c-189">[directoryObject](directoryobject.md) collection</span><span class="sxs-lookup"><span data-stu-id="e680c-189">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="e680c-190">已将此策略应用于的[directoryObject](directoryObject.md)集合。</span><span class="sxs-lookup"><span data-stu-id="e680c-190">The [directoryObject](directoryObject.md) collection that this policy has been applied to.</span></span> <span data-ttu-id="e680c-191">只读。</span><span class="sxs-lookup"><span data-stu-id="e680c-191">Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="e680c-192">JSON 表示形式</span><span class="sxs-lookup"><span data-stu-id="e680c-192">JSON representation</span></span>

<span data-ttu-id="e680c-193">下面是资源的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="e680c-193">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.claimsMappingPolicy",
  "baseType": "microsoft.graph.stsPolicy",
  "keyProperty": "id"
}-->

```json
{
  "definition": ["String"],
  "description": "String",
  "displayName": "String",
  "id": "String (identifier)",
  "isOrganizationDefault": false,
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "claimsMappingPolicy resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->