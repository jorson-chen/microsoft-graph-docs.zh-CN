---
title: 'informationProtectionLabel: evaluateRemoval'
description: 评估要删除的标签以及如何根据现有内容信息将其删除。
localization_priority: Normal
author: tommoser
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: ca1a27b30152debe51add8f0b418d3983c13b746
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/05/2019
ms.locfileid: "37995933"
---
# <a name="informationprotectionlabel-evaluateremoval"></a>informationProtectionLabel: evaluateRemoval

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

向正在使用的应用程序指示删除标签信息应采取的操作。

给定[contentInfo](../resources/contentinfo.md)作为输入（其中包括现有的内容元数据[密钥/值对](../resources/keyvaluepair.md)），API 将返回一个[informationProtectionAction](../resources/informationprotectionaction.md) ，其中包含以下一个或多个部分的组合： 

* [justifyAction](../resources/justifyaction.md)
* [metadataAction](../resources/metadataaction.md)
* [removeContentFooterAction](../resources/removecontentfooteraction.md)
* [removeContentHeaderAction](../resources/removecontentheaderaction.md)
* [removeProtectionAction](../resources/removeprotectionaction.md)
* [removeWatermarkAction](../resources/removewatermarkaction.md)

## <a name="permissions"></a>权限

要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。

| 权限类型                        | 权限（从最低特权到最高特权） |
| :------------------------------------- | :------------------------------------------ |
| 委派（工作或学校帐户）     | InformationProtectionPolicy。请阅读            |
| 委派（个人 Microsoft 帐户） | 不支持。                              |
| 应用程序                            | InformationProtectionPolicy        |

## <a name="http-request"></a>HTTP 请求

<!-- { "blockType": "ignored" } -->

```http
POST /informationprotection/policy/labels/evaluateRemoval
```

## <a name="request-headers"></a>请求标头

| 名称          | 说明                 |
| :------------ | :-------------------------- |
| Authorization | Bearer {token}。必需。   |
| Content-type  | application/json. Required. |

## <a name="request-body"></a>请求正文

在请求正文中，提供具有以下参数的 JSON 对象。

| 参数              | 类型                                                             | 说明                                                                                                                                                                                                   |
| :--------------------- | :--------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| contentInfo            | [contentInfo](../resources/contentinfo.md)                       | 提供有关内容格式、内容状态和现有[元数据](../resources/keyvaluepair.md)的详细信息，作为键/值对。 |
| downgradeJustification | [downgradeJustification](../resources/downgradejustification.md) | 必须由用户或应用程序逻辑提供的理由。                                                                                                                                         |


## <a name="response"></a>响应

如果成功，此方法在响应`200 OK`正文中返回响应代码和新的[informationProtectionAction](../resources/informationprotectionaction.md)集合对象。 [InformationProtectionAction 对象](../resources/informationprotectionaction.md)将包含一个[metadataAction](../resources/metadataaction.md)对象，该对象通知应用程序要删除的元数据。 

## <a name="examples"></a>示例

下面是一个如何调用此 API 的示例。

### <a name="request"></a>请求

下面展示了示例请求。

# <a name="httptabhttp"></a>[HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "informationprotectionlabel_evaluateremoval"
}-->

```http
POST https://graph.microsoft.com/beta/informationprotection/policy/labels/evaluateRemoval
Content-type: application/json

{
  "contentInfo": {
    "@odata.type": "#microsoft.graph.contentInfo",
    "format@odata.type": "#microsoft.graph.contentFormat",
    "format": "default",
    "identifier": null,
    "state@odata.type": "#microsoft.graph.contentState",
    "state": "rest",
    "metadata@odata.type": "#Collection(microsoft.graph.keyValuePair)",
    "metadata": [
      {
        "@odata.type": "#microsoft.graph.keyValuePair",
        "name": "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Enabled",
        "value": "True"
      },
      {
        "@odata.type": "#microsoft.graph.keyValuePair",
        "name": "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Method",
        "value": "Standard"
      },
      {
        "@odata.type": "#microsoft.graph.keyValuePair",
        "name": "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_SetDate",
        "value": "1/1/0001 12:00:00 AM"
      },
      {
        "@odata.type": "#microsoft.graph.keyValuePair",
        "name": "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_SiteId",
        "value": "cfa4cf1d-a337-4481-aa99-19d8f3d63f7c"
      },
      {
        "@odata.type": "#microsoft.graph.keyValuePair",
        "name": "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Name",
        "value": "General"
      },
      {
        "@odata.type": "#microsoft.graph.keyValuePair",
        "name": "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_ContentBits",
        "value": "0"
      },
      {
        "@odata.type": "#microsoft.graph.keyValuePair",
        "name": "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_ActionId",
        "value": "00000000-0000-0000-0000-000000000000"
      }
    ]
  },
  "downgradeJustification": {
        "justificationMessage": "The information has been declassified.",
        "isDowngradeJustified": true
    }
}
```
# <a name="ctabcsharp"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/informationprotectionlabel-evaluateremoval-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/informationprotectionlabel-evaluateremoval-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/informationprotectionlabel-evaluateremoval-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


### <a name="response"></a>响应

下面展示了示例响应。

> **注意：** 为了提高可读性，可能缩短了此处显示的响应对象。所有属性都将通过实际调用返回。

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.informationProtectionAction",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.informationProtectionAction)",
    "value": [
        {
            "@odata.type": "#microsoft.graph.metadataAction",
            "metadataToRemove": [
                "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Enabled",
                "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Method",
                "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_SetDate",
                "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_SiteId",
                "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Name",
                "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_ContentBits",
                "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_ActionId"
            ],
            "metadataToAdd": []
        }
    ]
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "informationProtectionLabel: evaluateRemoval",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->