---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 6def86f3d0bb6ceee681b5a40d590c6f316cdf6d
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2020
ms.locfileid: "48956936"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

ContinuousAccessEvaluationPolicy continuousAccessEvaluationPolicy = new ContinuousAccessEvaluationPolicy();
LinkedList<String> usersList = new LinkedList<String>();
usersList.add("88139f01-1f8d-4c06-ad74-a2544cee9aee");
continuousAccessEvaluationPolicy.users = usersList;
LinkedList<String> groupsList = new LinkedList<String>();
groupsList.add("9972fb3f-7a40-49f5-85f6-129d9dfbd47a");
groupsList.add("ea178055-4713-4d9a-a06c-ff17466b7e77");
continuousAccessEvaluationPolicy.groups = groupsList;

graphClient.identity().continuousAccessEvaluationPolicy()
    .buildRequest()
    .patch(continuousAccessEvaluationPolicy);

```