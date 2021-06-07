# ListUsers

Queries the users of a specified Bastionhost instance.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=ListUsers&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ListUsers|The operation that you want to perform.

 Set the value to **ListUsers**. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance to which the users to be queried belong.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance to which the users to be queried belong.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |
|PageNumber|String|No|1|The number of the page to return. Default value: **1**. |
|PageSize|String|No|20|The number of entries to return on each page.

 The value of the PageSize parameter must not exceed 100. By default, the number of entries on each page is 20. If you do not set the PageSize parameter, 20 entries are returned per page by default.

 **Note:** We recommend that you do not leave this parameter empty. |
|UserName|String|No|abc|The logon name of the user to be queried. Only exact match is supported. |
|DisplayName|String|No|User|The display name of the user to be queried. Only exact match is supported. |
|Source|String|No|Local|The source of the user to be queried. Valid values:

 -   **Local**: a local user
-   **Ram**: a RAM user |
|Mobile|String|No|1359999\*\*\*\*|The mobile number of the user to be queried. Only exact match is supported. |
|UserState|String|No|Normal|The status of the user to be queried. Valid values:

 -   **Normal**: The user can access the Bastionhost instance.
-   **Frozen**: The user is locked and cannot access the Bastionhost instance.
-   **Expired**: The user has expired and cannot access the Bastionhost instance. |
|SourceUserId|String|No|122748924538\*\*\*\*|The unique ID of the user to be queried. Only exact match is supported.

 **Note:** This parameter uniquely identifies a RAM user of the Bastionhost instance. This parameter takes effect only when the **Source** parameter is set to **Ram**. You can call the [ListUsers](~~28684~~) operation to obtain the unique ID of the user from the **UserId** response parameter. |
|UserGroupId|String|No|1|The ID of the user group to be queried.

 **Note:** You can call the [ListUserGroups](~~204509~~) operation to query the ID of the user group. |

All Alibaba Cloud API operations must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section of this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|The ID of the request. |
|TotalCount|Integer|1|The total number of users that were queried. |
|Users|Array of Item| |The list of users that were queried. |
|Comment|String|comment|The description of the user. |
|DisplayName|String|Bob|The display name of the user. |
|Email|String|1099\*\*@qq.com|The email address of the user. |
|Mobile|String|1359999\*\*\*\*|The mobile number of the user. |
|MobileCountryCode|String|CN|The country where the mobile number of the user is registered. Valid values:

 -   **CN**: mainland China, whose country calling code is +86
-   **HK**: Hong Kong \(China\), whose country calling code is +852
-   **MO**: Macau \(China\), whose country calling code is +853
-   **TW**: Taiwan \(China\), whose country calling code is +886
-   **RU**: Russia, whose country calling code is +7
-   **SG**: Singapore, whose country calling code is +65
-   **MY**: Malaysia, whose country calling code is +60
-   **ID**: Indonesia, whose country calling code is +62
-   **DE**: Germany, whose country calling code is +49
-   **AU**: Australia, whose country calling code is +61
-   **US**: United States, whose country calling code is +1
-   **AE**: United Arab Emirates, whose country calling code is +971
-   **JP**: Japan, whose country calling code is +81
-   **GB**: United Kingdom, whose country calling code is +44
-   **IN**: India, whose country calling code is +91
-   **KR**: South Korea, whose country calling code is +82
-   **PH**: Philippines, whose country calling code is +63
-   **CH**: Switzerland, whose country calling code is +41
-   **SE**: Sweden, whose country calling code is +46 |
|Source|String|Local|The source of the user. Valid values:

 -   **Local**: a local user
-   **Ram**: a RAM user |
|SourceUserId|String|122748924538\*\*\*\*|The unique ID of the user.

 **Note:** This parameter uniquely identifies a RAM user of the Bastionhost instance. A value is returned for this parameter if the **Source** parameter is set to **Ram**. No value is returned for this parameter if the **Source** parameter is set to **Local**. |
|UserId|String|1|The ID of the user. |
|UserName|String|abc\_def|The logon name of the user. |
|UserState|List|\["Normal"\]|The status of the user. Valid values:

 -   **Normal**: The user can access the Bastionhost instance.
-   **Frozen**: The user is locked and cannot access the Bastionhost instance.
-   **Expired**: The user has expired and cannot access the Bastionhost instance. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=ListUsers
&InstanceId=bastionhost-cn-st220aw****
&<Common request parameters>
```

Sample success responses

`XML` format

```
<ListUsersResponse>
      <TotalCount>1</TotalCount>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <Users>
            <Comment>comment</Comment>
            <UserName>abc_def</UserName>
            <Email>1099**@qq.com</Email>
            <UserId>1</UserId>
            <SourceUserId>122748924538****</SourceUserId>
            <MobileCountryCode>CN</MobileCountryCode>
            <DisplayName>Bob</DisplayName>
            <Mobile>1359999****</Mobile>
            <Source>Local</Source>
            <UserState>Normal</UserState>
      </Users>
</ListUsersResponse>
```

`JSON` format

```
{
	"TotalCount": "1",
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
	"Users": [{
		"Comment": "comment",
		"UserName": "abc_def",
		"Email": "1099**@qq.com",
		"UserId": "1",
		"SourceUserId": "122748924538****",
		"MobileCountryCode": "CN",
		"DisplayName": "Bob",
		"Mobile": "1359999****",
		"Source": "Local",
		"UserState": ["Normal"]
	}]
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

