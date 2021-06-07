# ModifyHost

Modifies the basic information of a specified host, such as the endpoint, name, operating system, and description of the host.

You can call this operation to modify the basic information of an on-premises host, an Elastic Compute Service \(ECS\) instance, or a host in a dedicated cluster.

**Note:** The basic information of ECS instances and hosts in dedicated clusters within your Alibaba Cloud account is synchronized to Bastionhost on a regular basis. After you modify the basic information of an ECS instance or a host in a dedicated cluster, the modification result may be overwritten by the synchronized information.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=ModifyHost&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ModifyHost|The operation that you want to perform.

 Set the value to **ModifyHost**. |
|HostId|String|Yes|1|The ID of the host.

 **Note:** You can call the [ListHosts](~~200665~~) operation to query the ID of the host. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance where you want to modify the information of the host.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance where you want to modify the information of the host.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |
|HostPrivateAddress|String|No|193.168.XX.XX|The new internal endpoint of the host. You can set this parameter to a domain name or an IP address. |
|HostPublicAddress|String|No|200.1.XX.XX|The new public endpoint of the host. You can set this parameter to a domain name or an IP address. |
|OSType|String|No|Linux|The new operating system of the host. Valid values:

 -   **Linux**
-   **Windows** |
|HostName|String|No|TestHost|The new name of the host. The name can be up to 128 characters. |
|Comment|String|No|Host for test.|The new description of the host. The value can be up to 500 characters in length. |

All Alibaba Cloud API operations must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section of this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=ModifyHost
&HostId=1
&InstanceId=bastionhost-cn-st220aw****
&HostPublicAddress=200.1.XX.XX
&<Common request parameters>
```

Sample success responses

`XML` format

```
<ModifyHostResponse>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
</ModifyHostResponse>
```

`JSON` format

```
{
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

