---
title: signInActivity 资源类型
description: 提供特定用户的上次登录日期。
localization_priority: Normal
author: besiler
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: e8300e787fe516a9712359f99ebf215f4813a0b9
ms.sourcegitcommit: 9f88b7e41a4a4a4d5f52bd995ce07c6f702bd5d6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/01/2020
ms.locfileid: "49521227"
---
# <a name="signinactivity-resource-type"></a>signInActivity 资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

提供特定 [用户](user.md)的上次登录日期。

## <a name="properties"></a>属性

| 属性     | 类型        | 说明 |
|:-------------|:------------|:------------|
|lastSignInDateTime|DateTimeOffset|特定用户的上次登录日期。 您可以使用此字段来计算用户上次登录目录的时间。 此字段可用于生成报表，如非活动用户。 时间戳表示使用 ISO 8601 格式的日期和时间信息，并且始终处于 UTC 时间。 例如，2014 年 1 月 1 日午夜 UTC 如下所示：`'2014-01-01T00:00:00Z'`。 若要详细了解如何使用此属性的值，请参阅 [管理 AZURE AD 中的非活动用户帐户](/azure/active-directory/reports-monitoring/howto-manage-inactive-user-accounts)。|
|lastSignInRequestId|String|此用户执行的最后一个登录的请求 ID。|

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.signInActivity",
  "baseType": null
}-->

```json
{
  "lastSignInDateTime": "String (timestamp)",
  "lastSignInRequestId": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "signInActivity resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->