# DetachHostAccountsFromUser

Revokes permissions on specified hosts and host accounts from a specified user.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=DetachHostAccountsFromUser&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DetachHostAccountsFromUser|The operation that you want to perform.

Set the value to **DetachHostAccountsFromUser**. |
|Hosts|String|Yes|\[ \{"HostId":"1"\}, \{"HostId":"2","HostAccountIds":\["1","2","3"\]\}, \{"HostId":"3","HostAccountIds":\["4","5","6"\]\}, \{"HostId":"4","HostAccountIds":\["9","8","7"\]\} \]|The IDs of the host and host account on which you want to revoke permissions from the user. You can specify up to 10 host IDs and up to 10 host account IDs for each host. You can leave the host account ID empty, which indicates that permissions on the specified hosts and all host accounts on the hosts are revoked from the user. For more information about this parameter, see the "Description of the Hosts parameter" section of this topic.

**Note:** You can call the [ListHosts](~~200665~~) operation to query the ID of the host and the [ListHostAccounts](~~204372~~) operation to query the ID of the host account. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance where you want to revoke permissions on the specified hosts and host accounts from the user.

**Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|UserId|String|Yes|1|The ID of the user from which you want to revoke permissions on the specified hosts and host accounts.

**Note:** You can call the [ListUsers](~~204522~~) operation to query the ID of the user ID. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance where you want to revoke permissions on the specified hosts and host accounts from the user.

**Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |

Description of the Hosts parameter

|Parameter

|Type

|Example

|Description |
|-----------|------|---------|-------------|
|HostId

|string

|1

|The ID of the host. |
|HostAccountIds

|array\[string\]

|\["9","8","7"\]

|The ID of the host account. The value is a JSON string. You can specify up to 10 host account IDs for each host. |

The following sample code provides an example of the settings of the Hosts parameter:

```
 
[
{"HostId":"1"},
{"HostId":"2","HostAccountIds":["1","2","3",...]},
{"HostId":"3","HostAccountIds":["4","5","6",...]},
{"HostId":"4","HostAccountIds":["9","8","7",...]}
]
            
```

All Bastionhost API requests must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section of this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|The ID of the request. |
|Results|Array of Item| |The call result of the operation. |
|Code|String|OK|The return code that indicates whether the call was successful. Valid values:

-   **OK**: The call was successful.
-   **UNEXPECTED**: An unknown error has occurred.
-   **INVALID\_ARGUMENT**: A request parameter is invalid.
-   **OBJECT\_NOT\_FOUND**: The specified user is invalid.
-   **OBJECT\_AlREADY\_EXISTS**: Permissions on the specified host have been revoked from the specified user. |
|HostAccounts|Array of Item| |The result of revoking permissions on the specified host accounts from the specified user. |
|Code|String|OK|The return code that indicates whether permissions on the specified host account were revoked from the specified user. Valid values:

-   **OK**: Permissions on the specified host account were revoked from the specified user.
-   **UNEXPECTED**: An unknown error has occurred.
-   **INVALID\_ARGUMENT**: A request parameter is invalid.
-   **OBJECT\_NOT\_FOUND**: The specified host account is invalid.
-   **OBJECT\_AlREADY\_EXISTS**: Permissions on the specified host account have been revoked from the specified user. |
|HostAccountId|String|1|The ID of the host account. |
|Message|String|N/A|This parameter is obsolete. |
|HostId|String|1|The ID of the host. |
|Message|String|N/A|This parameter is obsolete. |
|UserId|String|1|The ID of the user. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=DetachHostAccountsFromUser
&Hosts=[ {"HostId":"1"}, {"HostId":"2","HostAccountIds":["1","2","3"]}, {"HostId":"3","HostAccountIds":["4","5","6"]}, {"HostId":"4","HostAccountIds":["9","8","7"]} ]
&InstanceId=bastionhost-cn-st220aw****
&UserId=1
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DetachHostAccountsFromUserResponse>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <Results>
            <Message></Message>
            <HostId>1</HostId>
            <Code>OK</Code>
            <UserId>1</UserId>
      </Results>
      <Results>
            <HostAccounts>
                  <Message></Message>
                  <Code>OK</Code>
                  <HostAccountId>1</HostAccountId>
            </HostAccounts>
      </Results>
</DetachHostAccountsFromUserResponse>
```

`JSON` format

```
{
    "RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
    "Results": [
        {
            "Message": "",
            "HostId": 1,
            "Code": "OK",
            "UserId": 1
        },
        {
            "HostAccounts": {
                "Message": "",
                "Code": "OK",
                "HostAccountId": 1
            }
        }
    ]
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

