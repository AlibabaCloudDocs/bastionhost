# BS运维操作 {#task_lvg_44p_y2b .task}

使用RAM子账号或主账号登录云盾堡垒机主机运维页面后，可以看到该账号能够访问的服务器信息。

**说明：** 管理员必须给RAM子账号或主账号授权相应的服务器，否则无法看到服务器信息。

## 配置单点登录 {#task_qp4_p4p_y2b}

1.   在系统页面的右上角单击用户名，在下拉菜单中单击**工具下载**。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18825/153663013910552_zh-CN.png)

 
2.   在工具下载页面，选择下载**单点登录器**。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18825/153663013910553_zh-CN.png)

 
3.  安装单点登录器到本地。 
4.   配置各协议的单点登录所用客户端。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18825/153663013910554_zh-CN.png)

 
5.  配置完成后退出。 

## Web运维配置 {#task_em3_r4p_y2b}

1.   进入**运维** \> **主机运维**页。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18825/153663013910555_zh-CN.png)

 
2.  单击页面右上角的**WEB运维配置**。 
3.   在RDP子页，设置分辨率、连接模式、本地设备和资源、本地驱动后，单击**保存**。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18825/153663013910556_zh-CN.png)

 
4.   前往SSH & TELNET & Rlogin子页，选择客户端程序、终端类型、编码格式后，单击**保存**。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18825/153663013910557_zh-CN.png)

 
5.  前往FTP子页，选择对应的客户端程序后，单击**保存**。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18825/153663013910885_zh-CN.png)

 
6.  参照步骤5，分别在SFTP和VNC子页，设置SFTP和VNC参数。 

## 主机登录 {#task_klh_54p_y2b}

在主机运维列表中，单击相应主机条目的登录图标框，会自动弹出配置好的客户端，登录主机进行操作。以SSH运维为例。

1.  进入**运维** \> **主机运维**页。 
2.  在主机运维列表中，选择需要登录的服务器，单击右侧登录图标框，自动调用所配置的SSH客户端。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18825/153663013910886_zh-CN.png)

 
3.  自动登入服务器，进行运维操作。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18825/153663013910887_zh-CN.png)

 

## 快速运维 {#task_ogd_v4p_y2b}

通过快速运维可快速找到最近多次登录的目标主机进行运维。主要用于需要频繁登录某些主机账户进行运维的场景。

1.  进入**运维** \> **主机运维**页。 
2.   单击搜索框，将自动显示最近运维的主机账户。在搜索框中输入主机IP/主机名/账户名、或关键信息，系统会自动过滤出与目标主机有关的信息。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18825/153663014010558_zh-CN.png)

 
3.  单击需要登录的目标主机及帐户后，即可成功登录。 

## 搜索主机 {#task_mqx_v4p_y2b}

1.  进入**运维** \> **主机运维**页。 
2.  在搜索框中输入主机名称或主机IP实现模糊搜索。您也可以通过主机协议过滤列表。 

## 合并重复IP {#task_twg_w4p_y2b}

主机运维中的重复IP合并将相同主机IP地址的不同主机账户全部整合在相应主机IP地址下，方便查看。

1.   进入**运维** \> **主机运维**页。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18825/153663014010559_zh-CN.png)

 
2.   单击主机IP地址对应的**主机账户**即可查看。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18825/153663014010560_zh-CN.png)

 

