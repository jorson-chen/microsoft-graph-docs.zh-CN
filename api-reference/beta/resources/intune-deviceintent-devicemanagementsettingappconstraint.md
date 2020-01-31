---
title: deviceManagementSettingAppConstraint 资源类型
description: 强制实施设置的约束仅包含 vaild 应用程序类型。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: 218e4ca91d69c1d68b19e12ed659a3cd87884b5b
ms.sourcegitcommit: b12904a27b6d0e197f562aca0dac5e74cd7bd3a1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2020
ms.locfileid: "41636789"
---
# <a name="devicemanagementsettingappconstraint-resource-type"></a><span data-ttu-id="bd7c6-103">deviceManagementSettingAppConstraint 资源类型</span><span class="sxs-lookup"><span data-stu-id="bd7c6-103">deviceManagementSettingAppConstraint resource type</span></span>

> <span data-ttu-id="bd7c6-104">**重要说明：**/Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。</span><span class="sxs-lookup"><span data-stu-id="bd7c6-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="bd7c6-105">**注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。</span><span class="sxs-lookup"><span data-stu-id="bd7c6-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="bd7c6-106">强制实施设置的约束仅包含 vaild 应用程序类型。</span><span class="sxs-lookup"><span data-stu-id="bd7c6-106">Constraint enforcing the setting contains only vaild app types.</span></span>


<span data-ttu-id="bd7c6-107">继承自[deviceManagementConstraint](../resources/intune-deviceintent-devicemanagementconstraint.md)</span><span class="sxs-lookup"><span data-stu-id="bd7c6-107">Inherits from [deviceManagementConstraint](../resources/intune-deviceintent-devicemanagementconstraint.md)</span></span>

## <a name="properties"></a><span data-ttu-id="bd7c6-108">属性</span><span class="sxs-lookup"><span data-stu-id="bd7c6-108">Properties</span></span>
|<span data-ttu-id="bd7c6-109">属性</span><span class="sxs-lookup"><span data-stu-id="bd7c6-109">Property</span></span>|<span data-ttu-id="bd7c6-110">类型</span><span class="sxs-lookup"><span data-stu-id="bd7c6-110">Type</span></span>|<span data-ttu-id="bd7c6-111">Description</span><span class="sxs-lookup"><span data-stu-id="bd7c6-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bd7c6-112">supportedTypes</span><span class="sxs-lookup"><span data-stu-id="bd7c6-112">supportedTypes</span></span>|<span data-ttu-id="bd7c6-113">String 集合</span><span class="sxs-lookup"><span data-stu-id="bd7c6-113">String collection</span></span>|<span data-ttu-id="bd7c6-114">允许此设置的可接受的应用程序类型</span><span class="sxs-lookup"><span data-stu-id="bd7c6-114">Acceptable app types to allow for this setting</span></span>|

## <a name="relationships"></a><span data-ttu-id="bd7c6-115">关系</span><span class="sxs-lookup"><span data-stu-id="bd7c6-115">Relationships</span></span>
<span data-ttu-id="bd7c6-116">无</span><span class="sxs-lookup"><span data-stu-id="bd7c6-116">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="bd7c6-117">JSON 表示形式</span><span class="sxs-lookup"><span data-stu-id="bd7c6-117">JSON Representation</span></span>
<span data-ttu-id="bd7c6-118">下面是资源的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="bd7c6-118">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceManagementSettingAppConstraint"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementSettingAppConstraint",
  "supportedTypes": [
    "String"
  ]
}
```


