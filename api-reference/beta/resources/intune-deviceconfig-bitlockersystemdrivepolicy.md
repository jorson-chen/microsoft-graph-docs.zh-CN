---
title: bitLockerSystemDrivePolicy 资源类型
description: BitLocker 加密基本策略。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 605236c0f1a1a1f5a4aea3554ff118aebaac15f7
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49260521"
---
# <a name="bitlockersystemdrivepolicy-resource-type"></a>bitLockerSystemDrivePolicy 资源类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

BitLocker 加密基本策略。

## <a name="properties"></a>属性
|属性|类型|描述|
|:---|:---|:---|
|encryptionMethod|[bitLockerEncryptionMethod](../resources/intune-deviceconfig-bitlockerencryptionmethod.md)|选择操作系统驱动器的加密方法。 可取值为：`aesCbc128`、`aesCbc256`、`xtsAes128`、`xtsAes256`。|
|startupAuthenticationRequired|Boolean|启动时需要其他身份验证。|
|startupAuthenticationBlockWithoutTpmChip|Boolean|指示是否允许没有兼容的 TPM (的 BitLocker 在 USB 闪存驱动器) 上需要密码或启动密钥。|
|startupAuthenticationTpmUsage|[configurationUsage](../resources/intune-deviceconfig-configurationusage.md)|指示是否允许或不允许 TPM 启动。 可取值为：`blocked`、`required`、`allowed`、`notConfigured`。|
|startupAuthenticationTpmPinUsage|[configurationUsage](../resources/intune-deviceconfig-configurationusage.md)|指示是否允许或不允许 TPM 启动 pin。 可取值为：`blocked`、`required`、`allowed`、`notConfigured`。|
|startupAuthenticationTpmKeyUsage|[configurationUsage](../resources/intune-deviceconfig-configurationusage.md)|指示是否允许或不允许 TPM 启动密钥。 可取值为：`blocked`、`required`、`allowed`、`notConfigured`。|
|startupAuthenticationTpmPinAndKeyUsage|[configurationUsage](../resources/intune-deviceconfig-configurationusage.md)|指示是否允许/不允许使用 TPM 启动 pin 密钥和密钥。 可取值为：`blocked`、`required`、`allowed`、`notConfigured`。|
|minimumPinLength|Int32|指示启动 pin 的最小长度。 有效值为4至20|
|recoveryOptions|[bitLockerRecoveryOptions](../resources/intune-deviceconfig-bitlockerrecoveryoptions.md)|允许在缺少所需的启动密钥信息时恢复 BitLocker 加密的操作系统驱动器。 启用 BitLocker 时，将应用此策略设置。|
|prebootRecoveryEnableMessageAndUrl|Boolean|启用预引导恢复消息和 Url。 如果 requireStartupAuthentication 为 false，则此值不起作用。|
|prebootRecoveryMessage|String|定义自定义恢复消息。|
|prebootRecoveryUrl|String|定义自定义恢复 URL。|

## <a name="relationships"></a>关系
无

## <a name="json-representation"></a>JSON 表示形式
下面是资源的 JSON 表示形式。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.bitLockerSystemDrivePolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.bitLockerSystemDrivePolicy",
  "encryptionMethod": "String",
  "startupAuthenticationRequired": true,
  "startupAuthenticationBlockWithoutTpmChip": true,
  "startupAuthenticationTpmUsage": "String",
  "startupAuthenticationTpmPinUsage": "String",
  "startupAuthenticationTpmKeyUsage": "String",
  "startupAuthenticationTpmPinAndKeyUsage": "String",
  "minimumPinLength": 1024,
  "recoveryOptions": {
    "@odata.type": "microsoft.graph.bitLockerRecoveryOptions",
    "blockDataRecoveryAgent": true,
    "recoveryPasswordUsage": "String",
    "recoveryKeyUsage": "String",
    "hideRecoveryOptions": true,
    "enableRecoveryInformationSaveToStore": true,
    "recoveryInformationToStore": "String",
    "enableBitLockerAfterRecoveryInformationToStore": true
  },
  "prebootRecoveryEnableMessageAndUrl": true,
  "prebootRecoveryMessage": "String",
  "prebootRecoveryUrl": "String"
}
```




