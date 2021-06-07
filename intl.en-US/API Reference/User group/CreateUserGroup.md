# CreateUserGroup

Creates a user group in a specified Bastionhost instance.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=CreateUserGroup&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|CreateUserGroup|The operation that you want to perform.

 Set the value to **CreateUserGroup**. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance where you want to create the user group.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|UserGroupName|String|Yes|group|The name of the user group that you want to create. The value can be up to 128 characters in length. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance where you want to create the user group.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |
|Comment|String|No|comment|The description of the user group that you want to create. The value can be up to 500 characters in length. |

All Bastionhost API requests must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section of this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|The ID of the request. |
|UserGroupId|String|1|The ID of the user group that was created. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=CreateUserGroup
&InstanceId=bastionhost-cn-st220aw****
&UserGroupName=group
&<Common request parameters>
```

Sample success responses

`XML` format

```
<CreateUserGroupResponse>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <UserGroupId>1</UserGroupId>
</CreateUserGroupResponse>
```

`JSON` format

```
{
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
	"UserGroupId": "1"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

