# ListHostsForUser

Queries the hosts that a specified user is authorized or not authorized to manage.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=ListHostsForUser&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ListHostsForUser|The operation that you want to perform.

 Set the value to **ListHostsForUser**. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance where you want to query the hosts that the user is authorized or not authorized to manage.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|UserId|String|Yes|1|The ID of the user.

 **Note:** You can call the [ListUsers](~~204522~~) operation to query the ID of the user ID. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance where you want to query the hosts that the user is authorized or not authorized to manage.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |
|Mode|String|No|Authorized|The category of the host that you want to query. Valid values:

 -   **Authorized**: Query the hosts that the user is authorized to manage. This is the default value.
-   **Unauthorized**: Query the hosts that the user is not authorized to manage. |
|PageNumber|String|No|1|The number of the page to return. Default value: 1. |
|PageSize|String|No|20|The number of entries to return on each page.

 The value of the PageSize parameter must not exceed 100. Default value: 20. If you leave the PageSize parameter empty, 20 entries are returned on each page.

 **Note:** We recommend that you do not leave the PageSize parameter empty. |
|HostAddress|String|No|192.168.XX.XX|The endpoint of the host that you want to query. You can set this parameter to a domain name or an IP address. Only exact match is supported. |
|HostName|String|No|abc|The name of the host that you want to query. Only exact match is supported. |
|OSType|String|No|Linux|The operating system of the host that you want to query. Valid values:

 -   **Linux**
-   **Windows** |

All Bastionhost API requests must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section of this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Hosts|Array of Item| |The hosts returned. |
|ActiveAddressType|String|Public|The endpoint type of the host. Valid values:

 -   **Public**: a public endpoint
-   **Private**: an internal endpoint |
|Comment|String|comment|The description of the host. |
|HostId|String|1|The ID of the host. |
|HostName|String|host01|The name of the host. |
|HostPrivateAddress|String|192.168.XX.XX|The internal endpoint of the host. The value is a domain name or an IP address. |
|HostPublicAddress|String|10.158.XX.XX|The public endpoint of the host. The value is a domain name or an IP address. |
|OSType|String|Linux|The operating system of the host. Valid values:

 -   **Linux**
-   **Windows** |
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|The ID of the request. |
|TotalCount|Integer|1|The total number of hosts returned. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=ListHostsForUser
&InstanceId=bastionhost-cn-st220aw****
&UserId=1
&<Common request parameters>
```

Sample success responses

`XML` format

```
<ListHostsForUserResponse>
      <Hosts>
            <Comment>comment</Comment>
            <ActiveAddressType>Public</ActiveAddressType>
            <HostPrivateAddress>192.168.XX.XX</HostPrivateAddress>
            <HostPublicAddress>10.158.XX.XX</HostPublicAddress>
            <OSType>Linux</OSType>
            <HostId>1</HostId>
            <HostName>host01</HostName>
      </Hosts>
      <TotalCount>1</TotalCount>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE </RequestId>
</ListHostsForUserResponse>
```

`JSON` format

```
{
	"Hosts": [{
		"Comment": "comment",
		"ActiveAddressType": "Public",
		"HostPrivateAddress": "192.168.XX.XX",
		"HostPublicAddress": "10.158.XX.XX",
		"OSType": "Linux",
		"HostId": "1",
		"HostName": "host01"
	}],
	"TotalCount": "1",
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE "
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

