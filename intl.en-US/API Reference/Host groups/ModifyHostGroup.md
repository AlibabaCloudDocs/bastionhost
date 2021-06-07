# ModifyHostGroup

Modifies the name or description of a specified host group.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=ModifyHostGroup&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ModifyHostGroup|The operation that you want to perform.

 Set the value to **ModifyHostGroup**. |
|HostGroupId|String|Yes|1|The ID of the host group that you want to modify.

 **Note:** You can call the [ListHostGroups](~~201307~~) operation to query the ID of the host group. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance where you want to modify the information of the host group.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance where you want to modify the information of the host group.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |
|HostGroupName|String|No|Group01|The new name of the host group. The name can be up to 128 characters in length. |
|Comment|String|No|comment|The new description of the host group. The value can be up to 500 characters in length. |

All Alibaba Cloud API operations must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section of this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=ModifyHostGroup
&HostGroupId=1
&InstanceId=bastionhost-cn-st220aw****
&HostGroupName=Group01
&<Common request parameters>
```

Sample success responses

`XML` format

```
<ModifyHostGroupResponse>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
</ModifyHostGroupResponse>
```

`JSON` format

```
{
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

