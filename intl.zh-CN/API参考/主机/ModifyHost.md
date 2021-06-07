# ModifyHost

调用ModifyHost接口修改主机基本信息，支持修改主机的地址、名称、操作系统类型和备注信息。

该接口支持修改本地主机、ECS主机、RDS专属集群主机的基本信息。

**说明：** 如果您修改了ECS主机或RDS专属集群主机的基本信息，由于堡垒机系统会定期同步ECS主机、RDS专属集群主机的基本信息，修改结果可能会被ECS主机或RDS专属集群主机所同步的基本信息覆盖。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Yundun-bastionhost&api=ModifyHost&type=RPC&version=2019-12-09)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ModifyHost|需要执行的操作。

 取值：**ModifyHost**。 |
|HostId|String|是|1|指定要修改的主机ID。

 **说明：** 您可以调用[ListHosts](~~200665~~)接口获取该参数。 |
|InstanceId|String|是|bastionhost-cn-st220aw\*\*\*\*|指定要修改的主机所在堡垒机的实例ID。

 **说明：** 您可以调用[DescribeInstances](~~153281~~)接口获取该参数。 |
|RegionId|String|否|cn-hangzhou|指定要修改的主机所在堡垒机的区域ID。

 **说明：** Region ID和区域名称的对应关系，请参见[地域和可用区](~~40654~~)。 |
|HostPrivateAddress|String|否|193.168.XX.XX|指定修改后主机的私网地址，可使用域名或IP地址。 |
|HostPublicAddress|String|否|200.1.XX.XX|指定修改后主机的公网地址，可使用域名或IP地址。 |
|OSType|String|否|Linux|指定修改后主机的操作系统类型。取值：

 -   **Linux**
-   **Windows** |
|HostName|String|否|TestHost|指定修改后主机的名称，最多支持128字符。 |
|Comment|String|否|Host for test.|指定修改后主机的备注信息，最多支持500字符。 |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](~~148139~~)。

调用API的请求格式，请参见本文示例中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|阿里云为该请求生成的唯一标识符。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=ModifyHost
&HostId=1
&InstanceId=bastionhost-cn-st220aw****
&HostPublicAddress=200.1.XX.XX
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<ModifyHostResponse>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
</ModifyHostResponse>
```

`JSON`格式

```
{
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE"
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost)查看更多错误码。

