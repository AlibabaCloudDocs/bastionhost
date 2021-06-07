# ModifyHostsActiveAddressType

调用ModifyHostsActiveAddressType接口修改运维主机时使用的连接地址类型。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Yundun-bastionhost&api=ModifyHostsActiveAddressType&type=RPC&version=2019-12-09)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ModifyHostsActiveAddressType|需要执行的操作。

 取值：**ModifyHostsActiveAddressType**。 |
|ActiveAddressType|String|是|Private|指定修改后的主机连接地址的类型。取值：

 -   **Public**：公网
-   **Private**：私网 |
|HostIds|String|是|\["1","2"\]|指定要修改连接地址类型的主机ID。该参数为Json格式的字符串，最多可输入100个主机ID。

 **说明：** 您可以调用[ListHosts](~~200665~~)接口获取该参数。 |
|InstanceId|String|是|bastionhost-cn-st220aw\*\*\*\*|指定要修改连接地址类型的主机所在堡垒机的实例ID。

 **说明：** 您可以调用[DescribeInstances](~~153281~~)接口获取该参数。 |
|RegionId|String|否|cn-hangzhou|指定要修改连接地址类型的主机所在堡垒机的区域ID。

 **说明：** 区域ID和区域名称的对应关系，请参见[地域和可用区](~~40654~~)。 |

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
|HostId|String|1|主机ID。 |
|Message|String|无|该参数已废弃，无需关注。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=ModifyHostsActiveAddressType
&ActiveAddressType=Private
&HostIds= ["1","2"]
&InstanceId=bastionhost-cn-st220aw****
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<ModifyHostsActiveAddressTypeResponse>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <Results>
           <Message></Message>
            <HostId>1</HostId>
            <Code>OK</Code>
      </Results>
</ModifyHostsActiveAddressTypeResponse>
```

`JSON`格式

```
{
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
	"Results": [{
		"Message": "",
		"HostId": "1",
		"Code": "OK"
	}]
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost)查看更多错误码。

