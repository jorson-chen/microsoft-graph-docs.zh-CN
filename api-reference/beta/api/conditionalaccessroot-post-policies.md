---
title: 创建 conditionalAccessPolicy
description: 创建新的 conditionalAccessPolicy。
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: 161e9824b9018d0504d48bbefa15412364c24960
ms.sourcegitcommit: 3ee6a3a949be7f0a9028bde90092a10a42e0f1fc
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2019
ms.locfileid: "37638433"
---
# <a name="create-conditionalaccesspolicy"></a><span data-ttu-id="19c68-103">创建 conditionalAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="19c68-103">Create conditionalAccessPolicy</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="19c68-104">创建新的[conditionalAccessPolicy](../resources/conditionalaccesspolicy.md)。</span><span class="sxs-lookup"><span data-stu-id="19c68-104">Create a new [conditionalAccessPolicy](../resources/conditionalaccesspolicy.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="19c68-105">权限</span><span class="sxs-lookup"><span data-stu-id="19c68-105">Permissions</span></span>

<span data-ttu-id="19c68-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="19c68-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="19c68-108">权限类型</span><span class="sxs-lookup"><span data-stu-id="19c68-108">Permission type</span></span>                        | <span data-ttu-id="19c68-109">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="19c68-109">Permissions (from least to most privileged)</span></span>                    |
|:--------------------------------------|:---------------------------------------------------------------|
|<span data-ttu-id="19c68-110">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="19c68-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="19c68-111">ConditionalAccess 和 Directory.accessasuser.all 的所有</span><span class="sxs-lookup"><span data-stu-id="19c68-111">Policy.ReadWrite.ConditionalAccess and Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="19c68-112">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="19c68-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="19c68-113">不支持。</span><span class="sxs-lookup"><span data-stu-id="19c68-113">Not supported.</span></span> |
|<span data-ttu-id="19c68-114">应用程序</span><span class="sxs-lookup"><span data-stu-id="19c68-114">Application</span></span>                            | <span data-ttu-id="19c68-115">不支持。</span><span class="sxs-lookup"><span data-stu-id="19c68-115">Not supported.</span></span> |

