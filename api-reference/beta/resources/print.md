---
title: 打印资源类型
description: 当附带通用打印订阅时，打印功能启用打印机的管理和 printServiceEndpoints 的发现，可用于管理通用打印中的打印机和打印作业。
author: braedenp-msft
localization_priority: Normal
ms.prod: universal-print
doc_type: resourcePageType
ms.openlocfilehash: 309b7c8e62b94703bb00e21fb8c8ed2a2e917efe
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "47985886"
---
# <a name="print-resource-type"></a>打印资源类型

命名空间：microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

当附带通用打印订阅时，打印功能启用打印机的管理和 [printServiceEndpoints](printserviceendpoint.md) 的发现，可用于管理通用打印中的打印机和打印作业。

## <a name="methods"></a>方法
| 方法       | 返回类型 | 说明 |
|:-------------|:------------|:------------|
| [List connectors](../api/print-list-connectors.md) | [printConnector](printconnector.md) 集合 | 获取打印连接器的列表。 |
| [列出打印机](../api/print-list-printers.md) | [打印机](printer.md) 集合 | 获取打印机的列表。 |
| [列出共享项](../api/print-list-shares.md) | [printerShare](printershare.md) 集合 | 获取打印机共享的列表。 |
| [列出服务](../api/print-list-services.md) | [printService](printservice.md) 集合 | 获取服务的列表。 |
| [创建 printerShare](../api/print-post-shares.md) | [printerShare](printershare.md) | 通过发布到 **共享** 集合创建新的打印机共享。 |
| [创建打印机](../api/printer-create.md) | [printerCreateOperation](printerCreateOperation.md) | 创建 (注册) 具有通用打印的新打印机。 |
| [更新设置](../api/print-update-settings.md) |  [printSettings](printsettings.md) | 更新通用打印服务的租户范围设置。 |
| [List taskDefinitions](../api/print-list-taskdefinitions.md) | [printTaskDefinition](printtaskdefinition.md) 集合 | 获取在通用打印中创建的 printTaskDefinitions 的租户范围列表。 |
| [Create taskDefinition](../api/print-post-taskdefinitions.md) | [printTaskDefinition](printtaskdefinition.md) | 创建新的 printTaskDefinition。 |
| [Update taskDefinition](../api/print-update-taskdefinition.md) | [printTaskDefinition](printtaskdefinition.md) | 更新 printTaskDefinition。 |
| [Delete taskDefinition](../api/print-delete-taskdefinition.md) | 无 | 删除 printTaskDefinition。 |

## <a name="properties"></a>属性
| 属性     | 类型        | 说明 |
|:-------------|:------------|:------------|
|settings|[printSettings](printsettings.md)|通用打印服务的租户范围内的设置。|

## <a name="relationships"></a>关系
| 关系 | 类型        | 说明 |
|:-------------|:------------|:------------|
|服务行业|[printService](printservice.md) 集合|可用通用打印服务终结点的列表。|
|台|[打印机](printer.md) 集合|在租户中注册的打印机的列表。|
|shares|[printerShare](printershare.md) 集合|在租户中注册的打印机共享的列表。|
|插槽|[printConnector](printconnector.md) 集合|可用打印连接器的列表。|

## <a name="json-representation"></a>JSON 表示形式

下面是资源的 JSON 表示形式。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.print",
  "keyProperty": "settings"
}-->

```json
{
  "settings": {"@odata.type": "microsoft.graph.printSettings"}
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "print resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [ 
    "Error: Resource print has documented navigation properties, but we thought it was a complex type!",
    "Resource print has documented navigation properties, but we thought it was a complex type!"
}-->


