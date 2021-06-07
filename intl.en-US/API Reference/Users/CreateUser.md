# CreateUser

Creates a user of a specified Bastionhost instance.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=CreateUser&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|CreateUser|The operation that you want to perform.

 Set the value to **CreateUser**. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance to which the user to be created belongs.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|Source|String|Yes|Local|The source of the new user. Valid values:

 -   **Local**: a local user
-   **Ram**: a RAM user |
|UserName|String|Yes|abc\_def|The logon name of the new user. The value of this parameter can contain only letters, digits, and underscores \(\_\). It can be up to 128 characters in length. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance to which the new user belongs.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |
|DisplayName|String|No|Bob|The display name of the new user. The value can be up to 128 characters in length. |
|Password|String|No|\*\*\*\*|The password of the new user. The value can be up to 128 characters in length.

 **Note:** This parameter is required if the **Source** parameter is set to **Local**. |
|Comment|String|No|comment|The description of the new user. The value can be up to 500 characters in length. |
|Email|String|No|123@qq.com|The email address of the new user. |
|Mobile|String|No|1359999\*\*\*\*|The mobile number of the new user. |
|SourceUserId|String|No|122748924538\*\*\*\*|The unique ID of the new user.

 **Note:** This parameter uniquely identifies a RAM user of the Bastionhost instance. This parameter is required if the **Source** parameter is set to **Ram**. You can call the [ListUsers](~~28684~~) operation to obtain the unique ID of the user from the **UserId** response parameter. |
|MobileCountryCode|String|No|CN|The country where the mobile number of the new user is registered. Default value: **CN**. Valid values:

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

All Alibaba Cloud API operations must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section of this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|The ID of the request. |
|UserId|String|1|The ID of the new user. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=CreateUser
&InstanceId=bastionhost-cn-st220aw****
&Source=Local
&UserName=abc_def
&<Common request parameters>
```

Sample success responses

`XML` format

```
<CreateUserResponse>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <UserId>1</UserId>
</CreateUserResponse>
```

`JSON` format

```
{
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
	"UserId": "1"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

