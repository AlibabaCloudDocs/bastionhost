# ListHostAccountsForUserGroup

Queries the host accounts that a specified user group is authorized to manage on a specified host.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=ListHostAccountsForUserGroup&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ListHostAccountsForUserGroup|The operation that you want to perform.

 Set the value to **ListHostAccountsForUserGroup**. |
|HostId|String|Yes|1|The ID of the host for which you want to query the host accounts that the user group is authorized to manage.

 **Note:** You can call the [ListHosts](~~200665~~) operation to query the ID of the host. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance where you want to query the host accounts that the user group is authorized to manage on the host.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|UserGroupId|String|Yes|1|The ID of the user group for which you want to query authorized host accounts.

 **Note:** You can call the [ListUserGroups](~~204509~~) operation to query the ID of the user group. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance where you want to query the host accounts that the user group is authorized to manage on the host.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |
|PageNumber|String|No|1|The number of the page to return. Default value: **1**. |
|PageSize|String|No|20|The number of entries to return on each page.

 The value of the PageSize parameter must not exceed 100. Default value: 20. If you leave the PageSize parameter empty, 20 entries are returned on each page.

 **Note:** We recommend that you do not leave the PageSize parameter empty. |
|HostAccountName|String|No|root|The name of the host account that you want to query. Exact match is supported. |

All Bastionhost API requests must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section of this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|HostAccounts|Array of Item| |The host accounts returned. |
|HostAccountId|String|1|The ID of the host account. |
|HostAccountName|String|host1|The name of the host account. |
|HostId|String|1|The ID of the host for which the host accounts were queried. |
|IsAuthorized|Boolean|true|Indicates whether the user group is authorized to manage the host account. Valid values:

 -   **true**: The user group is authorized to manage the host account.
-   **false**: The user group is not authorized to manage the host account. |
|ProtocolName|String|SSH|The protocol that is used by the host account. Valid values:

 -   **SSH**
-   **RDP** |
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|The ID of the request. |
|TotalCount|Integer|1|The total number of host accounts returned. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=ListHostAccountsForUserGroup
&HostId=1
&InstanceId=bastionhost-cn-st220aw****
&UserGroupId=1
&<Common request parameters>
```

Sample success responses

`XML` format

```
<ListHostAccountsForUserGroupResponse>
      <TotalCount>1</TotalCount>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <HostAccounts>
            <HostAccountName>host1</HostAccountName>
            <ProtocolName>SSH</ProtocolName>
            <IsAuthorized>true</IsAuthorized>
            <HostId>1</HostId>
            <HostAccountId>1</HostAccountId>
      </HostAccounts>
</ListHostAccountsForUserGroupResponse>
```

`JSON` format

```
{
	"TotalCount": "1",
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
	"HostAccounts": [{
		"HostAccountName": "host1",
		"ProtocolName": "SSH",
		"IsAuthorized": "true",
		"HostId": "1",
		"HostAccountId": "1"
	}]
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

