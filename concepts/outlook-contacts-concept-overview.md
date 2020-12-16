---
title: Outlook 个人联系人 API 概述
description: Outlook 联系人可让你存储个人联系人的数据，并且属于Microsoft 365 中 Outlook 邮件中心的一部分。 通过 Outlook，可以管理电子邮件、安排会议、在组织中查找有关用户的信息、启动在线对话、共享文件，以及实现小组协作。
author: angelgolfer-ms
localization_priority: Priority
ms.prod: outlook
ms.custom: scenarios:getting-started
ms.openlocfilehash: 4c95c27615cf1e74c78630b9983e98461160883d
ms.sourcegitcommit: 7153a13f4e95c7d9fed3f2c10a3d075ff87b368d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/26/2020
ms.locfileid: "44897167"
---
# <a name="outlook-personal-contacts-api-overview"></a><span data-ttu-id="8c223-104">Outlook 个人联系人 API 概述</span><span class="sxs-lookup"><span data-stu-id="8c223-104">Outlook personal contacts API overview</span></span>

<span data-ttu-id="8c223-105">Outlook 联系人可让你存储个人联系人的数据，并且属于Microsoft 365 中 Outlook 邮件中心的一部分。</span><span class="sxs-lookup"><span data-stu-id="8c223-105">Outlook contacts lets you store personal contacts' data, and is part of the Outlook messaging hub in Microsoft 365.</span></span> <span data-ttu-id="8c223-106">通过 Outlook，可以管理电子邮件、安排会议、在组织中查找有关用户的信息、启动在线对话、共享文件，以及实现小组协作。</span><span class="sxs-lookup"><span data-stu-id="8c223-106">Through Outlook, you can manage emails, schedule meetings, find information about users in an organization, initiate online conversations, share files, and collaborate in groups.</span></span>

## <a name="why-integrate-with-outlook-personal-contacts"></a><span data-ttu-id="8c223-107">为何要与 Outlook 个人联系人集成？</span><span class="sxs-lookup"><span data-stu-id="8c223-107">Why integrate with Outlook personal contacts?</span></span>

### <a name="complement-messaging-and-calendaring-scenarios-for-hundreds-of-millions-of-customers"></a><span data-ttu-id="8c223-108">为亿万客户补充邮件和日历应用场景</span><span class="sxs-lookup"><span data-stu-id="8c223-108">Complement messaging and calendaring scenarios for hundreds of millions of customers</span></span>

<span data-ttu-id="8c223-109">亿万消费者和数千万组织客户选择 Outlook 作为他们的电子邮件客户端。</span><span class="sxs-lookup"><span data-stu-id="8c223-109">Hundreds of millions of consumers and tens of millions of organization customers choose Outlook as their email client.</span></span> <span data-ttu-id="8c223-110">通过让客户在 Outlook 中维护一个方便、集成的联系人数据存储，联系人为邮件和日历提供了一项补充功能。</span><span class="sxs-lookup"><span data-stu-id="8c223-110">Contacts provide a complementary function for messaging and calendaring by letting customers maintain a convenient, integrated store of contacts data within Outlook.</span></span> <span data-ttu-id="8c223-111">对于开发者而言，利用[邮件](outlook-mail-concept-overview.md)或[日历](outlook-calendar-concept-overview.md)的丰富功能，就意味着通过用户的联系人数据开发更丰富的应用场景。</span><span class="sxs-lookup"><span data-stu-id="8c223-111">For developers, tapping into the rich functionality of [mail](outlook-mail-concept-overview.md) or [calendar](outlook-calendar-concept-overview.md) means opening up richer scenarios with the user's contacts data.</span></span>

### <a name="automate-contact-organization"></a><span data-ttu-id="8c223-112">自动执行联系人组织</span><span class="sxs-lookup"><span data-stu-id="8c223-112">Automate contact organization</span></span>

<span data-ttu-id="8c223-113">通过联系人 API，可以保持客户的组织性，与客户通过 Outlook 自己执行此操作等效：</span><span class="sxs-lookup"><span data-stu-id="8c223-113">The contacts API lets you keep your customers organized, in close parity as the customers do it themselves through Outlook:</span></span>

