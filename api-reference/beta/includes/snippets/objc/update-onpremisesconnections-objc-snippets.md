---
description: 自动生成文件。 请不要修改
ms.openlocfilehash: 4c5a6940e44a5e20b8f51ccc7a0fa0348e8a64d0
ms.sourcegitcommit: 9f88b7e41a4a4a4d5f52bd995ce07c6f702bd5d6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/01/2020
ms.locfileid: "49521605"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/deviceManagement/virtualEndpoint/onPremisesConnections/{id}"]]];
[urlRequest setHTTPMethod:@"PATCH"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphCloudPcOnPremisesConnection *cloudPcOnPremisesConnection = [[MSGraphCloudPcOnPremisesConnection alloc] init];
[cloudPcOnPremisesConnection setDisplayName:@"Display Name value"];
[cloudPcOnPremisesConnection setSubscriptionId:@"0ac520ee-14c0-480f-b6c9-0a90c585ffff"];
[cloudPcOnPremisesConnection setSubscriptionName:@"Subscription Name value"];
[cloudPcOnPremisesConnection setAdDomainName:@"Active Directory Domain Name value"];
[cloudPcOnPremisesConnection setAdDomainUsername:@"Active Directory Domain User Name value"];
[cloudPcOnPremisesConnection setOrganizationalUnit:@"Organization Unit value"];
[cloudPcOnPremisesConnection setResourceGroupId:@"/subscriptions/0ac520ee-14c0-480f-b6c9-0a90c585ffff/resourceGroups/ExampleRG"];
[cloudPcOnPremisesConnection setVirtualNetworkId:@"/subscriptions/0ac520ee-14c0-480f-b6c9-0a90c58ffff/resourceGroups/ExampleRG/providers/Microsoft.Network/virtualNetworks/ExampleVNet"];
[cloudPcOnPremisesConnection setSubnetId:@"/subscriptions/0ac520ee-14c0-480f-b6c9-0a90c585ffff/resourceGroups/ExampleRG/providers/Microsoft.Network/virtualNetworks/ExampleVNet/subnets/default"];

NSError *error;
NSData *cloudPcOnPremisesConnectionData = [cloudPcOnPremisesConnection getSerializedDataWithError:&error];
[urlRequest setHTTPBody:cloudPcOnPremisesConnectionData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```