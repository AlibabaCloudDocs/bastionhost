# ModifyHostAccount

Modifies the information of a specified host account of a specified Bastionhost instance, such as the name, password, and private key.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=ModifyHostAccount&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ModifyHostAccount|The operation that you want to perform.

 Set the value to **ModifyHostAccount**. |
|HostAccountId|String|Yes|1|The ID of the host account that you want to modify.

 **Note:** You can call the [ListHostAccounts](~~204372~~) operation to query the ID of the host account. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance where you want to modify the details of the host account .

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance where you want to modify the host account.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |
|HostAccountName|String|No|abc|The new name of the host account. The name can be up to 128 characters in length. |
|Password|String|No|\*\*\*\*|The new password of the host account. |
|PrivateKey|String|No|\*\*\*\*|The new private key of the host account. The value is a Base64-encoded string.

 **Note:** This parameter takes effect only when the ProtocolName parameter is set to **SSH**. If the ProtocolName parameter is set to **RDP**, this parameter is not required. You can call the [GetHostAccount](~~204391~~) operation to query the protocol used by the host account. You can set a password and a private key for the host account at the same time. If both a password and a private key are set for the host account, Bastionhost preferentially uses the private key to log on to the host. |
|PassPhrase|String|No|\*\*\*\*|The passphrase of the new private key for the host account.

 **Note:** This parameter takes effect only when the ProtocolName parameter is set to **SSH**. If the ProtocolName parameter is set to **RDP**, this parameter is not required. |

All Alibaba Cloud API operations must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section in this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=ModifyHostAccount
&HostAccountId=1
&InstanceId=bastionhost-cn-st220aw****
&HostAccountName=abc
&<Common request parameters>
```

Sample success responses

`XML` format

```
<ModifyHostAccountResponse>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
</ModifyHostAccountResponse>
```

`JSON` format

```
{
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

