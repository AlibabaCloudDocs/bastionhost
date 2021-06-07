# AddHostsToGroup

Adds one or more hosts to a specified host group.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=AddHostsToGroup&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|AddHostsToGroup|The operation that you want to perform.

 Set the value to **AddHostsToGroup**. |
|HostGroupId|String|Yes|1|The ID of the host group to which you want to add hosts.

 **Note:** You can call the [ListHostGroups](~~201307~~) operation to query the ID of the host group. |
|HostIds|String|Yes|\["1","2","3"\]|The ID of the host that you want to add to the host group. The value is a JSON string. You can add up to 100 host IDs.

 **Note:** You can call the [ListHosts](~~200665~~) operation to query the IDs of hosts. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance where you want to add hosts to the host group.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance where you want to add hosts to the host group.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |

All Alibaba Cloud API operations must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section of this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|81500666-d7f5-4143-8329-0223cc738105|The ID of the request. |
|Results|Array of Item| |The call result of the operation. |
|Code|String|OK|The return code that indicates whether the call was successful. Valid values:

 -   **OK**: The call was successful.
-   **UNEXPECTED**: An unknown error has occurred.
-   **INVALID\_ARGUMENT**: A request parameter is invalid.
-   **OBJECT\_NOT\_FOUND**: The specified host is invalid.
-   **OBJECT\_AlREADY\_EXISTS**: The specified host has been added to the host group. |
|HostGroupId|String|1|The ID of the host group. |
|HostId|String|1|The ID of the host. |
|Message|String|N/A|This parameter is obsolete. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=AddHostsToGroup
&HostGroupId=1
&HostIds=["1","2","3"]
&InstanceId=bastionhost-cn-st220aw****
&<Common request parameters>
```

Sample success responses

`XML` format

```
<AddHostsToGroupResponse>
      <RequestId>81500666-d7f5-4143-8329-0223cc738105</RequestId>
      <Results>
            <HostGroupId>1</HostGroupId>
            <Message></Message>
            <HostId>1</HostId>
            <Code>OK</Code>
      </Results>
</AddHostsToGroupResponse>
```

`JSON` format

```
{
	"RequestId": "81500666-d7f5-4143-8329-0223cc738105",
	"Results": {
		"HostGroupId": "1",
		"Message": "",
		"HostId": "1",
		"Code": "OK"
	}
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

