---
title: macOSContentCachingPeerPolicy 枚举类型
description: 确定哪些内容缓存其他内容缓存将对等。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: enumPageType
ms.openlocfilehash: 7305c42098782d9e69e734037fb08d3238c7b4a9
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49268746"
---
# <a name="macoscontentcachingpeerpolicy-enum-type"></a>macOSContentCachingPeerPolicy 枚举类型

命名空间：microsoft.graph

> **重要说明：** /Beta 版本下的 Microsoft Graph Api 可能会发生更改;不支持生产使用。

> **注意：** 适用于 Intune 的 Microsoft Graph API 需要适用于租户的 [活动 Intune 许可证](https://go.microsoft.com/fwlink/?linkid=839381)。

确定哪些内容缓存其他内容缓存将对等。

## <a name="members"></a>成员
|成员|值|说明|
|:---|:---|:---|
|notConfigured|0|默认值为本地网络中的对等方。|
|peersInLocalNetwork|1|内容缓存将仅对其直接本地网络中的缓存具有同等的对等缓存。|
|peersWithSamePublicIpAddress|双面|内容缓存将仅对共享相同公用 IP 地址的缓存具有同等的对等缓存。|
|peersInCustomLocalNetworks|第三章|内容缓存将使用 contentCachingPeerFilterRanges 和 contentCachingPeerListenRanges 来确定与对等方的缓存。|




