---
title: workbookTableColumn 资源类型
description: 代表表格中的一列。
author: lumine2008
localization_priority: Normal
ms.prod: excel
doc_type: resourcePageType
ms.openlocfilehash: 27a44c0b75cfe62d27b1187616f9626772575cf4
ms.sourcegitcommit: 9a03b719d1316729dd022bf4d268894e91515475
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2021
ms.locfileid: "50034014"
---
# <a name="workbooktablecolumn-resource-type"></a><span data-ttu-id="38a7a-103">workbookTableColumn 资源类型</span><span class="sxs-lookup"><span data-stu-id="38a7a-103">workbookTableColumn resource type</span></span>

<span data-ttu-id="38a7a-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="38a7a-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="38a7a-105">代表表格中的一列。</span><span class="sxs-lookup"><span data-stu-id="38a7a-105">Represents a column in a table.</span></span>


## <a name="methods"></a><span data-ttu-id="38a7a-106">方法</span><span class="sxs-lookup"><span data-stu-id="38a7a-106">Methods</span></span>

| <span data-ttu-id="38a7a-107">方法</span><span class="sxs-lookup"><span data-stu-id="38a7a-107">Method</span></span>           | <span data-ttu-id="38a7a-108">返回类型</span><span class="sxs-lookup"><span data-stu-id="38a7a-108">Return Type</span></span>    |<span data-ttu-id="38a7a-109">说明</span><span class="sxs-lookup"><span data-stu-id="38a7a-109">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="38a7a-110">获取 TableColumn</span><span class="sxs-lookup"><span data-stu-id="38a7a-110">Get TableColumn</span></span>](../api/tablecolumn-get.md) | [<span data-ttu-id="38a7a-111">workbookTableColumn</span><span class="sxs-lookup"><span data-stu-id="38a7a-111">workbookTableColumn</span></span>](workbooktablecolumn.md) |<span data-ttu-id="38a7a-112">读取 tablecolumn 对象的属性和关系。</span><span class="sxs-lookup"><span data-stu-id="38a7a-112">Read properties and relationships of tableColumn object.</span></span>|
|[<span data-ttu-id="38a7a-113">更新</span><span class="sxs-lookup"><span data-stu-id="38a7a-113">Update</span></span>](../api/tablecolumn-update.md) | [<span data-ttu-id="38a7a-114">workbookTableColumn</span><span class="sxs-lookup"><span data-stu-id="38a7a-114">workbookTableColumn</span></span>](workbooktablecolumn.md) |<span data-ttu-id="38a7a-115">更新 TableColumn 对象</span><span class="sxs-lookup"><span data-stu-id="38a7a-115">Update TableColumn object.</span></span> |
|[<span data-ttu-id="38a7a-116">Databodyrange</span><span class="sxs-lookup"><span data-stu-id="38a7a-116">Databodyrange</span></span>](../api/tablecolumn-databodyrange.md)|[<span data-ttu-id="38a7a-117">workbookRange</span><span class="sxs-lookup"><span data-stu-id="38a7a-117">workbookRange</span></span>](workbookrange.md)|<span data-ttu-id="38a7a-118">获取与列的数据体相关的 range 对象。</span><span class="sxs-lookup"><span data-stu-id="38a7a-118">Gets the range object associated with the data body of the column.</span></span>|
|[<span data-ttu-id="38a7a-119">Headerrowrange</span><span class="sxs-lookup"><span data-stu-id="38a7a-119">Headerrowrange</span></span>](../api/tablecolumn-headerrowrange.md)|[<span data-ttu-id="38a7a-120">workbookRange</span><span class="sxs-lookup"><span data-stu-id="38a7a-120">workbookRange</span></span>](workbookrange.md)|<span data-ttu-id="38a7a-121">获取与列的标头行相关的 range 对象。</span><span class="sxs-lookup"><span data-stu-id="38a7a-121">Gets the range object associated with the header row of the column.</span></span>|
|[<span data-ttu-id="38a7a-122">Range</span><span class="sxs-lookup"><span data-stu-id="38a7a-122">Range</span></span>](../api/tablecolumn-range.md)|[<span data-ttu-id="38a7a-123">workbookRange</span><span class="sxs-lookup"><span data-stu-id="38a7a-123">workbookRange</span></span>](workbookrange.md)|<span data-ttu-id="38a7a-124">获取与整个列相关的 range 对象。</span><span class="sxs-lookup"><span data-stu-id="38a7a-124">Gets the range object associated with the entire column.</span></span>|
|[<span data-ttu-id="38a7a-125">Totalrowrange</span><span class="sxs-lookup"><span data-stu-id="38a7a-125">Totalrowrange</span></span>](../api/tablecolumn-totalrowrange.md)|[<span data-ttu-id="38a7a-126">workbookRange</span><span class="sxs-lookup"><span data-stu-id="38a7a-126">workbookRange</span></span>](workbookrange.md)|<span data-ttu-id="38a7a-127">获取与列的总计行相关的 range 对象。</span><span class="sxs-lookup"><span data-stu-id="38a7a-127">Gets the range object associated with the totals row of the column.</span></span>|
|[<span data-ttu-id="38a7a-128">删除</span><span class="sxs-lookup"><span data-stu-id="38a7a-128">Delete</span></span>](../api/tablecolumn-delete.md)|<span data-ttu-id="38a7a-129">无</span><span class="sxs-lookup"><span data-stu-id="38a7a-129">None</span></span>|<span data-ttu-id="38a7a-130">从表中删除列。</span><span class="sxs-lookup"><span data-stu-id="38a7a-130">Deletes the column from the table.</span></span>|
|[<span data-ttu-id="38a7a-131">列出</span><span class="sxs-lookup"><span data-stu-id="38a7a-131">List</span></span>](../api/tablecolumn-list.md) | <span data-ttu-id="38a7a-132">[workbookTableColumn](workbooktablecolumn.md) 集合</span><span class="sxs-lookup"><span data-stu-id="38a7a-132">[workbookTableColumn](workbooktablecolumn.md) collection</span></span> |<span data-ttu-id="38a7a-133">获取 tableColumn 对象的集合。</span><span class="sxs-lookup"><span data-stu-id="38a7a-133">Get tableColumn object collection.</span></span> |
|[<span data-ttu-id="38a7a-134">Itemat</span><span class="sxs-lookup"><span data-stu-id="38a7a-134">Itemat</span></span>](../api/tablecolumncollection-itemat.md)|[<span data-ttu-id="38a7a-135">workbookTableColumn</span><span class="sxs-lookup"><span data-stu-id="38a7a-135">workbookTableColumn</span></span>](workbooktablecolumn.md)|<span data-ttu-id="38a7a-136">根据其在集合中的位置获取列。</span><span class="sxs-lookup"><span data-stu-id="38a7a-136">Gets a column based on its position in the collection.</span></span>|
|[<span data-ttu-id="38a7a-137">添加</span><span class="sxs-lookup"><span data-stu-id="38a7a-137">Add</span></span>](../api/tablecolumncollection-add.md)|[<span data-ttu-id="38a7a-138">workbookTableColumn</span><span class="sxs-lookup"><span data-stu-id="38a7a-138">workbookTableColumn</span></span>](workbooktablecolumn.md)|<span data-ttu-id="38a7a-139">向表中添加新列。</span><span class="sxs-lookup"><span data-stu-id="38a7a-139">Adds a new column to the table.</span></span>|

