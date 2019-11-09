---
title: 搜索日历事件
description: 您可以在用户自己的日历中进行搜索。
author: knightsu
localization_priority: Normal
ms.prod: search
ms.openlocfilehash: 1b749c0b45b8250d011589e20b05a3d715b40bcb
ms.sourcegitcommit: 62507617292d5ad8598e83a8a253c986d9bac787
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/02/2019
ms.locfileid: "37939556"
---
# <a name="search-calendar-events"></a>搜索日历事件

您的应用程序可以在用户自己的主日历中。 用于搜索的用户标识基于授权令牌。

## <a name="example"></a>示例

### <a name="request"></a>请求

本示例将在用户的日历中搜索关键字 "contoso"，并检索最大25个结果。

```HTTP
POST https://graph.microsoft.com/beta/search/query
Content-Type: application/json
```

```json
{
  "requests": [
    {
       "entityTypes": ["microsoft.graph.event"],
       "query": {
        "query_string": {
          "query": "contoso"
        }
      },
      "from": 0,
      "size": 25
    }
  ]
}
```

## <a name="known-limitations"></a>已知限制

您只能访问用户自己的日历。 共享日历，不支持委派访问权限。

## <a name="next-steps"></a>后续步骤

详细了解以下信息：

- [使用搜索 API](/graph/api/resources/search-api-overview?view=graph-rest-beta)