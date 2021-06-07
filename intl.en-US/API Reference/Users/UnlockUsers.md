# UnlockUsers

Unlocks one or more users of a specified Bastionhost instance.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=UnlockUsers&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|UnlockUsers|The operation that you want to perform.

 Set the value to **UnlockUsers**. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance to which the users to be unlocked belong.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|UserIds|String|Yes|\["1","2"\]|The IDs of the users to be unlocked. The value is a JSON string. You can add up to 100 user IDs.

 **Note:** You can call the [ListUsers](~~204522~~) operation to query the IDs of the users. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance to which the users to be unlocked belong.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |

All Alibaba Cloud API operations must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section of this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Results|Array of Item| |The call result of the operation. |
|Code|String|OK|The return code that indicates whether the call was successful. Valid values:

 -   **OK**: The call was successful.
-   **UNEXPECTED**: An unknown error has occurred.
-   **INVALID\_ARGUMENT**: A request parameter is invalid.
-   **OBJECT\_NOT\_FOUND**: The specified user is invalid.
-   **OBJECT\_AlREADY\_EXISTS**: The specified user has been unlocked. |
|Message|String|N/A|This parameter is obsolete. |
|UserId|String|1|The ID of the user. |
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=UnlockUsers
&InstanceId=bastionhost-cn-st220aw****
&UserIds=["1","2"]
&<Common request parameters>
```

Sample success responses

`XML` format

```
<UnlockUsersResponse>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <Results>
            <Message></Message>
            <UserId>1</UserId>
            <Code>OK</Code>
      </Results>
</UnlockUsersResponse>
```

`JSON` format

```
{
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
	"Results": [{
		"Message": "",
		"UserId": "1",
		"Code": "OK"
	}]
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

