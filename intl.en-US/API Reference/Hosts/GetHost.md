# GetHost

Queries the details of a specified host, such as the name, source, endpoint, protocol, and service port of the host.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=GetHost&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|GetHost|The operation that you want to perform.

 Set the value to **GetHost**. |
|HostId|String|Yes|1|The ID of the host that you want to query. You can specify only one host ID.

 **Note:** You can call the [ListHosts](~~200665~~) operation to query the ID of the host. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance where you want to query the host.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance where you want to query the host.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |

All Alibaba Cloud API operations must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section of this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Host|Struct| |The information of the host that was queried. |
|ActiveAddressType|String|Public|The endpoint type of the host. Valid values:

 -   **Public**: a public endpoint
-   **Private**: an internal endpoint |
|Comment|String|host|The description of the host. |
|HostId|String|1|The ID of the host. |
|HostName|String|host|The name of the host. |
|HostPrivateAddress|String|192.168.XX.XX|The internal endpoint of the host. You can set this parameter to a domain name or an IP address. |
|HostPublicAddress|String|1.1.XX.XX|The public endpoint of the host. You can set this parameter to a domain name or an IP address. |
|OSType|String|Linux|The operating system of the host. Valid values:

 -   **Linux**
-   **Windows** |
|Protocols|Array of Item| |The protocol information of the host. |
|HostFingerPrint|String|ssh-ed25519\|3e:46:5a:e1:1f:0d:39:7e:61:35:d5:fa:7b:2b:\*\*:\*\*|The fingerprint of the host. This parameter uniquely identifies a host. |
|Port|Integer|22|The service port of the host. |
|ProtocolName|String|SSH|The protocol that is used to connect to the host. Valid values:

 -   **SSH**
-   **RDP** |
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

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=GetHost
&HostId=1
&InstanceId=bastionhost-cn-st220aw****
&<Common request parameters>
```

Sample success responses

`XML` format

```
<GetHostResponse>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <Host>
            <Comment>host</Comment>
            <Protocols>
                  <ProtocolName>SSH</ProtocolName>
                  <HostFingerPrint></HostFingerPrint>
                  <Port>22</Port>
            </Protocols>
            <ActiveAddressType>Public</ActiveAddressType>
            <HostPrivateAddress>192.168.XX.XX</HostPrivateAddress>
            <HostPublicAddress>1.1.XX.XX</HostPublicAddress>
            <OSType>Linux</OSType>
            <HostId>1</HostId>
            <SourceInstanceId>i-bp19ienyt0yax748****</SourceInstanceId>
            <HostName>host</HostName>
            <SourceInstanceState>Normal</SourceInstanceState>
            <Source>Local</Source>
      </Host>
</GetHostResponse>
```

`JSON` format

```
{
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
	"Host": {
		"Comment": "host",
		"Protocols": [{
			"ProtocolName": "SSH",
			"HostFingerPrint": "",
			"Port": "22"
		}],
		"ActiveAddressType": "Public",
		"HostPrivateAddress": "192.168.XX.XX",
		"HostPublicAddress": "1.1.XX.XX",
		"OSType": "Linux",
		"HostId": "1",
		"SourceInstanceId": "i-bp19ienyt0yax748****",
		"HostName": "host",
		"SourceInstanceState": "Normal",
		"Source": "Local"
	}
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

