# CreateHostAccount

调用CreateHostAccount接口为指定主机创建主机账户。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Yundun-bastionhost&api=CreateHostAccount&type=RPC&version=2019-12-09)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateHostAccount|需要执行的操作。

 取值：**CreateHostAccount**。 |
|HostAccountName|String|是|abc|指定新建主机账户的名称，最长支持128字符。 |
|HostId|String|是|1|指定要创建主机账户的主机ID。

 **说明：** 您可以调用[ListHosts](~~200665~~)接口获取该参数。 |
|InstanceId|String|是|bastionhost-cn-st220aw\*\*\*\*|指定要创建主机账户的主机所在堡垒机的实例ID。

 **说明：** 您可以调用[DescribeInstances](~~153281~~)接口获取该参数。 |
|ProtocolName|String|是|SSH|指定新建主机账户的协议名称。取值：

 -   **SSH**
-   **RDP** |
|RegionId|String|否|cn-hangzhou|指定要创建主机账户的主机所在堡垒机的区域ID。

 **说明：** 区域ID和区域名称的对应关系，请参见[地域和可用区](~~40654~~)。 |
|Password|String|否|\*\*\*\*|指定新建主机账户的密码。 |
|PrivateKey|String|否|\*\*\*\*|指定新建主机账户的私钥，即使用Base64编码后的字符串。

 **说明：** 主机账户协议**ProtocolName**为**SSH**时，该参数生效。**ProtocolName**为**RDP**时，无需配置该参数。支持同时为主机账户配置密码和私钥。在连接资产时，堡垒机会优先使用私钥进行连接。 |
|PassPhrase|String|否|\*\*\*\*|指定新建主机账户的私钥口令。

 **说明：** 主机账户协议**ProtocolName**为**SSH**时，您可以配置该参数。**ProtocolName**为**RDP**时，无需配置该参数。 |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](~~148139~~)。

调用API的请求格式，请参见本文示例中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|HostAccountId|String|1|主机账户ID。 |
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|阿里云为该请求生成的唯一标识符。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=CreateHostAccount
&HostAccountName=abc
&HostId=1
&InstanceId=bastionhost-cn-st220aw****
&ProtocolName=SSH
&Password=****
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<CreateHostAccountResponse>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <HostAccountId>1</HostAccountId>
</CreateHostAccountResponse>
```

`JSON`格式

```
{
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
	"HostAccountId": "1"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Yundun-bastionhost)查看更多错误码。