- <span data-ttu-id="8c223-114">与客户体验类似，可以创建 [contact](/graph/api/resources/contact?view=graph-rest-1.0) 实例并将其分配给 [contactFolder](/graph/api/resources/contactfolder?view=graph-rest-1.0) 对象。</span><span class="sxs-lookup"><span data-stu-id="8c223-114">Similarly to the customer experience, you can create [contact](/graph/api/resources/contact?view=graph-rest-1.0) instances and assign them to [contactFolder](/graph/api/resources/contactfolder?view=graph-rest-1.0) objects.</span></span>
- <span data-ttu-id="8c223-115">通过联系人 API，可以采用一致的方式分配类别联系人及事件、消息、任务和组帖子，从而增强组织和发现。</span><span class="sxs-lookup"><span data-stu-id="8c223-115">The contacts API lets you assign categories contacts, as well as events, messages, tasks, and group posts in a consistent way to enhance organization and discovery.</span></span> <span data-ttu-id="8c223-116">此外，可以[定义用户的主类别列表](/graph/api/outlookuser-post-mastercategories?view=graph-rest-1.0)，从而开发其他创造性方案。</span><span class="sxs-lookup"><span data-stu-id="8c223-116">In addition, you can [define a user's master list of categories](/graph/api/outlookuser-post-mastercategories?view=graph-rest-1.0), which can open up additional creative scenarios.</span></span>
- <span data-ttu-id="8c223-117">你可以对[联系人](/graph/api/resources/contact?view=graph-rest-1.0)设置一个标志以进行跟进。</span><span class="sxs-lookup"><span data-stu-id="8c223-117">You can set a flag on a [contact](/graph/api/resources/contact?view=graph-rest-1.0) for follow-up.</span></span> <span data-ttu-id="8c223-118">（Microsoft Graph 中的标记目前为[预览状态](versioning-and-support.md#beta-version)。）</span><span class="sxs-lookup"><span data-stu-id="8c223-118">(Flagging is currently [in preview](versioning-and-support.md#beta-version) in Microsoft Graph.)</span></span>

### <a name="share-contact-information"></a><span data-ttu-id="8c223-119">共享联系人信息</span><span class="sxs-lookup"><span data-stu-id="8c223-119">Share contact information</span></span>

<span data-ttu-id="8c223-120">通过联系人 API，使你能够获得已登录用户或将其联系人共享或委派给已登录用户的用户的联系人项目。</span><span class="sxs-lookup"><span data-stu-id="8c223-120">The contacts API lets you get contact items of the signed-in user, or of the users who have shared or delegated their contacts to the signed-in user.</span></span> <span data-ttu-id="8c223-121">例如，如果 Garth 与 John 共享联系人文件夹，或者如果 Garth 向 John 委派了访问权限，则来自 John 的[委派权限](auth/auth-concepts.md#microsoft-graph-permissions)将授予你对 Garth 共享日历和内容的读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="8c223-121">For example, if Garth has shared a contact folder with John, or if Garth has delegated access to John, then [delegated permissions](auth/auth-concepts.md#microsoft-graph-permissions) from John would give you read access to Garth's shared calendar and contents as well.</span></span>

### <a name="leverage-people-api-in-microsoft-graph-to-make-better-use-of-all-people-data"></a><span data-ttu-id="8c223-122">利用 Microsoft Graph 中的人员 API 更好地利用所有人员数据</span><span class="sxs-lookup"><span data-stu-id="8c223-122">Leverage people API in Microsoft Graph to make better use of all people data</span></span>

<span data-ttu-id="8c223-123">你可以对 Outlook [联系人](/graph/api/resources/contact?view=graph-rest-1.0)使用典型 CRUD 操作来创建和管理联系人。</span><span class="sxs-lookup"><span data-stu-id="8c223-123">You can use the typical CRUD operations for an Outlook [contact](/graph/api/resources/contact?view=graph-rest-1.0) to create and manage contacts.</span></span> <span data-ttu-id="8c223-124">作为 Microsoft Graph 的一部分，还可以使用[人员 API](people-example.md)，查看用户的 Outlook 联系人，以及社交网络、组织目录和最近通信中的人员，并返回有关所有这些来源中人员的与用户相关度最大的信息。</span><span class="sxs-lookup"><span data-stu-id="8c223-124">As part of Microsoft Graph, you can also use the [people API](people-example.md) that looks at a user's Outlook contacts, as well as social networks, organization directory, and people from recent communication, and return information about people from all these sources that are most relevant to the user.</span></span> <span data-ttu-id="8c223-125">在人员选取器应用场景中利用这一额外智能。</span><span class="sxs-lookup"><span data-stu-id="8c223-125">Take advantage of this additional intelligence in people picker scenarios.</span></span>

### <a name="take-advantage-of-other-shared-features-and-conveniences-in-microsoft-graph"></a><span data-ttu-id="8c223-126">利用 Microsoft Graph 中的其他共享功能和便利</span><span class="sxs-lookup"><span data-stu-id="8c223-126">Take advantage of other shared features and conveniences in Microsoft Graph</span></span>

- <span data-ttu-id="8c223-127">**contact** 实体支持与存储在 Exchange Online 或 Azure Active Directory 中的用户照片相同的 [profilePhoto](/graph/api/resources/profilephoto?view=graph-rest-1.0) 实体实现的联系人照片。</span><span class="sxs-lookup"><span data-stu-id="8c223-127">The **contact** entity supports a contact photo which is implemented as the same [profilePhoto](/graph/api/resources/profilephoto?view=graph-rest-1.0) entity as a user photo stored in Exchange Online or Azure Active Directory.</span></span> <span data-ttu-id="8c223-128">这消除了在联系人与用户个人资料照片之间进行转换的开销。</span><span class="sxs-lookup"><span data-stu-id="8c223-128">This eliminates the overhead in converting between contact and user profile photos.</span></span>
- <span data-ttu-id="8c223-129">你可以通过订阅[更改通知](/graph/api/resources/webhooks?view=graph-rest-1.0)和[跟踪对联系人和联系人文件夹所做的更改](delta-query-overview.md)，使应用本地存储保持同步。</span><span class="sxs-lookup"><span data-stu-id="8c223-129">You can keep the app local store synchronized by subscribing to [change notifications](/graph/api/resources/webhooks?view=graph-rest-1.0) and [tracking changes](delta-query-overview.md) to contacts and contact folders.</span></span>
- <span data-ttu-id="8c223-130">可以将联系人实例中的应用存储扩展为[开放扩展](extensibility-overview.md#open-extensions)，或者将强类型化的自定义数据添加到联系人架构中作为[架构扩展](extensibility-overview.md#schema-extensions)。</span><span class="sxs-lookup"><span data-stu-id="8c223-130">You can extend app storage in a contact instance as an [open extension](extensibility-overview.md#open-extensions), or add strongly typed custom data to the contact schema as a [schema extension](extensibility-overview.md#schema-extensions).</span></span>

## <a name="where-is-the-data"></a><span data-ttu-id="8c223-131">数据在什么位置？</span><span class="sxs-lookup"><span data-stu-id="8c223-131">Where is the data?</span></span>

[!INCLUDE [outlook-mailbox-type-support](../includes/outlook-mailbox-type-support.md)]

## <a name="api-reference"></a><span data-ttu-id="8c223-132">API 参考</span><span class="sxs-lookup"><span data-stu-id="8c223-132">API reference</span></span>

<span data-ttu-id="8c223-133">在查找此服务的 API 参考？</span><span class="sxs-lookup"><span data-stu-id="8c223-133">Looking for the API reference for this service?</span></span>

- [<span data-ttu-id="8c223-134">Microsoft Graph v1.0 中的 Outlook 联系人 API</span><span class="sxs-lookup"><span data-stu-id="8c223-134">Outlook contacts API in Microsoft Graph v1.0</span></span>](/graph/api/resources/contact?view=graph-rest-1.0)
- [<span data-ttu-id="8c223-135">Microsoft Graph beta 中的 Outlook 联系人 API</span><span class="sxs-lookup"><span data-stu-id="8c223-135">Outlook contacts API in Microsoft Graph beta</span></span>](/graph/api/resources/contact?view=graph-rest-beta)

## <a name="next-steps"></a><span data-ttu-id="8c223-136">后续步骤</span><span class="sxs-lookup"><span data-stu-id="8c223-136">Next steps</span></span>

- <span data-ttu-id="8c223-137">在 [Graph 浏览器](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Fcontacts&version=v1.0)中选择和试用联系人示例查询。</span><span class="sxs-lookup"><span data-stu-id="8c223-137">Select and try contacts sample queries in [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Fcontacts&version=v1.0).</span></span> <span data-ttu-id="8c223-138">选择左侧列中的“显示更多示例”。</span><span class="sxs-lookup"><span data-stu-id="8c223-138">Choose **Show more samples** in the column on the left.</span></span> <span data-ttu-id="8c223-139">使用菜单启用“个人联系人”。</span><span class="sxs-lookup"><span data-stu-id="8c223-139">Use the menu to turn on **Personal contacts**.</span></span>
- <span data-ttu-id="8c223-140">了解如何：</span><span class="sxs-lookup"><span data-stu-id="8c223-140">Learn about:</span></span>
  - [<span data-ttu-id="8c223-141">获取 Outlook 资源的不可变标识符</span><span class="sxs-lookup"><span data-stu-id="8c223-141">Getting immutable identifiers for Outlook resources</span></span>](outlook-immutable-id.md)
  - [<span data-ttu-id="8c223-142">获取共享联系人</span><span class="sxs-lookup"><span data-stu-id="8c223-142">Getting shared contacts</span></span>](outlook-get-shared-contacts-folders.md)
- <span data-ttu-id="8c223-143">查看 Outlook [联系人 API](/graph/api/resources/contact?view=graph-rest-1.0) 参考。</span><span class="sxs-lookup"><span data-stu-id="8c223-143">Take a look at the Outlook [contacts API](/graph/api/resources/contact?view=graph-rest-1.0) reference.</span></span>
