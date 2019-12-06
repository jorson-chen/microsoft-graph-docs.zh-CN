---
title: 趋势资源类型
description: 将用户连接到在用户周围进行趋势分析的文档（与用户相关）的丰富关系。 OneDrive 文件和存储在 SharePoint 团队网站上的文件可围绕用户进行趋势。
author: simonhult
localization_priority: Normal
ms.prod: insights
doc_type: resourcePageType
ms.openlocfilehash: 624319d216758228de1c3fbed4e7b4f172a9e7ce
ms.sourcegitcommit: 1cdb3bcddf34e7445e65477b9bf661d4d10c7311
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2019
ms.locfileid: "39844998"
---
# <a name="trending-resource-type"></a><span data-ttu-id="4733e-104">趋势资源类型</span><span class="sxs-lookup"><span data-stu-id="4733e-104">trending resource type</span></span>

<span data-ttu-id="4733e-105">将用户连接到在用户周围进行趋势分析的文档（与用户相关）的丰富关系。</span><span class="sxs-lookup"><span data-stu-id="4733e-105">Rich relationship connecting a user to documents that are trending around the user (are relevant to the user).</span></span> <span data-ttu-id="4733e-106">OneDrive 文件和存储在 SharePoint 团队网站上的文件可围绕用户进行趋势。</span><span class="sxs-lookup"><span data-stu-id="4733e-106">OneDrive files, and files stored on SharePoint team sites can trend around the user.</span></span>

## <a name="methods"></a><span data-ttu-id="4733e-107">方法</span><span class="sxs-lookup"><span data-stu-id="4733e-107">Methods</span></span>

| <span data-ttu-id="4733e-108">方法</span><span class="sxs-lookup"><span data-stu-id="4733e-108">Method</span></span>       | <span data-ttu-id="4733e-109">返回类型</span><span class="sxs-lookup"><span data-stu-id="4733e-109">Return Type</span></span>  |<span data-ttu-id="4733e-110">说明</span><span class="sxs-lookup"><span data-stu-id="4733e-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="4733e-111">列出趋势</span><span class="sxs-lookup"><span data-stu-id="4733e-111">List trending</span></span>](../api/insights-list-trending.md) |<span data-ttu-id="4733e-112">[trending](insights-trending.md) 集合</span><span class="sxs-lookup"><span data-stu-id="4733e-112">[trending](insights-trending.md) collection</span></span>| <span data-ttu-id="4733e-113">获取趋势文件的列表。</span><span class="sxs-lookup"><span data-stu-id="4733e-113">Get a list of trending files.</span></span>|

## <a name="properties"></a><span data-ttu-id="4733e-114">属性</span><span class="sxs-lookup"><span data-stu-id="4733e-114">Properties</span></span>

