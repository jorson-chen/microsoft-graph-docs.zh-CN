---
title: appLockerApplicationControlType 枚举类型
description: AppLocker 应用程序控件类型的可能值
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: enumPageType
ms.openlocfilehash: e34472e8f534f78167d57309bd7315102bf8a3b2
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48051093"
---
# <a name="applockerapplicationcontroltype-enum-type"></a>appLockerApplicationControlType 枚举类型

命名空间：microsoft.graph

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的[活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

AppLocker 应用程序控件类型的可能值

## <a name="members"></a>成员
|成员|值|说明|
|:---|:---|:---|
|notConfigured|0|设备默认值，未选择应用程序控件类型。|
|enforceComponentsAndStoreApps|1 |强制实施 Windows 组件和应用商店应用。|
|auditComponentsAndStoreApps|2 |审核 Windows 组件和存储应用程序。|
|enforceComponentsStoreAppsAndSmartlocker|第三章|强制实施 Windows 组件、存储应用和智能保险箱。|
|auditComponentsStoreAppsAndSmartlocker|4 |审核 Windows 组件、存储应用和智能保险箱。|









