---
title: networkLocationDetail 资源类型
description: 提供用户登录时所采用的网络的名称和类型。
localization_priority: Normal
author: besiler
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 7c43341ab5799da83a084e035c680a1926b3d8e8
ms.sourcegitcommit: 9f88b7e41a4a4a4d5f52bd995ce07c6f702bd5d6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/01/2020
ms.locfileid: "49523012"
---
# <a name="networklocationdetail-resource-type"></a><span data-ttu-id="79ed2-103">networkLocationDetail 资源类型</span><span class="sxs-lookup"><span data-stu-id="79ed2-103">networkLocationDetail resource type</span></span>

<span data-ttu-id="79ed2-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="79ed2-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="79ed2-105">提供用户登录时所采用的网络的名称和类型。</span><span class="sxs-lookup"><span data-stu-id="79ed2-105">Provides the name and type of network from which the user signed in.</span></span>

## <a name="properties"></a><span data-ttu-id="79ed2-106">属性</span><span class="sxs-lookup"><span data-stu-id="79ed2-106">Properties</span></span>

| <span data-ttu-id="79ed2-107">属性</span><span class="sxs-lookup"><span data-stu-id="79ed2-107">Property</span></span>     | <span data-ttu-id="79ed2-108">类型</span><span class="sxs-lookup"><span data-stu-id="79ed2-108">Type</span></span>        | <span data-ttu-id="79ed2-109">说明</span><span class="sxs-lookup"><span data-stu-id="79ed2-109">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="79ed2-110">networkNames</span><span class="sxs-lookup"><span data-stu-id="79ed2-110">networkNames</span></span>|<span data-ttu-id="79ed2-111">字符串集合</span><span class="sxs-lookup"><span data-stu-id="79ed2-111">String collection</span></span>|<span data-ttu-id="79ed2-112">提供登录时使用的网络的名称。</span><span class="sxs-lookup"><span data-stu-id="79ed2-112">Provides the name of the network used when signing in.</span></span>|
|<span data-ttu-id="79ed2-113">网络</span><span class="sxs-lookup"><span data-stu-id="79ed2-113">networkType</span></span>|<span data-ttu-id="79ed2-114">网络</span><span class="sxs-lookup"><span data-stu-id="79ed2-114">networkType</span></span>| <span data-ttu-id="79ed2-115">提供登录时使用的网络类型。</span><span class="sxs-lookup"><span data-stu-id="79ed2-115">Provides the type of network used when signing in.</span></span> <span data-ttu-id="79ed2-116">可取值为：`intranet`、`extranet`、`namedNetwork`、`trusted`、`unknownFutureValue`。</span><span class="sxs-lookup"><span data-stu-id="79ed2-116">Possible values are: `intranet`, `extranet`, `namedNetwork`, `trusted`, `unknownFutureValue`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="79ed2-117">JSON 表示形式</span><span class="sxs-lookup"><span data-stu-id="79ed2-117">JSON representation</span></span>

<span data-ttu-id="79ed2-118">下面是资源的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="79ed2-118">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.networkLocationDetail",
  "baseType": null
}-->

```json
{
  "networkNames": ["String"],
  "networkType": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "networkLocationDetail resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