>[!NOTE]
><span data-ttu-id="19c68-116">此 API 需要多个权限。</span><span class="sxs-lookup"><span data-stu-id="19c68-116">This API requires multiple permissions.</span></span> <span data-ttu-id="19c68-117">有关详细信息，请参阅[已知问题](/graph/known-issues#conditional-access-policies-and-named-locations)。</span><span class="sxs-lookup"><span data-stu-id="19c68-117">For details, see [Known issues](/graph/known-issues#conditional-access-policies-and-named-locations).</span></span>

## <a name="http-request"></a><span data-ttu-id="19c68-118">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="19c68-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /conditionalAccess/policies
```

## <a name="request-headers"></a><span data-ttu-id="19c68-119">请求标头</span><span class="sxs-lookup"><span data-stu-id="19c68-119">Request headers</span></span>

| <span data-ttu-id="19c68-120">名称</span><span class="sxs-lookup"><span data-stu-id="19c68-120">Name</span></span>          | <span data-ttu-id="19c68-121">说明</span><span class="sxs-lookup"><span data-stu-id="19c68-121">Description</span></span>      |
|:--------------|:-----------------|
| <span data-ttu-id="19c68-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="19c68-122">Authorization</span></span> | <span data-ttu-id="19c68-p103">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="19c68-p103">Bearer {token}. Required.</span></span>   |
| <span data-ttu-id="19c68-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="19c68-125">Content-Type</span></span>  | <span data-ttu-id="19c68-p104">application/json. Required.</span><span class="sxs-lookup"><span data-stu-id="19c68-p104">application/json. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="19c68-128">请求正文</span><span class="sxs-lookup"><span data-stu-id="19c68-128">Request body</span></span>

<span data-ttu-id="19c68-129">在请求正文中，提供[conditionalAccessPolicy](../resources/conditionalaccesspolicy.md)对象的 JSON 表示形式。</span><span class="sxs-lookup"><span data-stu-id="19c68-129">In the request body, supply a JSON representation of a [conditionalAccessPolicy](../resources/conditionalaccesspolicy.md) object.</span></span>

<span data-ttu-id="19c68-130">有效策略应包含至少一个[应用程序](../resources/conditionalaccessapplications.md) `'includeApplications': 'none'`规则，例如，一个[用户](../resources/conditionalaccessusers.md)规则，例如`'includeUsers': 'none'`，至少一个 "[授予](../resources/conditionalaccessgrantcontrols.md)/[会话](../resources/conditionalaccesssessioncontrols.md)" 控制。</span><span class="sxs-lookup"><span data-stu-id="19c68-130">A valid policy should contain at least one [application](../resources/conditionalaccessapplications.md) rule - for example, `'includeApplications': 'none'`, one [user](../resources/conditionalaccessusers.md) rule - for example, `'includeUsers': 'none'`, and at least one [grant](../resources/conditionalaccessgrantcontrols.md)/[session](../resources/conditionalaccesssessioncontrols.md) control.</span></span>

## <a name="response"></a><span data-ttu-id="19c68-131">响应</span><span class="sxs-lookup"><span data-stu-id="19c68-131">Response</span></span>

<span data-ttu-id="19c68-132">如果成功，此方法在响应`201 Created`正文中返回响应代码和新的[conditionalAccessPolicy](../resources/conditionalaccesspolicy.md)对象。</span><span class="sxs-lookup"><span data-stu-id="19c68-132">If successful, this method returns a `201 Created` response code and a new [conditionalAccessPolicy](../resources/conditionalaccesspolicy.md) object in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="19c68-133">示例</span><span class="sxs-lookup"><span data-stu-id="19c68-133">Examples</span></span>

### <a name="example-1-require-mfa-to-access-exchange-online-outside-of-trusted-locations"></a><span data-ttu-id="19c68-134">示例1：要求进行 MFA 以在受信任位置之外访问 Exchange Online</span><span class="sxs-lookup"><span data-stu-id="19c68-134">Example 1: Require MFA to access Exchange Online outside of trusted locations</span></span>

#### <a name="request"></a><span data-ttu-id="19c68-135">请求</span><span class="sxs-lookup"><span data-stu-id="19c68-135">Request</span></span>
<span data-ttu-id="19c68-136">下面的示例显示了要求对来自特定组的受信任位置之外的浏览器或新式 auth 客户端访问 Exchange Online 的多因素身份验证的常见请求。</span><span class="sxs-lookup"><span data-stu-id="19c68-136">The following example shows a common request to require multi-factor authentication for access to Exchange Online from a browser or modern auth client outside of trusted locations for a particular group.</span></span>

><span data-ttu-id="19c68-137">**注意：** 在使用此操作之前，您必须设置受信任位置。</span><span class="sxs-lookup"><span data-stu-id="19c68-137">**Note:** You must set up your trusted locations before using this operation.</span></span>

<!-- {
  "blockType": "request",
  "name": "create_conditionalaccesspolicy_from_conditionalaccessroot"
}-->

```http
POST https://graph.microsoft.com/beta/conditionalAccess/policies
Content-type: application/json

{
    "displayName": "Access to EXO requires MFA",
    "state": "enabled",
    "conditions": {
        "clientAppTypes": [
            "modern",
            "browser"
        ],
        "applications": {
            "includeApplications": [
                "00000002-0000-0ff1-ce00-000000000000"
            ]
        },
        "users": {
            "includeGroups": ["ba8e7ded-8b0f-4836-ba06-8ff1ecc5c8ba"],
        },
        "locations": {
            "includeLocations": [
                "All"
            ],
            "excludeLocations": [
                "AllTrusted"
            ]
        }
    },
    "grantControls": {
        "operator": "OR",
        "builtInControls": [
            "mfa"
        ]
    }
}
```

#### <a name="response"></a><span data-ttu-id="19c68-138">响应</span><span class="sxs-lookup"><span data-stu-id="19c68-138">Response</span></span>

<span data-ttu-id="19c68-139">下面是一个响应示例。</span><span class="sxs-lookup"><span data-stu-id="19c68-139">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.conditionalAccessPolicy"
} -->

```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#conditionalAccess/policies/$entity",
    "id": "7359d0e0-d8a9-4afa-8a93-e23e099d7be8",
    "displayName": "Access to EXO requires MFA",
    "createdDateTime": "2019-10-14T19:52:00.050958Z",
    "modifiedDateTime": null,
    "state": "enabled",
    "sessionControls": null,
    "conditions": {
        "signInRiskLevels": [],
        "clientAppTypes": [
            "modern",
            "browser"
        ],
        "platforms": null,
        "deviceStates": null,
        "applications": {
            "includeApplications": [
                "00000002-0000-0ff1-ce00-000000000000"
            ],
            "excludeApplications": [],
            "includeUserActions": []
        },
        "users": {
            "includeUsers": [],
            "excludeUsers": [],
            "includeGroups": [
                "ba8e7ded-8b0f-4836-ba06-8ff1ecc5c8ba"
            ],
            "excludeGroups": [],
            "includeRoles": [],
            "excludeRoles": []
        },
        "locations": {
            "includeLocations": [
                "All"
            ],
            "excludeLocations": [
                "AllTrusted"
            ]
        }
    },
    "grantControls": {
        "operator": "OR",
        "builtInControls": [
            "mfa"
        ],
        "customAuthenticationFactors": [],
        "termsOfUse": []
    }
}
```

### <a name="example-2-block-access-to-exchange-online-from-non-trusted-regions"></a><span data-ttu-id="19c68-140">示例2：阻止来自不受信任区域的 Exchange Online 的访问</span><span class="sxs-lookup"><span data-stu-id="19c68-140">Example 2: Block access to Exchange Online from non-trusted regions</span></span>

#### <a name="request"></a><span data-ttu-id="19c68-141">请求</span><span class="sxs-lookup"><span data-stu-id="19c68-141">Request</span></span>
<span data-ttu-id="19c68-142">下面的示例演示了一个阻止从非信任/未知区域访问 Exchange Online 的请求。</span><span class="sxs-lookup"><span data-stu-id="19c68-142">The following example shows a request to block access to Exchange Online from non-trusted/unknown regions.</span></span>
<span data-ttu-id="19c68-143">此示例假定 id 为 "198ad66e-87b3-4157-85a3-8a7b51794ee9" 的命名位置与 "不受信任/未知" 区域的列表相对应。</span><span class="sxs-lookup"><span data-stu-id="19c68-143">This example assumes that the named location with id = 198ad66e-87b3-4157-85a3-8a7b51794ee9 corresponds to a list of non-trusted/unknown regions.</span></span>

<!-- {
  "blockType": "request",
  "name": "create_conditionalaccesspolicy_from_conditionalaccessroot"
}-->

```http
POST https://graph.microsoft.com/beta/conditionalAccess/policies
Content-type: application/json

