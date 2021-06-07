# ListHostGroupAccountNamesForUserGroup

Queries the names of the host accounts that a specified user group is authorized to manage in a specified host group.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=ListHostGroupAccountNamesForUserGroup&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ListHostGroupAccountNamesForUserGroup|The operation that you want to perform.

 Set the value to **ListHostGroupAccountNamesForUserGroup**. |
|HostGroupId|String|Yes|1|The ID of the host group.

 **Note:** You can call the [ListHostGroups](~~201307~~) operation to query the ID of the host group. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance where you want to query the host account names that the user group is authorized to manage in a specified host group.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|UserGroupId|String|Yes|1|The ID of the user group.

 **Note:** You can call the [ListUserGroups](~~204509~~) operation to query the ID of the user group. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance where you want to query the host account names that the user group is authorized to manage in a specified host group.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |

All Bastionhost API requests must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section of this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|HostAccountNames|List|\["root","abc"\]|The names of host accounts returned. |
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=ListHostGroupAccountNamesForUserGroup
&HostGroupId=1
&InstanceId=bastionhost-cn-st220aw****
&UserGroupId=1
&<Common request parameters>
```

Sample success responses

`XML` format

```
<ListHostGroupAccountNamesForUserGroupResponse>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <HostAccountNames>root</HostAccountNames>
      <HostAccountNames>abc</HostAccountNames>
</ListHostGroupAccountNamesForUserGroupResponse>
```

`JSON` format

```
{
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
	"HostAccountNames": ["root", "abc"]
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

