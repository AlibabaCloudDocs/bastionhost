# ListHosts

调用ListHosts接口查询指定堡垒机实例下的主机列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Yundun-bastionhost&api=ListHosts&type=RPC&version=2019-12-09)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ListHosts|需要执行的操作。

 取值：**ListHosts**。 |
|InstanceId|String|是|bastionhost-cn-st220aw\*\*\*\*|指定要查询主机的堡垒机实例ID。

 **说明：** 您可以调用[DescribeInstances](~~153281~~)接口获取该参数。 |
|RegionId|String|否|cn-hangzhou|指定要查询主机的堡垒机所在区域的ID。

 **说明：** 区域ID和区域名称的对应关系，请参见[地域和可用区](~~40654~~)。 |
|PageNumber|String|否|1|指定分页查询时，当前页的页码。默认值为**1**。 |
|PageSize|String|否|20|指定分页查询时，每页显示的数据最大条数。

 PageSize参数最大取值为100。每页默认显示的数据条数为20条，PageSize参数值为空时，将默认返回20条数据。

 **说明：** 建议PageSize取值不要为空。 |
|OSType|String|否|Linux|指定要查询的主机的操作系统。取值：

 -   **Linux**
-   **Windows** |
|HostName|String|否|host|指定要查询的主机名称。不支持模糊查询，只支持精确查询。 |
|HostAddress|String|否|1.1.XX.XX|指定要查询的主机地址，可使用域名或IP地址。不支持模糊查询，只支持精确查询。 |
|Source|String|否|Local|指定要查询主机的来源。取值：

 -   **Local**：本地主机
-   **Ecs**：ECS实例
-   **Rds**：RDS专属集群主机 |
|SourceInstanceId|String|否|i-bp19ienyt0yax748\*\*\*\*|指定要查询的主机对应的ECS实例ID或专属集群主机ID。不支持模糊查询，只支持精确查询。 |
|SourceInstanceState|String|否|Normal|指定要查询的主机状态。取值：

 -   **Normal**：正常

 -   **Release**：已释放 |
|HostGroupId|String|否|1|指定要查询的主机所在主机组的ID。

 **说明：** 您可以调用[ListHostGroups](~~201307~~)接口获取主机组ID。 |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](~~148139~~)。

调用API的请求格式，请参见本文示例中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Hosts|Array of Item| |查询到的主机列表。 |
|ActiveAddressType|String|Public|主机地址类型。取值：

 -   **Public** ：公网地址
-   **Private** ：私网地址 |
|Comment|String|host|主机的备注信息。 |
|HostAccountCount|Integer|1|主机账号数。 |
|HostId|String|1|主机ID。 |
|HostName|String|name|主机名称。 |
|HostPrivateAddress|String|192.168.XX.XX|主机的私网地址，可为域名或IP地址。 |
|HostPublicAddress|String|1.1.XX.XX|主机的公网地址，可为域名或IP地址。 |
|OSType|String|Linux|主机的操作系统。取值：

 -   **Linux**
-   **Windows** |
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
|TotalCount|Integer|1|查询到的主机总数量。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=ListHosts
&InstanceId=bastionhost-cn-st220aw****
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<ListHostsResponse>
      <Hosts>
            <Comment>host</Comment>
            <ActiveAddressType>Public</ActiveAddressType>
            <HostPrivateAddress>192.168.XX.XX</HostPrivateAddress>
            <HostPublicAddress>1.1.XX.XX</HostPublicAddress>
            <OSType>Linux</OSType>
            <HostId>1</HostId>
            <HostAccountCount>1</HostAccountCount>
            <SourceInstanceId>i-bp19ienyt0yax748****</SourceInstanceId>
            <SourceInstanceState>Normal</SourceInstanceState>
            <HostName>name</HostName>
            <Source>Local</Source>
      </Hosts>
      <TotalCount>1</TotalCount>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
</ListHostsResponse>
```

`JSON`格式

```
{
	"Hosts": [{
		"Comment": "host",
		"ActiveAddressType": "Public",
		"HostPrivateAddress": "192.168.XX.XX",
		"HostPublicAddress": "1.1.XX.XX",
		"OSType": "Linux",
		"HostId": "1",
		"HostAccountCount": "1",
		"SourceInstanceId": "i-bp19ienyt0yax748****",
		"SourceInstanceState": "Normal",
		"HostName": "name",
		"Source": "Local"
	}],
	"TotalCount": "1",
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE"
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost)查看更多错误码。

