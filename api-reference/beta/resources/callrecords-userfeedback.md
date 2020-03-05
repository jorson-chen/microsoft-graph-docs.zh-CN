---
title: userFeedback 资源类型
description: UserFeedback 类型。
localization_priority: Normal
author: stephenjust
ms.prod: cloud-communications
doc_type: resourcePageType
ms.openlocfilehash: 0ab9c49563bb4715b1736618a939b681178ddae8
ms.sourcegitcommit: d3b6e4d11012e6b4c775afcec4fe5444e3a99bd3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/03/2020
ms.locfileid: "42394684"
---
# <a name="userfeedback-resource-type"></a><span data-ttu-id="0b9d3-103">userFeedback 资源类型</span><span class="sxs-lookup"><span data-stu-id="0b9d3-103">userFeedback resource type</span></span>

<span data-ttu-id="0b9d3-104">命名空间： callRecords</span><span class="sxs-lookup"><span data-stu-id="0b9d3-104">Namespace: microsoft.graph.callRecords</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="0b9d3-105">代表用户提供的有关会话质量的终结点的反馈。</span><span class="sxs-lookup"><span data-stu-id="0b9d3-105">Represents the feedback provided by the user an endpoint about the quality of the session.</span></span>

## <a name="properties"></a><span data-ttu-id="0b9d3-106">属性</span><span class="sxs-lookup"><span data-stu-id="0b9d3-106">Properties</span></span>

| <span data-ttu-id="0b9d3-107">属性</span><span class="sxs-lookup"><span data-stu-id="0b9d3-107">Property</span></span>     | <span data-ttu-id="0b9d3-108">类型</span><span class="sxs-lookup"><span data-stu-id="0b9d3-108">Type</span></span>        | <span data-ttu-id="0b9d3-109">说明</span><span class="sxs-lookup"><span data-stu-id="0b9d3-109">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="0b9d3-110">评估</span><span class="sxs-lookup"><span data-stu-id="0b9d3-110">rating</span></span>|<span data-ttu-id="0b9d3-111">String</span><span class="sxs-lookup"><span data-stu-id="0b9d3-111">String</span></span>|<span data-ttu-id="0b9d3-112">此终结点的用户提供的有关此会话的质量的分级。</span><span class="sxs-lookup"><span data-stu-id="0b9d3-112">The rating provided by the user of this endpoint about the quality of this Session.</span></span> <span data-ttu-id="0b9d3-113">可取值为：`notRated`、`bad`、`poor`、`fair`、`good`、`excellent` 或 `unknownFutureValue`。</span><span class="sxs-lookup"><span data-stu-id="0b9d3-113">Possible values are: `notRated`, `bad`, `poor`, `fair`, `good`, `excellent`, `unknownFutureValue`.</span></span>|
|<span data-ttu-id="0b9d3-114">text</span><span class="sxs-lookup"><span data-stu-id="0b9d3-114">text</span></span>|<span data-ttu-id="0b9d3-115">String</span><span class="sxs-lookup"><span data-stu-id="0b9d3-115">String</span></span>|<span data-ttu-id="0b9d3-116">此终结点的用户提供的反馈文本，用于会话。</span><span class="sxs-lookup"><span data-stu-id="0b9d3-116">The feedback text provided by the user of this endpoint for the session.</span></span>|
|<span data-ttu-id="0b9d3-117">等级</span><span class="sxs-lookup"><span data-stu-id="0b9d3-117">tokens</span></span>|[<span data-ttu-id="0b9d3-118">callRecords。 feedbackTokenSet</span><span class="sxs-lookup"><span data-stu-id="0b9d3-118">microsoft.graph.callRecords.feedbackTokenSet</span></span>](callrecords-feedbacktokenset.md)|<span data-ttu-id="0b9d3-119">此终结点的用户为会话提供的一组反馈令牌。</span><span class="sxs-lookup"><span data-stu-id="0b9d3-119">The set of feedback tokens provided by the user of this endpoint for the session.</span></span> <span data-ttu-id="0b9d3-120">这是一组布尔属性。</span><span class="sxs-lookup"><span data-stu-id="0b9d3-120">This is a set of Boolean properties.</span></span> <span data-ttu-id="0b9d3-121">属性名称不应依赖，因为它们可能会根据向用户提供的令牌而发生变化。</span><span class="sxs-lookup"><span data-stu-id="0b9d3-121">The property names should not be relied upon since they may change depending on what tokens are offered to the user.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="0b9d3-122">JSON 表示形式</span><span class="sxs-lookup"><span data-stu-id="0b9d3-122">JSON representation</span></span>

<span data-ttu-id="0b9d3-123">下面是资源的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="0b9d3-123">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.callRecords.userFeedback",
  "baseType": null
}-->

```json
{
  "rating": "String",
  "text": "String",
  "tokens": {"@odata.type": "microsoft.graph.callRecords.feedbackTokenSet"}
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "userFeedback resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->