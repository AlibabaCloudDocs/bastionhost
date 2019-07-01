# 导入RAM子账号 {#task_wjb_m4t_vgb .task}

本文介绍如何在阿里云访问控制（RAM）中创建用于堡垒机管理和运维的子账号，以及如何导入RAM子账号到堡垒机账号系统。

1.  新建RAM子账号。 
    1.  使用阿里云主账号登录[访问控制控制台](https://ram.console.aliyun.com)。
    2.  在**人员管理** \> **用户**页面，单击**新建用户**。
    3.  在新建用户页面，设置用户**登录名称**和**显示名称**，并选择**访问方式**。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/127539/156195880639032_zh-CN.png)


    4.  单击**确定**完成用户创建。
2.  为RAM子账号启多因素认证（MFA）登录。 
    1.  使用阿里云主账号登录[访问控制控制台](https://ram.console.aliyun.com)。
    2.  在**人员管理** \> **用户**页面，单击新创建的用户登录名。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/127539/156195880739033_zh-CN.png)


    3.  在用户详情页，单击**启用虚拟MFA设备**。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/127539/156195880739035_zh-CN.png)


    4.  在启用虚拟MFA设备页面，（RAM子账号使用者）使用阿里云App（或其他MFA应用程序）扫码添加账号。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/127539/156195880739037_zh-CN.png)

 成功添加账号后，在阿里云App的虚拟MFA页面会显示已关联账号和每60s自动刷新生成的安全码。
    5.  在启用虚拟MFA设备页面的**第一组安全码**和**第二组安全码**中输入阿里云App中连续获取的两组安全码，然后单击**确定启用**。 成功启用MFA设备后，每次使用子账号登录时，都要输入从已绑定的MFA设备（即阿里云App）中获得的安全码。
3.  向RAM子账号授权。 
    1.  使用阿里云主账号登录[访问控制控制台](https://ram.console.aliyun.com)。
    2.  在**人员管理** \> **用户**页面，选择要操作的子账号，单击**添加权限**。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/127539/156195880739038_zh-CN.png)


    3.  在添加权限页面，搜索以下系统授权策略，并选择要授权给当前子账号的权限： 

        -   AliyunYundunBastionHostFullAccess（管理员权限）
        -   AliyunYundunBastionHostReadOnlyAccess（运维员权限）
        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/127539/156195880739039_zh-CN.png)

    4.  选择要授予当前子账号的权限后，单击**确定**完成授权。 被授予权限的子账号可用来执行相应操作。
4.  导入RAM子账号。 

    1.  登录[云盾堡垒机控制台](https://yundunnext.console.aliyun.com/?p=bastion)。
    2.  在子账号管理页面，单击列表下方的**刷新子账号数据**。
    3.  在子账号管理页面右上角，单击**导入子账号**。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/127539/156195880839040_zh-CN.png)


    4.  在导入阿里云子账号用户对话框，勾选要导入的子账号，单击**导入子账号**。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/127539/156195880839041_zh-CN.png)


    勾选的子账号被导入到子账号列表中。


