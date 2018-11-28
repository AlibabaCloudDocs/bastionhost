# BS运维操作 {#concept_xqy_v5m_cfb .concept}

BS运维指普通运维用户以RAM子账号身份登录堡垒机控制台并进入Web运维界面，调用本地客户端，单点登录ECS进行运维。该运维方式仅支持RAM子账号用户以及主账号使用，可以在Windows和MAC环境下使用。

与BS运维方式相对的CS运维，指运维人员通过本地客户端工具登录云盾堡垒机，访问目标服务器主机进行运维操作。本文主要介绍BS运维的操作方法。

## RAM子账号登录 {#section_fdx_zj5_cfb .section}

在进行BS运维前，请根据需求设置好RAM子账号权限。您可以使用主账号登录[访问控制RAM-用户管理](https://ram.console.aliyun.com/#/user/list) ，给需要运维的RAM子账号授权。建议赋予子账号只读权限，只允许使用运维 ，避免子账号进入管理页面，发生越权操作。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18825/154337019210888_zh-CN.png)

参照以下步骤使用RAM子账号登录运维页面：

1.  通过RAM子账号登录界面，登录云盾堡垒机控制台。
2.  选择要操作的实例，单击**运维**，进入Web运维界面。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18825/154337019212002_zh-CN.png)


## 配置单点登录 {#section_i14_z5s_cfb .section}

参照以下步骤配置单点登录：

1.  在系统页面的右上角单击用户名，在下拉菜单中单击**工具下载**。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18825/154337019210552_zh-CN.png)

2.  在工具下载页面，选择下载**单点登录器**。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18825/154337019210553_zh-CN.png)

3.  安装单点登录器到本地。
4.  配置各协议的单点登录所用客户端。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18825/154337019210554_zh-CN.png)

5.  配置完成后退出。

## Web运维配置 {#section_w4x_cvs_cfb .section}

参照以下步骤进行Web运维配置：

1.  进入**运维** \> **主机运维**页。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18825/154337019210555_zh-CN.png)

2.  单击页面右上角的**WEB运维配置**。
3.  在RDP子页，设置**分辨率**、**连接模式**、**本地设备和资源**、**本地驱动器**后，单击**保存**。

    **说明：** 本地驱动器只需勾选要映射的盘符即可。请勿勾选全部盘符，否则该设置无效。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18825/154337019210556_zh-CN.png)

4.  前往SSH & TELNET & Rlogin页，选择客户端程序、终端类型、编码格式后，单击**保存**。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18825/154337019210557_zh-CN.png)

5.  前往FTP页，选择对应的客户端程序后，单击**保存**。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18825/154337019210885_zh-CN.png)

6.  参照步骤5，分别在SFTP和VNC页，设置SFTP和VNC参数。

## 主机登录 {#section_i2b_gvs_cfb .section}

在主机运维列表中，单击相应主机条目的登录图标框，会自动弹出配置好的客户端，登录主机进行操作。

以SSH运维为例，参照以下步骤登录主机：

1.  进入**运维** \> **主机运维**页。
2.  在主机运维列表中，选择需要登录的服务器，单击右侧登录图标框，自动调用所配置的SSH客户端。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18825/154337019210886_zh-CN.png)

3.  自动登入服务器，进行运维操作。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18825/154337019210887_zh-CN.png)


## 快速运维 {#section_sv2_3vs_cfb .section}

通过快速运维可快速找到最近多次登录的目标主机进行运维。快速运维主要用于需要频繁登录某些主机账户进行运维的场景。

参照以下步骤进行快速运维：

1.  进入**运维** \> **主机运维**页。
2.  单击搜索框，将自动显示最近运维的主机账户。在搜索框中输入主机IP/主机名/账户名、或关键信息，系统会自动过滤出与目标主机有关的信息。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18825/154337019210558_zh-CN.png)

3.  单击需要登录的目标主机及帐户后，即可成功登录。

## 搜索主机 {#section_kx4_kvs_cfb .section}

参照以下步骤搜索主机：

1.  进入**运维** \> **主机运维**页。
2.  在搜索框中输入主机名称或主机IP实现模糊搜索。您也可以通过主机协议过滤列表。

## 合并重复IP {#section_vkw_lvs_cfb .section}

主机运维中的重复IP合并将相同主机IP地址的不同主机账户全部整合在相应主机IP地址下，方便查看。

参照以下步骤合并重复IP：

1.  进入**运维** \> **主机运维**页。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18825/154337019210559_zh-CN.png)

2.  单击主机IP地址对应的**主机账户**即可查看。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18825/154337019210560_zh-CN.png)


