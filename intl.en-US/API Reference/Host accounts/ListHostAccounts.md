# ListHostAccounts

Queries the host accounts of a host on a specified Bastionhost instance.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=ListHostAccounts&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ListHostAccounts|The operation that you want to perform.

Set the value to **ListHostAccounts**. |
|HostId|String|Yes|1|The ID of the host for which the host accounts are to be queried.

**Note:** You can call the [ListHosts](~~200665~~) operation to query the ID of the host. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance where you want to query accounts of the host.

**Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance where you want to query accounts of the host.

**Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |
|PageNumber|String|No|1|The number of the page to return. Default value: **1**. |
|PageSize|String|No|20|The number of entries to return on each page.

The value of the PageSize parameter must not exceed 100. Default value: 20. If you leave the PageSize parameter empty, 20 entries are returned on each page by default.

**Note:** We recommend that you do not leave the PageSize parameter empty. |
|HostAccountName|String|No|abc|The name of the host account that you want to query. The name can be up to 128 characters in length. Only exact match is supported. |
|ProtocolName|String|No|SSH|The protocol used by the host account that you want to query. Valid values:

-   **SSH**
-   **RDP** |

All Alibaba Cloud API operations must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section in this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|HostAccounts|Array of Item| |The host accounts that were queried. |
|HasPassword|Boolean|true|Indicates whether a password is set for the host account. Valid values:

-   **true**: indicates that a password is set for the host account.
-   **false**: indicates that no password is set for the host account. |
|HostAccountId|String|1|The ID of the host account. |
|HostAccountName|String|abc|The name of the host account. |
|HostId|String|1|The ID of the host. |
|PrivateKeyFingerprint|String|fe:ca:37:42:30:00:9d:95:e6:73:e5:b0:32:0a:\*\*:\*\*|The fingerprint of the private key for the host account. |
|ProtocolName|String|SSH|The protocol used by the host account. Valid values:

-   **SSH**
-   **RDP** |
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|The ID of the request. |
|TotalCount|Integer|1|The total number of host accounts that were queried. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=ListHostAccounts
&HostId=1
&InstanceId=bastionhost-cn-st220aw****
&<Common request parameters>
```

Sample success responses

`XML` format

```
<ListHostAccountsResponse>
      <TotalCount>1</TotalCount>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <HostAccounts>
            <HostAccountName>abc</HostAccountName>
            <ProtocolName>SSH</ProtocolName>
            <PrivateKeyFingerprint>fe:ca:37:42:30:00:9d:95:e6:73:e5:b0:32:0a:**:**</PrivateKeyFingerprint>
            <HostId>1</HostId>
            <HasPassword>true</HasPassword>
            <HostAccountId>1</HostAccountId>
      </HostAccounts>
</ListHostAccountsResponse>
```

`JSON` format

```
{
    "TotalCount": "1",
    "RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
    "HostAccounts": [{
        "HostAccountName": "abc",
        "ProtocolName": "SSH",
        "PrivateKeyFingerprint": "fe:ca:37:42:30:00:9d:95:e6:73:e5:b0:32:0a:**:**",
        "HostId": "1",
        "HasPassword": "true",
        "HostAccountId": "1"
    }]
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

