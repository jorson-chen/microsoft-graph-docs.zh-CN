---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: c1f0ae3ccc1f91ede8583a7e291a231424159793
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/20/2020
ms.locfileid: "48617127"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me/drive/items/{id}/workbook/worksheets/Sheet1/range(address='$A$1')/format/font"]]];
[urlRequest setHTTPMethod:@"PATCH"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphWorkbookRangeFont *workbookRangeFont = [[MSGraphWorkbookRangeFont alloc] init];
[workbookRangeFont setBold: true];
[workbookRangeFont setColor:@"#4B180E"];
[workbookRangeFont setSize: 26];

NSError *error;
NSData *workbookRangeFontData = [workbookRangeFont getSerializedDataWithError:&error];
[urlRequest setHTTPBody:workbookRangeFontData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```