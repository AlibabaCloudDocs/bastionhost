# AttachHostGroupAccountsToUserGroup

Authorizes a specified user group to manage specified host groups and host accounts.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=AttachHostGroupAccountsToUserGroup&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|AttachHostGroupAccountsToUserGroup|The operation that you want to perform.

 Set the value to **AttachHostGroupAccountsToUserGroup**. |
|HostGroups|String|Yes|\[ \{"HostGroupId":"1"\}, \{"HostGroupId":"2","HostAccountNames":\["root","111","abc"\]\}, \{"HostGroupId":"3","HostAccountNames":\["root","111","abc"\]\}, \{"HostGroupId":"4","HostAccountNames":\["root","111","abc"\]\}\]|The ID of the host group and the name of the host account that you want to authorize the user group to manage. You can specify up to 10 host group IDs and up to 10 host account names for each host group. You can leave the host account name empty, which indicates that the user group is authorized to manage only the specified host groups. For more information about this parameter, see the "Description of the HostGroups parameter" section of this topic.

 **Note:** You can call the [ListHostGroups](~~201307~~) operation to query the ID of the host group and the [ListHostAccounts](~~204372~~) operation to query the name of the host account. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance where you want to authorize the user group to manage the specified host groups and host accounts.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|UserGroupId|String|Yes|1|The ID of the user group that you want to authorize to manage the specified host groups and host accounts.

 **Note:** You can call the [ListUserGroups](~~204509~~) operation to query the ID of the user group. |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance where you want to authorize the user group to manage the specified host groups and host accounts.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |

Description of the HostGroups parameter

|Parameter

|Type

|Example

|Description |
|-----------|------|---------|-------------|
|HostGroupId

|string

|1

|The ID of the host group. |
|HostAccountNames

|array\[string\]

|\["root","111","abc"\]

|The name of the host account. The value is a JSON string. You can specify up to 10 host account names for each host group. |

The following sample code provides an example of the settings of the HostGroups parameter:

```
 
[
{"HostGroupId":"1"}, 
{"HostGroupId":"2","HostAccountNames":["root","111","abc"]}, 
{"HostGroupId":"3","HostAccountNames":["root","111","abc"]},  
{"HostGroupId":"4","HostAccountNames":["root","111","abc"]} 
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
-   **OBJECT\_NOT\_FOUND**: The specified user group is invalid.
-   **OBJECT\_AlREADY\_EXISTS**: The specified user group has been authorized to manage the specified host group. |
|HostAccountNames|Array of Item| |The result of authorizing the specified user group to manage the specified host accounts. |
|Code|String|OK|The return code that indicates whether the specified user group was authorized to manage the specified host account. Valid values:

 -   **OK**: The specified user group was authorized to manage the specified host account.
-   **UNEXPECTED**: An unknown error has occurred.
-   **INVALID\_ARGUMENT**: A request parameter is invalid.
-   **OBJECT\_NOT\_FOUND**: The specified host account is invalid.
-   **OBJECT\_AlREADY\_EXISTS**: The specified user group has been authorized to manage the specified host account. |
|HostAccountName|String|abc|The name of the host account. |
|Message|String|N/A|This parameter is obsolete. |
|HostGroupId|String|1|The ID of the host group. |
|Message|String|N/A|This parameter is obsolete. |
|UserGroupId|String|1|The ID of the user group. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=AttachHostGroupAccountsToUserGroup
&HostGroups=[ {"HostGroupId":"1"}, {"HostGroupId":"2","HostAccountNames":["root","111","abc"]}, {"HostGroupId":"3","HostAccountNames":["root","111","abc"]}, {"HostGroupId":"4","HostAccountNames":["root","111","abc"]}]
&InstanceId=bastionhost-cn-st220aw****
&UserGroupId=1
&<Common request parameters>
```

Sample success responses

`XML` format

```
<AttachHostGroupAccountsToUserGroupResponse>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <Results>
            <Message></Message>
            <HostGroupId>1</HostGroupId>
            <Code>OK</Code>
            <UserGroupId>1</UserGroupId>
      </Results>
      <Results>
            <HostAccountNames>
                  <HostAccountName>abc</HostAccountName>
                  <Message></Message>
                  <Code>OK</Code>
            </HostAccountNames>
      </Results>
</AttachHostGroupAccountsToUserGroupResponse>
```

`JSON` format

```
{
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
	"Results": [{
		"Message": "",
		"HostGroupId": "1",
		"Code": "OK",
		"UserGroupId": "1"
	}, {
		"HostAccountNames": [{
			"HostAccountName": "abc",
			"Message": "",
			"Code": "OK"
		}]
	}]
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

