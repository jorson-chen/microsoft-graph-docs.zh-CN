---
title: evaluateDynamicMembershipResult 资源类型
description: 表示成员资格评估的结果。
localization_priority: Normal
author: yyuank
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: b6e40c796468a8c31d2cd75dd2b6815440bfb71e
ms.sourcegitcommit: 62c900af626e46439d949462f09061cc5c41d6ff
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/16/2020
ms.locfileid: "44272826"
---
# <a name="evaluatedynamicmembershipresult-resource-type"></a><span data-ttu-id="e4d29-103">evaluateDynamicMembershipResult 资源类型</span><span class="sxs-lookup"><span data-stu-id="e4d29-103">evaluateDynamicMembershipResult resource type</span></span>

<span data-ttu-id="e4d29-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="e4d29-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="e4d29-105">表示成员资格评估的结果。</span><span class="sxs-lookup"><span data-stu-id="e4d29-105">Represents the result of membership evaluation.</span></span>

## <a name="properties"></a><span data-ttu-id="e4d29-106">属性</span><span class="sxs-lookup"><span data-stu-id="e4d29-106">Properties</span></span>

| <span data-ttu-id="e4d29-107">属性</span><span class="sxs-lookup"><span data-stu-id="e4d29-107">Property</span></span> | <span data-ttu-id="e4d29-108">类型</span><span class="sxs-lookup"><span data-stu-id="e4d29-108">Type</span></span> | <span data-ttu-id="e4d29-109">Description</span><span class="sxs-lookup"><span data-stu-id="e4d29-109">Description</span></span> |
|:-------- |:---- |:----------- |
| <span data-ttu-id="e4d29-110">membershipRule</span><span class="sxs-lookup"><span data-stu-id="e4d29-110">membershipRule</span></span> | <span data-ttu-id="e4d29-111">String</span><span class="sxs-lookup"><span data-stu-id="e4d29-111">String</span></span> | <span data-ttu-id="e4d29-112">如果提供了组 ID，则此值为组的成员身份规则。</span><span class="sxs-lookup"><span data-stu-id="e4d29-112">If a group ID is provided, the value is the membership rule for the group.</span></span> <span data-ttu-id="e4d29-113">如果未提供组 ID，则值是作为参数提供的成员身份规则。</span><span class="sxs-lookup"><span data-stu-id="e4d29-113">If a group ID is not provided, the value is the membership rule that was provided as a parameter.</span></span> <span data-ttu-id="e4d29-114">有关详细信息，请参阅[Azure Active Directory 中的组的动态成员身份规则](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-dynamic-membership)。</span><span class="sxs-lookup"><span data-stu-id="e4d29-114">For more information, see [Dynamic membership rules for groups in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-dynamic-membership).</span></span> |
| <span data-ttu-id="e4d29-115">membershipRuleEvaluationDetails</span><span class="sxs-lookup"><span data-stu-id="e4d29-115">membershipRuleEvaluationDetails</span></span> | [<span data-ttu-id="e4d29-116">expressionEvaluationDetails</span><span class="sxs-lookup"><span data-stu-id="e4d29-116">expressionEvaluationDetails</span></span>](expressionevaluationdetails.md) | <span data-ttu-id="e4d29-117">提供成员资格评估结果的详细 anaylsis。</span><span class="sxs-lookup"><span data-stu-id="e4d29-117">Provides a detailed anaylsis of the membership evaluation result.</span></span> |
| <span data-ttu-id="e4d29-118">membershipRuleEvaluationResult</span><span class="sxs-lookup"><span data-stu-id="e4d29-118">membershipRuleEvaluationResult</span></span> | <span data-ttu-id="e4d29-119">Boolean</span><span class="sxs-lookup"><span data-stu-id="e4d29-119">Boolean</span></span> | <span data-ttu-id="e4d29-120">值为 `true` 用户或设备是否为组的成员。</span><span class="sxs-lookup"><span data-stu-id="e4d29-120">The value is `true` if the user or device is a member of the group.</span></span> <span data-ttu-id="e4d29-121">`true`如果提供了成员身份规则，并且用户或设备传递了规则评估，则也可以是值; 否则，也是如此 `false` 。</span><span class="sxs-lookup"><span data-stu-id="e4d29-121">The value can also be `true` if a membership rule was provided and the user or device passes the rule evaluation; otherwise `false`.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="e4d29-122">JSON 表示形式</span><span class="sxs-lookup"><span data-stu-id="e4d29-122">JSON representation</span></span>

<span data-ttu-id="e4d29-123">下面是资源的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="e4d29-123">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.evaluateDynamicMembershipResult",
  "baseType": null
}-->

```json
{
  "membershipRule": "String",
  "membershipRuleEvaluationDetails": {"@odata.type": "microsoft.graph.expressionEvaluationDetails"},
  "membershipRuleEvaluationResult": true
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "evaluateDynamicMembershipResult resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->