---
title: orgContact 资源类型
description: 表示组织联系人
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: a6c604fa008c66447457f1c5736a31df0f39f28b
ms.sourcegitcommit: c9b9ff2c862f8d96d282a7bdf641cdb9c53a4600
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/22/2019
ms.locfileid: "37622603"
---
# <a name="orgcontact-resource-type"></a><span data-ttu-id="a87e0-103">orgContact 资源类型</span><span class="sxs-lookup"><span data-stu-id="a87e0-103">orgContact resource type</span></span>

<span data-ttu-id="a87e0-104">表示一个组织联系人。</span><span class="sxs-lookup"><span data-stu-id="a87e0-104">Represents an organizational contact.</span></span> <span data-ttu-id="a87e0-105">组织联系人由组织的管理员管理，不同于[个人联系人](contact.md)。</span><span class="sxs-lookup"><span data-stu-id="a87e0-105">Organizational contacts are managed by an organization's administrators and are different from [personal contacts](contact.md).</span></span> <span data-ttu-id="a87e0-106">此外，组织联系人既可以从本地目录同步，也可以从 Exchange Online 同步，也可以是只读的。</span><span class="sxs-lookup"><span data-stu-id="a87e0-106">Additionally, organizational contacts are either synchronized from on-premises directories or from Exchange Online, and are read-only.</span></span>

<span data-ttu-id="a87e0-107">继承自 [directoryObject](directoryobject.md)。</span><span class="sxs-lookup"><span data-stu-id="a87e0-107">Inherits from [directoryObject](directoryobject.md).</span></span>

## <a name="methods"></a><span data-ttu-id="a87e0-108">方法</span><span class="sxs-lookup"><span data-stu-id="a87e0-108">Methods</span></span>

| <span data-ttu-id="a87e0-109">方法</span><span class="sxs-lookup"><span data-stu-id="a87e0-109">Method</span></span>           | <span data-ttu-id="a87e0-110">返回类型</span><span class="sxs-lookup"><span data-stu-id="a87e0-110">Return Type</span></span>    |<span data-ttu-id="a87e0-111">说明</span><span class="sxs-lookup"><span data-stu-id="a87e0-111">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="a87e0-112">列出 organizationl 联系人</span><span class="sxs-lookup"><span data-stu-id="a87e0-112">List organizationl contacts</span></span>](../api/orgcontact-list.md) | [<span data-ttu-id="a87e0-113">orgContact</span><span class="sxs-lookup"><span data-stu-id="a87e0-113">orgContact</span></span>](orgcontact.md) |<span data-ttu-id="a87e0-114">列出组织联系人的属性。</span><span class="sxs-lookup"><span data-stu-id="a87e0-114">List properties of organizational contacts.</span></span>|
|[<span data-ttu-id="a87e0-115">获取 organizationl 联系人</span><span class="sxs-lookup"><span data-stu-id="a87e0-115">Get organizationl contact</span></span>](../api/orgcontact-get.md) | [<span data-ttu-id="a87e0-116">orgContact</span><span class="sxs-lookup"><span data-stu-id="a87e0-116">orgContact</span></span>](orgcontact.md) |<span data-ttu-id="a87e0-117">读取组织联系人的属性和关系。</span><span class="sxs-lookup"><span data-stu-id="a87e0-117">Read properties and relationships of an organizational contact.</span></span>|
|[<span data-ttu-id="a87e0-118">获取管理器</span><span class="sxs-lookup"><span data-stu-id="a87e0-118">Get manager</span></span>](../api/orgcontact-get-manager.md) |[<span data-ttu-id="a87e0-119">directoryObject</span><span class="sxs-lookup"><span data-stu-id="a87e0-119">directoryObject</span></span>](directoryobject.md)| <span data-ttu-id="a87e0-120">获取组织联系人的经理。</span><span class="sxs-lookup"><span data-stu-id="a87e0-120">Get the organizational contact's manager.</span></span>|
|[<span data-ttu-id="a87e0-121">List directReports</span><span class="sxs-lookup"><span data-stu-id="a87e0-121">List directReports</span></span>](../api/orgcontact-list-directreports.md) |<span data-ttu-id="a87e0-122">[directoryObject](directoryobject.md) collection</span><span class="sxs-lookup"><span data-stu-id="a87e0-122">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="a87e0-123">列出组织联系人的直接下属。</span><span class="sxs-lookup"><span data-stu-id="a87e0-123">List the organizational contact's direct reports.</span></span>|
|[<span data-ttu-id="a87e0-124">List memberOf</span><span class="sxs-lookup"><span data-stu-id="a87e0-124">List memberOf</span></span>](../api/orgcontact-list-memberof.md) |<span data-ttu-id="a87e0-125">[directoryObject](directoryobject.md) 集合</span><span class="sxs-lookup"><span data-stu-id="a87e0-125">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="a87e0-126">列出组织联系人所属的组。</span><span class="sxs-lookup"><span data-stu-id="a87e0-126">List the groups an organizational contact is a member of.</span></span>|
|[<span data-ttu-id="a87e0-127">列出 transitiveMemberOf</span><span class="sxs-lookup"><span data-stu-id="a87e0-127">List transitiveMemberOf</span></span>](../api/orgcontact-list-transitivememberof.md) |<span data-ttu-id="a87e0-128">[directoryObject](directoryobject.md) collection</span><span class="sxs-lookup"><span data-stu-id="a87e0-128">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="a87e0-129">列出组织联系人所属的组，包括组织联系人所嵌套的组。</span><span class="sxs-lookup"><span data-stu-id="a87e0-129">List the groups an organizational contact is a member of, including groups that the organizational contact is nested under.</span></span>|
|[<span data-ttu-id="a87e0-130">checkMemberGroups</span><span class="sxs-lookup"><span data-stu-id="a87e0-130">checkMemberGroups</span></span>](../api/orgcontact-checkmembergroups.md)|<span data-ttu-id="a87e0-131">String collection</span><span class="sxs-lookup"><span data-stu-id="a87e0-131">String collection</span></span>| <span data-ttu-id="a87e0-132">检查组成员身份。</span><span class="sxs-lookup"><span data-stu-id="a87e0-132">Check for group membership.</span></span> |
|[<span data-ttu-id="a87e0-133">getMemberGroups</span><span class="sxs-lookup"><span data-stu-id="a87e0-133">getMemberGroups</span></span>](../api/orgcontact-getmembergroups.md)|<span data-ttu-id="a87e0-134">String collection</span><span class="sxs-lookup"><span data-stu-id="a87e0-134">String collection</span></span>| <span data-ttu-id="a87e0-135">返回指定的组织联系人所属的所有组。</span><span class="sxs-lookup"><span data-stu-id="a87e0-135">Return all the groups that the specified organizational contact is a member of.</span></span> |
|[<span data-ttu-id="a87e0-136">getMemberObjects</span><span class="sxs-lookup"><span data-stu-id="a87e0-136">getMemberObjects</span></span>](../api/orgcontact-getmemberobjects.md)|<span data-ttu-id="a87e0-137">String collection</span><span class="sxs-lookup"><span data-stu-id="a87e0-137">String collection</span></span>| <span data-ttu-id="a87e0-138">返回组织联系人所属的 directoryObjects 的列表。</span><span class="sxs-lookup"><span data-stu-id="a87e0-138">Returns a list of directoryObjects the organizational contact is a member of.</span></span> |

