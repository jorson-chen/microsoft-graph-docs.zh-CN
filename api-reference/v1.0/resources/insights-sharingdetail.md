---
title: sharingDetail 资源类型
description: '包含共享项目的属性的复杂类型。 '
author: simonhult
localization_priority: Normal
ms.prod: insights
doc_type: resourcePageType
ms.openlocfilehash: f82601867e890d9a733932fab66ab18235c780e4
ms.sourcegitcommit: 1cdb3bcddf34e7445e65477b9bf661d4d10c7311
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2019
ms.locfileid: "39845005"
---
# <a name="sharingdetail-resource-type"></a><span data-ttu-id="1353e-103">sharingDetail 资源类型</span><span class="sxs-lookup"><span data-stu-id="1353e-103">sharingDetail resource type</span></span>

<span data-ttu-id="1353e-104">包含[sharedInsight](insights-shared.md)项目的属性的复杂类型。</span><span class="sxs-lookup"><span data-stu-id="1353e-104">Complex type containing properties of [sharedInsight](insights-shared.md) items.</span></span> 

## <a name="json-representation"></a><span data-ttu-id="1353e-105">JSON 表示形式</span><span class="sxs-lookup"><span data-stu-id="1353e-105">JSON representation</span></span>
<span data-ttu-id="1353e-106">下面是资源的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="1353e-106">Here is a JSON representation of the resource</span></span>
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.sharingDetail"
}-->
```json
{
  "sharedDateTime": "dateTimeOffset",
  "sharingSubject": "string",
  "sharingType": "string",
  "sharedBy": "insightIdentity",
  "resourceReference": "resourceReference"
}
```

## <a name="properties"></a><span data-ttu-id="1353e-107">属性</span><span class="sxs-lookup"><span data-stu-id="1353e-107">Properties</span></span>

| <span data-ttu-id="1353e-108">属性</span><span class="sxs-lookup"><span data-stu-id="1353e-108">Property</span></span>              | <span data-ttu-id="1353e-109">类型</span><span class="sxs-lookup"><span data-stu-id="1353e-109">Type</span></span>          | <span data-ttu-id="1353e-110">说明</span><span class="sxs-lookup"><span data-stu-id="1353e-110">Description</span></span>  |
| -------------         |-----------    | -------------|
| <span data-ttu-id="1353e-111">sharedDateTime</span><span class="sxs-lookup"><span data-stu-id="1353e-111">sharedDateTime</span></span>        | <span data-ttu-id="1353e-112">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1353e-112">DateTimeOffset</span></span>| <span data-ttu-id="1353e-113">上次共享文件的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="1353e-113">The date and time the file was last shared.</span></span> <span data-ttu-id="1353e-114">时间戳表示使用 ISO 8601 格式的日期和时间信息，并且始终处于 UTC 时间。</span><span class="sxs-lookup"><span data-stu-id="1353e-114">The timestamp represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="1353e-115">例如，2014 年 1 月 1 日午夜 UTC 如下所示：`2014-01-01T00:00:00Z`。</span><span class="sxs-lookup"><span data-stu-id="1353e-115">For example, midnight UTC on Jan 1, 2014 would look like this: `2014-01-01T00:00:00Z`.</span></span> <span data-ttu-id="1353e-116">只读。</span><span class="sxs-lookup"><span data-stu-id="1353e-116">Read-only.</span></span>  |
| <span data-ttu-id="1353e-117">sharingSubject</span><span class="sxs-lookup"><span data-stu-id="1353e-117">sharingSubject</span></span>        | <span data-ttu-id="1353e-118">String</span><span class="sxs-lookup"><span data-stu-id="1353e-118">String</span></span>          | <span data-ttu-id="1353e-119">共享文档的主题。</span><span class="sxs-lookup"><span data-stu-id="1353e-119">The subject with which the document was shared.</span></span> |
| <span data-ttu-id="1353e-120">sharingType</span><span class="sxs-lookup"><span data-stu-id="1353e-120">sharingType</span></span>             | <span data-ttu-id="1353e-121">String</span><span class="sxs-lookup"><span data-stu-id="1353e-121">String</span></span>        | <span data-ttu-id="1353e-122">确定文档的共享方式，可以是 "链接"、"附件"、"组"、"网站"。</span><span class="sxs-lookup"><span data-stu-id="1353e-122">Determines the way the document was shared, can be by a "Link", "Attachment", "Group", "Site".</span></span>     |
| <span data-ttu-id="1353e-123">sharedBy</span><span class="sxs-lookup"><span data-stu-id="1353e-123">sharedBy</span></span>                | [<span data-ttu-id="1353e-124">insightIdentity</span><span class="sxs-lookup"><span data-stu-id="1353e-124">insightIdentity</span></span>](insights-insightidentity.md)      | <span data-ttu-id="1353e-125">共享文档的用户。</span><span class="sxs-lookup"><span data-stu-id="1353e-125">The user who shared the document.</span></span>  |
| <span data-ttu-id="1353e-126">sharingReference</span><span class="sxs-lookup"><span data-stu-id="1353e-126">sharingReference</span></span>        | [<span data-ttu-id="1353e-127">resourceReference</span><span class="sxs-lookup"><span data-stu-id="1353e-127">resourceReference</span></span>](insights-resourcereference.md)      |  |