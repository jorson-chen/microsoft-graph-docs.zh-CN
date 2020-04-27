---
title: androidManagedStoreAppAssignmentSettings 资源类型
description: 包含用于将 Android 托管存储移动应用程序分配给组的属性。
author: dougeby
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: cfdca91e3499a495ba810b1c791653d62c769e4a
ms.sourcegitcommit: bbcf074f0be9d5e02f84c290122850cc5968fb1f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2020
ms.locfileid: "43440501"
---
# <a name="androidmanagedstoreappassignmentsettings-resource-type"></a><span data-ttu-id="a79be-103">androidManagedStoreAppAssignmentSettings 资源类型</span><span class="sxs-lookup"><span data-stu-id="a79be-103">androidManagedStoreAppAssignmentSettings resource type</span></span>

<span data-ttu-id="a79be-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="a79be-104">Namespace: microsoft.graph</span></span>

> <span data-ttu-id="a79be-105">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="a79be-105">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="a79be-106">**注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="a79be-106">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="a79be-107">包含用于将 Android 托管存储移动应用程序分配给组的属性。</span><span class="sxs-lookup"><span data-stu-id="a79be-107">Contains properties used to assign an Android Managed Store mobile app to a group.</span></span>


<span data-ttu-id="a79be-108">继承自 [mobileAppAssignmentSettings](../resources/intune-shared-mobileappassignmentsettings.md)</span><span class="sxs-lookup"><span data-stu-id="a79be-108">Inherits from [mobileAppAssignmentSettings](../resources/intune-shared-mobileappassignmentsettings.md)</span></span>

## <a name="properties"></a><span data-ttu-id="a79be-109">属性</span><span class="sxs-lookup"><span data-stu-id="a79be-109">Properties</span></span>
|<span data-ttu-id="a79be-110">属性</span><span class="sxs-lookup"><span data-stu-id="a79be-110">Property</span></span>|<span data-ttu-id="a79be-111">类型</span><span class="sxs-lookup"><span data-stu-id="a79be-111">Type</span></span>|<span data-ttu-id="a79be-112">说明</span><span class="sxs-lookup"><span data-stu-id="a79be-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a79be-113">androidManagedStoreAppTrackIds</span><span class="sxs-lookup"><span data-stu-id="a79be-113">androidManagedStoreAppTrackIds</span></span>|<span data-ttu-id="a79be-114">String 集合</span><span class="sxs-lookup"><span data-stu-id="a79be-114">String collection</span></span>|<span data-ttu-id="a79be-115">要为此应用分配启用的跟踪 Id。</span><span class="sxs-lookup"><span data-stu-id="a79be-115">The track IDs to enable for this app assignment.</span></span>|

## <a name="relationships"></a><span data-ttu-id="a79be-116">关系</span><span class="sxs-lookup"><span data-stu-id="a79be-116">Relationships</span></span>
<span data-ttu-id="a79be-117">无</span><span class="sxs-lookup"><span data-stu-id="a79be-117">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="a79be-118">JSON 表示形式</span><span class="sxs-lookup"><span data-stu-id="a79be-118">JSON Representation</span></span>
<span data-ttu-id="a79be-119">下面是资源的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="a79be-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.androidManagedStoreAppAssignmentSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidManagedStoreAppAssignmentSettings",
  "androidManagedStoreAppTrackIds": [
    "String"
  ]
}
```


