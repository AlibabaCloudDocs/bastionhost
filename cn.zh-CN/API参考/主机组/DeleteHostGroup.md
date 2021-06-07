# DeleteHostGroup

调用DeleteHostGroup接口删除单个主机组。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Yundun-bastionhost&api=DeleteHostGroup&type=RPC&version=2019-12-09)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteHostGroup|需要执行的操作。

 取值：**DeleteHostGroup**。 |
|HostGroupId|String|是|1|指定要删除的主机组ID。

 **说明：** 您可以调用[ListHostGroups](~~201307~~)接口获取该参数。 |
|InstanceId|String|是|bastionhost-cn-st220aw\*\*\*\*|指定要删除的主机组所在堡垒机的实例ID。

 **说明：** 您可以调用[DescribeInstances](~~153281~~)接口获取该参数。 |
|RegionId|String|否|cn-hangzhou|指定要删除的主机组所在堡垒机的区域ID。

 **说明：** 区域ID和区域名称的对应关系，请参见[地域和可用区](~~40654~~)。 |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](~~148139~~)。

调用API的请求格式，请参见本文示例中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|阿里云为该请求生成的唯一标识符。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DeleteHostGroup
&HostGroupId=1
&InstanceId=bastionhost-cn-st220aw****
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<DeleteHostGroupResponse>
        <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
</DeleteHostGroupResponse>
```

`JSON`格式

```
{
    "RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Yundun-bastionhost)查看更多错误码。

