# ListHostGroups

调用ListHostGroups接口获取指定堡垒机下的主机组列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Yundun-bastionhost&api=ListHostGroups&type=RPC&version=2019-12-09)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ListHostGroups|需要执行的操作。

 取值：**ListHostGroups**。 |
|InstanceId|String|是|bastionhost-cn-st220aw\*\*\*\*|指定要查询的堡垒机的实例ID。

 **说明：** 您可以调用[DescribeInstances](~~153281~~)接口获取该参数。 |
|RegionId|String|否|cn-hangzhou|指定要查询的堡垒机的区域ID。

 **说明：** 区域ID和区域名称的对应关系，请参见[地域和可用区](~~40654~~)。 |
|PageNumber|String|否|1|指定分页查询时，当前页的页码。默认值为**1**。 |
|PageSize|String|否|20|指定分页查询时，每页显示的数据最大条数。

 PageSize参数最大取值为100。每页默认显示的数据条数为20条，PageSize参数值为空时，将默认返回20条数据。

 **说明：** 建议PageSize取值不要为空。 |
|HostGroupName|String|否|主机组1|指定要查询的主机组名称，不支持模糊查询，只支持精确查询。 |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](~~148139~~)。

调用API的请求格式，请参见本文示例中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|HostGroups|Array of Item| |查询到的主机组列表。 |
|Comment|String|备注|主机组的备注信息。 |
|HostGroupId|String|1|主机组ID。 |
|HostGroupName|String|主机组1|主机组名称。 |
|MemberCount|Integer|1|主机组内的主机数量。 |
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|阿里云为该请求生成的唯一标识符。 |
|TotalCount|Integer|1|查询到的主机组总数量。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=ListHostGroups
&InstanceId=bastionhost-cn-st220aw****
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<ListHostGroupsResponse>
      <TotalCount>1</TotalCount>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <HostGroups>
            <Comment>备注</Comment>
            <MemberCount>1</MemberCount>
            <HostGroupId>1</HostGroupId>
            <HostGroupName>主机组1</HostGroupName>
      </HostGroups>
</ListHostGroupsResponse>
```

`JSON`格式

```
{
	"TotalCount": "1",
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
	"HostGroups": [{
		"Comment": "备注",
		"HostGroupId": "1",
		"MemberCount": "1",
		"HostGroupName": "主机组1"
	}]
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost)查看更多错误码。

