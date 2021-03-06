---
author: JeremyKelley
ms.author: jeremyke
title: 获取捆绑包
description: 获取 Driveitem 的捆绑包
localization_priority: Normal
ms.prod: sharepoint
doc_type: apiPageType
ms.openlocfilehash: f9deca81a99d36e91247ddd042fc875d0ffc1cad
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2020
ms.locfileid: "48960293"
---
# <a name="get-bundle"></a>获取捆绑包

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

根据捆绑包的唯一 ID 检索 [捆绑][] 的元数据。

## <a name="permissions"></a>权限

要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。

|权限类型      | 权限（从最低特权到最高特权）              |
|:--------------------|:---------------------------------------------------------|
|委派（工作或学校帐户） | 不支持。                             |
|委派（个人 Microsoft 帐户） | Files.Read、Files.ReadWrite、Files.Read.All、Files.ReadWrite.All    |
|应用程序          | 不支持。                                           |

## <a name="http-request"></a>HTTP 请求

```http
GET /drive/bundles/{bundle-id}
GET /drive/items/{bundle-id}
```

由于捆绑包是项，因此可以使用 **items** 集合返回有关捆绑包的元数据。
你也可以使用 **捆绑包** 集合来确保你在响应时获得捆绑包。

## <a name="optional-query-parameters"></a>可选的查询参数

可以使用 [OData查询参数][odata-parameters]限制通过此调用返回的对象的形状。

## <a name="request-headers"></a>请求标头
| 名称          | 说明  |
|:------------- |:------------ |
| Authorization | 持有者 \{token\}。 必需。 |
| if-none-match | eTag. 可选。 如果包含此请求标头，且提供的 eTag（或 cTag）与文件中的当前标记不匹配，则返回 `HTTP 304 Not Modified` 响应。

## <a name="request-body"></a>请求正文

请勿为此方法提供请求正文。

## <a name="response"></a>响应

如果成功，此方法[driveItem][driveItem] resource with the [bundle][bundle] 在响应正文中返回 driveItem。

阅读 " [错误响应][error-response] " 主题，了解有关如何返回错误的详细信息。

## <a name="examples"></a>示例

### <a name="example-1-get-a-bundle"></a>示例1：获取捆绑包

#### <a name="request"></a>请求


# <a name="http"></a>[HTTP](#tab/http)
<!-- { "blockType": "request", "name": "get-bundle-metadata" } -->

```msgraph-interactive
GET https://graph.microsoft.com/beta/drive/bundles/{bundle-id}
```
# <a name="c"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-bundle-metadata-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-bundle-metadata-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-bundle-metadata-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/get-bundle-metadata-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


#### <a name="response"></a>响应

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "truncated": true } -->

```json
HTTP/1.1 200 OK
Content-type: application/json

{
  "id": "0123456789abc",
  "name": "My Photo Album Bundle",
  "eTag": "etag",
  "cTag": "etag",
  "createdBy": { "user": { "id": "1234", "displayName": "Ryan Gregg" } },
  "createdDateTime": "datetime",
  "lastModifiedBy": { "user": { "id": "1234", "displayName": "Ryan Gregg" } },
  "lastModifiedDateTime": "datetime",
  "size": 1234,
  "webUrl": "http://onedrive.com/...",
  "bundle": {
    "childCount": 4,
     "album": { }
  }
}
```

为了提高可读性，可能缩短了此处显示的响应对象。 所有属性都是从实际调用返回。

### <a name="example-2-get-a-bundle-and-its-children-in-a-single-call"></a>示例2：在单个调用中获取捆绑包及其子项

您可以使用 [`expand`](/graph/query-parameters) 查询字符串参数在与检索捆绑的元数据的相同调用中添加捆绑包的子项。

#### <a name="request"></a>请求


# <a name="http"></a>[HTTP](#tab/http)
<!-- { "blockType": "request", "name": "get-bundle-and-children" } -->

```msgraph-interactive
GET https://graph.microsoft.com/beta/drive/items/{bundle-id}?expand=children
```
# <a name="c"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-bundle-and-children-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-bundle-and-children-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-bundle-and-children-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/get-bundle-and-children-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


#### <a name="response"></a>响应

此调用将返回捆绑包元数据和捆绑的子项列表。
如果捆绑包没有任何子级，则将返回一个空集合。

如果捆绑包中的子项数量大于默认页面大小，则将使用可用于请求捆绑中的下一页子页面的 URL 返回 **children@odata 的 nextLink** 属性。

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "truncated": true } -->

```json
HTTP/1.1 200 OK
Content-Type: application/json

{
  "id": "101230100alkc",
  "name": "My Cool Day at the Beach",
  "children": [
    { "id": "120100abab", "name": "image1.jpg", "file": {} },
    { "id": "120100abo1", "name": "image2.jpg", "file": {} }
  ],
  "children@odata.nextLink": "https://api.onedrive.com/v1.0/..."
}
```

为了提高可读性，可能缩短了此处显示的响应对象。 所有属性都是从实际调用返回。


[bundle]: ../resources/bundle.md
[driveItem]: ../resources/driveItem.md
[error-response]: /graph/errors
[odata-parameters]: /graph/query-parameters


<!-- {
  "type": "#page.annotation",
  "description": "Retrieve metadata about a bundle and its children in OneDrive",
  "keywords": "retrieve,item,bundle,metadata",
  "section": "documentation",
  "tocPath": "Bundles/Get Bundle Metadata"
} -->


