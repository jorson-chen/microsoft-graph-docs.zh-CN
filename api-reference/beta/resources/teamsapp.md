---
title: teamsApp 资源类型
description: Microsoft Teams 应用对话框中的应用。
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
doc_type: resourcePageType
ms.openlocfilehash: 5a944c9aa1f679b053fa7ceda645885b584a1dce
ms.sourcegitcommit: 59e79cf2693cbb550da3e61eb4f68d9e0f57faf6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/09/2020
ms.locfileid: "49606788"
---
# <a name="teamsapp-resource-type"></a><span data-ttu-id="065dc-103">teamsApp 资源类型</span><span class="sxs-lookup"><span data-stu-id="065dc-103">teamsApp resource type</span></span>

<span data-ttu-id="065dc-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="065dc-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="065dc-105">代表[Microsoft Teams](teams-api-overview.md) 应用目录中的一个应用.</span><span class="sxs-lookup"><span data-stu-id="065dc-105">Represents an app in the [Microsoft Teams](teams-api-overview.md) app catalog.</span></span>

<span data-ttu-id="065dc-106">用户可以在 Microsoft Teams 商店中看到这些应用，并且可以使用“[向团队添加应用](../api/team-post-installedapps.md)”方法将这些应用安装到 [Teams](team.md) 中。</span><span class="sxs-lookup"><span data-stu-id="065dc-106">Users can see these apps in the Microsoft Teams Store, and these apps can be installed in [teams](team.md) using the [Add app to team](../api/team-post-installedapps.md) method.</span></span>

## <a name="methods"></a><span data-ttu-id="065dc-107">方法</span><span class="sxs-lookup"><span data-stu-id="065dc-107">Methods</span></span>

| <span data-ttu-id="065dc-108">方法</span><span class="sxs-lookup"><span data-stu-id="065dc-108">Method</span></span>       | <span data-ttu-id="065dc-109">返回类型</span><span class="sxs-lookup"><span data-stu-id="065dc-109">Return Type</span></span>  |<span data-ttu-id="065dc-110">说明</span><span class="sxs-lookup"><span data-stu-id="065dc-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="065dc-111">列出已发布的应用</span><span class="sxs-lookup"><span data-stu-id="065dc-111">List published apps</span></span>](../api/appcatalogs-list-teamsapps.md) | <span data-ttu-id="065dc-112">[teamsApp](teamsapp.md) 集合</span><span class="sxs-lookup"><span data-stu-id="065dc-112">[teamsApp](teamsapp.md) collection</span></span> | <span data-ttu-id="065dc-113">列出 Microsoft Teams 应用目录中已发布的应用。</span><span class="sxs-lookup"><span data-stu-id="065dc-113">List published apps from the Microsoft Teams apps catalog.</span></span>|
|[<span data-ttu-id="065dc-114">发布应用</span><span class="sxs-lookup"><span data-stu-id="065dc-114">Publish an app</span></span>](../api/teamsapp-publish.md) | [<span data-ttu-id="065dc-115">teamsApp</span><span class="sxs-lookup"><span data-stu-id="065dc-115">teamsApp</span></span>](teamsapp.md) | <span data-ttu-id="065dc-116">将应用发布到组织的应用目录。</span><span class="sxs-lookup"><span data-stu-id="065dc-116">Publish an app to your organization's app catalog.</span></span>|
|[<span data-ttu-id="065dc-117">更新已发布的应用</span><span class="sxs-lookup"><span data-stu-id="065dc-117">Update a published app</span></span>](../api/teamsapp-update.md) | [<span data-ttu-id="065dc-118">teamsApp</span><span class="sxs-lookup"><span data-stu-id="065dc-118">teamsApp</span></span>](teamsapp.md) | <span data-ttu-id="065dc-119">更新组织应用目录中的已发布应用。</span><span class="sxs-lookup"><span data-stu-id="065dc-119">Update a published app in your organization's app catalog.</span></span>|
|[<span data-ttu-id="065dc-120">删除已发布的应用</span><span class="sxs-lookup"><span data-stu-id="065dc-120">Delete a published app</span></span>](../api/teamsapp-delete.md) | <span data-ttu-id="065dc-121">无</span><span class="sxs-lookup"><span data-stu-id="065dc-121">None</span></span> | <span data-ttu-id="065dc-122">更新组织应用目录中已发布的应用。</span><span class="sxs-lookup"><span data-stu-id="065dc-122">Remove a published app from your organization's app catalog.</span></span>|

