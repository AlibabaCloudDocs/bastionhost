# GetHost

调用GetHost接口获取指定主机的详细信息，包括主机名称、来源、主机地址、协议端口等信息。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Yundun-bastionhost&api=GetHost&type=RPC&version=2019-12-09)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|GetHost|需要执行的操作。

 取值：**GetHost**。 |
|HostId|String|是|1|指定要查询的主机ID。仅支持输入一个主机ID。

 **说明：** 您可以调用[ListHosts](~~200665~~)接口获取该参数。 |
|InstanceId|String|是|bastionhost-cn-st220aw\*\*\*\*|指定要查询的主机所在堡垒机的实例ID。

 **说明：** 您可以调用[DescribeInstances](~~153281~~)接口获取该参数。 |
|RegionId|String|否|cn-hangzhou|指定要查询的主机所在堡垒机的区域ID。

 **说明：** Region ID和区域名称的对应关系，请参见[地域和可用区](~~40654~~)。 |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](~~148139~~)。

调用API的请求格式，请参见本文示例中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Host|Struct| |查询到的主机信息。 |
|ActiveAddressType|String|Public|主机地址类型。取值：

 -   **Public** ：公网地址
-   **Private** ：私网地址 |
|Comment|String|host|主机的备注信息。 |
|HostId|String|1|主机ID。 |
|HostName|String|host|主机名称。 |
|HostPrivateAddress|String|192.168.XX.XX|主机的私网地址，可为域名或IP地址。 |
|HostPublicAddress|String|1.1.XX.XX|主机的公网地址，可为域名或IP地址。 |
|OSType|String|Linux|主机的操作系统。取值：

 -   **Linux**
-   **Windows** |
|Protocols|Array of Item| |主机的协议信息。 |
|HostFingerPrint|String|ssh-ed25519\|3e:46:5a:e1:1f:0d:39:7e:61:35:d5:fa:7b:2b:\*\*:\*\*|主机指纹信息，可以唯一标识一台主机。 |
|Port|Integer|22|主机的服务端口。 |
|ProtocolName|String|SSH|主机使用的协议名称。取值：

 -   **SSH**
-   **RDP** |
|Source|String|Local|主机的来源。取值：

 -   **Local**：本地主机
-   **Ecs**：ECS实例
-   **Rds**：RDS专属集群主机 |
|SourceInstanceId|String|i-bp19ienyt0yax748\*\*\*\*|主机对应的ECS实例ID或专属集群主机ID。

 **说明：** **Source**为**Local**时，该参数返回值为空。 |
|SourceInstanceState|String|Normal|主机状态。取值：

 -   **Normal** ：正常

 -   **Release**： 已释放 |
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|阿里云为该请求生成的唯一标识符。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=GetHost
&HostId=1
&InstanceId=bastionhost-cn-st220aw****
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<GetHostResponse>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <Host>
            <Comment>host</Comment>
            <Protocols>
                  <ProtocolName>SSH</ProtocolName>
                  <HostFingerPrint></HostFingerPrint>
                  <Port>22</Port>
            </Protocols>
            <ActiveAddressType>Public</ActiveAddressType>
            <HostPrivateAddress>192.168.XX.XX</HostPrivateAddress>
            <HostPublicAddress>1.1.XX.XX</HostPublicAddress>
            <OSType>Linux</OSType>
            <HostId>1</HostId>
            <SourceInstanceId>i-bp19ienyt0yax748****</SourceInstanceId>
            <HostName>host</HostName>
            <SourceInstanceState>Normal</SourceInstanceState>
            <Source>Local</Source>
      </Host>
</GetHostResponse>
```

`JSON`格式

```
{
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
	"Host": {
		"Comment": "host",
		"Protocols": [{
			"ProtocolName": "SSH",
			"HostFingerPrint": "",
			"Port": "22"
		}],
		"ActiveAddressType": "Public",
		"HostPrivateAddress": "192.168.XX.XX",
		"HostPublicAddress": "1.1.XX.XX",
		"OSType": "Linux",
		"HostId": "1",
		"SourceInstanceId": "i-bp19ienyt0yax748****",
		"HostName": "host",
		"SourceInstanceState": "Normal",
		"Source": "Local"
	}
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Yundun-bastionhost)查看更多错误码。

