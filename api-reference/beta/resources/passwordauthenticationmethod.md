---
title: passwordAuthenticationMethod 资源类型
description: 注册到用户的密码的表示形式。
localization_priority: Normal
author: mmcla
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: ba932538e984af37a4f005ddcc2167c29d2267d0
ms.sourcegitcommit: 9c16d84eac9c34134864ad63a9bb95c309218a44
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2020
ms.locfileid: "43557911"
---
# <a name="passwordauthenticationmethod-resource-type"></a><span data-ttu-id="bbe43-103">passwordAuthenticationMethod 资源类型</span><span class="sxs-lookup"><span data-stu-id="bbe43-103">passwordAuthenticationMethod resource type</span></span>

<span data-ttu-id="bbe43-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="bbe43-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="bbe43-105">用户密码的表示形式。</span><span class="sxs-lookup"><span data-stu-id="bbe43-105">A representation of a user's password.</span></span> <span data-ttu-id="bbe43-106">出于安全考虑，密码本身永远不会返回到对象中，但可以采取措施重置密码。</span><span class="sxs-lookup"><span data-stu-id="bbe43-106">For security, the password itself will never be returned in the object, but action can be taken to reset a password.</span></span>

## <a name="methods"></a><span data-ttu-id="bbe43-107">方法</span><span class="sxs-lookup"><span data-stu-id="bbe43-107">Methods</span></span>

| <span data-ttu-id="bbe43-108">方法</span><span class="sxs-lookup"><span data-stu-id="bbe43-108">Method</span></span>       | <span data-ttu-id="bbe43-109">返回类型</span><span class="sxs-lookup"><span data-stu-id="bbe43-109">Return Type</span></span> | <span data-ttu-id="bbe43-110">说明</span><span class="sxs-lookup"><span data-stu-id="bbe43-110">Description</span></span> |
|:-------------|:------------|:------------|
|[<span data-ttu-id="bbe43-111">列出 passwordAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="bbe43-111">List passwordAuthenticationMethods</span></span>](../api/authentication-list-passwordmethods.md) | <span data-ttu-id="bbe43-112">[passwordAuthenticationMethod](passwordauthenticationmethod.md)集合</span><span class="sxs-lookup"><span data-stu-id="bbe43-112">[passwordAuthenticationMethod](passwordauthenticationmethod.md) collection</span></span> | <span data-ttu-id="bbe43-113">读取此用户的所有**passwordAuthenticationMethod**对象的属性和关系。</span><span class="sxs-lookup"><span data-stu-id="bbe43-113">Read the properties and relationships of all of this user's **passwordAuthenticationMethod** objects.</span></span> |
|[<span data-ttu-id="bbe43-114">获取 passwordAuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="bbe43-114">Get passwordAuthenticationMethod</span></span>](../api/passwordauthenticationmethod-get.md) | [<span data-ttu-id="bbe43-115">passwordAuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="bbe43-115">passwordAuthenticationMethod</span></span>](passwordauthenticationmethod.md) | <span data-ttu-id="bbe43-116">读取**passwordAuthenticationMethod**对象的属性和关系。</span><span class="sxs-lookup"><span data-stu-id="bbe43-116">Read the properties and relationships of a **passwordAuthenticationMethod** object.</span></span> |
|[<span data-ttu-id="bbe43-117">重置密码</span><span class="sxs-lookup"><span data-stu-id="bbe43-117">Reset password</span></span>](../api/passwordauthenticationmethod-resetpassword.md)|<span data-ttu-id="bbe43-118">无</span><span class="sxs-lookup"><span data-stu-id="bbe43-118">None</span></span>|<span data-ttu-id="bbe43-119">在云中重置用户的密码，如果同步，则在本地进行同步。</span><span class="sxs-lookup"><span data-stu-id="bbe43-119">Reset a user's password in the cloud and, if synced, on-premises.</span></span>|

## <a name="properties"></a><span data-ttu-id="bbe43-120">属性</span><span class="sxs-lookup"><span data-stu-id="bbe43-120">Properties</span></span>

| <span data-ttu-id="bbe43-121">属性</span><span class="sxs-lookup"><span data-stu-id="bbe43-121">Property</span></span>     | <span data-ttu-id="bbe43-122">类型</span><span class="sxs-lookup"><span data-stu-id="bbe43-122">Type</span></span>        | <span data-ttu-id="bbe43-123">说明</span><span class="sxs-lookup"><span data-stu-id="bbe43-123">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="bbe43-124">creationDateTime</span><span class="sxs-lookup"><span data-stu-id="bbe43-124">creationDateTime</span></span>|<span data-ttu-id="bbe43-125">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bbe43-125">DateTimeOffset</span></span>|<span data-ttu-id="bbe43-126">上次更新此密码的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="bbe43-126">The date and time when this password was last updated.</span></span> <span data-ttu-id="bbe43-127">当前未填充此属性。</span><span class="sxs-lookup"><span data-stu-id="bbe43-127">This property is currently not populated.</span></span> <span data-ttu-id="bbe43-128">只读。</span><span class="sxs-lookup"><span data-stu-id="bbe43-128">Read-only.</span></span> <span data-ttu-id="bbe43-129">时间戳类型表示采用 ISO 8601 格式的日期和时间信息，始终采用 UTC 时区。</span><span class="sxs-lookup"><span data-stu-id="bbe43-129">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="bbe43-130">例如，2014 年 1 月 1 日午夜 UTC 如下所示：`'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="bbe43-130">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="bbe43-131">id</span><span class="sxs-lookup"><span data-stu-id="bbe43-131">id</span></span>|<span data-ttu-id="bbe43-132">字符串</span><span class="sxs-lookup"><span data-stu-id="bbe43-132">String</span></span>| <span data-ttu-id="bbe43-133">为此用户注册的此密码的标识符。</span><span class="sxs-lookup"><span data-stu-id="bbe43-133">The identifier of this password registered to this user.</span></span> <span data-ttu-id="bbe43-134">只读。</span><span class="sxs-lookup"><span data-stu-id="bbe43-134">Read-only.</span></span>|
|<span data-ttu-id="bbe43-135">密码</span><span class="sxs-lookup"><span data-stu-id="bbe43-135">password</span></span>|<span data-ttu-id="bbe43-136">String</span><span class="sxs-lookup"><span data-stu-id="bbe43-136">String</span></span>|<span data-ttu-id="bbe43-137">出于安全的的情况，密码始终在列表或 GET 操作中以 null 的形式返回。</span><span class="sxs-lookup"><span data-stu-id="bbe43-137">For security, the password is always returned as null from a LIST or GET operation.</span></span>|

## <a name="relationships"></a><span data-ttu-id="bbe43-138">关系</span><span class="sxs-lookup"><span data-stu-id="bbe43-138">Relationships</span></span>

<span data-ttu-id="bbe43-139">无。</span><span class="sxs-lookup"><span data-stu-id="bbe43-139">None.</span></span>

## <a name="json-representation"></a><span data-ttu-id="bbe43-140">JSON 表示形式</span><span class="sxs-lookup"><span data-stu-id="bbe43-140">JSON representation</span></span>

<span data-ttu-id="bbe43-141">下面是资源的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="bbe43-141">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.passwordAuthenticationMethod",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "creationDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "password": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "passwordAuthenticationMethod resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->