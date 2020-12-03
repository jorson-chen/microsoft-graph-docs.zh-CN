---
title: advancedBitLockerState 枚举类型
description: 高级 BitLocker 状态
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: enumPageType
ms.openlocfilehash: 5e68f3b608548b5dfd8eb942799a64a4147b6467
ms.sourcegitcommit: 9f88b7e41a4a4a4d5f52bd995ce07c6f702bd5d6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/01/2020
ms.locfileid: "49522774"
---
# <a name="advancedbitlockerstate-enum-type"></a>advancedBitLockerState 枚举类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

高级 BitLocker 状态

## <a name="members"></a>成员
|成员|值|说明|
|:---|:---|:---|
|success|0|高级 BitLocker 状态成功|
|noUserConsent|1 |用户永远不同意加密|
|osVolumeUnprotected|2 |检测到未受保护的 OS 卷|
|osVolumeTpmRequired|4 |TPM 不用于保护 OS 卷，但策略是必需的|
|osVolumeTpmOnlyRequired|8 |仅 TPM 保护未用于 OS 卷，但策略是必需的|
|osVolumeTpmPinRequired|16 |TPM + PIN 保护不用于 OS 卷，但策略要求|
|osVolumeTpmStartupKeyRequired|32|TPM + 启动密钥保护不用于 OS 卷，但策略要求|
|osVolumeTpmPinStartupKeyRequired|64|TPM + PIN + 启动密钥不用于 OS 卷，但策略是必需的|
|osVolumeEncryptionMethodMismatch|128|OS 卷的加密方法与策略设置的不同|
|recoveryKeyBackupFailed|256|恢复密钥备份失败|
|fixedDriveNotEncrypted|512|固定驱动器未加密|
|fixedDriveEncryptionMethodMismatch|1024|固定驱动器的加密方法与策略设置不同|
|loggedOnUserNonAdmin|2048|登录用户是非管理员的。这需要将 "AllowStandardUserEncryption" 策略设置为1|
|windowsRecoveryEnvironmentNotConfigured|4096|未配置 WinRE|
|tpmNotAvailable|8192|TPM 对 BitLocker 不可用。 这意味着 TPM 不存在，或者设置了 TPM 不可用注册表替代，或者主机 OS 位于便携/罗马盘上|
|tpmNotReady|16384|TPM 尚未准备好用于 BitLocker|
|networkError|32768|网络不可用。 这是恢复密钥备份所必需的。 此报告适用于支持驱动器加密的设备|