## <a name="properties"></a><span data-ttu-id="38a7a-140">属性</span><span class="sxs-lookup"><span data-stu-id="38a7a-140">Properties</span></span>
| <span data-ttu-id="38a7a-141">属性</span><span class="sxs-lookup"><span data-stu-id="38a7a-141">Property</span></span>     | <span data-ttu-id="38a7a-142">类型</span><span class="sxs-lookup"><span data-stu-id="38a7a-142">Type</span></span>   |<span data-ttu-id="38a7a-143">说明</span><span class="sxs-lookup"><span data-stu-id="38a7a-143">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="38a7a-144">id</span><span class="sxs-lookup"><span data-stu-id="38a7a-144">id</span></span>|<span data-ttu-id="38a7a-145">string</span><span class="sxs-lookup"><span data-stu-id="38a7a-145">string</span></span>|<span data-ttu-id="38a7a-p101">返回标识表内的列的唯一键。只读。</span><span class="sxs-lookup"><span data-stu-id="38a7a-p101">Returns a unique key that identifies the column within the table. Read-only.</span></span>|
|<span data-ttu-id="38a7a-148">Index</span><span class="sxs-lookup"><span data-stu-id="38a7a-148">index</span></span>|<span data-ttu-id="38a7a-149">int</span><span class="sxs-lookup"><span data-stu-id="38a7a-149">int</span></span>|<span data-ttu-id="38a7a-p102">返回表的列集合内列的索引编号。从零开始编制索引。只读。</span><span class="sxs-lookup"><span data-stu-id="38a7a-p102">Returns the index number of the column within the columns collection of the table. Zero-indexed. Read-only.</span></span>|
|<span data-ttu-id="38a7a-153">name</span><span class="sxs-lookup"><span data-stu-id="38a7a-153">name</span></span>|<span data-ttu-id="38a7a-154">string</span><span class="sxs-lookup"><span data-stu-id="38a7a-154">string</span></span>|<span data-ttu-id="38a7a-155">返回表格列的名称。</span><span class="sxs-lookup"><span data-stu-id="38a7a-155">Returns the name of the table column.</span></span>|
|<span data-ttu-id="38a7a-156">values</span><span class="sxs-lookup"><span data-stu-id="38a7a-156">values</span></span>|<span data-ttu-id="38a7a-157">Json</span><span class="sxs-lookup"><span data-stu-id="38a7a-157">Json</span></span>|<span data-ttu-id="38a7a-p103">表示指定区域的原始值。返回的数据类型可能是字符串、数字或布尔值。包含一个将返回错误字符串的错误的单元格。</span><span class="sxs-lookup"><span data-stu-id="38a7a-p103">Represents the raw values of the specified range. The data returned could be of type string, number, or a boolean. Cell that contain an error will return the error string.</span></span>|

