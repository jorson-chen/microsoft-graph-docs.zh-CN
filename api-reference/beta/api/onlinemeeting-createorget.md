---
title: 'onlineMeeting: createOrGet'
description: 使用自定义指定的外部 ID 创建联机会议。 如果已存在外部 ID，此 API 将返回具有该外部 ID 的 onlineMeeting 对象。
author: ananmishr
localization_priority: Normal
ms.prod: cloud-communications
doc_type: apiPageType
ms.openlocfilehash: 51e619e6f09f98fcaa12423881a930df72c0597a
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2020
ms.locfileid: "48980137"
---
# <a name="onlinemeeting-createorget"></a>onlineMeeting: createOrGet

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

创建具有自定义的指定外部 ID 的 [onlineMeeting](../resources/onlinemeeting.md) 对象。 如果已存在外部 ID，此 API 将返回具有该外部 ID 的 [onlineMeeting](../resources/onlinemeeting.md) 对象。 

> **注释** ：会议不会显示在用户的日历上。

## <a name="permissions"></a>权限
要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。

| 权限类型                        | 权限（从最低特权到最高特权） |
| :------------------------------------- | :------------------------------------------ |
| 委派（工作或学校帐户）     | OnlineMeetings.ReadWrite                    |
| 委派（个人 Microsoft 帐户） | 不支持。                              |
| 应用程序                            | OnlineMeetings.ReadWrite.All*                |

> [!IMPORTANT]
> \* 管理员必须创建 [应用程序访问策略](/graph/cloud-communication-online-meeting-application-access-policy) 并将其授予用户，授权在该策略中配置的应用程序，以创建或获取一个外部 ID 代表该用户的联机会议， (用户 id 在请求路径) 中指定。

## <a name="http-request"></a>HTTP 请求

使用委派令牌时的请求：
<!-- { "blockType": "ignored" } -->
```http
POST /me/onlineMeetings/createOrGet
```

使用应用程序令牌时的请求：
<!-- { "blockType": "ignored" } -->
```http
POST /users/{userId}/onlineMeetings/createOrGet
```

> **注意：** `userId` 是 [Azure 用户管理门户](https://portal.azure.com/#blade/Microsoft_AAD_IAM/UsersManagementMenuBlade)中用户的对象 ID。 有关详细信息，请参阅[应用程序访问策略](/graph/cloud-communication-online-meeting-application-access-policy)。

## <a name="request-headers"></a>请求标头
| 名称          | 说明                 |
| :------------ | :-------------------------- |
| Authorization | Bearer {token}。必需。   |
| Content-type  | application/json. Required. |

## <a name="request-body"></a>请求正文
在请求正文中，提供具有以下参数的 JSON 对象。

| 参数     | 类型                                                       | 说明                                                                                          |
| :------------ | :--------------------------------------------------------- | :--------------------------------------------------------------------------------------------------- |
| chatInfo      | [chatInfo](../resources/chatinfo.md)                       | 与此联机会议关联的聊天信息。                                            |
| endDateTime   | 日期时间                                                   | 以 UTC 表示的会议结束时间。                                                                         |
| externalId    | String                                                     | 外部 ID。 自定义 ID。  (必需的)                                                              |
| participants  | [meetingParticipants](../resources/meetingparticipants.md) | 与联机会议关联的参与者。  这包括组织者和与会者。 |
| startDateTime | 日期时间                                                   | 以 UTC 表示的会议开始时间。                                                                       |
| subject       | String                                                     | 联机会议的主题。                                                                   |

> **注意：**
>
> - 如果未提供 **startDateTime** 和 **EndDateTime** ，则 **StartDateTime** 将默认为当前 dateTime 值， **endDateTime** 值将等于 **startDateTime** + 1 小时。
>
> - 如果提供了 **startDateTime** ，但 **endDateTime** 不是，则 **endDateTime** 值将等于 **startDateTime** + 1 小时。
>
> - 如果在没有 **startDateTime** 的情况下提供 **EndDateTime** ，或者 **endDateTime** 早于 **startDateTime** ，则将引发错误。
>
> - 当前 **chatInfo** 仅在 beta 中受支持。

## <a name="response"></a>响应
如果成功，此方法将在 `201 Created` 创建新会议时返回响应代码，或者在 `200 OK` 检索现有会议时返回响应代码。 在这两种情况下，响应正文中都会返回一个 [onlineMeeting](../resources/onlinemeeting.md) 对象。

## <a name="examples"></a>示例

### <a name="example-1-create-or-get-an-online-meeting-with-an-external-id"></a>示例1：创建或获取具有外部 ID 的联机会议

#### <a name="request"></a>请求


# <a name="http"></a>[HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "create-or-get-onlinemeeting"
}-->

```http
POST https://graph.microsoft.com/beta/me/onlineMeetings/createOrGet
Content-Type: application/json

{
    "startDateTime": "2020-02-06T01:49:21.3524945+00:00",
    "endDateTime": "2020-02-06T02:19:21.3524945+00:00",
    "subject": "Create a meeting with customId provided",
    "externalId": "7eb8263f-d0e0-4149-bb1c-1f0476083c56",
    "participants": {
        "attendees": [
            {
                "identity": {
                    "user": {
                        "id": "1f35f2e6-9cab-44ad-8d5a-b74c14720000"
                    }
                },
                "role": "presenter",
                "upn": "test1@contoso.com"
            }
        ]
    }
}
```
# <a name="c"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/create-or-get-onlinemeeting-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/create-or-get-onlinemeeting-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/create-or-get-onlinemeeting-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/create-or-get-onlinemeeting-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


