# 步骤1：同步阿里云ECS资产 {#task_264171 .task}

在使用堡垒机进行主机运维前，管理员需要在堡垒机实例中添加要管理的主机资产。本文将指导管理员在堡垒机实例中导入当前阿里云账号下的ECS资产。

开通堡垒机实例的阿里云账号下开通有ECS实例。关于如何开通ECS实例，请参见[创建ECS实例](../../../../cn.zh-CN/个人版快速入门/创建ECS实例.md#)。

除了导入阿里云ECS作为堡垒机资产外，您还可以手动添加或批量导入非阿里云主机作为堡垒机资产。更多信息，请参见[主机管理](../../../../cn.zh-CN/用户指南（V3版本）/管理员手册/资产/主机管理.md#)。

1.  授权堡垒机读取ECS列表信息。 

    首次登录堡垒机控制台时，您会收到提示，需要授权堡垒机读取ECS列表信息，以实现ECS快速接入。您可以参照以下步骤进行授权：

    1.  登录[云盾堡垒机控制台](https://yundunnext.console.aliyun.com/?p=bastion)。
    2.  在页面上方提示中单击**授权**，完成授权。

        **说明：** 已完成授权时，不会出现该提示。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64889/156229081233111_zh-CN.png)

2.  [登录云盾堡垒机实例](cn.zh-CN/快速入门/V3版本/登录实例.md#)。
3.  前往**资产** \> **主机管理** 页面，并打开**ECS同步**页签。
4.  单击页面右上角的**同步阿里云ECS**。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64889/156229081232919_zh-CN.png)


5.  在导入云主机对话框中，勾选要导入的主机，并单击**导入**。 

    **说明：** 如果ECS数据不是最新的，单击**手工刷新**进行重新检测。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64889/156229081232920_zh-CN.png)

    成功导入ECS主机。您需要进一步为已导入的主机添加主机帐户信息。 如果提示操作失败，建议您前往RAM访问控制控制台的[RAM角色管理](https://ram.console.aliyun.com/roles)页面，删除**AliyunBastionHostDefaultRole**角色，并参照步骤1重新完成授权。完成授权后，堡垒机默认使用上述角色访问其他云产品的资源。若该角色失效，则可能导致操作失败；通过重新授权，可以修复该问题。重新授权后，请重新执行步骤2~步骤5，同步阿里云ECS。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/217856/156229081250907_zh-CN.png)

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/217856/156229081350908_zh-CN.png)

6.  在**资产** \> **主机管理**页面，打开主机列表页签，并单击要操作的主机IP。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64889/156229081332921_zh-CN.png)


7.  打开**主机帐户**页签，单击**添加主机帐户**。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64889/156229081332922_zh-CN.png)


8.  在新建主机帐户对话框中，选择**协议**类型， 填写有效的主机帐户**登录名**和**密码**（服务器上已经创建并存在的帐户和对应密码），并单击**创建主机帐户**。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64889/156229081432923_zh-CN.png)

 成功创建主机帐户，完成阿里云ECS资产同步。

[步骤2：导入阿里云子账号](cn.zh-CN/快速入门/V3版本/步骤2：导入阿里云子账号.md#)

