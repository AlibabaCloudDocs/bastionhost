# GetHostGroup

Queries the details of a specified host group.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=GetHostGroup&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|GetHostGroup|The operation that you want to perform.

 Set the value to **GetHostGroup**. |
|HostGroupId|String|Yes|1|The ID of the host group that you want to query.

 **Note:** You can call the [ListHostGroups](~~201307~~) operation to query the ID of the host group. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance where you want to query the host group.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance where you want to query the host group.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |

All Alibaba Cloud API operations must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section of this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|HostGroup|Struct| |The details of the host group returned. |
|Comment|String|Description|The description of the host group. |
|HostGroupId|String|1|The ID of the host group. |
|HostGroupName|String|Host group 1|The name of the host group. |
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=GetHostGroup
&HostGroupId=1
&InstanceId=bastionhost-cn-st220aw****
&<Common request parameters>
```

Sample success responses

`XML` format

```
<GetHostGroupResponse>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <HostGroup>
            <Comment>Description</Comment>
            <HostGroupId>1</HostGroupId>
            <HostGroupName>Host group 1</HostGroupName>
      </HostGroup>
</GetHostGroupResponse>
```

`JSON` format

```
{
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
	"HostGroup": {
		"Comment": "Description",
		"HostGroupId": "1",
		"HostGroupName": "Host group 1"
	}
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