{
    "displayName": "Block access to EXO non-trusted regions.",
    "state": "enabled",
    "conditions": {
        "clientAppTypes": [
            "modern",
            "browser",
            "easSupported",
            "easUnsupported",
            "other"
        ],
        "applications": {
            "includeApplications": [
                "00000002-0000-0ff1-ce00-000000000000"
            ]
        },
        "users": {
            "includeGroups": ["ba8e7ded-8b0f-4836-ba06-8ff1ecc5c8ba"],
        },
        "locations": {
            "includeLocations": [
                "198ad66e-87b3-4157-85a3-8a7b51794ee9"
            ]
        }
    },
    "grantControls": {
        "operator": "OR",
        "builtInControls": [
            "block"
        ]
    }
}
```

#### <a name="response"></a><span data-ttu-id="19c68-144">响应</span><span class="sxs-lookup"><span data-stu-id="19c68-144">Response</span></span>

<span data-ttu-id="19c68-145">下面是一个响应示例。</span><span class="sxs-lookup"><span data-stu-id="19c68-145">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.conditionalAccessPolicy"
} -->

```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context": "https://canary.graph.microsoft.com/testprodbetaconditionalAccessBetaDocs/$metadata#conditionalAccess/policies/$entity",
    "id": "c98e6c3d-f6ca-42ea-a927-773b6f12a0c2",
    "displayName": "Block access to EXO non-trusted regions.",
    "createdDateTime": "2019-10-14T19:53:11.3705634Z",
    "modifiedDateTime": null,
    "state": "enabled",
    "sessionControls": null,
    "conditions": {
        "signInRiskLevels": [],
        "clientAppTypes": [
            "modern",
            "browser",
            "easSupported",
            "easUnsupported",
            "other"
        ],
        "platforms": null,
        "deviceStates": null,
        "applications": {
            "includeApplications": [
                "00000002-0000-0ff1-ce00-000000000000"
            ],
            "excludeApplications": [],
            "includeUserActions": []
        },
        "users": {
            "includeUsers": [],
            "excludeUsers": [],
            "includeGroups": [
                "ba8e7ded-8b0f-4836-ba06-8ff1ecc5c8ba"
            ],
            "excludeGroups": [],
            "includeRoles": [],
            "excludeRoles": []
        },
        "locations": {
            "includeLocations": [
                "198ad66e-87b3-4157-85a3-8a7b51794ee9"
            ],
            "excludeLocations": []
        }
    },
    "grantControls": {
        "operator": "OR",
        "builtInControls": [
            "block"
        ],
        "customAuthenticationFactors": [],
        "termsOfUse": []
    }
}
```

### <a name="example-3-use-all-conditionscontrols"></a><span data-ttu-id="19c68-146">示例3：使用所有条件/控件</span><span class="sxs-lookup"><span data-stu-id="19c68-146">Example 3: Use all conditions/controls</span></span>

#### <a name="request"></a><span data-ttu-id="19c68-147">请求</span><span class="sxs-lookup"><span data-stu-id="19c68-147">Request</span></span>
<span data-ttu-id="19c68-148">下面是一个使用所有条件/控件的请求示例。</span><span class="sxs-lookup"><span data-stu-id="19c68-148">The following is an example of the request to use all the conditions/controls.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_conditionalaccesspolicy_from_conditionalaccessroot"
}-->

```http
POST https://graph.microsoft.com/beta/conditionalAccess/policies
Content-type: application/json

