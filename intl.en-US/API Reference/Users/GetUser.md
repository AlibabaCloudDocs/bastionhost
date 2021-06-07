# GetUser

Queries the information of a specified user of a specified Bastionhost instance.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=GetUser&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|GetUser|The operation that you want to perform.

 Set the value to **GetUser**. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance to which the user to be queried belongs.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|UserId|String|Yes|1|The ID of the user to be queried.

 **Note:** You can call the [ListUsers](~~204522~~) operation to query the ID of the user. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance to which the user to be queried belongs.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |

All Alibaba Cloud API operations must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section of this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|The ID of the request. |
|User|Struct| |The information of the user that was queried. |
|Comment|String|commet|The description of the user. |
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
|UserName|String|abcabc\_def|The logon name of the user. |
|UserState|List|\["Normal"\]|The status of the user. Valid values:

 -   **Normal**: The user can access the Bastionhost instance.
-   **Frozen**: The user is locked and cannot access the Bastionhost instance.
-   **Expired**: The user has expired and cannot access the Bastionhost instance. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=GetUser
&InstanceId=bastionhost-cn-st220aw****
&UserId=1
&<Common request parameters>
```

Sample success responses

`XML` format

```
<GetUserResponse>
      <User>
            <Comment>commet</Comment>
            <Email>1099**@qq.com</Email>
            <UserName>abcabc_def</UserName>
            <UserId>1</UserId>
            <SourceUserId>122748924538****</SourceUserId>
            <DisplayName>Bob</DisplayName>
            <MobileCountryCode>CN</MobileCountryCode>
            <Mobile>1359999****</Mobile>
            <Source>Local</Source>
            <UserState>Normal</UserState>
      </User>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
</GetUserResponse>
```

`JSON` format

```
{
	"User": {
		"Comment": "commet",
		"Email": "1099**@qq.com",
		"UserName": "abcabc_def",
		"UserId": "1",
		"SourceUserId": "122748924538****",
		"DisplayName": "Bob",
		"MobileCountryCode": "CN",
		"Mobile": "1359999****",
		"Source": "Local",
		"UserState": ["Normal"]
	},
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