## <a name="relationships"></a><span data-ttu-id="38a7a-161">关系</span><span class="sxs-lookup"><span data-stu-id="38a7a-161">Relationships</span></span>
| <span data-ttu-id="38a7a-162">关系</span><span class="sxs-lookup"><span data-stu-id="38a7a-162">Relationship</span></span> | <span data-ttu-id="38a7a-163">类型</span><span class="sxs-lookup"><span data-stu-id="38a7a-163">Type</span></span>   |<span data-ttu-id="38a7a-164">说明</span><span class="sxs-lookup"><span data-stu-id="38a7a-164">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="38a7a-165">筛选器</span><span class="sxs-lookup"><span data-stu-id="38a7a-165">filter</span></span>|[<span data-ttu-id="38a7a-166">workbookFilter</span><span class="sxs-lookup"><span data-stu-id="38a7a-166">workbookFilter</span></span>](workbookfilter.md)|<span data-ttu-id="38a7a-p104">检索应用于列的筛选器。只读。</span><span class="sxs-lookup"><span data-stu-id="38a7a-p104">Retrieve the filter applied to the column. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="38a7a-169">JSON 表示形式</span><span class="sxs-lookup"><span data-stu-id="38a7a-169">JSON representation</span></span>

<span data-ttu-id="38a7a-170">下面是资源的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="38a7a-170">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "keyProperty": "id",
  "baseType":"microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookTableColumn"
}-->

```json
{
  "id": "1024",
  "index": 1024,
  "name": "string",
  "values": "json"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "TableColumn resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


