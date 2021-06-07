# ListHostGroupsForUser

Queries the host groups that a specified user is authorized or not authorized to manage.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=ListHostGroupsForUser&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ListHostGroupsForUser|The operation that you want to perform.

 Set the value to **ListHostGroupsForUser**. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance where you want to query the host groups that the user is authorized or not authorized to manage.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|UserId|String|Yes|1|The ID of the user.

 **Note:** You can call the [ListUsers](~~204522~~) operation to query the ID of the user. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance where you want to query the host groups that the user is authorized or not authorized to manage.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |
|Mode|String|No|Authorized|The category of the host group that you want to query. Valid values:

 -   **Authorized**: Query the host groups that the user is authorized to manage. This is the default value.
-   **Unauthorized**: Query the host groups that the user is not authorized to manage. |
|PageNumber|String|No|1|The number of the page to return. Default value: **1**. |
|PageSize|String|No|20|The number of entries to return on each page.

 The value of the PageSize parameter must not exceed 100. Default value: 20. If you leave the PageSize parameter empty, 20 entries are returned on each page.

 **Note:** We recommend that you do not leave the PageSize parameter empty. |
|HostGroupName|String|No|group|The name of the host group that you want to query. The name can be up to 128 characters in length. Only exact match is supported. |

All Bastionhost API requests must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section of this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|HostGroups|Array of Item| |The host groups returned. |
|Comment|String|comment|The description of the host group. |
|HostGroupId|String|1|The ID of the host group. |
|HostGroupName|String|group|The name of the host group. |
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|The ID of the request. |
|TotalCount|Integer|1|The total number of host groups returned. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=ListHostGroupsForUser
&InstanceId=bastionhost-cn-st220aw****
&UserId=1
&<Common request parameters>
```

Sample success responses

`XML` format

```
<ListHostGroupsForUserResponse>
      <TotalCount>1</TotalCount>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <HostGroups>
            <Comment>comment</Comment>
            <HostGroupId>1</HostGroupId>
            <HostGroupName>group</HostGroupName>
      </HostGroups>
</ListHostGroupsForUserResponse>
```

`JSON` format

```
{
	"TotalCount": "1",
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
	"HostGroups": [{
		"Comment": "comment",
		"HostGroupId": "1",
		"HostGroupName": "group"
	}]
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

