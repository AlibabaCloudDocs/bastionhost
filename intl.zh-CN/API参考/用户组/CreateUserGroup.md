# CreateUserGroup

调用CreateUserGroup接口创建堡垒机用户组。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Yundun-bastionhost&api=CreateUserGroup&type=RPC&version=2019-12-09)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateUserGroup|需要执行的操作。

 取值：**CreateUserGroup**。 |
|InstanceId|String|是|bastionhost-cn-st220aw\*\*\*\*|指定新创建用户组的堡垒机的实例ID。

 **说明：** 您可以调用[DescribeInstances](~~153281~~)接口获取该参数。 |
|UserGroupName|String|是|group|指定新创建的用户组名称。最多支持128字符。 |
|RegionId|String|否|cn-hangzhou|指定新创建用户组的堡垒机的区域ID。

 **说明：** 区域ID和区域名称的对应关系，请参见[地域和可用区](~~40654~~)。 |
|Comment|String|否|comment|指定新创建用户组的备注信息。最多支持500字符。 |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](~~148139~~)。

调用API的请求格式，请参见本文示例中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|阿里云为该请求生成的唯一标识符。 |
|UserGroupId|String|1|新创建用户组的ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=CreateUserGroup
&InstanceId=bastionhost-cn-st220aw****
&UserGroupName=group
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<CreateUserGroupResponse>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <UserGroupId>1</UserGroupId>
</CreateUserGroupResponse>
```

`JSON`格式

```
{
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
	"UserGroupId": "1"
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost)查看更多错误码。

