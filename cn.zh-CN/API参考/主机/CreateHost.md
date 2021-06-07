# CreateHost

调用CreateHost接口在堡垒机中创建需要运维的主机。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Yundun-bastionhost&api=CreateHost&type=RPC&version=2019-12-09)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateHost|需要执行的操作。

 取值：**CreateHost**。 |
|ActiveAddressType|String|是|Public|指定新创建主机的地址类型。取值：

 -   **Public**：公网地址
-   **Private**：私网地址 |
|HostName|String|是|host01|指定新创建主机的名称，最多支持128字符。 |
|InstanceId|String|是|bastionhost-cn-st220aw\*\*\*\*|指定新创建主机所在堡垒机的实例ID。

 **说明：** 您可以调用[DescribeInstances](~~153281~~)接口获取该参数。 |
|OSType|String|是|Linux|指定新创建主机的操作系统。取值：

 -   **Linux**
-   **Windows** |
|Source|String|是|Local|指定新创建主机的来源。取值：

 -   **Local**：本地主机
-   **Ecs**：ECS实例
-   **Rds**：RDS专属集群主机 |
|RegionId|String|否|cn-hangzhou|指定新创建主机所在堡垒机的区域ID。

 **说明：** Region ID和区域名称的对应关系，请参见[地域和可用区](~~40654~~)。 |
|HostPublicAddress|String|否|172.16.XX.XX|指定新创建主机的公网地址，可使用域名或IP地址。

 **说明：** **ActiveAddressType**选择**Public**时，该参数为必填项。 |
|HostPrivateAddress|String|否|192.168.XX.XX|指定新创建主机的私网地址，可使用域名或IP地址。

 **说明：** **ActiveAddressType**选择**Private**时，该参数为必填项。 |
|Comment|String|否|Local Host|指定主机的备注信息，最多支持500字符。 |
|SourceInstanceId|String|否|i-dfabfda|指定新创建的ECS实例ID或专属集群主机ID。

 **说明：** **Source**选择**Ecs**或**Rds**时，该参数为必填项。 |
|InstanceRegionId|String|否|cn-hangzhou|指定新创建的ECS实例或专属集群主机所属区域ID。

 **说明：** **Source**选择**Ecs**或**Rds**时，该参数为必填项。 |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](~~148139~~)。

调用API的请求格式，请参见本文示例中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|HostId|String|1|新创建主机的ID。 |
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|阿里云为该请求生成的唯一标识符。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=CreateHost
&ActiveAddressType=Public
&HostName=host01
&InstanceId=bastionhost-cn-st220aw****
&OSType=Linux
&Source=Local
&HostPublicAddress=172.16.XX.XX
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<CreateHostResponse>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <HostId>1</HostId>
</CreateHostResponse>
```

`JSON`格式

```
{
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
	"HostId": "1"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Yundun-bastionhost)查看更多错误码。

