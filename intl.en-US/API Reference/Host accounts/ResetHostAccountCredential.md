# ResetHostAccountCredential

Deletes the logon credential of a specified host account of a specified Bastionhost instance. The logon credential can be the password or SSH private key.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=ResetHostAccountCredential&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ResetHostAccountCredential|The operation that you want to perform.

 Set the value to **ResetHostAccountCredential**. |
|CredentialType|String|Yes|Password|The type of the logon credential that you want to delete. Valid values:

 -   **Password**: You want to delete the password.
-   **PrivateKey**: You want to delete the SSH private key. |
|HostAccountId|String|Yes|1|The ID of the host account for which the logon credential is to be deleted.

 **Note:** You can call the [ListHostAccounts](~~204372~~) operation to query the ID of the host account. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance where you want to delete the logon credential for the host account.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance where you want to delete the logon credential for the host account.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |

All Alibaba Cloud API operations must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section in this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=ResetHostAccountCredential
&CredentialType=Password
&HostAccountId=1
&InstanceId=bastionhost-cn-xxx
&<Common request parameters>
```

Sample success responses

`XML` format

```
<ResetHostAccountCredentialResponse>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
</ResetHostAccountCredentialResponse>
```

`JSON` format

```
{
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

