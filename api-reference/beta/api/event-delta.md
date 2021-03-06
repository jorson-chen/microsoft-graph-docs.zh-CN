---
title: 'event: delta'
description: 获取 **calendarView** （事件范围）中已添加、删除或更新的事件集。
localization_priority: Normal
author: harini84
ms.prod: outlook
doc_type: apiPageType
ms.openlocfilehash: 2862bd8fc7af58d9521d043e4b23020a7991a7e2
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2020
ms.locfileid: "48954861"
---
# <a name="event-delta"></a>event: delta

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

获取一组在一个或多个日历中添加、删除或更新的 [事件](../resources/event.md) 资源。 

您可以在邮箱的所有日历或特定日历中的事件中或在 **calendarView** 的事件集合中获取这些增量更改的特定类型， (由日历的开始日期和结束日期) 定义的事件的范围。 日历可以是用户的默认日历或其他指定的日历。 在 **calendarView** 中获取增量更改的情况下，日历也可以是组日历。

**Delta** 函数调用类似于 `GET /events` 或 `GET /calendarview` 请求指定的日历，不同之处在于，通过在一个或多个调用中正确应用 [状态令牌](/graph/delta-query-overview#state-tokens)，可以在该日历中查询事件的增量更改。 这样，您就可以在指定的日历中维护和同步事件的本地存储，而无需每次从服务器提取该日历的所有事件。

下表列出了事件中的 **delta** 函数和日历中的 **calendarView** 上的 **delta** 函数之间的差异。

| 事件的 Delta 函数  | CalendarView 上的 Delta 函数  |
|:--------------------------|:---------------------------------------------------------|
| 获取不受开始和结束日期范围限制的日历中的所有事件的增量更改。 此外，还可以在开始时间之后的日历中获取事件的增量更改，该日历在日期/时间开始或之后。 | 获取 **calendarView** 的开始和结束日期/时间内的事件的增量更改。 |
| 出于性能原因，仅返回一组有限的 **事件** 属性。 随后用于 `GET /events/{id}` 扩展任何事件的客户端。 | 服务器端扩展返回一组更完整的 **事件** 属性。 |
| 响应包括单个实例和定期系列主机。 | 响应包括单个实例以及定期系列的匹配项和例外。 |
| 适用于用户日历中的事件，但不是组日历中的事件。 | 适用于用户和组日历中的事件。 |
| 当前仅在 beta 版本中可用。 | 在 v1.0 和 beta 版本中可用。 |

## <a name="permissions"></a>权限
要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。

|权限类型      | 权限（从最低特权到最高特权）              |
|:--------------------|:---------------------------------------------------------|
|委派（工作或学校帐户） | Calendars.Read、Calendars.ReadWrite    |
|委派（个人 Microsoft 帐户） | Calendars.Read、Calendars.ReadWrite    |
|应用程序 | Calendars.Read、Calendars.ReadWrite |

## <a name="http-request"></a>HTTP 请求

此部分显示初始 **delta** 函数调用的 HTTP 请求语法，以启动完全同步，以检索指定日历视图或日历视图中的所有事件。 此语法不包含任何 [状态令牌](/graph/delta-query-overview#state-tokens)。 

在或成功响应中返回的查询 URL `nextLink` `deltaLink` 包括状态令牌。 对于任何后续的 **delta** 函数调用，使用 `nextLink` 或在其前面的查询 URL `deltaLink` 。

### <a name="delta-function-on-events-in-a-user-calendar-preview"></a>用户日历中事件的 Delta 函数 (预览) 
在指定的用户日历 (s) 中，对在特定日期/时间开始或之后开始的所有事件或事件应用 **delta** 函数：

* 若要获取 _用户邮箱中_ 的所有事件或在指定的日期/时间之后或之后开始的事件的增量更改，请执行以下操作：
  <!-- { "blockType": "ignored" } -->
  ```http
  GET /me/events/delta 
  GET /users/{id | userPrincipalName}/events/delta 

  GET /me/events/delta?startDateTime={start_datetime}
  GET /users/{id | userPrincipalName}/events/delta?startDateTime={start_datetime}
  ```

* 若要获取 _用户的默认日历中_ 的所有事件或在指定的日期/时间之后或之后开始的事件的增量更改，请执行下列操作：
  <!-- { "blockType": "ignored" } -->
  ```http
  GET /me/calendar/events/delta 
  GET /users/{id | userPrincipalName}/calendar/events/delta 

  GET /me/calendar/events/delta?startDateTime={start_datetime} 
  GET /users/{id | userPrincipalName}/calendar/events/delta?startDateTime={start_datetime}
  ```

* 若要获取对 _指定的用户日历中_ 的所有事件或在指定的日期/时间之后开始或之后的事件的增量更改，请执行以下操作：
  <!-- { "blockType": "ignored" } -->
  ```http
  GET /me/calendars/{id}/events/delta 
  GET /users/{id | userPrincipalName}/calendars/{id}/events/delta 

  GET /me/calendars/{id}/events/delta?startDateTime={start_datetime} 
  GET /users/{id | userPrincipalName}/calendars/{id}/events/delta?startDateTime={start_datetime}
  ```

* 若要获取 _默认日历组的指定日历中_ 的所有事件或在指定的日期/时间之后或之后开始或之后的事件的增量更改，请执行以下操作：
  <!-- { "blockType": "ignored" } -->
  ```http
  GET /me/calendargroup/calendars/{id}/events/delta 
  GET /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/delta 

  GET /me/calendargroup/calendars/{id}/events/delta?startDateTime={start_datetime} 
  GET /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/delta?startDateTime={start_datetime}
  ```

* 若要获取增量更改 _指定的日历组和日历中_ 的所有事件或在指定的日期/时间之后或之后开始的事件，请执行以下操作：
  <!-- { "blockType": "ignored" } -->
  ```http
  GET /me/calendargroups/{id}/calendars/{id}/events/delta 
  GET /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/delta 

  GET /me/calendargroups/{id}/calendars/{id}/events/delta?startDateTime={start_datetime} 
  GET /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/delta?startDateTime={start_datetime}
  ```

<!-- Add back and fix html when group calendars are supported

### Delta function on events in a group calendar (preview)
* To get incremental changes of all the events, or of events starting on or after the specified date/time _in a group calendar_:
  !-- { "blockType": "ignored" } --
  ```http
  GET /groups/{id}/events/delta
  GET /groups/{id}/calendar/events/delta

  GET /groups/{id}/events/delta?startDateTime={start_datetime}
  GET /groups/{id}/calendar/events/delta?startDateTime={start_datetime}
  ```

  -->

### <a name="delta-function-on-calendarview-in-a-user-calendar"></a>用户日历中的 calendarView 上的 Delta 函数
在指定的用户日历中，对由开始和结束日期/时间分隔的一系列事件应用 **delta** 函数：

* 在 _用户的默认日历_ 的 "日历" 视图中获取增量更改：
  <!-- { "blockType": "ignored" } -->
  ```http
  GET /me/calendarView/delta?startDateTime={start_datetime}&endDateTime={end_datetime}
  GET /users/{id}/calendarView/delta?startDateTime={start_datetime}&endDateTime={end_datetime}
  ```

* 若要获取 _指定用户日历_ 的日历视图中的增量更改，请执行以下操作：
  <!-- { "blockType": "ignored" } -->
  ```http
  GET /me/calendars/{id}/calendarView/delta?startDateTime={start_datetime}&endDateTime={end_datetime}
  GET /users/{id}/calendars/{id}/calendarView/delta?startDateTime={start_datetime}&endDateTime={end_datetime}
  ```

### <a name="delta-function-on-calendarview-in-a-group-calendar"></a>组日历中的 calendarView 上的 Delta 函数
* 若要在 _组日历_ 的日历视图中获取增量更改，请执行以下操作：
  <!-- { "blockType": "ignored" } -->
  ```http
  GET /groups/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
  ```

## <a name="query-parameters"></a>查询参数

跟踪更改会产生一个或多个 **delta** 函数调用的往返。 如果要使用任意查询参数（`$deltatoken` 和 `$skiptoken` 除外），则必须在最初的 **delta** 请求中指定它。 Microsoft Graph 自动将指定的任意参数编码为响应中提供的 `nextLink` 或 `deltaLink` URL 的令牌部分。 只需预先指定所需的任何查询参数一次。
在后续请求中，只需复制并 `nextLink` 应用 `deltaLink` 上一个响应中的或 url，因为该 URL 已包含已编码的所需参数。

| 查询参数      | 类型   |说明|
|:---------------|:--------|:----------|
|startDateTime|String|时间范围的开始日期和时间，以 ISO 8601 格式表示。例如，“2019-11-08T19:00:00-08:00”。<br>时区在参数值的 "时区偏移" 部分中指定，如果存在，则不受 `Prefer: outlook.timezone` 标头的影响。 如果值中未包含时区偏移量，则将其解释为 UTC。<br>对于日历中事件的 **delta** 是可选的。 <br>对于 **calendarView** 上的 **delta** 是必需的。 |
|endDateTime|String|时间范围的结束日期和时间，以 ISO 8601 格式表示。例如，“2019-11-08T20:00:00-08:00”。<br>时区在参数值的 "时区偏移" 部分中指定，如果存在，则不受 `Prefer: outlook.timezone` 标头的影响。 如果值中未包含时区偏移量，则将其解释为 UTC。<br>日历中的事件 _不支持_**增量** 。 <br>对于 **calendarView** 上的 **delta** 是必需的。|
| $deltatoken | string | 对同一个日历视图之前的 **delta** 函数调用的 `deltaLink` URL 中返回的 [状态令牌](/graph/delta-query-overview)，指示该组更改跟踪的完成状态。将此令牌包含在对该日历视图的下一组更改追踪的首次请求中，并保存和应用整个 `deltaLink` URL。|
| $skiptoken | string | 之前的 **delta** 函数调用的 `nextLink` URL 中返回的 [状态令牌](/graph/delta-query-overview)，指示同一个日历视图中有进一步的更改需要跟踪。 |

不支持 `$expand` 、 `$filter` 、、 `$orderby` `$select` 和 `$search` 。


## <a name="request-headers"></a>请求标头
| 名称       | 类型 | 说明 |
|:---------------|:----------|:----------|
| Authorization  | string  | Bearer {token}。必需。 |
| Content-Type  | string  | application/json. Required. |
| Prefer | string  | odata.maxpagesize={x}。可选。 |
| Prefer | string | outlook. 时区 = {时区字符串}。 可选，如果缺省，则采用 UTC。|

## <a name="response"></a>响应

### <a name="delta-function-on-events-preview"></a> (预览的事件的 Delta 函数) 
如果成功，此方法 `200 OK` 在响应正文中返回响应代码和 [event](../resources/event.md) 集合。 由于性能原因，响应中的每个 **事件** 仅包含 **id** 、 **类型** 、 **起始** 和 **结束** 属性。 随后使用将 `GET /events/{id}` 任何事件从响应中展开。  

### <a name="delta-function-on-calendarview"></a>CalendarView 上的 Delta 函数
如果成功，此方法 `200 OK` 在响应正文中返回响应代码和 [event](../resources/event.md) 集合。

希望获取您通常从请求获取的所有属性 `GET /calendarview` 。 

## <a name="examples"></a>示例

### <a name="example-1-delta-function-on-events-in-a-calendar-preview"></a>示例1：日历中事件 (预览的 Delta 函数) 
#### <a name="request"></a>请求
以下示例显示了用于获取登录用户的默认日历中的事件的初始同步请求，该事件发生在指定参数之前或之后 `startDateTime` 。 初始请求不包含任何状态令牌。 

请求使用 `Prefer: odata.maxpagesize` 标头将每个响应中的最大事件数限制为1。 在 `delta` 收到响应之前，使用返回的查询继续调用该函数 `@odata.nextLink` `@odata.deltaLink` 。

<!-- {
  "blockType": "request",
  "name": "event_delta_events"
}-->
```msgraph-interactive
GET https://graph.microsoft.com/beta/me/calendar/events/delta?startDateTime=2020-06-12T00:00:00Z

Prefer: odata.maxpagesize=1
```

#### <a name="response"></a>响应

如果请求成功，则响应包含一个状态令牌，该令牌是 _\@ nextLink_ 响应) 头中的 _skipToken_ (，也可以是 _deltaToken_ (在 _\@ odata. deltaLink_ 响应头) 中。
它们分别指示是否应继续进行循环，或者是否已完成对该轮的所有更改的获取。

下面的响应显示 _\@ nextLink_ 响应头中的 _skipToken_ 。

<!-- {
  "blockType": "response",
  "name": "event_delta_events",
  "truncated": true,
  "@odata.type": "microsoft.graph.event",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.nextLink":"https://graph.microsoft.com/beta/me/calendar/events/delta?$skiptoken=R0usmcdvmMu7jxWP8",
  "value": [
    { 
      "id": " AAMkADllMWMwNDkzLWJlY2EtNDIyOS1iZjAA=", 
      "type": "singleInstance", 
      "start": {  
             "DateTime": "2020-02-19T10:00:00.0000000",  
             "TimeZone": "UTC" 
         },  
       "end": {  
                "DateTime": "2020-02-19T11:00:00.0000000",  
                "TimeZone": "UTC"        
          }  
        } 
  ]
}
```


### <a name="example-2-delta-function-on-calendarview"></a>示例2： calendarView 上的 Delta 函数
#### <a name="request"></a>请求

下面的示例显示了在 **calendarView** 指定的日期范围内，要获取已登录用户的指定日历中的事件的初始同步请求。 初始请求不包含任何状态令牌。 

请求使用 `Prefer: odata.maxpagesize` 标头将每个响应中的最大事件数限制为2个。 使用返回的查询继续调用该 `delta` 函数 `@odata.nextLink` ，直到您获取该日历视图中的所有事件以及 `@odata.deltaLink` 响应中的。

# <a name="http"></a>[HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "sampleKeys": ["AAMkADI5M1BbeAAA="],
  "name": "event_delta_calendarview"
}-->
```msgraph-interactive
GET https://graph.microsoft.com/beta/me/calendars/AAMkADI5M1BbeAAA=/calendarview/delta?startDateTime=2020-06-01T00:00:00Z&endDateTime=2020-06-10T00:00:00Z

Prefer: odata.maxpagesize=2
```
# <a name="c"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/event-delta-calendarview-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/event-delta-calendarview-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/event-delta-calendarview-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


#### <a name="response"></a>响应

如果请求成功，则响应包含一个状态令牌，该令牌是 _\@ nextLink_ 响应) 头中的 _skipToken_ (，也可以是 _deltaToken_ (在 _\@ odata. deltaLink_ 响应头) 中。
它们分别指示是否应继续进行循环，或者是否已完成对该轮的所有更改的获取。

下面的响应显示 _\@ nextLink_ 响应头中的 _skipToken_ 。

注意：为简洁起见，可能会截断此处显示的响应对象。 
<!-- {
  "blockType": "response",
  "name": "event_delta_calendarview",
  "truncated": true,
  "@odata.type": "microsoft.graph.event",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(event)",
    "@odata.nextLink": "https://graph.microsoft.com/beta/me/calendars/AAMkADI5M1BbeAAA=/calendarview/delta?$skiptoken=R0usmcdvmMu7jxWP8",
    "value": [
        {
            "@odata.type": "#microsoft.graph.event",
            "@odata.etag": "W/\"Jdsb3FEkPk2qoUHCdliYowACwixTgw==\"",
            "createdDateTime": "2020-06-16T04:05:43.8668791Z",
            "lastModifiedDateTime": "2020-06-16T04:08:27.354268Z",
            "changeKey": "Jdsb3FEkPk2qoUHCdliYowACwixTgw==",
            "categories": [],
            "transactionId": null,
            "originalStartTimeZone": "Pacific Standard Time",
            "originalEndTimeZone": "Pacific Standard Time",
            "uid": "040000008200E00074C5B7101A82E00800000000F088B8B95843D601000000000000000010000000165CD5547CFC9545B6492B261750B48C",
            "reminderMinutesBeforeStart": 15,
            "isReminderOn": false,
            "hasAttachments": false,
            "subject": "Summer party",
            "bodyPreview": "",
            "importance": "normal",
            "sensitivity": "normal",
            "isAllDay": false,
            "isCancelled": false,
            "isOrganizer": true,
            "IsRoomRequested": false,
            "AutoRoomBookingStatus": "None",
            "responseRequested": true,
            "seriesMasterId": null,
            "showAs": "busy",
            "type": "singleInstance",
            "webLink": "https://outlook.office365.com/owa/?itemid=AAMkADI5MAAKkeE1QAAA%3D&exvsurl=1&path=/calendar/item",
            "onlineMeetingUrl": null,
            "isOnlineMeeting": false,
            "onlineMeetingProvider": "unknown",
            "allowNewTimeProposals": true,
            "OccurrenceId": null,
            "isDraft": false,
            "recurrence": null,
            "AutoRoomBookingOptions": null,
            "onlineMeeting": null,
            "id": "AAMkADI5MAAKkeE1QAAA=",
            "responseStatus": {
                "response": "none",
                "time": "0001-01-01T00:00:00Z"
            },
            "body": {
                "contentType": "html",
                "content": "<html>\r\n<head></head>\r\n<body lang=\"EN-US\" link=\"#0563C1\" vlink=\"#954F72\" style=\"\">\r\n<div class=\"WordSection1\">\r\n<p class=\"MsoNormal\">&nbsp;</p>\r\n</div>\r\n</body>\r\n</html>\r\n"
            },
            "start": {
                "dateTime": "2020-06-02T20:00:00.0000000",
                "timeZone": "UTC"
            },
            "end": {
                "dateTime": "2020-06-02T22:30:00.0000000",
                "timeZone": "UTC"
            },
            "location": {
                "displayName": "",
                "locationType": "default",
                "uniqueIdType": "unknown",
                "address": {
                    "type": "unknown"
                },
                "coordinates": {}
            },
            "locations": [],
            "attendees": [
                {
                    "type": "required",
                    "status": {
                        "response": "none",
                        "time": "0001-01-01T00:00:00Z"
                    },
                    "emailAddress": {
                        "name": "Samantha Booth",
                        "address": "samanthab@contoso.onmicrosoft.com"
                    }
                }
            ],
            "organizer": {
                "emailAddress": {
                    "name": "Samantha Booth",
                    "address": "samanthab@contoso.onmicrosoft.com"
                }
            }
        },
        {
            "@odata.type": "#microsoft.graph.event",
            "@odata.etag": "W/\"Jdsb3FEkPk2qoUHCdliYowACwixTfw==\"",
            "createdDateTime": "2020-06-16T04:06:18.386713Z",
            "lastModifiedDateTime": "2020-06-16T04:08:19.5694048Z",
            "changeKey": "Jdsb3FEkPk2qoUHCdliYowACwixTfw==",
            "categories": [],
            "transactionId": null,
            "originalStartTimeZone": "Pacific Standard Time",
            "originalEndTimeZone": "Pacific Standard Time",
            "uid": "040000008200E00074C5B7101A82E0080000000060074BC55843D6010000000000000000100000002D33A89F36B10D43A12FD990B62858B2",
            "reminderMinutesBeforeStart": 15,
            "isReminderOn": true,
            "hasAttachments": false,
            "subject": "Summer party part 2",
            "bodyPreview": "",
            "importance": "normal",
            "sensitivity": "normal",
            "isAllDay": false,
            "isCancelled": false,
            "isOrganizer": true,
            "IsRoomRequested": false,
            "AutoRoomBookingStatus": "None",
            "responseRequested": true,
            "seriesMasterId": null,
            "showAs": "busy",
            "type": "singleInstance",
            "webLink": "https://outlook.office365.com/owa/?itemid=AAMkADI5MAAKkeE1RAAA%3D&exvsurl=1&path=/calendar/item",
            "onlineMeetingUrl": null,
            "isOnlineMeeting": false,
            "onlineMeetingProvider": "unknown",
            "allowNewTimeProposals": true,
            "OccurrenceId": null,
            "isDraft": false,
            "recurrence": null,
            "AutoRoomBookingOptions": null,
            "onlineMeeting": null,
            "id": "AAMkADI5MAAKkeE1RAAA=",
            "responseStatus": {
                "response": "none",
                "time": "0001-01-01T00:00:00Z"
            },
            "body": {
                "contentType": "html",
                "content": "<html>\r\n<head></head>\r\n<body lang=\"EN-US\" link=\"#0563C1\" vlink=\"#954F72\" style=\"\">\r\n<div class=\"WordSection1\">\r\n<p class=\"MsoNormal\">&nbsp;</p>\r\n</div>\r\n</body>\r\n</html>\r\n"
            },
            "start": {
                "dateTime": "2020-06-04T19:30:00.0000000",
                "timeZone": "UTC"
            },
            "end": {
                "dateTime": "2020-06-04T22:30:00.0000000",
                "timeZone": "UTC"
            },
            "location": {
                "displayName": "",
                "locationType": "default",
                "uniqueIdType": "unknown",
                "address": {
                    "type": "unknown"
                },
                "coordinates": {}
            },
            "locations": [],
            "attendees": [
                {
                    "type": "required",
                    "status": {
                        "response": "none",
                        "time": "0001-01-01T00:00:00Z"
                    },
                    "emailAddress": {
                        "name": "Samantha Booth",
                        "address": "samanthab@contoso.onmicrosoft.com"
                    }
                }
            ],
            "organizer": {
                "emailAddress": {
                    "name": "Samantha Booth",
                    "address": "samanthab@contoso.onmicrosoft.com"
                }
            }
        }
    ]
}
```

## <a name="see-also"></a>另请参阅

- [Microsoft Graph 增量查询](/graph/delta-query-overview)
- [获取文件夹中事件的增量更改](/graph/delta-query-events)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "event: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->


