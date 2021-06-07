# ListHostGroups

Queries the host groups in a specified Bastionhost instance.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=ListHostGroups&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ListHostGroups|The operation that you want to perform.

 Set the value to **ListHostGroups**. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance where you want to query host groups.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance where you want to query host groups.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |
|PageNumber|String|No|1|The number of the page to return. Default value: **1**. |
|PageSize|String|No|20|The number of entries to return on each page.

 The value of the PageSize parameter must not exceed 100. Default value: 20. If you leave the PageSize parameter empty, 20 entries are returned on each page by default.

 **Note:** We recommend that you do not leave the PageSize parameter empty. |
|HostGroupName|String|No|Host group 1|The name of the host group that you want to query. Only exact match is supported. |

All Alibaba Cloud API operations must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section of this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|HostGroups|Array of Item| |The host groups returned. |
|Comment|String|Description|The description of the host group. |
|HostGroupId|String|1|The ID of the host group. |
|HostGroupName|String|Host group 1|The name of the host group. |
|MemberCount|Integer|1|The number of hosts in the host group. |
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|The ID of the request. |
|TotalCount|Integer|1|The total number of host groups returned. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=ListHostGroups
&InstanceId=bastionhost-cn-st220aw****
&<Common request parameters>
```

Sample success responses

`XML` format

```
<ListHostGroupsResponse>
      <TotalCount>1</TotalCount>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <HostGroups>
            <Comment>Description</Comment>
            <MemberCount>1</MemberCount>
            <HostGroupId>1</HostGroupId>
            <HostGroupName>Host group 1</HostGroupName>
      </HostGroups>
</ListHostGroupsResponse>
```

`JSON` format

```
{
	"TotalCount": "1",
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
	"HostGroups": [{
		"Comment": "Description",
		"HostGroupId": "1",
		"MemberCount": "1",
		"HostGroupName": "Host group 1"
	}]
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

