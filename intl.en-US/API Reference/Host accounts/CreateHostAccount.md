# CreateHostAccount

Creates an account for a specified host in a specified Bastionhost instance.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=CreateHostAccount&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|CreateHostAccount|The operation that you want to perform.

 Set the value to **CreateHostAccount**. |
|HostAccountName|String|Yes|abc|The name of the host account. The name can be up to 128 characters in length. |
|HostId|String|Yes|1|The ID of the host for which you want to create an account.

 **Note:** You can call the [ListHosts](~~200665~~) operation to query the ID of the host. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance where you want to create an account for the host.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|ProtocolName|String|Yes|SSH|The protocol used by the host account. Valid values:

 -   **SSH**
-   **RDP** |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance where you want to create the account for the host.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |
|Password|String|No|\*\*\*\*|The password of the host account. |
|PrivateKey|String|No|\*\*\*\*|The private key of the host account. The value is a Base64-encoded string.

 **Note:** This parameter takes effect only when the **ProtocolName** parameter is set to **SSH**. If the **ProtocolName** parameter is set to **RDP**, this parameter is not required. You can set a password and a private key for the host account at the same time. If both a password and a private key are set for the host account, Bastionhost preferentially uses the private key to log on to the host. |
|PassPhrase|String|No|\*\*\*\*|The passphrase of the private key for the host account.

 **Note:** You can specify this parameter when the **ProtocolName** parameter is set to **SSH**. If the **ProtocolName** parameter is set to **RDP**, this parameter is not required. |

All Alibaba Cloud API operations must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section in this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|HostAccountId|String|1|The ID of the host account. |
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=CreateHostAccount
&HostAccountName=abc
&HostId=1
&InstanceId=bastionhost-cn-st220aw****
&ProtocolName=SSH
&Password=****
&<Common request parameters>
```

Sample success responses

`XML` format

```
<CreateHostAccountResponse>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <HostAccountId>1</HostAccountId>
</CreateHostAccountResponse>
```

`JSON` format

```
{
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
	"HostAccountId": "1"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