{
    "displayName": "Demo app for documentation",
    "state": "disabled",
    "conditions": {
        "signInRiskLevels": [
            "high",
            "medium"
        ],
        "clientAppTypes": [
            "modern",
            "easSupported",
            "easUnsupported",
            "other"
        ],
        "applications": {
            "includeApplications": [
                "All"
            ],
            "excludeApplications": [
                "499b84ac-1321-427f-aa17-267ca6975798",
                "00000007-0000-0000-c000-000000000000",
                "de8bc8b5-d9f9-48b1-a8ad-b748da725064",
                "00000012-0000-0000-c000-000000000000",
                "797f4846-ba00-4fd7-ba43-dac1f8f63013",
                "05a65629-4c1b-48c1-a78b-804c4abdd4af",
                "7df0a125-d3be-4c96-aa54-591f83ff541c"
            ],
            "includeUserActions": []
        },
        "users": {
            "includeUsers": [
                "a702a13d-a437-4a07-8a7e-8c052de62dfd"
            ],
            "excludeUsers": [
                "124c5b6a-ffa5-483a-9b88-04c3fce5574a",
                "GuestsOrExternalUsers"
            ],
            "includeGroups": [],
            "excludeGroups": [],
            "includeRoles": [
                "9b895d92-2cd3-44c7-9d02-a6ac2d5ea5c3",
                "cf1c38e5-3621-4004-a7cb-879624dced7c",
                "c4e39bd9-1100-46d3-8c65-fb160da0071f"
            ],
            "excludeRoles": [
                "b0f54661-2d74-4c50-afa3-1ec803f12efe"
            ]
        },
        "platforms": {
            "includePlatforms": [
                "all"
            ],
            "excludePlatforms": [
                "iOS",
                "windowsPhone"
            ]
        },
        "locations": {
            "includeLocations": [
                "AllTrusted"
            ],
            "excludeLocations": [
                "00000000-0000-0000-0000-000000000000",
                "d2136c9c-b049-47ae-b9cf-316e04ef7198"
            ]
        },
        "deviceStates": {
            "includeStates": [
                "All"
            ],
            "excludeStates": [
                "Compliant"
            ]
        }
    },
    "grantControls": {
        "operator": "OR",
        "builtInControls": [
            "mfa",
            "compliantDevice",
            "domainJoinedDevice",
            "approvedApplication",
            "compliantApplication"
        ],
        "customAuthenticationFactors": [],
        "termsOfUse": [
            "ce580154-086a-40fd-91df-8a60abac81a0",
            "7f29d675-caff-43e1-8a53-1b8516ed2075"
        ]
    },
    "sessionControls": {
        "applicationEnforcedRestrictions": null,
        "persistentBrowser": null,
        "cloudAppSecurity": {
            "cloudAppSecurityType": "blockDownloads",
            "isEnabled": true
        },
        "signInFrequency": {
            "value": 4,
            "type": "hours",
            "isEnabled": true
        }
    }
}
```

#### <a name="response"></a><span data-ttu-id="19c68-149">响应</span><span class="sxs-lookup"><span data-stu-id="19c68-149">Response</span></span>

<span data-ttu-id="19c68-150">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="19c68-150">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.conditionalAccessPolicy"
} -->

```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#conditionalAccess/policies/$entity",
    "id": "6b5e999b-0ba8-4186-a106-e0296c1c4358",
    "displayName": "Demo app for documentation",
    "createdDateTime": "2019-09-26T23:12:16.0792706Z",
    "modifiedDateTime": null,
    "state": "disabled",
    "conditions": {
        "signInRiskLevels": [
            "high",
            "medium"
        ],
        "clientAppTypes": [
            "modern",
            "easSupported",
            "easUnsupported",
            "other"
        ],
        "applications": {
            "includeApplications": [
                "All"
            ],
            "excludeApplications": [
                "499b84ac-1321-427f-aa17-267ca6975798",
                "00000007-0000-0000-c000-000000000000",
                "de8bc8b5-d9f9-48b1-a8ad-b748da725064",
                "00000012-0000-0000-c000-000000000000",
                "797f4846-ba00-4fd7-ba43-dac1f8f63013",
                "05a65629-4c1b-48c1-a78b-804c4abdd4af",
                "7df0a125-d3be-4c96-aa54-591f83ff541c"
            ],
            "includeUserActions": []
        },
        "users": {
            "includeUsers": [
                "a702a13d-a437-4a07-8a7e-8c052de62dfd"
            ],
            "excludeUsers": [
                "124c5b6a-ffa5-483a-9b88-04c3fce5574a",
                "GuestsOrExternalUsers"
            ],
            "includeGroups": [],
            "excludeGroups": [],
            "includeRoles": [
                "9b895d92-2cd3-44c7-9d02-a6ac2d5ea5c3",
                "cf1c38e5-3621-4004-a7cb-879624dced7c",
                "c4e39bd9-1100-46d3-8c65-fb160da0071f"
            ],
            "excludeRoles": [
                "b0f54661-2d74-4c50-afa3-1ec803f12efe"
            ]
        },
        "platforms": {
            "includePlatforms": [
                "all"
            ],
            "excludePlatforms": [
                "iOS",
                "windowsPhone"
            ]
        },
        "locations": {
            "includeLocations": [
                "AllTrusted"
            ],
            "excludeLocations": [
                "00000000-0000-0000-0000-000000000000",
                "d2136c9c-b049-47ae-b9cf-316e04ef7198"
            ]
        },
        "deviceStates": {
            "includeStates": [
                "All"
            ],
            "excludeStates": [
                "Compliant"
            ]
        }
    },
    "grantControls": {
        "operator": "OR",
        "builtInControls": [
            "mfa",
            "compliantDevice",
            "domainJoinedDevice",
            "approvedApplication",
            "compliantApplication"
        ],
        "customAuthenticationFactors": [],
        "termsOfUse": [
            "ce580154-086a-40fd-91df-8a60abac81a0",
            "7f29d675-caff-43e1-8a53-1b8516ed2075"
        ]
    },
    "sessionControls": {
        "applicationEnforcedRestrictions": null,
        "persistentBrowser": null,
        "cloudAppSecurity": {
            "cloudAppSecurityType": "blockDownloads",
            "isEnabled": true
        },
        "signInFrequency": {
            "value": 4,
            "type": "hours",
            "isEnabled": true
        }
    }
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create conditionalAccessPolicy",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->