## <a name="properties"></a><span data-ttu-id="a87e0-139">属性</span><span class="sxs-lookup"><span data-stu-id="a87e0-139">Properties</span></span>

| <span data-ttu-id="a87e0-140">属性</span><span class="sxs-lookup"><span data-stu-id="a87e0-140">Property</span></span>     | <span data-ttu-id="a87e0-141">类型</span><span class="sxs-lookup"><span data-stu-id="a87e0-141">Type</span></span>   |<span data-ttu-id="a87e0-142">说明</span><span class="sxs-lookup"><span data-stu-id="a87e0-142">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="a87e0-143">探讨</span><span class="sxs-lookup"><span data-stu-id="a87e0-143">addresses</span></span>                    | <span data-ttu-id="a87e0-144">[physicalOfficeAddress](physicalofficeaddress.md)集合</span><span class="sxs-lookup"><span data-stu-id="a87e0-144">[physicalOfficeAddress](physicalofficeaddress.md) collection</span></span>           | <span data-ttu-id="a87e0-145">此组织联系人的邮政地址。</span><span class="sxs-lookup"><span data-stu-id="a87e0-145">Postal addresses for this organizational contact.</span></span> <span data-ttu-id="a87e0-146">目前，一个联系人只能有一个实际地址。</span><span class="sxs-lookup"><span data-stu-id="a87e0-146">For now a contact can only have one physical address.</span></span> |
| <span data-ttu-id="a87e0-147">companyName</span><span class="sxs-lookup"><span data-stu-id="a87e0-147">companyName</span></span>                  | <span data-ttu-id="a87e0-148">String</span><span class="sxs-lookup"><span data-stu-id="a87e0-148">String</span></span>                                                    | <span data-ttu-id="a87e0-149">此组织联系人所属的公司的名称。</span><span class="sxs-lookup"><span data-stu-id="a87e0-149">Name of the company that this organizational contact belong to.</span></span>                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="a87e0-150">department</span><span class="sxs-lookup"><span data-stu-id="a87e0-150">department</span></span>                   | <span data-ttu-id="a87e0-151">String</span><span class="sxs-lookup"><span data-stu-id="a87e0-151">String</span></span>                                                     | <span data-ttu-id="a87e0-152">联系人工作所在的部门的名称。</span><span class="sxs-lookup"><span data-stu-id="a87e0-152">The name for the department in which the contact works.</span></span>                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="a87e0-153">displayName</span><span class="sxs-lookup"><span data-stu-id="a87e0-153">displayName</span></span>                  | <span data-ttu-id="a87e0-154">String</span><span class="sxs-lookup"><span data-stu-id="a87e0-154">String</span></span>                                                     | <span data-ttu-id="a87e0-155">此组织联系人的显示名称。</span><span class="sxs-lookup"><span data-stu-id="a87e0-155">Display name for this organizational contact.</span></span>                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="a87e0-156">givenName</span><span class="sxs-lookup"><span data-stu-id="a87e0-156">givenName</span></span>                    | <span data-ttu-id="a87e0-157">String</span><span class="sxs-lookup"><span data-stu-id="a87e0-157">String</span></span>                                                     | <span data-ttu-id="a87e0-158">此组织联系人的名字。</span><span class="sxs-lookup"><span data-stu-id="a87e0-158">First name for this organizational contact.</span></span>                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="a87e0-159">id</span><span class="sxs-lookup"><span data-stu-id="a87e0-159">id</span></span>                           | <span data-ttu-id="a87e0-160">字符串</span><span class="sxs-lookup"><span data-stu-id="a87e0-160">String</span></span>                                                     | <span data-ttu-id="a87e0-161">此组织联系人的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="a87e0-161">Unique identifier for this organizational contact.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="a87e0-162">jobTitle</span><span class="sxs-lookup"><span data-stu-id="a87e0-162">jobTitle</span></span>                     | <span data-ttu-id="a87e0-163">String</span><span class="sxs-lookup"><span data-stu-id="a87e0-163">String</span></span>                                                     | <span data-ttu-id="a87e0-164">此组织联系人的职务。</span><span class="sxs-lookup"><span data-stu-id="a87e0-164">Job title for this organizational contact.</span></span>                                                                                                                                                                                                                                                                                                                                      |
|<span data-ttu-id="a87e0-165">mail</span><span class="sxs-lookup"><span data-stu-id="a87e0-165">mail</span></span>|<span data-ttu-id="a87e0-166">String</span><span class="sxs-lookup"><span data-stu-id="a87e0-166">String</span></span>| <span data-ttu-id="a87e0-167">联系人的 SMTP 地址，例如，"jeff@contoso.onmicrosoft.com"。</span><span class="sxs-lookup"><span data-stu-id="a87e0-167">The SMTP address for the contact, for example, "jeff@contoso.onmicrosoft.com".</span></span> |
| <span data-ttu-id="a87e0-168">mailNickname</span><span class="sxs-lookup"><span data-stu-id="a87e0-168">mailNickname</span></span>                 | <span data-ttu-id="a87e0-169">字符串</span><span class="sxs-lookup"><span data-stu-id="a87e0-169">String</span></span>                                                     | <span data-ttu-id="a87e0-170">此组织联系人的电子邮件别名（电子邮件地址的部分预挂起的 "@" 符号）。</span><span class="sxs-lookup"><span data-stu-id="a87e0-170">Email alias (portion of email address pre-pending the @ symbol) for this organizational contact.</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="a87e0-171">onPremisesLastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="a87e0-171">onPremisesLastSyncDateTime</span></span>   | <span data-ttu-id="a87e0-172">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a87e0-172">DateTimeOffset</span></span>                                             | <span data-ttu-id="a87e0-173">上次从本地 AD 同步此组织联系人的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="a87e0-173">Date and time when this organizational contact was last synchronized from on-premises AD.</span></span> <span data-ttu-id="a87e0-174">此日期和时间信息使用 ISO 8601 格式，并且始终采用 UTC 时间。</span><span class="sxs-lookup"><span data-stu-id="a87e0-174">This date and time information uses ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="a87e0-175">例如，2014 年 1 月 1 日午夜 (UTC) 如下所示：“2014-01-01T00:00:00Z”。</span><span class="sxs-lookup"><span data-stu-id="a87e0-175">For example, midnight UTC on Jan 1, 2014 would look like this: '2014-01-01T00:00:00Z'.</span></span>   |
| <span data-ttu-id="a87e0-176">onPremisesProvisioningErrors</span><span class="sxs-lookup"><span data-stu-id="a87e0-176">onPremisesProvisioningErrors</span></span> |<span data-ttu-id="a87e0-177">[onPremisesProvisioningError](onpremisesprovisioningerror.md) 集合</span><span class="sxs-lookup"><span data-stu-id="a87e0-177">[onPremisesProvisioningError](onpremisesprovisioningerror.md) collection</span></span>       | <span data-ttu-id="a87e0-178">此组织联系人的任何同步设置错误列表。</span><span class="sxs-lookup"><span data-stu-id="a87e0-178">List of any synchronization provisioning errors for this organizational contact.</span></span>                                                                                                                                                                                                                                                                                                |
|<span data-ttu-id="a87e0-179">onPremisesSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="a87e0-179">onPremisesSyncEnabled</span></span>|<span data-ttu-id="a87e0-180">Boolean</span><span class="sxs-lookup"><span data-stu-id="a87e0-180">Boolean</span></span>|<span data-ttu-id="a87e0-181">如果此对象从本地目录同步，**则为 true** ; 否则为 false。**假**如果此对象最初是从本地目录同步，但不再同步，并且现在在 Exchange 中的 mastered;如果从未从本地目录同步此对象（默认），则**为 null** 。</span><span class="sxs-lookup"><span data-stu-id="a87e0-181">**true** if this object is synced from an on-premises directory; **false** if this object was originally synced from an on-premises directory but is no longer synced and now mastered in Exchange; **null** if this object has never been synced from an on-premises directory (default).</span></span>|
| <span data-ttu-id="a87e0-182">phones</span><span class="sxs-lookup"><span data-stu-id="a87e0-182">phones</span></span>                       | <span data-ttu-id="a87e0-183">[phone](phone.md) collection</span><span class="sxs-lookup"><span data-stu-id="a87e0-183">[phone](phone.md) collection</span></span>                            | <span data-ttu-id="a87e0-184">此组织联系人的电话列表。</span><span class="sxs-lookup"><span data-stu-id="a87e0-184">List of phones for this organizational contact.</span></span> <span data-ttu-id="a87e0-185">电话类型可以是移动、商业和 businessFax。</span><span class="sxs-lookup"><span data-stu-id="a87e0-185">Phone types can be mobile, business, and businessFax.</span></span> <span data-ttu-id="a87e0-186">集合中仅有一种类型可以存在。</span><span class="sxs-lookup"><span data-stu-id="a87e0-186">Only one of each type can ever be present in the collection.</span></span>                                                                                                                       |
| <span data-ttu-id="a87e0-187">proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="a87e0-187">proxyAddresses</span></span>               | <span data-ttu-id="a87e0-188">String collection</span><span class="sxs-lookup"><span data-stu-id="a87e0-188">String collection</span></span>                                         | <span data-ttu-id="a87e0-189">例如： "SMTP： bob@contoso.com"、"SMTP： bob@sales.contoso.com"。</span><span class="sxs-lookup"><span data-stu-id="a87e0-189">For example: "SMTP: bob@contoso.com", "smtp: bob@sales.contoso.com".</span></span> <span data-ttu-id="a87e0-190">多值属性筛选器表达式需要 **any** 运算符。</span><span class="sxs-lookup"><span data-stu-id="a87e0-190">The **any** operator is required for filter expressions on multi-valued properties.</span></span> <span data-ttu-id="a87e0-191">支持\$筛选器。</span><span class="sxs-lookup"><span data-stu-id="a87e0-191">Supports \$filter.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="a87e0-192">surname</span><span class="sxs-lookup"><span data-stu-id="a87e0-192">surname</span></span>                      | <span data-ttu-id="a87e0-193">String</span><span class="sxs-lookup"><span data-stu-id="a87e0-193">String</span></span>                                                     | <span data-ttu-id="a87e0-194">此组织联系人的姓氏。</span><span class="sxs-lookup"><span data-stu-id="a87e0-194">Last name for this organizational contact.</span></span>                          |

