# BS运维 {#concept_py4_ng4_ydb .concept}

BS运维指普通运维用户以RAM子账号身份登录堡垒机控制台并进入Web运维界面，调用本地客户端，单点登录ECS运维。该运维方式仅支持RAM子账号用户使用，可以在Windows和MAC环境下使用。

在进行BS运维前，请根据需求设置好RAM子账号权限。您可以使用主账号登录[访问控制RAM-用户管理](https://ram.console.aliyun.com/#/user/list) ，给需要运维的RAM子账号授权。建议赋予子账号只读权限，只允许使用运维 ，避免子账号进入管理页面，发生越权操作。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12749/4094_zh-CN.png)

## RAM子账号登录 {#section_smc_ch4_ydb .section}

参照以下步骤，使用RAM子账号登录运维页面：

1.  通过RAM子账号登录界面，登录云盾堡垒机控制台。
2.  选择要操作的实例，单击**运维**，进入Web运维界面。

    **Note:** RAM子账号需要先导入堡垒机，否则可能无法看到**运维**按钮 ，导入方法参见[用户管理](cn.zh-CN/用户指南/管理员手册/用户管理.md#)。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12749/4096_zh-CN.png)

3.  单击**下载堡垒机运维助手**按钮，下载后进行安装。

    **Note:** 使用BS运维功能前，确保堡垒机运维助手启用。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12749/4097_zh-CN.png)

4.  安装完成后，刷新运维页面，不再提示未检测到堡垒机运维助手。
5.  单击**运维助手配置**，进入运维助手配置界面。
6.  分别对所需使用的SSH客户端、RDP客户端、SFTP客户端进行配置。以SFTP为例，步骤如下：

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12749/4098_zh-CN.png)


## BS运维操作 {#section_bv1_fh4_ydb .section}

使用RAM子账号登录云盾堡垒机运维页面后，可以看到该账号可以访问的服务器信息。

**Note:** 管理员必须给RAM子账号授权相应的服务器，否则无法看到服务器信息。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12749/4099_zh-CN.png)

-   RDP运维
    1.  选择需要登录的服务器，单击右侧**RDP登录**，自动调用mstsc客户端。
    2.  在弹出界面，单击**连接** 。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12749/4100_zh-CN.png)

    3.  在弹出界面，单击**是**，成功登录服务器。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12749/4101_zh-CN.png)

        **Note:** MAC环境下RDP客户端不支持自动登入服务器，您在调用RDP客户端后，需要人工选择运维的服务器，然后双击后连接进入。

-   SSH运维
    1.  选择需要登录的服务器，单击右侧**SSH登录**，自动调用所配置的SSH客户端。
    2.  自动登入服务器，进行运维操作。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12749/4102_zh-CN.png)

-   SFTP运维
    1.  选择需要登录的服务器，单击右侧**SFTP登录**，自动调用所配置的SFTP客户端。
    2.  自动登入服务器，进行运维操作。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12749/4103_zh-CN.png)


