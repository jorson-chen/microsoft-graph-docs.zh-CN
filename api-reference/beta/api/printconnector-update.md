---
title: 更新 printConnector
description: 更新 printConnector 对象的属性。
author: braedenp-msft
localization_priority: Normal
ms.prod: universal-print
doc_type: apiPageType
ms.openlocfilehash: 767f60c6db7b212cd33467bdad893fc8c8ac853b
ms.sourcegitcommit: eacd2a6e46c19dd3cd8519592b1668fabe14d85d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "49873547"
---
# <a name="update-printconnector"></a><span data-ttu-id="06b9b-103">更新 printConnector</span><span class="sxs-lookup"><span data-stu-id="06b9b-103">Update printConnector</span></span>

<span data-ttu-id="06b9b-104">命名空间：microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="06b9b-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="06b9b-105">更新 **printConnector 对象** 的属性。</span><span class="sxs-lookup"><span data-stu-id="06b9b-105">Update the properties of a **printConnector** object.</span></span>

## <a name="permissions"></a><span data-ttu-id="06b9b-106">权限</span><span class="sxs-lookup"><span data-stu-id="06b9b-106">Permissions</span></span>
<span data-ttu-id="06b9b-p101">要调用此 API，需要以下权限之一。要了解详细信息，包括如何选择权限的信息，请参阅[权限](/graph/permissions-reference)。</span><span class="sxs-lookup"><span data-stu-id="06b9b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

<span data-ttu-id="06b9b-109">若要使用通用打印服务，用户或应用的租户必须具有活动的通用打印订阅，以及下表中列出的权限。</span><span class="sxs-lookup"><span data-stu-id="06b9b-109">To use the Universal Print service, the user or app's tenant must have an active Universal Print subscription, in addition to the permissions listed in the following table.</span></span> <span data-ttu-id="06b9b-110">登录用户必须是打印机 [管理员](/azure/active-directory/users-groups-roles/directory-assign-admin-roles#printer-administrator)。</span><span class="sxs-lookup"><span data-stu-id="06b9b-110">The signed in user must be a [Printer Administrator](/azure/active-directory/users-groups-roles/directory-assign-admin-roles#printer-administrator).</span></span>

