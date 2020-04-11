---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 4e3e960bd572e309bfb987e425afe534c8e1276b
ms.sourcegitcommit: 11503211a31ea17f4e577c21ec36d364184c0580
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/08/2020
ms.locfileid: "43181160"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/roleManagement/directory/roleAssignments"]]];
[urlRequest setHTTPMethod:@"POST"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphUnifiedRoleAssignment *unifiedRoleAssignment = [[MSGraphUnifiedRoleAssignment alloc] init];
[unifiedRoleAssignment setRoleDefinitionId:@"fe930be7-5e62-47db-91af-98c3a49a38b1"];
[unifiedRoleAssignment setPrincipalId:@"f8ca5a85-489a-49a0-b555-0a6d81e56f0d"];
[unifiedRoleAssignment setDirectoryScopeId:@"5d107bba-d8e2-4e13-b6ae-884be90e5d1a"];

NSError *error;
NSData *unifiedRoleAssignmentData = [unifiedRoleAssignment getSerializedDataWithError:&error];
[urlRequest setHTTPBody:unifiedRoleAssignmentData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```