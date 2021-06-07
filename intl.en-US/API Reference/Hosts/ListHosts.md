# ListHosts

Queries the hosts in a specified Bastionhost instance.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=ListHosts&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ListHosts|The operation that you want to perform.

 Set the value to **ListHosts**. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance where you want to query hosts.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance where you want to query hosts.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |
|PageNumber|String|No|1|The number of the page to return. Default value: **1**. |
|PageSize|String|No|20|The number of entries to return on each page.

 The value of the PageSize parameter must not exceed 100. Default value: 20. If you leave the PageSize parameter empty, 20 entries are returned on each page by default.

 **Note:** We recommend that you do not leave the PageSize parameter empty. |
|OSType|String|No|Linux|The operating system of the host that you want to query. Valid values:

 -   **Linux**
-   **Windows** |
|HostName|String|No|host|The name of the host that you want to query. Only exact match is supported. |
|HostAddress|String|No|1.1.XX.XX|The endpoint of the host that you want to query. You can set this parameter to a domain name or an IP address. Only exact match is supported. |
|Source|String|No|Local|The source of the host that you want to query. Valid values:

 -   **Local**: an on-premises host
-   **Ecs**: an Elastic Compute Service \(ECS\) instance
-   **Rds**: a host in a dedicated cluster |
|SourceInstanceId|String|No|i-bp19ienyt0yax748\*\*\*\*|The ID of the ECS instance or dedicated cluster host that you want to query. Only exact match is supported. |
|SourceInstanceState|String|No|Normal|The status of the host that you want to query. Valid values:

 -   **Normal**: The host is normal.

 -   **Release**: The host is released. |
|HostGroupId|String|No|1|The ID of the host group to which the host that you want to query belongs.

 **Note:** You can call the [ListHostGroups](~~201307~~) operation to query the ID of the host group. |

All Alibaba Cloud API operations must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section of this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Hosts|Array of Item| |The hosts that were queried. |
|ActiveAddressType|String|Public|The endpoint type of the host. Valid values:

 -   **Public**: a public endpoint
-   **Private**: an internal endpoint |
|Comment|String|host|The description of the host. |
|HostAccountCount|Integer|1|The number of host accounts of the host. |
|HostId|String|1|The ID of the host. |
|HostName|String|name|The name of the host. |
|HostPrivateAddress|String|192.168.XX.XX|The internal endpoint of the host. You can set this parameter to a domain name or an IP address. |
|HostPublicAddress|String|1.1.XX.XX|The public endpoint of the host. You can set this parameter to a domain name or an IP address. |
|OSType|String|Linux|The operating system of the host. Valid values:

 -   **Linux**
-   **Windows** |
|Source|String|Local|The source of the host. Valid values:

 -   **Local**: an on-premises host
-   **Ecs**: an Elastic Compute Service \(ECS\) instance
-   **Rds**: a host in a dedicated cluster |
|SourceInstanceId|String|i-bp19ienyt0yax748\*\*\*\*|The ID of the ECS instance or dedicated cluster host that was queried.

 **Note:** No value is returned for this parameter if the **Source** parameter is set to **Local**. |
|SourceInstanceState|String|Normal|The status of the host. Valid values:

 -   **Normal**: The host is normal.

 -   **Release**: The host is released. |
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|The ID of the request. |
|TotalCount|Integer|1|The total number of hosts that were queried. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=ListHosts
&InstanceId=bastionhost-cn-st220aw****
&<Common request parameters>
```

Sample success responses

`XML` format

```
<ListHostsResponse>
      <Hosts>
            <Comment>host</Comment>
            <ActiveAddressType>Public</ActiveAddressType>
            <HostPrivateAddress>192.168.XX.XX</HostPrivateAddress>
            <HostPublicAddress>1.1.XX.XX</HostPublicAddress>
            <OSType>Linux</OSType>
            <HostId>1</HostId>
            <HostAccountCount>1</HostAccountCount>
            <SourceInstanceId>i-bp19ienyt0yax748****</SourceInstanceId>
            <SourceInstanceState>Normal</SourceInstanceState>
            <HostName>name</HostName>
            <Source>Local</Source>
      </Hosts>
      <TotalCount>1</TotalCount>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
</ListHostsResponse>
```

`JSON` format

```
{
	"Hosts": [{
		"Comment": "host",
		"ActiveAddressType": "Public",
		"HostPrivateAddress": "192.168.XX.XX",
		"HostPublicAddress": "1.1.XX.XX",
		"OSType": "Linux",
		"HostId": "1",
		"HostAccountCount": "1",
		"SourceInstanceId": "i-bp19ienyt0yax748****",
		"SourceInstanceState": "Normal",
		"HostName": "name",
		"Source": "Local"
	}],
	"TotalCount": "1",
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