## <a name="relationships"></a><span data-ttu-id="a87e0-195">关系</span><span class="sxs-lookup"><span data-stu-id="a87e0-195">Relationships</span></span>

| <span data-ttu-id="a87e0-196">关系</span><span class="sxs-lookup"><span data-stu-id="a87e0-196">Relationship</span></span> | <span data-ttu-id="a87e0-197">类型</span><span class="sxs-lookup"><span data-stu-id="a87e0-197">Type</span></span>   |<span data-ttu-id="a87e0-198">说明</span><span class="sxs-lookup"><span data-stu-id="a87e0-198">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a87e0-199">directReports</span><span class="sxs-lookup"><span data-stu-id="a87e0-199">directReports</span></span>|<span data-ttu-id="a87e0-200">[directoryObject](directoryobject.md) collection</span><span class="sxs-lookup"><span data-stu-id="a87e0-200">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="a87e0-201">联系人的直接下属。</span><span class="sxs-lookup"><span data-stu-id="a87e0-201">The contact's direct reports.</span></span> <span data-ttu-id="a87e0-202">（其 "经理" 属性设置为 "联系人" 的用户和联系人。） 只读。</span><span class="sxs-lookup"><span data-stu-id="a87e0-202">(The users and contacts that have their manager property set to this contact.)  Read-only.</span></span> <span data-ttu-id="a87e0-203">可为 Null。</span><span class="sxs-lookup"><span data-stu-id="a87e0-203">Nullable.</span></span>|
|<span data-ttu-id="a87e0-204">manager</span><span class="sxs-lookup"><span data-stu-id="a87e0-204">manager</span></span>|[<span data-ttu-id="a87e0-205">directoryObject</span><span class="sxs-lookup"><span data-stu-id="a87e0-205">directoryObject</span></span>](directoryobject.md)| <span data-ttu-id="a87e0-206">作为此联系人的经理的用户或联系人。</span><span class="sxs-lookup"><span data-stu-id="a87e0-206">The user or contact that is this contact's manager.</span></span> <span data-ttu-id="a87e0-207">只读。</span><span class="sxs-lookup"><span data-stu-id="a87e0-207">Read-only.</span></span>|
|<span data-ttu-id="a87e0-208">memberOf</span><span class="sxs-lookup"><span data-stu-id="a87e0-208">memberOf</span></span>|<span data-ttu-id="a87e0-209">[directoryObject](directoryobject.md) collection</span><span class="sxs-lookup"><span data-stu-id="a87e0-209">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="a87e0-210">此联系人所属的组。</span><span class="sxs-lookup"><span data-stu-id="a87e0-210">Groups that this contact is a member of.</span></span> <span data-ttu-id="a87e0-211">只读。</span><span class="sxs-lookup"><span data-stu-id="a87e0-211">Read-only.</span></span> <span data-ttu-id="a87e0-212">可为 Null。</span><span class="sxs-lookup"><span data-stu-id="a87e0-212">Nullable.</span></span>|
|<span data-ttu-id="a87e0-213">transitiveMemberOf</span><span class="sxs-lookup"><span data-stu-id="a87e0-213">transitiveMemberOf</span></span>|<span data-ttu-id="a87e0-214">[directoryObject](directoryobject.md) collection</span><span class="sxs-lookup"><span data-stu-id="a87e0-214">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="a87e0-215">此联系人所属的组，包括将联系人嵌套在其下的组。</span><span class="sxs-lookup"><span data-stu-id="a87e0-215">Groups that this contact is a member of, including groups that the contact is nested under.</span></span>|<span data-ttu-id="a87e0-216">.</span><span class="sxs-lookup"><span data-stu-id="a87e0-216"></span></span> <span data-ttu-id="a87e0-217">只读。</span><span class="sxs-lookup"><span data-stu-id="a87e0-217">Read-only.</span></span> <span data-ttu-id="a87e0-218">可为 Null。</span><span class="sxs-lookup"><span data-stu-id="a87e0-218">Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="a87e0-219">JSON 表示形式</span><span class="sxs-lookup"><span data-stu-id="a87e0-219">JSON representation</span></span>

<span data-ttu-id="a87e0-220">下面是资源的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="a87e0-220">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "directReports",
    "manager",
    "memberOf"
  ],
  "keyProperty": "id",
  "baseType":"microsoft.graph.entity",  
  "@odata.type": "microsoft.graph.orgcontact"
}-->

```json
{
  "addresses": [{"@odata.type": "microsoft.graph.physicalOfficeAddress"}],
  "companyName": "string",
  "department": "string",
  "displayName": "string",
  "givenName": "string",
  "id": "string (identifier)",
  "jobTitle": "string",
  "mail": "string",
  "mailNickname": "string",
  "onPremisesLastSyncDateTime": "string (timestamp)",
  "onPremisesProvisioningErrors": [{"@odata.type": "microsoft.graph.onPremisesProvisioningError"}],
  "onPremisesSyncEnabled": true,
  "phones": [{"@odata.type": "microsoft.graph.phone"}],
  "proxyAddresses": ["string"],
  "surname": "string"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "orgContact resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->