---
title: browserSyncSetting 枚举类型
description: 允许未配置 () 或阻止 (阻止) Microsoft Edge 浏览器设置的同步。 选项可阻止跨设备同步，但允许用户重写。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: enumPageType
ms.openlocfilehash: 74803f708fdf9f66c7b903c22cecf23cb06ae8dc
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49260500"
---
# <a name="browsersyncsetting-enum-type"></a>browserSyncSetting 枚举类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

允许未配置 () 或阻止 (阻止) Microsoft Edge 浏览器设置的同步。 选项可阻止跨设备同步，但允许用户重写。

## <a name="members"></a>成员
|成员|值|说明|
|:---|:---|:---|
|notConfigured|0|默认值–允许跨设备同步浏览器设置。|
|blockedWithUserOverride|1|阻止跨用户设备同步浏览器设置，允许用户重写设置。|
|堵塞|双面|绝对阻止跨用户设备同步浏览器设置。|