#### <a name="response"></a>响应

>**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。 

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.onlineMeeting"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "id": "(redacted)",
    "creationDateTime": "2020-09-11T06:30:18.1909168Z",
    "startDateTime": "2020-09-11T06:30:18.0615989Z",
    "endDateTime": "2020-09-11T07:30:18.0615989Z",
    "joinWebUrl": "(redacted)",
    "subject": "Create a meeting with customId provided",
    "isBroadcast": false,
    "autoAdmittedUsers": "EveryoneInCompany",
    "isEntryExitAnnounced": true,
    "allowedPresenters": "everyone",
    "videoTeleconferenceId": "(redacted)",
    "externalId": "7eb8263f-d0e0-4149-bb1c-1f0476083c56",
    "participants": {
        "organizer": {
            "upn": "(redacted)",
            "role": "presenter",
            "identity": {
                "user": {
                    "id": "(redacted)",
                }
            }
        },
        "attendees": [
            {
                "upn": "test1@contoso.com",
                "role": null,
                "identity": {
                    "user": {
                        "id": "1f35f2e6-9cab-44ad-8d5a-b74c14720000",
                    }
                }
            }
        ],
        "producers": [],
        "contributors": []
    },
    "lobbyBypassSettings": {
        "scope": "organization",
        "isDialInBypassEnabled": false
    },
    "audioConferencing": {
        "conferenceId": "(redacted)",
        "tollNumber": "+1 206-485-3005",
        "tollFreeNumber": null,
        "dialinUrl": "https://dialin.teams.microsoft.com/0e73a853-1cc2-436c-b18c-9f53e0a97c24?id=(redacted)"
    },
    "chatInfo": {
        "threadId": "19:7ebda77322dd4505ac4dedb5b67df076@thread.tacv2",
        "messageId": "0",
        "replyChainMessageId": null
    },
}
```


### <a name="example-2-create-or-get-an-online-meeting-in-a-microsoft-teams-channel-with-an-external-id"></a>示例2：在具有外部 ID 的 Microsoft 团队频道中创建或获取联机会议

#### <a name="request"></a>请求

<!-- {
  "blockType": "request",
  "name": "create-or-get-onlinemeeting"
}-->
```http
POST https://graph.microsoft.com/beta/me/onlineMeetings/createOrGet
Content-Type: application/json

{
    "chatInfo": {
        "threadId": "19:7ebda77322dd4505ac4dedb5b67df076@thread.tacv2"
    },
    "startDateTime": "2020-02-06T01:49:21.3524945+00:00",
    "endDateTime": "2020-02-06T02:19:21.3524945+00:00",
    "externalId": "7eb8263f-d0e0-4149-bb1c-1f0476083c56",
    "participants": {
        "attendees": [
            {
                "identity": {
                    "user": {
                        "id": "1f35f2e6-9cab-44ad-8d5a-b74c14720000"
                    }
                },
                "upn": "test1@contoso.com"
            }
        ]
    },
    "subject": "Create a meeting with customId provided"
}
```

#### <a name="response"></a>响应

>**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。 

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.onlineMeeting"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "id": "(redacted)",
    "creationDateTime": "2020-09-11T06:30:18.1909168Z",
    "startDateTime": "2020-09-11T06:30:18.0615989Z",
    "endDateTime": "2020-09-11T07:30:18.0615989Z",
    "joinWebUrl": "(redacted)",
    "subject": "Create a meeting with customId provided",
    "isBroadcast": false,
    "autoAdmittedUsers": "EveryoneInCompany",
    "isEntryExitAnnounced": true,
    "allowedPresenters": "everyone",
    "videoTeleconferenceId": "(redacted)",
    "externalId": "7eb8263f-d0e0-4149-bb1c-1f0476083c56",
    "participants": {
        "organizer": {
            "upn": "(redacted)",
            "role": "presenter",
            "identity": {
                "user": {
                    "id": "(redacted)",
                }
            }
        },
        "attendees": [
            {
                "upn": "test1@contoso.com",
                "role": null,
                "identity": {
                    "user": {
                        "id": "1f35f2e6-9cab-44ad-8d5a-b74c14720000",
                    }
                }
            }
        ],
        "producers": [],
        "contributors": []
    },
    "lobbyBypassSettings": {
        "scope": "organization",
        "isDialInBypassEnabled": false
    },
    "audioConferencing": {
        "conferenceId": "(redacted)",
        "tollNumber": "+1 206-485-3005",
        "tollFreeNumber": null,
        "dialinUrl": "https://dialin.teams.microsoft.com/0e73a853-1cc2-436c-b18c-9f53e0a97c24?id=(redacted)"
    },
    "chatInfo": {
        "threadId": "19:7ebda77322dd4505ac4dedb5b67df076@thread.tacv2",
        "messageId": "1599805818399",
        "replyChainMessageId": null
    },
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Create onlineMeeting",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->


