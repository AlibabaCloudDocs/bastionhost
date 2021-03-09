# ListHostAccountsForUserGroup

调用ListHostAccountsForUserGroup接口查询指定用户组在指定主机下已授权的主机账户列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Yundun-bastionhost&api=ListHostAccountsForUserGroup&type=RPC&version=2019-12-09)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ListHostAccountsForUserGroup|需要执行的操作。

 取值：**ListHostAccountsForUserGroup**。 |
|HostId|String|是|1|指定要查询的主机账户的主机ID。

 **说明：** 您可以调用[ListHosts](~~200665~~)接口获取该参数。 |
|InstanceId|String|是|bastionhost-cn-st220aw\*\*\*\*|指定要查询已授权主机账户列表的用户组所在堡垒机的实例ID。

 **说明：** 您可以调用[DescribeInstances](~~153281~~)接口获取该参数。 |
|UserGroupId|String|是|1|指定要查询已授权主机账户列表的用户组ID。

 **说明：** 您可以调用[ListUserGroups](~~204509~~)接口获取该参数。 |
|RegionId|String|否|cn-hangzhou|指定要查询已授权主机账户列表的用户组所在堡垒机的区域ID。

 **说明：** 区域ID和区域名称的对应关系，请参见[地域和可用区](~~40654~~)。 |
|PageNumber|String|否|1|指定分页查询时，当前页的页码。默认值为**1**。 |
|PageSize|String|否|20|指定分页查询时，每页显示的数据最大条数。

 PageSize参数最大取值为100。每页默认显示的数据条数为20条，PageSize参数值为空时，将默认返回20条数据。

 **说明：** 建议PageSize取值不要为空。 |
|HostAccountName|String|否|root|指定要查询的主机账户名称。支持精确查询。 |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](~~148139~~)。

调用API的请求格式，请参见本文示例中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|HostAccounts|Array of Item| |查询到的主机账户列表。 |
|HostAccountId|String|1|主机账户ID。 |
|HostAccountName|String|host１|主机账户名称。 |
|HostId|String|１|主机账户所在主机的ID。 |
|IsAuthorized|Boolean|true|主机账户是否授权给当前用户组。取值：

 -   **true**：已授权
-   **false**：未授权 |
|ProtocolName|String|SSH|主机账户的协议名称。取值：

 -   **SSH**
-   **RDP** |
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|阿里云为该请求生成的唯一标识符。 |
|TotalCount|Integer|1|查询到的主机账户总数量。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=ListHostAccountsForUserGroup
&HostId=1
&InstanceId=bastionhost-cn-st220aw****
&UserGroupId=1
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<ListHostAccountsForUserGroupResponse>
      <TotalCount>1</TotalCount>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <HostAccounts>
            <HostAccountName>host１</HostAccountName>
            <ProtocolName>SSH</ProtocolName>
            <IsAuthorized>true</IsAuthorized>
            <HostId>１</HostId>
            <HostAccountId>1</HostAccountId>
      </HostAccounts>
</ListHostAccountsForUserGroupResponse>
```

`JSON`格式

```
{
	"TotalCount": "1",
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
	"HostAccounts": [{
		"HostAccountName": "host１",
		"ProtocolName": "SSH",
		"IsAuthorized": "true",
		"HostId": "１",
		"HostAccountId": "1"
	}]
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Yundun-bastionhost)查看更多错误码。