|<span data-ttu-id="06b9b-111">权限类型</span><span class="sxs-lookup"><span data-stu-id="06b9b-111">Permission type</span></span> | <span data-ttu-id="06b9b-112">权限（从最低特权到最高特权）</span><span class="sxs-lookup"><span data-stu-id="06b9b-112">Permissions (from least to most privileged)</span></span> |
|:---------------|:--------------------------------------------|
|<span data-ttu-id="06b9b-113">委派（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="06b9b-113">Delegated (work or school account)</span></span>| <span data-ttu-id="06b9b-114">PrintConnector.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="06b9b-114">PrintConnector.ReadWrite.All</span></span> |
|<span data-ttu-id="06b9b-115">委派（个人 Microsoft 帐户）</span><span class="sxs-lookup"><span data-stu-id="06b9b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="06b9b-116">不支持。</span><span class="sxs-lookup"><span data-stu-id="06b9b-116">Not Supported.</span></span>|
|<span data-ttu-id="06b9b-117">应用程序</span><span class="sxs-lookup"><span data-stu-id="06b9b-117">Application</span></span>|<span data-ttu-id="06b9b-118">不支持。</span><span class="sxs-lookup"><span data-stu-id="06b9b-118">Not Supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="06b9b-119">HTTP 请求</span><span class="sxs-lookup"><span data-stu-id="06b9b-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /print/connectors/{id}
```
## <a name="request-headers"></a><span data-ttu-id="06b9b-120">请求标头</span><span class="sxs-lookup"><span data-stu-id="06b9b-120">Request headers</span></span>
| <span data-ttu-id="06b9b-121">名称</span><span class="sxs-lookup"><span data-stu-id="06b9b-121">Name</span></span>       | <span data-ttu-id="06b9b-122">说明</span><span class="sxs-lookup"><span data-stu-id="06b9b-122">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="06b9b-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="06b9b-123">Authorization</span></span> | <span data-ttu-id="06b9b-p103">Bearer {token}。必需。</span><span class="sxs-lookup"><span data-stu-id="06b9b-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="06b9b-126">Content-type</span><span class="sxs-lookup"><span data-stu-id="06b9b-126">Content-type</span></span>  | <span data-ttu-id="06b9b-p104">application/json. Required.</span><span class="sxs-lookup"><span data-stu-id="06b9b-p104">application/json. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="06b9b-129">请求正文</span><span class="sxs-lookup"><span data-stu-id="06b9b-129">Request body</span></span>
<span data-ttu-id="06b9b-130">在请求正文中，提供应更新的相关字段的值。</span><span class="sxs-lookup"><span data-stu-id="06b9b-130">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="06b9b-131">请求正文中不包括的现有属性将保留其以前的值，或根据对其他属性值的更改重新计算。</span><span class="sxs-lookup"><span data-stu-id="06b9b-131">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="06b9b-132">为了获得最佳性能，请勿加入尚未更改的现有值。</span><span class="sxs-lookup"><span data-stu-id="06b9b-132">For best performance, don't include existing values that haven't changed.</span></span>

| <span data-ttu-id="06b9b-133">属性</span><span class="sxs-lookup"><span data-stu-id="06b9b-133">Property</span></span>     | <span data-ttu-id="06b9b-134">类型</span><span class="sxs-lookup"><span data-stu-id="06b9b-134">Type</span></span>        | <span data-ttu-id="06b9b-135">Description</span><span class="sxs-lookup"><span data-stu-id="06b9b-135">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="06b9b-136">name</span><span class="sxs-lookup"><span data-stu-id="06b9b-136">name</span></span>|<span data-ttu-id="06b9b-137">String</span><span class="sxs-lookup"><span data-stu-id="06b9b-137">String</span></span>|<span data-ttu-id="06b9b-138">连接器的名称。</span><span class="sxs-lookup"><span data-stu-id="06b9b-138">The name of the connector.</span></span>|
|<span data-ttu-id="06b9b-139">fullyQualifiedDomainName</span><span class="sxs-lookup"><span data-stu-id="06b9b-139">fullyQualifiedDomainName</span></span>|<span data-ttu-id="06b9b-140">String</span><span class="sxs-lookup"><span data-stu-id="06b9b-140">String</span></span>|<span data-ttu-id="06b9b-141">连接器计算机主机名。</span><span class="sxs-lookup"><span data-stu-id="06b9b-141">The connector machine's hostname.</span></span>|
|<span data-ttu-id="06b9b-142">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="06b9b-142">operatingSystem</span></span>|<span data-ttu-id="06b9b-143">String</span><span class="sxs-lookup"><span data-stu-id="06b9b-143">String</span></span>|<span data-ttu-id="06b9b-144">连接器计算机的操作系统版本。</span><span class="sxs-lookup"><span data-stu-id="06b9b-144">The connector machine's operating system version.</span></span>|
|<span data-ttu-id="06b9b-145">appVersion</span><span class="sxs-lookup"><span data-stu-id="06b9b-145">appVersion</span></span>|<span data-ttu-id="06b9b-146">String</span><span class="sxs-lookup"><span data-stu-id="06b9b-146">String</span></span>|<span data-ttu-id="06b9b-147">连接器的版本。</span><span class="sxs-lookup"><span data-stu-id="06b9b-147">The connector's version.</span></span>|
|<span data-ttu-id="06b9b-148">location</span><span class="sxs-lookup"><span data-stu-id="06b9b-148">location</span></span>|[<span data-ttu-id="06b9b-149">printerLocation</span><span class="sxs-lookup"><span data-stu-id="06b9b-149">printerLocation</span></span>](../resources/printerlocation.md)|<span data-ttu-id="06b9b-150">连接器的物理和/或组织位置。</span><span class="sxs-lookup"><span data-stu-id="06b9b-150">The physical and/or organizational location of the connector.</span></span>|

## <a name="response"></a><span data-ttu-id="06b9b-151">响应</span><span class="sxs-lookup"><span data-stu-id="06b9b-151">Response</span></span>
<span data-ttu-id="06b9b-152">如果成功，此方法在响应正文中返回响应代码和更新的 `200 OK` [printConnector](../resources/printConnector.md) 对象。</span><span class="sxs-lookup"><span data-stu-id="06b9b-152">If successful, this method returns a `200 OK` response code and an updated [printConnector](../resources/printConnector.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="06b9b-153">示例</span><span class="sxs-lookup"><span data-stu-id="06b9b-153">Example</span></span>
##### <a name="request"></a><span data-ttu-id="06b9b-154">请求</span><span class="sxs-lookup"><span data-stu-id="06b9b-154">Request</span></span>
<span data-ttu-id="06b9b-155">下面展示了示例请求。</span><span class="sxs-lookup"><span data-stu-id="06b9b-155">The following is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="06b9b-156">HTTP</span><span class="sxs-lookup"><span data-stu-id="06b9b-156">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "update_connector"
}-->
```http
PATCH https://graph.microsoft.com/beta/print/connectors/{id}
Content-type: application/json
Content-length: 300

