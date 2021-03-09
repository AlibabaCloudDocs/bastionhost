# GetUser

调用GetUser接口获取指定堡垒机用户的详细信息。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Yundun-bastionhost&api=GetUser&type=RPC&version=2019-12-09)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|GetUser|需要执行的操作。

 取值：**GetUser**。 |
|InstanceId|String|是|bastionhost-cn-st220aw\*\*\*\*|指定要查询的用户所在堡垒机的实例ID。

 **说明：** 您可以调用[DescribeInstances](~~153281~~)接口获取该参数。 |
|UserId|String|是|1|指定要查询的用户ID。

 **说明：** 您可以调用[ListUsers](~~204522~~)接口获取该参数。 |
|RegionId|String|否|cn-hangzhou|指定要查询的用户所在堡垒机的区域ID。

 **说明：** 区域ID和区域名称的对应关系，请参见[地域和可用区](~~40654~~)。 |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](~~148139~~)。

调用API的请求格式，请参见本文示例中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|阿里云为该请求生成的唯一标识符。 |
|User|Struct| |查询到的用户详细信息。 |
|Comment|String|commet|用户备注信息。 |
|DisplayName|String|Bob|用户的显示姓名。 |
|Email|String|1099\*\*@qq.com|用户的邮箱地址。 |
|Mobile|String|1359999\*\*\*\*|用户的手机号码。 |
|MobileCountryCode|String|CN|用户手机号码的国际域名。取值：

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
|Source|String|Local|用户的来源。取值：

 -   **Local**：本地用户
-   **Ram**：RAM用户 |
|SourceUserId|String|122748924538\*\*\*\*|用户的唯一标识。

 **说明：** 该参数是堡垒机用户对应的RAM用户的唯一标识。用户来源为RAM用户（即**Source**取值为**Ram**）时，返回该参数。用户来源为本地用户（即**Source**取值为**Local**）时，该参数返回值为空。 |
|UserId|String|1|用户ID。 |
|UserName|String|abcabc\_def|用户的登录名称。 |
|UserState|List|\["Normal"\]|用户的状态。取值：

 -   **Normal**：正常状态
-   **Frozen**：被锁定状态
-   **Expired**：已过期状态 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=GetUser
&InstanceId=bastionhost-cn-st220aw****
&UserId=1
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<GetUserResponse>
      <User>
            <Comment>commet</Comment>
            <Email>1099**@qq.com</Email>
            <UserName>abcabc_def</UserName>
            <UserId>1</UserId>
            <SourceUserId>122748924538****</SourceUserId>
            <DisplayName>Bob</DisplayName>
            <MobileCountryCode>CN</MobileCountryCode>
            <Mobile>1359999****</Mobile>
            <Source>Local</Source>
            <UserState>Normal</UserState>
      </User>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
</GetUserResponse>
```

`JSON`格式

```
{
	"User": {
		"Comment": "commet",
		"Email": "1099**@qq.com",
		"UserName": "abcabc_def",
		"UserId": "1",
		"SourceUserId": "122748924538****",
		"DisplayName": "Bob",
		"MobileCountryCode": "CN",
		"Mobile": "1359999****",
		"Source": "Local",
		"UserState": ["Normal"]
	},
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE"
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost)查看更多错误码。

