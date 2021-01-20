---
title: groupLifecyclePolicy 资源类型
description: 表示 Microsoft 365 组的生命周期策略。
localization_priority: Normal
author: yyuank
ms.prod: groups
doc_type: resourcePageType
ms.openlocfilehash: 647187e7eee5c26a03cff800c5e6a7628d9166e3
ms.sourcegitcommit: 6314172db76ba9f2c192d8c099d818c5e772d2b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/20/2021
ms.locfileid: "49910316"
---
# <a name="grouplifecyclepolicy-resource-type"></a><span data-ttu-id="ac644-103">groupLifecyclePolicy 资源类型</span><span class="sxs-lookup"><span data-stu-id="ac644-103">groupLifecyclePolicy resource type</span></span>

<span data-ttu-id="ac644-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="ac644-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="ac644-105">表示 Microsoft 365 组的生命周期策略。</span><span class="sxs-lookup"><span data-stu-id="ac644-105">Represents a lifecycle policy for a Microsoft 365 group.</span></span> <span data-ttu-id="ac644-106">使用组生命周期策略，管理员可以为组设置到期期限。</span><span class="sxs-lookup"><span data-stu-id="ac644-106">A group lifecycle policy allows administrators to set an expiration period for groups.</span></span> <span data-ttu-id="ac644-107">例如，组在 180 天后到期。</span><span class="sxs-lookup"><span data-stu-id="ac644-107">For example, after 180 days, a group expires.</span></span> <span data-ttu-id="ac644-108">如果组到期，组的所有者必须在管理员定义的时间段内续订组。</span><span class="sxs-lookup"><span data-stu-id="ac644-108">When a group reaches its expiration, owners of the group are required to renew their group within a time interval defined by the administrator.</span></span> <span data-ttu-id="ac644-109">续订后，组的有效期就会延长策略中定义的天数。</span><span class="sxs-lookup"><span data-stu-id="ac644-109">Once renewed, the group expiration is extended by the number of days defined in the policy.</span></span> <span data-ttu-id="ac644-110">例如，续订后，组的新到期时间是在 180 天后。</span><span class="sxs-lookup"><span data-stu-id="ac644-110">For example, the group's new expiration is 180 days after renewal.</span></span> <span data-ttu-id="ac644-111">如果不续订组，组就会到期并被删除。</span><span class="sxs-lookup"><span data-stu-id="ac644-111">If the group is not renewed, it expires and is deleted.</span></span> <span data-ttu-id="ac644-112">可以在删除后的 30 天内还原组。</span><span class="sxs-lookup"><span data-stu-id="ac644-112">The group can be restored within a period of 30 days from deletion.</span></span>

## <a name="methods"></a><span data-ttu-id="ac644-113">Methods</span><span class="sxs-lookup"><span data-stu-id="ac644-113">Methods</span></span>

| <span data-ttu-id="ac644-114">方法</span><span class="sxs-lookup"><span data-stu-id="ac644-114">Method</span></span> | <span data-ttu-id="ac644-115">返回类型</span><span class="sxs-lookup"><span data-stu-id="ac644-115">Return Type</span></span> | <span data-ttu-id="ac644-116">说明</span><span class="sxs-lookup"><span data-stu-id="ac644-116">Description</span></span> |
|:---------------|:--------|:----------|
|[<span data-ttu-id="ac644-117">获取 groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="ac644-117">Get groupLifecyclePolicy</span></span>](../api/grouplifecyclepolicy-get.md) | [<span data-ttu-id="ac644-118">groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="ac644-118">groupLifecyclePolicy</span></span>](grouplifecyclepolicy.md) |<span data-ttu-id="ac644-119">读取 groupLifecyclePolicy 对象的属性和关系。</span><span class="sxs-lookup"><span data-stu-id="ac644-119">Read properties and relationships of a groupLifecyclePolicy object.</span></span>|
|[<span data-ttu-id="ac644-120">列出 groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="ac644-120">List groupLifecyclePolicies</span></span>](../api/grouplifecyclepolicy-list.md) | <span data-ttu-id="ac644-121">[groupLifecyclePolicy](grouplifecyclepolicy.md) 集合</span><span class="sxs-lookup"><span data-stu-id="ac644-121">[groupLifecyclePolicy](grouplifecyclepolicy.md) collection</span></span> | <span data-ttu-id="ac644-122">列出所有 groupLifecyclePolicy。</span><span class="sxs-lookup"><span data-stu-id="ac644-122">List all the groupLifecyclePolicies.</span></span> |
|[<span data-ttu-id="ac644-123">更新 groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="ac644-123">Update groupLifecyclePolicy</span></span>](../api/grouplifecyclepolicy-update.md) | [<span data-ttu-id="ac644-124">groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="ac644-124">groupLifecyclePolicy</span></span>](grouplifecyclepolicy.md) | <span data-ttu-id="ac644-125">更新 groupLifecyclePolicy 对象。</span><span class="sxs-lookup"><span data-stu-id="ac644-125">Update a groupLifecyclePolicy object.</span></span> |
|[<span data-ttu-id="ac644-126">删除 groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="ac644-126">Delete groupLifecyclePolicy</span></span>](../api/grouplifecyclepolicy-delete.md) | <span data-ttu-id="ac644-127">无</span><span class="sxs-lookup"><span data-stu-id="ac644-127">None</span></span> | <span data-ttu-id="ac644-128">删除 groupLifecyclePolicy 对象。</span><span class="sxs-lookup"><span data-stu-id="ac644-128">Delete a groupLifecyclePolicy object.</span></span> |
|[<span data-ttu-id="ac644-129">向 groupLifecyclePolicy 添加组</span><span class="sxs-lookup"><span data-stu-id="ac644-129">Add a group to a groupLifecyclePolicy</span></span>](../api/grouplifecyclepolicy-addgroup.md)|<span data-ttu-id="ac644-130">无</span><span class="sxs-lookup"><span data-stu-id="ac644-130">None</span></span>| <span data-ttu-id="ac644-131">向生命周期策略添加组</span><span class="sxs-lookup"><span data-stu-id="ac644-131">Add a group to a lifecycle policy</span></span> |
|[<span data-ttu-id="ac644-132">从 groupLifecyclePolicy 中删除组</span><span class="sxs-lookup"><span data-stu-id="ac644-132">Remove a group from a groupLifecyclePolicy</span></span>](../api/grouplifecyclepolicy-removegroup.md)|<span data-ttu-id="ac644-133">无</span><span class="sxs-lookup"><span data-stu-id="ac644-133">None</span></span>| <span data-ttu-id="ac644-134">从生命周期策略中删除组</span><span class="sxs-lookup"><span data-stu-id="ac644-134">Remove a group to a lifecycle policy.</span></span> |
|[<span data-ttu-id="ac644-135">续订组</span><span class="sxs-lookup"><span data-stu-id="ac644-135">Renew a group</span></span>](../api/grouplifecyclepolicy-renewgroup.md)|<span data-ttu-id="ac644-136">无</span><span class="sxs-lookup"><span data-stu-id="ac644-136">None</span></span>| <span data-ttu-id="ac644-137">续订组的到期日期。</span><span class="sxs-lookup"><span data-stu-id="ac644-137">Renew a group's expiration date.</span></span> |

