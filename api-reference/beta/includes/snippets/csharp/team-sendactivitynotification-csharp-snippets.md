---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 4e8232b9a30e6e14992861fa79766666590198f4
ms.sourcegitcommit: 6ec748ef00d025ee216274a608291be3c1257777
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/27/2021
ms.locfileid: "50015425"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var topic = new TeamworkActivityTopic
{
    Source = TeamworkActivityTopicSource.Text,
    Value = "Deployment Approvals Channel",
    WebUrl = "https://teams.microsoft.com/l/message/19:448cfd2ac2a7490a9084a9ed14cttr78c@thread.skype/1605223780000?tenantId=c8b1bf45-3834-4ecf-971a-b4c755ee677d&groupId=d4c2a937-f097-435a-bc91-5c1683ca7245&parentMessageId=1605223771864&teamName=Approvals&channelName=Azure%20DevOps&createdTime=1605223780000"
};

var activityType = "deploymentApprovalRequired";

var previewText = new ItemBody
{
    Content = "New deployment requires your approval"
};

var recipient = new AadUserNotificationRecipient
{
    UserId = "569363e2-4e49-4661-87f2-16f245c5d66a"
};

var templateParameters = new List<KeyValuePair>()
{
    new KeyValuePair
    {
        Name = "deploymentId",
        Value = "6788662"
    }
};

await graphClient.Teams["{teamId}"]
    .SendActivityNotification(topic,activityType,null,previewText,templateParameters,recipient)
    .Request()
    .PostAsync();

```