---
title: onPremEncryptedPayload 资源类型
description: 尚未记录
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 9bd49e99cfa9c5d6e17bdd77c713312d241f5f3c
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49259226"
---
# <a name="onpremencryptedpayload-resource-type"></a>onPremEncryptedPayload 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

尚未记录

## <a name="methods"></a>方法
|方法|返回类型|说明|
|:---|:---|:---|
|[列出 onPremEncryptedPayloads](../api/intune-raimportcerts-onpremencryptedpayload-list.md)|[onPremEncryptedPayload](../resources/intune-raimportcerts-onpremencryptedpayload.md) 集合|列出 [onPremEncryptedPayload](../resources/intune-raimportcerts-onpremencryptedpayload.md) 对象的属性和关系。|
|[获取 onPremEncryptedPayload](../api/intune-raimportcerts-onpremencryptedpayload-get.md)|[onPremEncryptedPayload](../resources/intune-raimportcerts-onpremencryptedpayload.md)|读取 [onPremEncryptedPayload](../resources/intune-raimportcerts-onpremencryptedpayload.md) 对象的属性和关系。|
|[创建 onPremEncryptedPayload](../api/intune-raimportcerts-onpremencryptedpayload-create.md)|[onPremEncryptedPayload](../resources/intune-raimportcerts-onpremencryptedpayload.md)|创建新的 [onPremEncryptedPayload](../resources/intune-raimportcerts-onpremencryptedpayload.md) 对象。|
|[删除 onPremEncryptedPayload](../api/intune-raimportcerts-onpremencryptedpayload-delete.md)|无|删除 [onPremEncryptedPayload](../resources/intune-raimportcerts-onpremencryptedpayload.md)。|
|[更新 onPremEncryptedPayload](../api/intune-raimportcerts-onpremencryptedpayload-update.md)|[onPremEncryptedPayload](../resources/intune-raimportcerts-onpremencryptedpayload.md)|更新 [onPremEncryptedPayload](../resources/intune-raimportcerts-onpremencryptedpayload.md) 对象的属性。|

## <a name="properties"></a>属性
|属性|类型|描述|
|:---|:---|:---|
|tenantId|Guid|尚未记录|
|userId|Guid|尚未记录|
|deviceId|Guid|尚未记录|
|payloadId|Guid|尚未记录|
|deviceKeyThumbprint|String|尚未记录|
|cert1PayloadUUID|String|尚未记录|
|cert2PayloadUUID|String|尚未记录|
|cert3PayloadUUID|String|尚未记录|
|plistTemplate|String|尚未记录|
|encryptedBlob|Binary|尚未记录|
|payloadVersion|Int32|尚未记录|
|status|Int32|尚未记录|
|createdTime|DateTimeOffset|尚未记录|
|lastModifiedTime|DateTimeOffset|尚未记录|
|eTag|String|尚未记录|
|isDeleted|Boolean|尚未记录|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.onPremEncryptedPayload"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.onPremEncryptedPayload",
  "tenantId": "Guid",
  "userId": "Guid",
  "deviceId": "Guid",
  "payloadId": "Guid",
  "deviceKeyThumbprint": "String",
  "cert1PayloadUUID": "String",
  "cert2PayloadUUID": "String",
  "cert3PayloadUUID": "String",
  "plistTemplate": "String",
  "encryptedBlob": "binary",
  "payloadVersion": 1024,
  "status": 1024,
  "createdTime": "String (timestamp)",
  "lastModifiedTime": "String (timestamp)",
  "eTag": "String",
  "isDeleted": true
}
```




