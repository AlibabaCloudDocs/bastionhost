# CreateHost

Creates a host for operations and maintenance \(O&M\) in a specified Bastionhost instance.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=CreateHost&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|CreateHost|The operation that you want to perform.

 Set the value to **CreateHost**. |
|ActiveAddressType|String|Yes|Public|The endpoint type of the host that you want to create. Valid values:

 -   **Public**: a public endpoint
-   **Private**: an internal endpoint |
|HostName|String|Yes|host01|The name of the host that you want to create. The name can be up to 128 characters in length. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance where you want to create the host.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|OSType|String|Yes|Linux|The operating system of the host that you want to create. Valid values:

 -   **Linux**
-   **Windows** |
|Source|String|Yes|Local|The source of the host that you want to create. Valid values:

 -   **Local**: an on-premises host
-   **Ecs**: an Elastic Compute Service \(ECS\) instance
-   **Rds**: a host in a dedicated cluster |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance where you want to create the host.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |
|HostPublicAddress|String|No|172.16.XX.XX|The public endpoint of the host that you want to create. You can set this parameter to a domain name or an IP address.

 **Note:** This parameter is required if the **ActiveAddressType** parameter is set to **Public**. |
|HostPrivateAddress|String|No|192.168.XX.XX|The internal endpoint of the host that you want to create. You can set this parameter to a domain name or an IP address.

 **Note:** This parameter is required if the **ActiveAddressType** parameter is set to **Private**. |
|Comment|String|No|Local Host|The description of the host that you want to create. The value can be up to 500 characters. |
|SourceInstanceId|String|No|i-dfabfda|The ID of the ECS instance or dedicated cluster host that you want to create.

 **Note:** This parameter is required if the **Source** parameter is set to **Ecs** or **Rds**. |
|InstanceRegionId|String|No|cn-hangzhou|The ID of the region where the ECS instance or dedicated cluster host that you want to create resides.

 **Note:** This parameter is required if the **Source** parameter is set to **Ecs** or **Rds**. |

All Alibaba Cloud API operations must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section of this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|HostId|String|1|The ID of the host that was created. |
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=CreateHost
&ActiveAddressType=Public
&HostName=host01
&InstanceId=bastionhost-cn-st220aw****
&OSType=Linux
&Source=Local
&HostPublicAddress=172.16.XX.XX
&<Common request parameters>
```

Sample success responses

`XML` format

```
<CreateHostResponse>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <HostId>1</HostId>
</CreateHostResponse>
```

`JSON` format

```
{
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
	"HostId": "1"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

