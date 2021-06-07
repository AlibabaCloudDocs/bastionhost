# ListUserGroups

Queries the user groups in a specified Bastionhost instance.

****

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=ListUserGroups&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ListUserGroups|The operation that you want to perform.

 Set the value to **ListUserGroups**. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance where you want to query user groups.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance where you want to query user groups.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |
|PageNumber|String|No|1|The number of the page to return. Default value: **1**. |
|PageSize|String|No|20|The number of entries to return on each page.

 The value of the PageSize parameter must not exceed 100. Default value: 20. If you leave the PageSize parameter empty, 20 entries are returned on each page.

 **Note:** We recommend that you do not leave the PageSize parameter empty. |
|UserGroupName|String|No|TestGroup01|The name of the user group that you want to query. Only exact match is supported. |

All Bastionhost API requests must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section of this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|The ID of the request. |
|TotalCount|Integer|1|The total number of user groups returned. |
|UserGroups|Array of Item| |The user groups returned. |
|Comment|String|comment|The description of the user group. |
|MemberCount|Integer|5|The number of users in the user group. |
|UserGroupId|String|1|The ID of the user group. |
|UserGroupName|String|TestGroup01|The name of the user group. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=ListUserGroups
&InstanceId=bastionhost-cn-st220aw****
&<Common request parameters>
```

Sample success responses

`XML` format

```
<ListUserGroupsResponse>
      <TotalCount>1</TotalCount>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <UserGroups>
            <Comment>comment</Comment>
            <UserGroupName>TestGroup01</UserGroupName>
            <UserGroupId>1</UserGroupId>
            <MemberCount>5</MemberCount>
      </UserGroups>
</ListUserGroupsResponse>
```

`JSON` format

```
{
	"TotalCount": "1",
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
	"UserGroups": [{
		"Comment": "comment",
		"UserGroupName": "TestGroup01",
		"UserGroupId": "1",
		"MemberCount": "5"
	}]
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

