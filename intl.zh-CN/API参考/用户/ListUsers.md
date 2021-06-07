# ListUsers

调用ListUsers接口获取指定堡垒机的用户列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Yundun-bastionhost&api=ListUsers&type=RPC&version=2019-12-09)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ListUsers|需要执行的操作。

 取值：**ListUsers**。 |
|InstanceId|String|是|bastionhost-cn-st220aw\*\*\*\*|指定要查询用户列表的堡垒机的实例ID。

 **说明：** 您可以调用[DescribeInstances](~~153281~~)接口获取该参数。 |
|RegionId|String|否|cn-hangzhou|指定要查询用户列表的堡垒机的区域ID。

 **说明：** 区域ID和区域名称的对应关系，请参见[地域和可用区](~~40654~~)。 |
|PageNumber|String|否|1|指定分页查询时，当前页的页码。默认值为**1**。 |
|PageSize|String|否|20|指定分页查询时，每页显示的数据最大条数。

 PageSize参数最大取值为100。每页默认显示的数据条数为20条，PageSize参数值为空时，将默认返回20条数据。

 **说明：** 建议PageSize取值不要为空。 |
|UserName|String|否|abc|指定要查询的用户登录名称。仅支持精确查询。 |
|DisplayName|String|否|用户|指定要查询的用户显示姓名。仅支持精确查询。 |
|Source|String|否|Local|指定要查询的用户的来源。取值：

 -   **Local**：本地用户
-   **Ram**：RAM用户 |
|Mobile|String|否|1359999\*\*\*\*|指定要查询的用户的手机号码。仅支持精确查询。 |
|UserState|String|否|Normal|指定要查询的用户状态。取值：

 -   **Normal**：正常状态
-   **Frozen**：被锁定状态
-   **Expired**：已过期状态 |
|SourceUserId|String|否|122748924538\*\*\*\*|指定要查询的用户的唯一标识。仅支持精确查询。

 **说明：** 该参数是堡垒机用户对应的RAM用户的唯一标识。新创建用户来源为RAM用户（即**Source**取值为**Ram**）时，该参数生效。您可以调用访问控制的[ListUsers](~~28684~~)接口从返回数据**UserId**获取该参数。 |
|UserGroupId|String|否|1|指定要查询的用户组ID。

 **说明：** 您可以调用[ListUserGroups](~~204509~~)接口获取该参数。 |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](~~148139~~)。

调用API的请求格式，请参见本文示例中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|阿里云为该请求生成的唯一标识符。 |
|TotalCount|Integer|1|查询到的用户总数。 |
|Users|Array of Item| |查询到的用户列表。 |
|Comment|String|comment|用户备注信息。 |
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
|UserName|String|abc\_def|用户的登录名称。 |
|UserState|List|\["Normal"\]|用户的状态。取值：

 -   **Normal**：正常状态
-   **Frozen**：被锁定状态
-   **Expired**：已过期状态 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=ListUsers
&InstanceId=bastionhost-cn-st220aw****
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<ListUsersResponse>
      <TotalCount>1</TotalCount>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <Users>
            <Comment>comment</Comment>
            <UserName>abc_def</UserName>
            <Email>1099**@qq.com</Email>
            <UserId>1</UserId>
            <SourceUserId>122748924538****</SourceUserId>
            <MobileCountryCode>CN</MobileCountryCode>
            <DisplayName>Bob</DisplayName>
            <Mobile>1359999****</Mobile>
            <Source>Local</Source>
            <UserState>Normal</UserState>
      </Users>
</ListUsersResponse>
```

`JSON`格式

```
{
	"TotalCount": "1",
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
	"Users": [{
		"Comment": "comment",
		"UserName": "abc_def",
		"Email": "1099**@qq.com",
		"UserId": "1",
		"SourceUserId": "122748924538****",
		"MobileCountryCode": "CN",
		"DisplayName": "Bob",
		"Mobile": "1359999****",
		"Source": "Local",
		"UserState": ["Normal"]
	}]
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost)查看更多错误码。

