# AddUsersToGroup

Adds one or more users to a specified user group.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=AddUsersToGroup&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|AddUsersToGroup|The operation that you want to perform.

 Set the value to **AddUsersToGroup**. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance where you want to add users to the user group.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|UserGroupId|String|Yes|1|The ID of the user group to which you want to add users.

 **Note:** You can call the [ListUserGroups](~~204509~~) operation to query the ID of the user group. |
|UserIds|String|Yes|\["1","2","3"\]|The ID of the user that you want to add to the user group. The value is a JSON string. You can add up to 100 user IDs.

 **Note:** You can call the [ListUsers](~~204522~~) operation to query the ID of the user. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance where you want to add users to the user group.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |

All Bastionhost API requests must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section of this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|The ID of the request. |
|Results|Array of Item| |The call result of the operation. |
|Code|String|OK|The return code that indicates whether the call was successful. Valid values:

 -   **OK**: The call was successful.
-   **UNEXPECTED**: An unknown error has occurred.
-   **INVALID\_ARGUMENT**: A request parameter is invalid.
-   **OBJECT\_NOT\_FOUND**: The specified user is invalid.
-   **OBJECT\_AlREADY\_EXISTS**: The specified user has been added to the user group. |
|Message|String|None|This parameter is obsolete. |
|UserGroupId|String|1|The ID of the user group. |
|UserId|String|1|The ID of the user. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=AddUsersToGroup
&InstanceId=bastionhost-cn-st220aw****
&UserGroupId=1
&UserIds= ["1","2","3"]
&<Common request parameters>
```

Sample success responses

`XML` format

```
<AddUsersToGroupResponse>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <Results>
            <Message></Message>
            <Code>OK</Code>
            <UserId>1</UserId>
            <UserGroupId>1</UserGroupId>
      </Results>
</AddUsersToGroupResponse>
```

`JSON` format

```
{
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
	"Results": [{
		"Message": "",
		"Code": "OK",
		"UserId": "1",
		"UserGroupId": "1"
	}]
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

