---
title: edgeKioskModeRestrictionType 枚举类型
description: 根据展台模式指定 Microsoft Edge 设置的限制方式。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: enumPageType
ms.openlocfilehash: a5fecf749b7aacef1c9eb0c465889f37e080ddb3
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49199117"
---
# <a name="edgekioskmoderestrictiontype-enum-type"></a>edgeKioskModeRestrictionType 枚举类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

根据展台模式指定 Microsoft Edge 设置的限制方式。

## <a name="members"></a>成员
|成员|值|说明|
|:---|:---|:---|
|notConfigured|0|未 (不受限制的) 配置。|
|digitalSignage|1|单应用模式中的交互/数字告示。|
|normalMode|双面|正常模式 (Microsoft Edge) 的完整版本。|
|publicBrowsingSingleApp|第三章|单应用模式中的公共浏览。|
|publicBrowsingMultiApp|4 |在多应用模式下，公共浏览 (inPrivate) 。|




