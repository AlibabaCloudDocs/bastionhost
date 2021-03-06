# AttachHostAccountsToUser

Authorizes a specified user to manage specified hosts and host accounts.

****

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=AttachHostAccountsToUser&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|AttachHostAccountsToUser|The operation that you want to perform.

 Set the value to **AttachHostAccountsToUser**. |
|Hosts|String|Yes|\[ \{"HostId":"1"\}, \{"HostId":"2","HostAccountIds":\["1","2","3"\]\}, \{"HostId":"3","HostAccountIds":\["4","5","6"\]\}, \{"HostId":"4","HostAccountIds":\["9","8","7"\]\} \]|The IDs of the host and host account that you want to authorize the user to manage. You can specify up to 10 host IDs and up to 10 host account IDs for each host. You can leave the host account ID empty, which indicates that the user is authorized to manage only the specified hosts. For more information about this parameter, see the "Description of the Hosts parameter" section of this topic.

 **Note:** You can call the [ListHosts](~~200665~~) operation to query the ID of the host and the [ListHostAccounts](~~204372~~) operation to query the ID of the host account. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance where you want to authorize the user to manage the specified hosts and host accounts.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|UserId|String|Yes|1|The ID of the user that you want to authorize to manage the specified hosts and host accounts.

 **Note:** You can call the [ListUsers](~~204522~~) operation to query the ID of the user ID. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance where you want to authorize the user to manage the specified hosts and host accounts.

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
|Results|Array of Item| |The call result of the operation. |
|Code|String|OK|The return code that indicates whether the call was successful. Valid values:

 -   **OK**: The call was successful.
-   **UNEXPECTED**: An unknown error has occurred.
-   **INVALID\_ARGUMENT**: A request parameter is invalid.
-   **OBJECT\_NOT\_FOUND**: The specified user is invalid.
-   **OBJECT\_AlREADY\_EXISTS**: The specified user has been authorized to manage the specified host. |
|HostAccounts|Array of Item| |The result of authorizing the specified user to manage the specified host accounts. |
|Code|String|OK|The return code that indicates whether the specified user was authorized to manage the specified host account. Valid values:

 -   **OK**: The specified user was authorized to manage the specified host account.
-   **UNEXPECTED**: An unknown error has occurred.
-   **INVALID\_ARGUMENT**: A request parameter is invalid.
-   **OBJECT\_NOT\_FOUND**: The specified host account is invalid.
-   **OBJECT\_AlREADY\_EXISTS**: The specified user has been authorized to manage the specified host account. |
|HostAccountId|String|1|The ID of the host account. |
|Message|String|N/A|This parameter is obsolete. |
|HostId|String|1|The ID of the host. |
|Message|String|N/A|This parameter is obsolete. |
|UserId|String|1|The ID of the user. |
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=AttachHostAccountsToUser
&Hosts=[ {"HostId":"1"}, {"HostId":"2","HostAccountIds":["1","2","3"]}, {"HostId":"3","HostAccountIds":["4","5","6"]}, {"HostId":"4","HostAccountIds":["9","8","7"]}  ]
&InstanceId=bastionhost-cn-st220aw****
&UserId=1
&<Common request parameters>
```

Sample success responses

`XML` format

```
<AttachHostAccountsToUserResponse>
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
</AttachHostAccountsToUserResponse>
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

