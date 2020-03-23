---
title: integerRange 资源类型
description: 表示由两个 Int64 边界描述的整数的包含范围。
author: braedenp-msft
localization_priority: Normal
ms.prod: universal-print
doc_type: resourcePageType
ms.openlocfilehash: c7c3a14e8b8772a0bc319d8415046f3e10871f52
ms.sourcegitcommit: 7baf4847486885edf08ead533c76503cd31a98a4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/21/2020
ms.locfileid: "42895615"
---
# <a name="integerrange-resource-type"></a><span data-ttu-id="97e81-103">integerRange 资源类型</span><span class="sxs-lookup"><span data-stu-id="97e81-103">integerRange resource type</span></span>

<span data-ttu-id="97e81-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="97e81-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="97e81-105">表示由两个 Int64 边界描述的整数的包含范围。</span><span class="sxs-lookup"><span data-stu-id="97e81-105">Represents an inclusive range of integers described by two Int64 boundaries.</span></span>

## <a name="properties"></a><span data-ttu-id="97e81-106">属性</span><span class="sxs-lookup"><span data-stu-id="97e81-106">Properties</span></span>
| <span data-ttu-id="97e81-107">属性</span><span class="sxs-lookup"><span data-stu-id="97e81-107">Property</span></span>     | <span data-ttu-id="97e81-108">类型</span><span class="sxs-lookup"><span data-stu-id="97e81-108">Type</span></span>        | <span data-ttu-id="97e81-109">说明</span><span class="sxs-lookup"><span data-stu-id="97e81-109">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="97e81-110">minimum</span><span class="sxs-lookup"><span data-stu-id="97e81-110">minimum</span></span>|<span data-ttu-id="97e81-111">Int64</span><span class="sxs-lookup"><span data-stu-id="97e81-111">Int64</span></span>|<span data-ttu-id="97e81-112">整数范围的非独占下限。</span><span class="sxs-lookup"><span data-stu-id="97e81-112">The inclusive lower bound of the integer range.</span></span>|
|<span data-ttu-id="97e81-113">maximum</span><span class="sxs-lookup"><span data-stu-id="97e81-113">maximum</span></span>|<span data-ttu-id="97e81-114">Int64</span><span class="sxs-lookup"><span data-stu-id="97e81-114">Int64</span></span>|<span data-ttu-id="97e81-115">整数范围的上下限。</span><span class="sxs-lookup"><span data-stu-id="97e81-115">The inclusive upper bound of the integer range.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="97e81-116">JSON 表示形式</span><span class="sxs-lookup"><span data-stu-id="97e81-116">JSON representation</span></span>

<span data-ttu-id="97e81-117">下面是资源的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="97e81-117">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.integerRange"
}-->

```json
{
    "minimum": 12345,
    "maximum": 12345
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "integerRange resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->