# ModifyUser

Modifies the information of a specified user of a specified Bastionhost instance.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=ModifyUser&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ModifyUser|The operation that you want to perform.

 Set the value to **ModifyUser**. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance where you want to modify user information.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|UserId|String|Yes|1|The ID of the user whose information you want to modify.

 **Note:** You can call the [ListUsers](~~204522~~) operation to query the ID of the user. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance where you want to modify user information.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |
|Password|String|No|\*\*\*\*|The new password of the user. The value of this parameter can contain letters, digits, and underscores \(\_\). It can be up to 128 characters in length.

 **Note:** This parameter takes effect only when the **Source** parameter is set to **Local**. |
|DisplayName|String|No|Bob|The new display name of the user. The value can be up to 128 characters in length. |
|Comment|String|No|comment|The new description of the user. The value can be up to 500 characters in length. |
|Email|String|No|123\*\*@qq.com|The new email address of the user. |
|Mobile|String|No|1358888\*\*\*\*|The new mobile number of the user. |
|MobileCountryCode|String|No|CN|The country where the new mobile number of the user is registered. Valid values:

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

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=ModifyUser
&InstanceId=bastionhost-cn-st220aw****
&UserId=1
&<Common request parameters>
```

Sample success responses

`XML` format

```
<ModifyUserResponse>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
</ModifyUserResponse>
```

`JSON` format

```
{
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

