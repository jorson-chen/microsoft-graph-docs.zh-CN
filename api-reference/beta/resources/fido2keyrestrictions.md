---
title: fido2KeyRestrictions 资源类型
description: 表示作为 FIDO2 安全密钥身份验证方法策略的一部分强制实施的主要限制。
author: mmcla
localization_priority: Normal
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: c606b1d7bdbf604bd5109379bffb2c1a20f60730
ms.sourcegitcommit: cfadc605014265e02b913bc77382025b0d156285
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "48418196"
---
# <a name="fido2keyrestrictions-resource-type"></a>fido2KeyRestrictions 资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

表示作为 [FIDO2 安全密钥身份验证方法策略](../resources/fido2authenticationmethodconfiguration.md)的一部分强制实施的主要限制。

## <a name="properties"></a>属性
|属性|类型|说明|
|:---|:---|:---|
|aaGuids|字符串集合|身份验证器证明 Guid 的集合。 AADGUIDs 定义密钥类型和制造商。|
|enforcementType|fido2RestrictionEnforcementType|强制类型。 可取值为：`allow`、`block`。|
|isEnforced|布尔|确定是否启用配置的键强制。|

## <a name="relationships"></a>关系
无。

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.fido2KeyRestrictions"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.fido2KeyRestrictions",
  "isEnforced": "Boolean",
  "enforcementType": "String",
  "aaGuids": [
    "String"
  ]
}
```
