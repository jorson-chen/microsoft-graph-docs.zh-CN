---
title: chatMessageAttachment 资源类型
description: 表示聊天消息实体的附件。
localization_priority: Normal
doc_type: resourcePageType
ms.prod: microsoft-teams
author: nkramer
ms.openlocfilehash: f1618356673cb164e3597212ab5767f52c236365
ms.sourcegitcommit: 62c900af626e46439d949462f09061cc5c41d6ff
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/16/2020
ms.locfileid: "44272759"
---
# <a name="chatmessageattachment-resource-type"></a><span data-ttu-id="4d63d-103">chatMessageAttachment 资源类型</span><span class="sxs-lookup"><span data-stu-id="4d63d-103">chatMessageAttachment resource type</span></span>

<span data-ttu-id="4d63d-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="4d63d-104">Namespace: microsoft.graph</span></span>

<span data-ttu-id="4d63d-105">表示[了 chatmessage](./chatmessage.md)实体的附件。</span><span class="sxs-lookup"><span data-stu-id="4d63d-105">Represents an attachment to a [chatMessage](./chatmessage.md) entity.</span></span>

## <a name="properties"></a><span data-ttu-id="4d63d-106">属性</span><span class="sxs-lookup"><span data-stu-id="4d63d-106">Properties</span></span>
| <span data-ttu-id="4d63d-107">属性</span><span class="sxs-lookup"><span data-stu-id="4d63d-107">Property</span></span>  | <span data-ttu-id="4d63d-108">类型</span><span class="sxs-lookup"><span data-stu-id="4d63d-108">Type</span></span> | <span data-ttu-id="4d63d-109">说明</span><span class="sxs-lookup"><span data-stu-id="4d63d-109">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4d63d-110">id</span><span class="sxs-lookup"><span data-stu-id="4d63d-110">id</span></span>|<span data-ttu-id="4d63d-111">string</span><span class="sxs-lookup"><span data-stu-id="4d63d-111">string</span></span>| <span data-ttu-id="4d63d-112">只读。</span><span class="sxs-lookup"><span data-stu-id="4d63d-112">Read-only.</span></span> <span data-ttu-id="4d63d-113">附件的唯一 id。</span><span class="sxs-lookup"><span data-stu-id="4d63d-113">Unique id of the attachment.</span></span>|
|<span data-ttu-id="4d63d-114">contentType</span><span class="sxs-lookup"><span data-stu-id="4d63d-114">contentType</span></span>| <span data-ttu-id="4d63d-115">string</span><span class="sxs-lookup"><span data-stu-id="4d63d-115">string</span></span> | <span data-ttu-id="4d63d-116">内容附件的媒体类型。</span><span class="sxs-lookup"><span data-stu-id="4d63d-116">The media type of the content attachment.</span></span> <span data-ttu-id="4d63d-117">它可以具有以下值：</span><span class="sxs-lookup"><span data-stu-id="4d63d-117">It can have the following values:</span></span> <br><ul><li><span data-ttu-id="4d63d-118">"引用：附件" 是指向其他文件的链接。</span><span class="sxs-lookup"><span data-stu-id="4d63d-118">reference: Attachment is a link to another file.</span></span> <span data-ttu-id="4d63d-119">使用指向对象的链接填充 contentURL。</span><span class="sxs-lookup"><span data-stu-id="4d63d-119">Populate the contentURL with the link to the object.</span></span><br></li><li><span data-ttu-id="4d63d-120">文件： Raw 文件附件。</span><span class="sxs-lookup"><span data-stu-id="4d63d-120">file: Raw file attachment.</span></span> <span data-ttu-id="4d63d-121">使用 data：格式的文件的 base64 编码填充 contenturl 字段。</span><span class="sxs-lookup"><span data-stu-id="4d63d-121">Populate the contenturl field with the base64 encoding of the file in data: format.</span></span><br></li><li><span data-ttu-id="4d63d-122">image/：带有指定图像类型（如 image/png、image/jpeg、image/gif）的图像类型。</span><span class="sxs-lookup"><span data-stu-id="4d63d-122">image/: Image type with the type of the image specified ex: image/png, image/jpeg, image/gif.</span></span> <span data-ttu-id="4d63d-123">使用 data：格式的文件的 base64 编码填充 contentUrl 字段。</span><span class="sxs-lookup"><span data-stu-id="4d63d-123">Populate the contentUrl field with the base64 encoding of the file in data: format.</span></span><br></li><li><span data-ttu-id="4d63d-124">视频/：具有指定格式的视频类型。</span><span class="sxs-lookup"><span data-stu-id="4d63d-124">video/: Video type with the format specified.</span></span> <span data-ttu-id="4d63d-125">Ex： video/.。</span><span class="sxs-lookup"><span data-stu-id="4d63d-125">Ex: video/mp4.</span></span> <span data-ttu-id="4d63d-126">使用 data：格式的文件的 base64 编码填充 contentUrl 字段。</span><span class="sxs-lookup"><span data-stu-id="4d63d-126">Populate the contentUrl field with the base64 encoding of the file in data: format.</span></span><br></li><li><span data-ttu-id="4d63d-127">音频/：指定格式的音频类型。</span><span class="sxs-lookup"><span data-stu-id="4d63d-127">audio/: Audio type with the format specified.</span></span> <span data-ttu-id="4d63d-128">Ex：音频/wmw。</span><span class="sxs-lookup"><span data-stu-id="4d63d-128">Ex: audio/wmw.</span></span> <span data-ttu-id="4d63d-129">使用 data：格式的文件的 base64 编码填充 contentUrl 字段。</span><span class="sxs-lookup"><span data-stu-id="4d63d-129">Populate the contentUrl field with the base64 encoding of the file in data: format.</span></span><br></li><li><span data-ttu-id="4d63d-130">应用程序/卡片类型：使用卡片类型指定要使用的确切卡片格式的富卡片附件类型。</span><span class="sxs-lookup"><span data-stu-id="4d63d-130">application/card type: Rich card attachment type with the card type specifying the exact card format to use.</span></span> <span data-ttu-id="4d63d-131">使用该卡片的 json 格式设置内容。</span><span class="sxs-lookup"><span data-stu-id="4d63d-131">Set content with the json format of the card.</span></span> <span data-ttu-id="4d63d-132">卡片类型支持的值包括：</span><span class="sxs-lookup"><span data-stu-id="4d63d-132">Supported values for card type include:</span></span><br><ul><li><span data-ttu-id="4d63d-133">应用程序/vnd.ms-excel：可包含文本、语音、图像、按钮和输入字段的任意组合的丰富卡片。</span><span class="sxs-lookup"><span data-stu-id="4d63d-133">application/vnd.microsoft.card.adaptive: A rich card that can contain any combination of text, speech, images,,buttons, and input fields.</span></span> <span data-ttu-id="4d63d-134">将 content 属性设置为一个自适应卡片对象。</span><span class="sxs-lookup"><span data-stu-id="4d63d-134">Set the content property to,an AdaptiveCard object.</span></span></li><li><span data-ttu-id="4d63d-135">应用程序/vnd.ms-excel：播放动画的富卡片。</span><span class="sxs-lookup"><span data-stu-id="4d63d-135">application/vnd.microsoft.card.animation: A rich card that plays animation.</span></span> <span data-ttu-id="4d63d-136">将 content 属性设置为 AnimationCardobject。</span><span class="sxs-lookup"><span data-stu-id="4d63d-136">Set the content property,to an AnimationCardobject.</span></span></li><li><span data-ttu-id="4d63d-137">vnd.ms-excel：一种播放音频文件的丰富卡片。</span><span class="sxs-lookup"><span data-stu-id="4d63d-137">application/vnd.microsoft.card.audio: A rich card that plays audio files.</span></span> <span data-ttu-id="4d63d-138">将 content 属性设置为 AudioCard 对象。</span><span class="sxs-lookup"><span data-stu-id="4d63d-138">Set the content property,to an AudioCard object.</span></span></li><li><span data-ttu-id="4d63d-139">vnd.ms-excel：一种播放视频的丰富卡片。</span><span class="sxs-lookup"><span data-stu-id="4d63d-139">application/vnd.microsoft.card.video: A rich card that plays videos.</span></span> <span data-ttu-id="4d63d-140">将 content 属性设置为 VideoCard 对象。</span><span class="sxs-lookup"><span data-stu-id="4d63d-140">Set the content property,to a VideoCard object.</span></span></li><li><span data-ttu-id="4d63d-141">应用程序/vnd.ms-excel：英雄卡片。</span><span class="sxs-lookup"><span data-stu-id="4d63d-141">application/vnd.microsoft.card.hero: A Hero card.</span></span> <span data-ttu-id="4d63d-142">将 content 属性设置为 HeroCard 对象。</span><span class="sxs-lookup"><span data-stu-id="4d63d-142">Set the content property to a HeroCard object.</span></span></li><li><span data-ttu-id="4d63d-143">application/vnd.ms-excel：缩略图卡片。</span><span class="sxs-lookup"><span data-stu-id="4d63d-143">application/vnd.microsoft.card.thumbnail: A Thumbnail card.</span></span> <span data-ttu-id="4d63d-144">将 content 属性设置为 ThumbnailCard 对象。</span><span class="sxs-lookup"><span data-stu-id="4d63d-144">Set the content property to a ThumbnailCard object.</span></span></li><li><span data-ttu-id="4d63d-145">应用程序/vnd.ms-excel：一个收据卡。</span><span class="sxs-lookup"><span data-stu-id="4d63d-145">application/vnd.microsoft.com.card.receipt: A Receipt card.</span></span> <span data-ttu-id="4d63d-146">将 content 属性设置为 ReceiptCard 对象。</span><span class="sxs-lookup"><span data-stu-id="4d63d-146">Set the content property to a ReceiptCard object.</span></span></li><li><span data-ttu-id="4d63d-147">应用程序/vnd.ms-excel：登录的用户的卡。</span><span class="sxs-lookup"><span data-stu-id="4d63d-147">application/vnd.microsoft.com.card.signin: A user Sign In card.</span></span> <span data-ttu-id="4d63d-148">将 content 属性设置为 SignInCard 对象。</span><span class="sxs-lookup"><span data-stu-id="4d63d-148">Set the content property to a SignInCard object.</span></span></ul></ul>|
|<span data-ttu-id="4d63d-149">contentUrl</span><span class="sxs-lookup"><span data-stu-id="4d63d-149">contentUrl</span></span>|<span data-ttu-id="4d63d-150">string</span><span class="sxs-lookup"><span data-stu-id="4d63d-150">string</span></span>|<span data-ttu-id="4d63d-151">附件内容的 URL。</span><span class="sxs-lookup"><span data-stu-id="4d63d-151">URL for the content of the attachment.</span></span> <span data-ttu-id="4d63d-152">支持的协议： http、https、文件和数据。</span><span class="sxs-lookup"><span data-stu-id="4d63d-152">Supported protocols: http, https, file and data.</span></span>|
|<span data-ttu-id="4d63d-153">content</span><span class="sxs-lookup"><span data-stu-id="4d63d-153">content</span></span>|<span data-ttu-id="4d63d-154">string</span><span class="sxs-lookup"><span data-stu-id="4d63d-154">string</span></span>|<span data-ttu-id="4d63d-155">附件的内容。</span><span class="sxs-lookup"><span data-stu-id="4d63d-155">The content of the attachment.</span></span> <span data-ttu-id="4d63d-156">如果附件是一个丰富的卡片，请将该属性设置为富卡片对象。</span><span class="sxs-lookup"><span data-stu-id="4d63d-156">If the attachment is a rich card, set the property to the rich card object.</span></span> <span data-ttu-id="4d63d-157">此属性和 contentUrl 相互排斥。</span><span class="sxs-lookup"><span data-stu-id="4d63d-157">This property and contentUrl are mutually exclusive.</span></span>|
|<span data-ttu-id="4d63d-158">name</span><span class="sxs-lookup"><span data-stu-id="4d63d-158">name</span></span>|<span data-ttu-id="4d63d-159">string</span><span class="sxs-lookup"><span data-stu-id="4d63d-159">string</span></span>|<span data-ttu-id="4d63d-160">附件的名称。</span><span class="sxs-lookup"><span data-stu-id="4d63d-160">Name of the attachment.</span></span>|
|<span data-ttu-id="4d63d-161">thumbnailUrl</span><span class="sxs-lookup"><span data-stu-id="4d63d-161">thumbnailUrl</span></span>| <span data-ttu-id="4d63d-162">string</span><span class="sxs-lookup"><span data-stu-id="4d63d-162">string</span></span> |<span data-ttu-id="4d63d-163">如果通道支持使用替代的较小的内容或 contentUrl 的缩略图图像的 URL。</span><span class="sxs-lookup"><span data-stu-id="4d63d-163">URL to a thumbnail image that the channel can use if it supports using an alternative, smaller form of content or contentUrl.</span></span> <span data-ttu-id="4d63d-164">例如，如果将 contentType 设置为 application/word 并将 contentUrl 设置为 Word 文档的位置，则可以包含表示该文档的缩略图图像。</span><span class="sxs-lookup"><span data-stu-id="4d63d-164">For example, if you set contentType to application/word and set contentUrl to the location of the Word document, you might include a thumbnail image that represents the document.</span></span> <span data-ttu-id="4d63d-165">频道可以显示缩略图图像而不是文档。</span><span class="sxs-lookup"><span data-stu-id="4d63d-165">The channel could display the thumbnail image instead of the document.</span></span> <span data-ttu-id="4d63d-166">当用户单击图像时，通道将打开文档。</span><span class="sxs-lookup"><span data-stu-id="4d63d-166">When the user clicks the image, the channel would open the document.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="4d63d-167">JSON 表示形式</span><span class="sxs-lookup"><span data-stu-id="4d63d-167">JSON representation</span></span>
 <span data-ttu-id="4d63d-168">下面是资源的 JSON 表示形式</span><span class="sxs-lookup"><span data-stu-id="4d63d-168">The following is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "thumbnailUrl",
    "content",
    "contentUrl"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.chatMessageAttachment"
}-->

```json
{
  "id": "string (identifier)",
  "contentType": "string",
  "contentUrl": "string",
  "content": "string",
  "name": "string",
  "thumbnailUrl": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "chat attachment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->