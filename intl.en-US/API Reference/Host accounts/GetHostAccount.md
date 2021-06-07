# GetHostAccount

Queries the details of a specified host account of a specified Bastionhost instance.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=GetHostAccount&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|GetHostAccount|The operation that you want to perform.

 Set the value to **GetHostAccount**. |
|HostAccountId|String|Yes|1|The ID of the host account that you want to query.

 **Note:** You can call the [ListHostAccounts](~~204372~~) operation to query the ID of the host account. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance where you want to query the details of the host account.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance where you want to query the details of the host account.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |

All Alibaba Cloud API operations must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section in this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|HostAccount|Struct| |The details of the host account that were queried. |
|HasPassword|Boolean|true|Indicates whether a password is set for the host account. Valid values:

 -   **true**: indicates that a password is set for the host account.
-   **false**: indicates that no password is set for the host account. |
|HostAccountId|String|1|The ID of the host account. |
|HostAccountName|String|abc|The name of the host account. |
|HostId|String|1|The ID of the host to which the host account belongs. |
|PrivateKeyFingerprint|String|fe:ca:37:42:30:00:9d:95:e6:73:e5:b0:32:0a:\*\*:\*\*|The fingerprint of the private key. |
|ProtocolName|String|SSH|The protocol used by the host account. Valid values:

 -   **SSH**
-   **RDP** |
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=GetHostAccount
&HostAccountId=1
&InstanceId=bastionhost-cn-st220aw****
&<Common request parameters>
```

Sample success responses

`XML` format

```
<GetHostAccountResponse>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <HostAccount>
            <HostAccountName>abc</HostAccountName>
            <ProtocolName>SSH</ProtocolName>
            <PrivateKeyFingerprint>fe:ca:37:42:30:00:9d:95:e6:73:e5:b0:32:0a:**:**</PrivateKeyFingerprint>
            <HostId>1</HostId>
            <HasPassword>true</HasPassword>
            <HostAccountId>1</HostAccountId>
      </HostAccount>
</GetHostAccountResponse>
```

`JSON` format

```
{
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
	"HostAccount": {
		"HostAccountName": "abc",
		"ProtocolName": "SSH",
		"PrivateKeyFingerprint": "fe:ca:37:42:30:00:9d:95:e6:73:e5:b0:32:0a:**:**",
		"HostId": "1",
		"HasPassword": "true",
		"HostAccountId": "1"
	}
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