| <span data-ttu-id="4733e-115">属性</span><span class="sxs-lookup"><span data-stu-id="4733e-115">Property</span></span>      | <span data-ttu-id="4733e-116">类型</span><span class="sxs-lookup"><span data-stu-id="4733e-116">Type</span></span>                              | <span data-ttu-id="4733e-117">说明</span><span class="sxs-lookup"><span data-stu-id="4733e-117">Description</span></span>  |
| ------------- |---------------                    | -------------|
| <span data-ttu-id="4733e-118">id</span><span class="sxs-lookup"><span data-stu-id="4733e-118">id</span></span>                    | <span data-ttu-id="4733e-119">String</span><span class="sxs-lookup"><span data-stu-id="4733e-119">String</span></span>                    | <span data-ttu-id="4733e-120">关系的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="4733e-120">Unique identifier of the relationship.</span></span> <span data-ttu-id="4733e-121">只读。</span><span class="sxs-lookup"><span data-stu-id="4733e-121">Read only.</span></span>        |
| <span data-ttu-id="4733e-122">weight</span><span class="sxs-lookup"><span data-stu-id="4733e-122">weight</span></span>                | <span data-ttu-id="4733e-123">双精度</span><span class="sxs-lookup"><span data-stu-id="4733e-123">Double</span></span>                    | <span data-ttu-id="4733e-124">值，该值指示文档当前正在进行趋势计算的程度。</span><span class="sxs-lookup"><span data-stu-id="4733e-124">Value indicating how much the document is currently trending.</span></span> <span data-ttu-id="4733e-125">数字越大，文档当前在用户周围的趋势分析越多（相关性越好）。</span><span class="sxs-lookup"><span data-stu-id="4733e-125">The larger the number, the more the document is currently trending around the user (the more relevant it is).</span></span> <span data-ttu-id="4733e-126">返回的文档按此值进行排序。</span><span class="sxs-lookup"><span data-stu-id="4733e-126">Returned documents are sorted by this value.</span></span>  |
| <span data-ttu-id="4733e-127">resourceVisualization</span><span class="sxs-lookup"><span data-stu-id="4733e-127">resourceVisualization</span></span> | [<span data-ttu-id="4733e-128">resourceVisualization</span><span class="sxs-lookup"><span data-stu-id="4733e-128">resourceVisualization</span></span>](insights-resourcevisualization.md)    | <span data-ttu-id="4733e-129">可用于在体验中可视化文档的属性。</span><span class="sxs-lookup"><span data-stu-id="4733e-129">Properties that you can use to visualize the document in your experience.</span></span> |
| <span data-ttu-id="4733e-130">resourceReference</span><span class="sxs-lookup"><span data-stu-id="4733e-130">resourceReference</span></span>     | [<span data-ttu-id="4733e-131">resourceReference</span><span class="sxs-lookup"><span data-stu-id="4733e-131">resourceReference</span></span>](insights-resourcereference.md)        | <span data-ttu-id="4733e-132">参考趋势文档的属性，例如文档的 url 和类型。</span><span class="sxs-lookup"><span data-stu-id="4733e-132">Reference properties of the trending document, such as the url and type of the document.</span></span> |
| <span data-ttu-id="4733e-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="4733e-133">lastModifiedDateTime</span></span>  | <span data-ttu-id="4733e-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4733e-134">DateTimeOffset</span></span>            | |
## <a name="relationships"></a><span data-ttu-id="4733e-135">关系</span><span class="sxs-lookup"><span data-stu-id="4733e-135">Relationships</span></span>

| <span data-ttu-id="4733e-136">属性</span><span class="sxs-lookup"><span data-stu-id="4733e-136">Property</span></span>      | <span data-ttu-id="4733e-137">类型</span><span class="sxs-lookup"><span data-stu-id="4733e-137">Type</span></span>          | <span data-ttu-id="4733e-138">说明</span><span class="sxs-lookup"><span data-stu-id="4733e-138">Description</span></span>  |
| ------------- |---------------| -------------|
| <span data-ttu-id="4733e-139">资源</span><span class="sxs-lookup"><span data-stu-id="4733e-139">resource</span></span>      | <span data-ttu-id="4733e-140">属性</span><span class="sxs-lookup"><span data-stu-id="4733e-140">entity</span></span>        | <span data-ttu-id="4733e-141">用于导航到趋势文档。</span><span class="sxs-lookup"><span data-stu-id="4733e-141">Used for navigating to the trending document.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="4733e-142">JSON 表示形式</span><span class="sxs-lookup"><span data-stu-id="4733e-142">JSON representation</span></span>

<span data-ttu-id="4733e-143">下面是资源的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="4733e-143">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "keyProperty":"id",
  "optionalProperties": [
    "resource"
  ],
  "@odata.type": "microsoft.graph.trending"
}-->

```json
{
  "id": "string",
  "weight": "double",
  "resourceVisualization": {"@odata.type": "microsoft.graph.resourceVisualization"},
  "resourceReference": {"@odata.type": "microsoft.graph.resourceReference"},
  "lastModifiedDateTime": "String (timestamp)"
}
```