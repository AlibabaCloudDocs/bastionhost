# SSH协议运维 {#concept_zy1_dyd_z2b .concept}

本文受众范围：运维工程师、云盾堡垒机管理员、持有阿里云账号的管理员。

运维人员需要通过本地的客户端工具登录云盾堡垒机，再访问目标服务器主机进行运维操作。

**说明：** 请确认在本地主机已安装支持 SSH 协议的运维工具，如 Xshell、SecureCRT、PuTTY 等工具。

## Xshell {#section_cd2_xy3_dfb .section}

下文以Xshell工具为例，介绍运维登录流程：

1.  打开Xshell工具，在连接设置中输入云盾堡垒机的IP和SSH端口号（SSH端口号默认为 60022）。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21381/153691446811972_zh-CN.png)

2.  在用户身份验证设置中输入云盾堡垒机的用户名和密码。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21381/153691446811973_zh-CN.png)

    **说明：** 如果管理员在云盾堡垒机中配置了用户公钥，则用户可以通过公私密钥对的方式登录，无需输入密码。在用户身份验证设置中，选择**Public Key**，输入云盾堡垒机用户名，选择对应的私钥。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21381/153691446811974_zh-CN.png)

3.  单击**确定**，连接云盾堡垒机。
4.  （可选）如果管理员启用了双因子认证登录，将会弹出双因子口令对话框，请输入您手机上收到的6位数字。

    **说明：** 云子账号账户使用MFA进行二次验证。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21381/153691446811975_zh-CN.png)

5.  成功登录云盾堡垒机后，进入资产管理界面。通过键盘上的上、下箭头选择您想要进行运维的服务器主机。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21381/153691446811976_zh-CN.png)

6.  按 Enter 键即可登录目标服务器主机进行运维操作。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21381/153691446811977_zh-CN.png)


## Usmshell使用说明 {#section_zwz_hz3_dfb .section}

参照以下步骤开启Usmshell使用命令行方式：

1.  进入**系统** \> **系统配置** \> **运维配置**页。
2.  在SSH登录选项中勾选**Usmshell使用命令行方式**。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21381/153691446811980_zh-CN.png)

3.  打开SSH协议客户端，使用CS运维方式登录堡垒机。输入`help`查看usmshell使用帮助。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21381/153691446811981_zh-CN.png)


|命令|描述|
|clear|清屏。|
|set|设置当前shell环境。|
|ls|列出可运维的资产列表。|
|open|按编号连接可运维列表中的资产。|
|ssh|连接ssh协议资产。|
|telnet|连接telnet协议资产。|
|rlogin|连接rlogin协议资产。|
|reload|重连。|
|passwd|修改用户密码。|
|connect|连接主机某个端口。|
|traceroute|将路由数据包跟踪打印到主机。|
|ping|检查连通性。|
|exit|退出登录。|

**说明：** 输入`help [command]`查看更详细的使用帮助。

以ls、open、ssh、passwd命令为例详细介绍其使用方法。

-   **ls**

    ls命令支持通过协议、用户名、主机名和主机IP过滤资产并列出资产，且支持模糊匹配功能。

    -   输入`ls`，列出所有可运维资产。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21381/153691446811982_zh-CN.png)

    -   输入`ls [protocol]`，列出通过协议过滤后的资产，支持模糊匹配。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21381/153691446811983_zh-CN.png)

    -   输入`ls [user]`，列出通过用户名过滤后的资产，支持模糊匹配。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21381/153691446911984_zh-CN.png)

    -   输入`ls [ip]`，列出通过主机IP过滤后的资产，支持模糊匹配。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21381/153691446911985_zh-CN.png)

    -   输入`ls [name]`，列出通过主机名过滤后的资产，支持模糊匹配。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21381/153691446911986_zh-CN.png)
-   **open**

    使用open命令可以按编号连接可运维列表中的资产，先输入ls命令获取资产列表，再通过open命令连接资产。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21381/153691446911987_zh-CN.png)

-   **ssh**

    通过ssh协议登录资产。前提是所登录资产的ssh账户已被授权。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21381/153691446911988_zh-CN.png)

-   **passwd**

    通过passwd命令修改堡垒机用户密码。登录堡垒机后，输入passwd命令并按Enter键。根据提示依次输入**当前用户密码**、**新密码**、**重复新密码**，并按 Enter 键。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21381/153691446911989_zh-CN.png)


