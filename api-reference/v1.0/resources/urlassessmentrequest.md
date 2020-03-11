---
title: urlAssessmentRequest 资源类型
description: 用于创建和检索 URL 威胁评估。
localization_priority: Normal
author: hafen-ms
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 27e728e172ec8870082f6b7d668f1f19f29f22dc
ms.sourcegitcommit: c4d6ccd343a6b298a2aa844f1bad66c736487251
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/11/2020
ms.locfileid: "42591479"
---
# <a name="urlassessmentrequest-resource-type"></a>urlAssessmentRequest 资源类型

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

用于创建和检索从[threatAssessmentRequest](threatAssessmentRequest.md)派生的 URL 威胁评估。

## <a name="methods"></a>Methods

| 方法       | 返回类型 | 说明 |
|:-------------|:------------|:------------|
| [创建 threatAssessmentRequest](../api/informationprotection-post-threatassessmentrequests.md) | [urlAssessmentRequest](urlAssessmentRequest.md) | 通过发布**urlAssessmentRequest**对象创建新的 URL 评估请求。 |
| [获取 threatAssessmentRequest](../api/threatassessmentrequest-get.md) | [urlAssessmentRequest](urlassessmentrequest.md) | 读取**urlAssessmentRequest**对象的属性和关系。 |

## <a name="properties"></a>属性

| 属性     | 类型        | Description |
|:-------------|:------------|:------------|
|url|String|URL 字符串。|
|“类别”|[threatCategory](enums.md#threatcategory-values)|威胁类别。 可取值为：`spam`、`phishing`、`malware`。|
|contentType|[threatAssessmentContentType](enums.md#threatassessmentcontenttype-values)|威胁评估的内容类型。 可取值为：`mail`、`url`、`file`。|
|createdBy|[identitySet](identityset.md)|威胁评估请求创建程序。|
|createdDateTime|DateTimeOffset|时间戳类型表示采用 ISO 8601 格式的日期和时间信息，始终采用 UTC 时区。 例如，2014 年 1 月 1 日午夜 UTC 如下所示：`'2014-01-01T00:00:00Z'`。|
|expectedAssessment|[threatExpectedAssessment](enums.md#threatexpectedassessment-values)|来自 ubmitter 的预期评估。 可能的值是：`block`、`unblock`。|
|id|字符串|威胁评估请求 ID 是一个全局唯一标识符（GUID）。|
|requestSource|[threatAssessmentRequestSource](enums.md#threatassessmentrequestsource-values)|威胁评估请求的来源。 可取值为：`user`、`administrator`。|
|状态|[threatAssessmentStatus](enums.md#threatassessmentstatus-values)|评估过程状态。 可取值为：`pending`、`completed`。|

## <a name="relationships"></a>关系

| 关系 | 类型        | Description |
|:-------------|:------------|:------------|
|results|[threatAssessmentResult](threatassessmentresult.md)集合|威胁评估结果的集合。 只读。 默认情况下， `GET /threatAssessmentRequests/{id}` a 不会返回此属性，除非`$expand`您应用于该属性。|

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.urlAssessmentRequest",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "url": "String",
  "category": "String",
  "contentType": "String",
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "expectedAssessment": "String",
  "id": "String (identifier)",
  "requestSource": "String",
  "status": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "urlAssessmentRequest resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->