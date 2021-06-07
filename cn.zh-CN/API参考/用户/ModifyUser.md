# ModifyUser

调用ModifyUser接口修改堡垒机用户信息。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Yundun-bastionhost&api=ModifyUser&type=RPC&version=2019-12-09)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ModifyUser|需要执行的操作。

 取值：**ModifyUser**。 |
|InstanceId|String|是|bastionhost-cn-st220aw\*\*\*\*|指定要修改用户信息的堡垒机实例ID。

 **说明：** 您可以调用[DescribeInstances](~~153281~~)接口获取该参数。 |
|UserId|String|是|1|指定要修改信息的用户ID。

 **说明：** 您可以调用[ListUsers](~~204522~~)接口获取该参数。 |
|RegionId|String|否|cn-hangzhou|指定要修改用户信息的堡垒机的区域ID。

 **说明：** 区域ID和区域名称的对应关系，请参见[地域和可用区](~~40654~~)。 |
|Password|String|否|\*\*\*\*|指定修改后的用户密码。 支持使用字母、数字、下划线，最多支持128字符。

 **说明：** 用户来源为本地用户（即**Source**取值为**Local**）时，该参数生效。 |
|DisplayName|String|否|Bob|指定修改后的用户显示姓名。最多支持128字符。 |
|Comment|String|否|comment|指定修改后的用户备注信息。最多支持500字符。 |
|Email|String|否|123\*\*@qq.com|指定修改后的用户邮箱地址。 |
|Mobile|String|否|1358888\*\*\*\*|指定修改后的用户手机号码。 |
|MobileCountryCode|String|否|CN|指定修改后的用户手机号的国际域名。取值：

 -   **CN**：中国内地（+86）
-   **HK**：中国香港（+852）
-   **MO**：中国澳门（+853）
-   **TW**：中国台湾（+886）
-   **RU**：俄罗斯（+7）
-   **SG**：新加坡（+65）
-   **MY**：马来西亚（+60）
-   **ID**：印度尼西亚（+62）
-   **DE**：德国（+49）
-   **AU**：澳大利亚（+61）
-   **US**：美国（+1）
-   **AE**：迪拜（+971）
-   **JP**：日本（+81）
-   **GB**：英国（+44）
-   **IN**：印度（+91）
-   **KR**：韩国（+82）
-   **PH**：菲律宾（+63）
-   **CH**：瑞士（+41）
-   **SE**：瑞典（+46） |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](~~148139~~)。

调用API的请求格式，请参见本文示例中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|阿里云为该请求生成的唯一标识符。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=ModifyUser
&InstanceId=bastionhost-cn-st220aw****
&UserId=1
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<ModifyUserResponse>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
</ModifyUserResponse>
```

`JSON`格式

```
{
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Yundun-bastionhost)查看更多错误码。