## <a name="properties"></a><span data-ttu-id="065dc-123">属性</span><span class="sxs-lookup"><span data-stu-id="065dc-123">Properties</span></span>

| <span data-ttu-id="065dc-124">属性</span><span class="sxs-lookup"><span data-stu-id="065dc-124">Property</span></span>            | <span data-ttu-id="065dc-125">类型</span><span class="sxs-lookup"><span data-stu-id="065dc-125">Type</span></span>     | <span data-ttu-id="065dc-126">说明</span><span class="sxs-lookup"><span data-stu-id="065dc-126">Description</span></span> |
|:------------------- |:-------- |:----------- |
| <span data-ttu-id="065dc-127">id</span><span class="sxs-lookup"><span data-stu-id="065dc-127">id</span></span>                  | <span data-ttu-id="065dc-128">string</span><span class="sxs-lookup"><span data-stu-id="065dc-128">string</span></span>   | <span data-ttu-id="065dc-129">目录应用生成的应用 ID（不同于开发人员在 [Microsoft Teams 应用压缩包](/microsoftteams/platform/concepts/apps/apps-package)中提供的 ID）。</span><span class="sxs-lookup"><span data-stu-id="065dc-129">The catalog app's generated app ID (different from the developer-provided ID in the [Microsoft Teams zip app package](/microsoftteams/platform/concepts/apps/apps-package).</span></span> |
| <span data-ttu-id="065dc-130">externalId</span><span class="sxs-lookup"><span data-stu-id="065dc-130">externalId</span></span>          | <span data-ttu-id="065dc-131">string</span><span class="sxs-lookup"><span data-stu-id="065dc-131">string</span></span>   | <span data-ttu-id="065dc-132">应用开发人员在 [Microsoft Teams 应用压缩包](/microsoftteams/platform/concepts/apps/apps-package)中提供的目录 ID。</span><span class="sxs-lookup"><span data-stu-id="065dc-132">The ID of the catalog provided by the app developer in the [Microsoft Teams zip app package](/microsoftteams/platform/concepts/apps/apps-package).</span></span> |
| <span data-ttu-id="065dc-133">displayName</span><span class="sxs-lookup"><span data-stu-id="065dc-133">displayName</span></span>                | <span data-ttu-id="065dc-134">string</span><span class="sxs-lookup"><span data-stu-id="065dc-134">string</span></span>   | <span data-ttu-id="065dc-135">应用开发人员在 [Microsoft Teams 应用压缩包](/microsoftteams/platform/concepts/apps/apps-package)中提供的目录名称。</span><span class="sxs-lookup"><span data-stu-id="065dc-135">The name of the catalog app provided by the app developer in the [Microsoft Teams zip app package](/microsoftteams/platform/concepts/apps/apps-package).</span></span> |
| <span data-ttu-id="065dc-136">distributionMethod</span><span class="sxs-lookup"><span data-stu-id="065dc-136">distributionMethod</span></span>  | <span data-ttu-id="065dc-137">teamsAppDistributionMethod</span><span class="sxs-lookup"><span data-stu-id="065dc-137">teamsAppDistributionMethod</span></span>     | <span data-ttu-id="065dc-138">应用的分配方法。</span><span class="sxs-lookup"><span data-stu-id="065dc-138">The method of distribution for the app.</span></span> <span data-ttu-id="065dc-139">只读。</span><span class="sxs-lookup"><span data-stu-id="065dc-139">Read-only.</span></span>|

### <a name="teamsappdistributionmethod-values"></a><span data-ttu-id="065dc-140">teamsAppDistributionMethod 值</span><span class="sxs-lookup"><span data-stu-id="065dc-140">teamsAppDistributionMethod values</span></span>