{
  "name": "ConnectorName",
  "fullyQualifiedDomainName": "CONNECTOR-MACHINE",
  "operatingSystem": "Microsoft Windows 10 Enterprise Insider Preview | 10.0.19555",
  "appVersion": "0.19.7338.23496",
  "location": {
    "latitude": 1.1,
    "longitude": 2.2,
    "altitudeInMeters": 3
  }
}
```
# <a name="c"></a>[<span data-ttu-id="06b9b-157">C#</span><span class="sxs-lookup"><span data-stu-id="06b9b-157">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/update-connector-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="06b9b-158">JavaScript</span><span class="sxs-lookup"><span data-stu-id="06b9b-158">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/update-connector-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="06b9b-159">Objective-C</span><span class="sxs-lookup"><span data-stu-id="06b9b-159">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/update-connector-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[<span data-ttu-id="06b9b-160">Java</span><span class="sxs-lookup"><span data-stu-id="06b9b-160">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/update-connector-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

##### <a name="response"></a><span data-ttu-id="06b9b-161">响应</span><span class="sxs-lookup"><span data-stu-id="06b9b-161">Response</span></span>
<span data-ttu-id="06b9b-162">下面展示了示例响应。</span><span class="sxs-lookup"><span data-stu-id="06b9b-162">The following is an example of the response.</span></span>
><span data-ttu-id="06b9b-p106">**注意：** 为了提高可读性，可能缩短了此处显示的响应对象。所有属性都将通过实际调用返回。</span><span class="sxs-lookup"><span data-stu-id="06b9b-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.printConnector"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 406

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#print/connectors/$entity",
  "id": "9953d245-3f6e-418c-a438-67f50e69a430",
  "name": "ConnectorName",
  "fullyQualifiedDomainName": "CONNECTOR-MACHINE",
  "operatingSystem": "Microsoft Windows 10 Enterprise Insider Preview | 10.0.19555",
  "appVersion": "0.19.7338.23496",
  "registeredDateTime": "2020-02-04T00:00:00.0000000Z",
  "location": {
    "latitude": 1.1,
    "longitude": 2.2,
    "altitudeInMeters": 3,
    "streetAddress": "One Microsoft Way",
    "subUnit": [
        "Main Plaza",
        "Unit 400"
    ],
    "city": "Redmond",
    "postalCode": "98052",
    "countryOrRegion": "USA",
    "site": "Puget Sound",
    "building": "Studio E",
    "floorNumber": 1,
    "floorDescription": "First Floor",
    "roomNumber": 1234,
    "roomDescription": "First floor copy room",
    "organization": [
        "C+AI",
        "Microsoft Graph"
    ],
    "subdivision": [
        "King County",
        "Red West"
    ],
    "stateOrProvince": "Washington"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update printConnector",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