## <a name="properties"></a><span data-ttu-id="ac644-138">属性</span><span class="sxs-lookup"><span data-stu-id="ac644-138">Properties</span></span>

| <span data-ttu-id="ac644-139">属性</span><span class="sxs-lookup"><span data-stu-id="ac644-139">Property</span></span> | <span data-ttu-id="ac644-140">类型</span><span class="sxs-lookup"><span data-stu-id="ac644-140">Type</span></span> | <span data-ttu-id="ac644-141">说明</span><span class="sxs-lookup"><span data-stu-id="ac644-141">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="ac644-142">alternateNotificationEmails</span><span class="sxs-lookup"><span data-stu-id="ac644-142">alternateNotificationEmails</span></span>|<span data-ttu-id="ac644-143">String</span><span class="sxs-lookup"><span data-stu-id="ac644-143">String</span></span>| <span data-ttu-id="ac644-144">针对没有所有者的组向其发送通知的电子邮件地址列表。</span><span class="sxs-lookup"><span data-stu-id="ac644-144">List of email address to send notifications for groups without owners.</span></span> <span data-ttu-id="ac644-145">可以用分号隔开电子邮件地址，从而定义多个电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="ac644-145">Multiple email address can be defined by separating email address with a semicolon.</span></span> |
|<span data-ttu-id="ac644-146">groupLifetimeInDays</span><span class="sxs-lookup"><span data-stu-id="ac644-146">groupLifetimeInDays</span></span>|<span data-ttu-id="ac644-147">Int32</span><span class="sxs-lookup"><span data-stu-id="ac644-147">Int32</span></span>| <span data-ttu-id="ac644-148">还剩多少天组就到期且需要续订。</span><span class="sxs-lookup"><span data-stu-id="ac644-148">Number of days before a group expires and needs to be renewed.</span></span> <span data-ttu-id="ac644-149">续订后，组的有效期就会延长定义的天数。</span><span class="sxs-lookup"><span data-stu-id="ac644-149">Once renewed, the group expiration is extended by the number of days defined.</span></span> |
|<span data-ttu-id="ac644-150">id</span><span class="sxs-lookup"><span data-stu-id="ac644-150">id</span></span>|<span data-ttu-id="ac644-151">Guid</span><span class="sxs-lookup"><span data-stu-id="ac644-151">Guid</span></span>| <span data-ttu-id="ac644-152">策略的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="ac644-152">A unique identifier for a policy.</span></span> <span data-ttu-id="ac644-153">只读。</span><span class="sxs-lookup"><span data-stu-id="ac644-153">Read-only.</span></span>|
|<span data-ttu-id="ac644-154">managedGroupTypes</span><span class="sxs-lookup"><span data-stu-id="ac644-154">managedGroupTypes</span></span>|<span data-ttu-id="ac644-155">String</span><span class="sxs-lookup"><span data-stu-id="ac644-155">String</span></span>| <span data-ttu-id="ac644-156">到期策略适用的组类型。</span><span class="sxs-lookup"><span data-stu-id="ac644-156">The group type for which the expiration policy applies.</span></span> <span data-ttu-id="ac644-157">可取值为 **All**、**Selected** 或 **None**。</span><span class="sxs-lookup"><span data-stu-id="ac644-157">Possible values are **All**, **Selected** or **None**.</span></span> |

## <a name="relationships"></a><span data-ttu-id="ac644-158">关系</span><span class="sxs-lookup"><span data-stu-id="ac644-158">Relationships</span></span>

<span data-ttu-id="ac644-159">无。</span><span class="sxs-lookup"><span data-stu-id="ac644-159">None.</span></span>

## <a name="json-representation"></a><span data-ttu-id="ac644-160">JSON 表示形式</span><span class="sxs-lookup"><span data-stu-id="ac644-160">JSON representation</span></span>

<span data-ttu-id="ac644-161">下面是资源的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="ac644-161">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.groupLifecyclePolicy"
}-->

```json
{
  "alternateNotificationEmails": "String",
  "groupLifetimeInDays": 180,
  "id": "Guid (identifier)",
  "managedGroupTypes": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "groupLifecyclePolicy resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


