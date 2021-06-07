# GetUserGroup

Queries the details of a specified user group in a specified Bastionhost instance.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=GetUserGroup&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|GetUserGroup|The operation that you want to perform.

 Set the value to **GetUserGroup**. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance where you want to query the details of the user group.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|UserGroupId|String|Yes|1|The ID of the user group to be queried.

 **Note:** You can call the [ListUserGroups](~~204509~~) operation to query the ID of the user group. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance where you want to query the details of the user group.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |

All Bastionhost API requests must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section of this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|The ID of the request. |
|UserGroup|Struct| |The details of the user group returned. |
|Comment|String|comment|The description of the user group. |
|UserGroupId|String|1|The ID of the user group. |
|UserGroupName|String|UserGroup01|The name of the user group. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=GetUserGroup
&InstanceId=bastionhost-cn-st220aw****
&UserGroupId=1
&<Common request parameters>
```

Sample success responses

`XML` format

```
<GetUserGroupResponse>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <UserGroup>
            <Comment>comment</Comment>
            <UserGroupName>UserGroup01</UserGroupName>
            <UserGroupId>1</UserGroupId>
      </UserGroup>
</GetUserGroupResponse>
```

`JSON` format

```
{
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
	"UserGroup": {
		"Comment": "comment",
		"UserGroupName": "UserGroup01",
		"UserGroupId": "1"
	}
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

