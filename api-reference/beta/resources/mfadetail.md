---
title: mfaDetail 资源类型
description: '指示特定登录的 MFA 详细信息。 它包括用于登录的身份验证方法以及身份验证详细信息 (例如：电话、短信或语音邮件)  '
localization_priority: Normal
doc_type: resourcePageType
ms.prod: microsoft-identity-platform
author: besiler
ms.openlocfilehash: 97e075d6f12c102d366f63fd231d83c1144d16f3
ms.sourcegitcommit: 9f88b7e41a4a4a4d5f52bd995ce07c6f702bd5d6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/01/2020
ms.locfileid: "49524545"
---
# <a name="mfadetail-resource-type"></a>mfaDetail 资源类型

命名空间： microsoft. graph 指示特定登录的 MFA 详细信息。 它包括用于登录的身份验证方法以及身份验证详细信息 (例如：电话、短信或语音邮件) 



## <a name="properties"></a>属性
| 属性     | 类型   |说明|
|:---------------|:--------|:----------|
|authDetail|String|当所需的 MFA 为 "是" 时，指示对应登录活动的 MFA 身份验证详细信息。|
|authMethod|String|指示当 "MFA 必需" 字段为 "是" 时， (SMS，Phone，身份验证器应用的 MFA 身份验证方法是相应登录活动的一些值) 。|

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.mfaDetail"
}-->

```json
{
  "authDetail": "String",
  "authMethod": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mfaDetail resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