|<span data-ttu-id="065dc-141">成员</span><span class="sxs-lookup"><span data-stu-id="065dc-141">Member</span></span>|<span data-ttu-id="065dc-142">值</span><span class="sxs-lookup"><span data-stu-id="065dc-142">Value</span></span>|<span data-ttu-id="065dc-143">说明</span><span class="sxs-lookup"><span data-stu-id="065dc-143">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="065dc-144">商店</span><span class="sxs-lookup"><span data-stu-id="065dc-144">store</span></span>|<span data-ttu-id="065dc-145">0</span><span class="sxs-lookup"><span data-stu-id="065dc-145">0</span></span>| <span data-ttu-id="065dc-146">应用适用于 Microsoft Teams 应用商店中的所有租户。</span><span class="sxs-lookup"><span data-stu-id="065dc-146">The app is available to all tenants through the Microsoft Teams app store.</span></span>|
|<span data-ttu-id="065dc-147">组织</span><span class="sxs-lookup"><span data-stu-id="065dc-147">organization</span></span>|<span data-ttu-id="065dc-148">1</span><span class="sxs-lookup"><span data-stu-id="065dc-148">1</span></span>|<span data-ttu-id="065dc-149">应用仅适用于此租户。</span><span class="sxs-lookup"><span data-stu-id="065dc-149">The app is available only in this tenant.</span></span>|
|<span data-ttu-id="065dc-150">旁加载</span><span class="sxs-lookup"><span data-stu-id="065dc-150">sideloaded</span></span>|<span data-ttu-id="065dc-151">2</span><span class="sxs-lookup"><span data-stu-id="065dc-151">2</span></span>|<span data-ttu-id="065dc-152">应用仅适用于安装它的用户/团队。</span><span class="sxs-lookup"><span data-stu-id="065dc-152">The app is available only to the user/team its installed to.</span></span>|

## <a name="relationships"></a><span data-ttu-id="065dc-153">关系</span><span class="sxs-lookup"><span data-stu-id="065dc-153">Relationships</span></span>

| <span data-ttu-id="065dc-154">关系</span><span class="sxs-lookup"><span data-stu-id="065dc-154">Relationship</span></span> | <span data-ttu-id="065dc-155">类型</span><span class="sxs-lookup"><span data-stu-id="065dc-155">Type</span></span>   | <span data-ttu-id="065dc-156">说明</span><span class="sxs-lookup"><span data-stu-id="065dc-156">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="065dc-157">appDefinitions</span><span class="sxs-lookup"><span data-stu-id="065dc-157">appDefinitions</span></span>|<span data-ttu-id="065dc-158">[teamsAppDefinition](teamsappdefinition.md) 集合</span><span class="sxs-lookup"><span data-stu-id="065dc-158">[teamsAppDefinition](teamsappdefinition.md) collection</span></span>| <span data-ttu-id="065dc-159">每个版本的应用的详细信息。</span><span class="sxs-lookup"><span data-stu-id="065dc-159">The details for each version of the app.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="065dc-160">JSON 表示形式</span><span class="sxs-lookup"><span data-stu-id="065dc-160">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsApp",
  "baseType": "microsoft.graph.entity"
}-->

```json
{
  "id": "string",
  "externalId": "string",
  "displayName": "string",
  "distributionMethod": "string"
}
```

## <a name="see-also"></a><span data-ttu-id="065dc-161">另请参阅</span><span class="sxs-lookup"><span data-stu-id="065dc-161">See also</span></span>

- [<span data-ttu-id="065dc-162">teamsAppInstallation</span><span class="sxs-lookup"><span data-stu-id="065dc-162">teamsAppInstallation</span></span>](teamsappinstallation.md)
- [<span data-ttu-id="065dc-163">teamsAppDefinition</span><span class="sxs-lookup"><span data-stu-id="065dc-163">teamsAppDefinition</span></span>](teamsappdefinition.md)
- [<span data-ttu-id="065dc-164">teamsTab</span><span class="sxs-lookup"><span data-stu-id="065dc-164">teamsTab</span></span>](../resources/teamstab.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "teamsApp resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->



