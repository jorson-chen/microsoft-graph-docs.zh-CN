---
title: macOSFileVaultRecoveryKeyTypes 枚举类型
description: MacOS FileVault 的恢复密钥类型
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: enumPageType
ms.openlocfilehash: 931e04d687590312a015ecc4e6f2e40f0e4dca10
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49279946"
---
# <a name="macosfilevaultrecoverykeytypes-enum-type"></a>macOSFileVaultRecoveryKeyTypes 枚举类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

MacOS FileVault 的恢复密钥类型

## <a name="members"></a>成员
|成员|值|说明|
|:---|:---|:---|
|notConfigured|0|设备默认值，无意向。|
|institutionalRecoveryKey|1|机构恢复密钥类似于 "主" 恢复密钥，可用于解锁已丢失密码的任何设备。|
|personalRecoveryKey|双面|个人恢复密钥是唯一的代码，可用于解锁用户的设备，即使设备的密码丢失也是如此。|




