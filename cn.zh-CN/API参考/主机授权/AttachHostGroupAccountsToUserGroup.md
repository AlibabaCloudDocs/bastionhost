# AttachHostGroupAccountsToUserGroup

调用AttachHostGroupAccountsToUserGroup接口为用户组授权主机组和主机账号。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Yundun-bastionhost&api=AttachHostGroupAccountsToUserGroup&type=RPC&version=2019-12-09)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|AttachHostGroupAccountsToUserGroup|需要执行的操作。

 取值：**AttachHostGroupAccountsToUserGroup**。 |
|HostGroups|String|是|\[ \{"HostGroupId":"1"\}, \{"HostGroupId":"2","HostAccountNames":\["root","111","abc"\]\}, \{"HostGroupId":"3","HostAccountNames":\["root","111","abc"\]\}, \{"HostGroupId":"4","HostAccountNames":\["root","111","abc"\]\}\]|指定要为用户组授权的主机组ID和主机账户名称。最多支持设置10个主机组ID，每个主机组最多支持设置10个主机账户名称。您可以不设置主机账户名称，不设置主机账户名称表示仅为用户组授权主机组。该参数的具体结构请参考请求参数列表下的HostGroups参数结构说明。

 **说明：** 您可以调用[ListHostGroups](~~201307~~)接口获取主机组ID，调用[ListHostAccounts](~~204372~~)接口获取主机账户名称。 |
|InstanceId|String|是|bastionhost-cn-st220aw\*\*\*\*|指定要授权主机组和主机账户的用户组所在堡垒机的实例ID。

 **说明：** 您可以调用[DescribeInstances](~~153281~~)接口获取该参数。 |
|UserGroupId|String|是|1|指定要授权主机组和主机账户的用户组ID。

 **说明：** 您可以调用[ListUserGroups](~~204509~~)接口获取该参数。 |
|RegionId|String|否|cn-hangzhou|指定要授权主机和主机账户的用户组所在堡垒机的区域ID。

 **说明：** 区域ID和区域名称的对应关系，请参见[地域和可用区](~~40654~~)。 |

HostGroups参数结构说明

|字段

|类型

|示例值

|描述 |
|----|----|-----|----|
|HostGroupId

|string

|1

|主机组ID。 |
|HostAccountNames

|array\[string\]

|\["root","111","abc"\]

|主机账户名称。该参数为Json格式的字符串，最多可设置10个主机账户名称。 |

以下是该参数的取值示例。

```
 
[
{"HostGroupId":"1"}, 
{"HostGroupId":"2","HostAccountNames":["root","111","abc"]}, 
{"HostGroupId":"3","HostAccountNames":["root","111","abc"]},  
{"HostGroupId":"4","HostAccountNames":["root","111","abc"]} 
]

```

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](~~148139~~)。

调用API的请求格式，请参见本文示例中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|阿里云为该请求生成的唯一标识符。 |
|Results|Array of Item| |接口的调用结果。 |
|Code|String|OK|接口的调用结果信息。取值：

 -   **OK**：操作成功。
-   **UNEXPECTED**：未知错误。
-   **INVALID\_ARGUMENT**：请求参数设置错误。
-   **OBJECT\_NOT\_FOUND**：操作的对象不存在。
-   **OBJECT\_AlREADY\_EXISTS** ：操作的对象已存在。 |
|HostAccountNames|Array of Item| |为用户组授权主机账户名称操作返回的结果信息。 |
|Code|String|OK|为用户组授权主机账户名称操作返回的结果。取值：

 -   **OK**：操作成功。
-   **UNEXPECTED**：未知错误。
-   **INVALID\_ARGUMENT**：请求参数设置错误。
-   **OBJECT\_NOT\_FOUND**：操作的对象不存在。
-   **OBJECT\_AlREADY\_EXISTS** ：操作的对象已存在。 |
|HostAccountName|String|abc|主机账户名称。 |
|Message|String|无|该参数已废弃，无需关注。 |
|HostGroupId|String|1|主机组ID。 |
|Message|String|无|该参数已废弃，无需关注。 |
|UserGroupId|String|1|用户组ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=AttachHostGroupAccountsToUserGroup
&HostGroups=[ {"HostGroupId":"1"}, {"HostGroupId":"2","HostAccountNames":["root","111","abc"]}, {"HostGroupId":"3","HostAccountNames":["root","111","abc"]}, {"HostGroupId":"4","HostAccountNames":["root","111","abc"]}]
&InstanceId=bastionhost-cn-st220aw****
&UserGroupId=1
&<公共请求参数>
```

正常返回示例

`XML`格式

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

`JSON`格式

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

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Yundun-bastionhost)查看更多错误码。

