---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: a871d9bf837fea7a8c17b0714173a76b15dbf0c6
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/20/2020
ms.locfileid: "48619647"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/planner/plans/xqQg5FS2LkCp935s-FIFm2QAFkHM/details"]]];
[urlRequest setHTTPMethod:@"PATCH"];
[urlRequest setValue:@"W/\"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc=\"" forHTTPHeaderField:@"If-Match"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphPlannerPlanDetails *plannerPlanDetails = [[MSGraphPlannerPlanDetails alloc] init];
MSGraphPlannerUserIds *sharedWith = [[MSGraphPlannerUserIds alloc] init];
[sharedWith set6463a5ce-2119-4198-9f2a-628761df4a62: true];
[sharedWith setD95e6152-f683-4d78-9ff5-67ad180fea4a: false];
[plannerPlanDetails setSharedWith:sharedWith];
MSGraphPlannerCategoryDescriptions *categoryDescriptions = [[MSGraphPlannerCategoryDescriptions alloc] init];
[categoryDescriptions setCategory1:@"Indoors"];
[categoryDescriptions setCategory3: null];
[plannerPlanDetails setCategoryDescriptions:categoryDescriptions];

NSError *error;
NSData *plannerPlanDetailsData = [plannerPlanDetails getSerializedDataWithError:&error];
[urlRequest setHTTPBody:plannerPlanDetailsData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```