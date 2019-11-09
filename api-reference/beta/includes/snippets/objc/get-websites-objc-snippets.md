---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 1a89ad157aa4ffc8826519d27cfda0fe63f188e1
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/05/2019
ms.locfileid: "37997872"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me/profile/websites"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *personWebsiteList = [[NSMutableArray alloc] init];
        personWebsiteList = [jsonFinal valueForKey:@"value"];
        MSGraphPersonWebsite *personWebsite = [[MSGraphPersonWebsite alloc] initWithDictionary:[personWebsiteList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```