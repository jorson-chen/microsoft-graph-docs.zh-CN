---
title: 更新 educationRubric
description: 更新 educationRubric 对象的属性。
localization_priority: Normal
author: dipakboyed
ms.prod: education
doc_type: apiPageType
ms.openlocfilehash: 17e2ff0f96706c50095a5620b6e729ace157c0c8
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2020
ms.locfileid: "48965971"
---
# <a name="update-educationrubric"></a>更新 educationRubric

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

更新 [educationRubric](../resources/educationrubric.md) 对象的属性。

仅在发布工作分配之前 () 更新附加到工作分配的 rubric `PATCH /education/me/assignments/{id}/rubric` ，而更新的内容实际上是中存在的原始 rubric `/education/users/{id}/rubrics` 。 发布工作分配后，将创建一个 rubric 的不可变副本，该副本将附加到该特定工作分配。 可以使用 [GET/education/me/assignments/{id}/rubric](educationrubric-get.md)检索 rubric，但不能对其进行更新。

## <a name="permissions"></a>权限

要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。

| 权限类型                        | 权限（从最低特权到最高特权） |
|:---------------------------------------|:--------------------------------------------|
| 委派（工作或学校帐户）     | EduAssignments、ReadWriteBasic、EduAssignments |
| 委派（个人 Microsoft 帐户） | 不支持。 |
| 应用程序                            | 不支持。 |

## <a name="http-request"></a>HTTP 请求

<!-- { "blockType": "ignored" } -->

```http
PATCH /education/me/rubrics/{id}
PATCH /education/me/assignments/{id}/rubric
```

## <a name="request-headers"></a>请求标头

| 名称       | 说明|
|:-----------|:-----------|
| Authorization | 持有者 {token} |

## <a name="request-body"></a>请求正文

在请求正文中，提供应更新的相关字段的值。 请求正文中不包括的现有属性将保留其以前的值，或根据对其他属性值的更改重新计算。 为了获得最佳性能，请勿加入尚未更改的现有值。

| 属性     | 类型        | 说明 |
|:-------------|:------------|:------------|
|说明|itemBody|此 rubric 的说明。|
|displayName|String|此 rubric 的名称。|
|评分|educationAssignmentGradeType|此 rubric 是否有积分。|
|等级|rubricLevel 集合|构成此 rubric 的级别的集合。|
|特质|rubricQuality 集合|构成此 rubric 的质量的集合。|

## <a name="response"></a>响应

如果成功，此方法 `200 OK` 在响应正文中返回响应代码和更新的 [educationRubric](../resources/educationrubric.md) 对象。

## <a name="examples"></a>示例

### <a name="request"></a>请求

下面展示了示例请求。

# <a name="http"></a>[HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "update_educationrubric"
}-->

```http
PATCH https://graph.microsoft.com/beta/education/me/rubrics/{id}
Content-type: application/json

{
  "displayName": "Example Credit Rubric after display name patch"
}
```
# <a name="c"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/update-educationrubric-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/update-educationrubric-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/update-educationrubric-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/update-educationrubric-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


### <a name="response"></a>响应

下面展示了示例响应。

> **注意：** 为了提高可读性，可能缩短了此处显示的响应对象。所有属性都将通过实际调用返回。

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationRubric"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "displayName": "Example Credit Rubric after display name patch",
    "id": "c4459fcb-a761-4f70-ac5b-e9466cb77c2a",
    "description": {
        "content": "This is an example of a credit rubric (no points)",
        "contentType": "text"
    },
    "levels": [
        {
            "levelId": "dec665d4-cf1b-4481-ac61-1d5b6188f4f5",
            "displayName": "Good",
            "description": {
                "content": "",
                "contentType": "text"
            }
        },
        {
            "levelId": "3f2e4b0f-508e-4005-984b-17e061bc5377",
            "displayName": "Poor",
            "description": {
                "content": "",
                "contentType": "text"
            }
        }
    ],
    "qualities": [
        {
            "qualityId": "dc79dcbf-b536-4797-9c5b-902f28129fd0",
            "description": {
                "content": "Argument",
                "contentType": "text"
            },
            "criteria": [
                {
                    "id": "8937fa15-4a7c-4f27-bd01-ca3471d2d1d5",
                    "description": {
                        "content": "The essay's argument is persuasive.",
                        "contentType": "text"
                    }
                },
                {
                    "id": "4dfb5263-1d3f-4f0a-93ef-d24d800d0f69",
                    "description": {
                        "content": "The essay's argument does not make sense.",
                        "contentType": "text"
                    }
                }
            ]
        },
        {
            "qualityId": "7e087062-ac25-4629-8386-a946350936db",
            "description": {
                "content": "Spelling and Grammar",
                "contentType": "text"
            },
            "criteria": [
                {
                    "id": "12276eb2-122c-4ad2-ba92-335ea798c88e",
                    "description": {
                        "content": "The essay uses proper spelling and grammar with few or no errors.",
                        "contentType": "text"
                    }
                },
                {
                    "id": "3db7e6b2-2b1b-4f8e-9fca-bea701159145",
                    "description": {
                        "content": "The essay has numerous errors in spelling and/or grammar.",
                        "contentType": "text"
                    }
                }
            ]
        }
    ]
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update educationrubric",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


