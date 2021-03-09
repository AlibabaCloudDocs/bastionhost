# API概览

本文介绍堡垒机提供的API接口。

堡垒机提供以下类型的API：

-   [堡垒机实例](#section_vb6_h2z_2uq)
-   [标签](#section_cik_lxz_si6)
-   [地域](#section_4xf_ju7_zb7)
-   [主机](#section_wmc_jrg_ur6)
-   [主机组](#section_fvj_ti8_3i0)
-   [主机账户](#section_cup_zvm_tpd)
-   [用户](#section_2hd_1bd_567)
-   [用户组](#section_rvd_lrp_2ip)
-   [主机授权](#section_30c_lgf_tkz)

## 堡垒机实例

|API|描述|
|---|--|
|[DescribeInstanceAttribute](/cn.zh-CN/API参考/实例/DescribeInstanceAttribute.md)|调用DescribeInstanceAttribute接口查询实例所有的属性信息。|
|[DescribeInstances](/cn.zh-CN/API参考/实例/DescribeInstances.md)|调用DescribeInstances接口查询实例的列表信息。|
|[ConfigInstanceSecurityGroups](/cn.zh-CN/API参考/实例/ConfigInstanceSecurityGroups.md)|调用ConfigInstanceSecurityGroups接口为指定的堡垒机实例配置安全组。|
|[ConfigInstanceWhiteList](/cn.zh-CN/API参考/实例/ConfigInstanceWhiteList.md)|调用ConfigInstanceWhiteList接口配置公网IP地址白名单。|
|[StartInstance](/cn.zh-CN/API参考/实例/StartInstance.md)|调用StartInstance接口启动堡垒机实例。|
|[EnableInstancePublicAccess](/cn.zh-CN/API参考/实例/EnableInstancePublicAccess.md)|调用EnableInstancePublicAccess接口开启指定堡垒机实例的公网访问能力。|
|[DisableInstancePublicAccess](/cn.zh-CN/API参考/实例/DisableInstancePublicAccess.md)|调用DisableInstancePublicAccess接口关闭堡垒机实例的公网访问能力。|
|[ModifyInstanceAttribute](/cn.zh-CN/API参考/实例/ModifyInstanceAttribute.md)|调用ModifyInstanceAttribute接口修改指定堡垒机实例的信息。|
|[MoveResourceGroup](/cn.zh-CN/API参考/实例/MoveResourceGroup.md)|调用MoveResourceGroup接口移动资源组堡垒机实例至其他资源组。|

## 标签

|API|描述|
|---|--|
|[ListTagKeys](/cn.zh-CN/API参考/标签/ListTagKeys.md)|调用ListTagKeys接口查询指定堡垒机实例已绑定的标签列表。|
|[ListTagResources](/cn.zh-CN/API参考/标签/ListTagResources.md)|调用ListTagResources接口查询一个或多个堡垒机实例已经绑定的标签列表。|
|[UntagResources](/cn.zh-CN/API参考/标签/UntagResources.md)|调用UntagResources接口为指定的堡垒机实例资源统一解绑并删除标签。|
|[TagResources](/cn.zh-CN/API参考/标签/TagResources.md)|调用TagResources接口为指定的堡垒机实例资源统一创建并绑定标签。|

## 地域

|API|描述|
|---|--|
|[DescribeRegions](/cn.zh-CN/API参考/地域/DescribeRegions.md)|调用DescribeRegions接口查询堡垒机实例支持的阿里云地域。|

## 主机

|API|描述|
|---|--|
|[CreateHost](/cn.zh-CN/API参考/主机/CreateHost.md)|调用CreateHost接口在堡垒机中创建需要运维的主机。|
|[GetHost](/cn.zh-CN/API参考/主机/GetHost.md)|调用GetHost接口获取指定主机的详细信息。|
|[ListHosts](/cn.zh-CN/API参考/主机/ListHosts.md)|调用ListHosts接口查询指定堡垒机实例下的主机列表。|
|[DeleteHost](/cn.zh-CN/API参考/主机/DeleteHost.md)|调用DeleteHost接口删除单个主机。|
|[ModifyHostsPort](/cn.zh-CN/API参考/主机/ModifyHostsPort.md)|调用ModifyHostsPort接口批量修改主机指定协议的端口。|
|[ModifyHostsActiveAddressType](/cn.zh-CN/API参考/主机/ModifyHostsActiveAddressType.md)|调用ModifyHostsActiveAddressType接口修改运维主机时使用的连接地址类型。|
|[ModifyHost](/cn.zh-CN/API参考/主机/ModifyHost.md)|调用ModifyHost接口修改主机基本信息。|

## 主机组

|API|描述|
|---|--|
|[CreateHostGroup](/cn.zh-CN/API参考/主机组/CreateHostGroup.md)|调用CreateHostGroup接口创建主机组。|
|[GetHostGroup](/cn.zh-CN/API参考/主机组/GetHostGroup.md)|调用GetHostGroup接口获取指定主机组详情。|
|[ListHostGroups](/cn.zh-CN/API参考/主机组/ListHostGroups.md)|调用ListHostGroups接口获取指定堡垒机下的主机组列表。|
|[ModifyHostGroup](/cn.zh-CN/API参考/主机组/ModifyHostGroup.md)|调用ModifyHostGroup接口修改主机组名称或备注信息。|
|[DeleteHostGroup](/cn.zh-CN/API参考/主机组/DeleteHostGroup.md)|调用DeleteHostGroup接口删除单个主机组。|
|[AddHostsToGroup](/cn.zh-CN/API参考/主机组/AddHostsToGroup.md)|调用AddHostsToGroup接口批量将主机加入指定主机组。|
|[RemoveHostsFromGroup](/cn.zh-CN/API参考/主机组/RemoveHostsFromGroup.md)|调用RemoveHostsFromGroup接口从指定主机组中批量移除主机。|

## 主机账户

|API|描述|
|---|--|
|[CreateHostAccount](/cn.zh-CN/API参考/主机账户/CreateHostAccount.md)|调用CreateHostAccount接口为指定主机创建主机账户。|
|[GetHostAccount](/cn.zh-CN/API参考/主机账户/GetHostAccount.md)|调用GetHostAccount接口获取指定主机账户详情。|
|[ListHostAccounts](/cn.zh-CN/API参考/主机账户/ListHostAccounts.md)|调用ListHostAccounts接口获取主机账户列表。|
|[ModifyHostAccount](/cn.zh-CN/API参考/主机账户/ModifyHostAccount.md)|调用ModifyHostAccount接口修改主机账户信息，支持修改主机账户的名称、密码和私钥信息。|
|[DeleteHostAccount](/cn.zh-CN/API参考/主机账户/DeleteHostAccount.md)|调用DeleteHostAccount接口删除单个主机账户。|
|[ResetHostAccountCredential](/cn.zh-CN/API参考/主机账户/ResetHostAccountCredential.md)|调用ResetHostAccountCredential接口清除指定主机账户登录凭据（密码或SSH私钥）。|

## 用户

|API|描述|
|---|--|
|[CreateUser](/cn.zh-CN/API参考/用户/CreateUser.md)|调用CreateUser接口创建用户。|
|[GetUser](/cn.zh-CN/API参考/用户/GetUser.md)|调用GetUser接口获取指定堡垒机用户的详细信息。|
|[ListUsers](/cn.zh-CN/API参考/用户/ListUsers.md)|调用ListUsers接口获取指定堡垒机的用户列表。|
|[ModifyUser](/cn.zh-CN/API参考/用户/ModifyUser.md)|调用ModifyUser接口修改堡垒机用户信息。|
|[DeleteUser](/cn.zh-CN/API参考/用户/DeleteUser.md)|调用DeleteUser接口删除单个堡垒机用户。|
|[LockUsers](/cn.zh-CN/API参考/用户/LockUsers.md)|调用LockUsers接口批量锁定堡垒机用户。|
|[UnlockUsers](/cn.zh-CN/API参考/用户/UnlockUsers.md)|调用UnlockUsers接口批量解锁堡垒机用户。|

## 用户组

|API|描述|
|---|--|
|[CreateUserGroup](/cn.zh-CN/API参考/用户组/CreateUserGroup.md)|调用CreateUserGroup接口创建堡垒机用户组。|
|[GetUserGroup](/cn.zh-CN/API参考/用户组/GetUserGroup.md)|调用GetUserGroup接口获取指定堡垒机用户组的详细信息。|
|[ListUserGroups](/cn.zh-CN/API参考/用户组/ListUserGroups.md)|调用ListUserGroups接口获取指定堡垒机下的用户组列表。|
|[ModifyUserGroup](/cn.zh-CN/API参考/用户组/ModifyUserGroup.md)|调用ModifyUserGroup接口修改用户组信息。|
|[DeleteUserGroup](/cn.zh-CN/API参考/用户组/DeleteUserGroup.md)|调用DeleteUserGroup接口删除单个堡垒机用户组。|
|[AddUsersToGroup](/cn.zh-CN/API参考/用户组/AddUsersToGroup.md)|调用AddUsersToGroup接口批量为用户组添加用户。|
|[RemoveUsersFromGroup](/cn.zh-CN/API参考/用户组/RemoveUsersFromGroup.md)|调用RemoveUsersFromGroup接口批量移除用户组内用户。|

## 主机授权

|API|描述|
|---|--|
|[AttachHostAccountsToUser](/cn.zh-CN/API参考/主机授权/AttachHostAccountsToUser.md)|调用AttachHostAccountsToUser接口为用户授权主机和主机账户。|
|[ListHostsForUser](/cn.zh-CN/API参考/主机授权/ListHostsForUser.md)|调用ListHostsForUser接口查询指定堡垒机用户已授权或未授权的主机列表。|
|[ListHostAccountsForUser](/cn.zh-CN/API参考/主机授权/ListHostAccountsForUser.md)|调用ListHostAccountsForUser接口查询指定用户在指定主机下已授权的主机账户列表。|
|[DetachHostAccountsFromUser](/cn.zh-CN/API参考/主机授权/DetachHostAccountsFromUser.md)|调用DetachHostAccountsFromUser接口移除给用户授权的主机及主机账户。|
|[AttachHostAccountsToUserGroup](/cn.zh-CN/API参考/主机授权/AttachHostAccountsToUserGroup.md)|调用AttachHostAccountsToUserGroup接口为用户组授权主机及主机账户。|
|[ListHostsForUserGroup](/cn.zh-CN/API参考/主机授权/ListHostsForUserGroup.md)|调用ListHostsForUserGroup接口查询指定堡垒机用户组已授权或未授权的主机列表。|
|[ListHostAccountsForUserGroup](/cn.zh-CN/API参考/主机授权/ListHostAccountsForUserGroup.md)|调用ListHostAccountsForUserGroup接口查询指定用户组在指定主机下已授权的主机账户列表。|
|[DetachHostAccountsFromUserGroup](/cn.zh-CN/API参考/主机授权/DetachHostAccountsFromUserGroup.md)|调用DetachHostAccountsFromUserGroup接口移除给用户组授权的主机及主机账户。|
|[AttachHostGroupAccountsToUser](/cn.zh-CN/API参考/主机授权/AttachHostGroupAccountsToUser.md)|调用AttachHostGroupAccountsToUser接口为用户授权主机组和主机账号。|
|[ListHostGroupsForUser](/cn.zh-CN/API参考/主机授权/ListHostGroupsForUser.md)|调用ListHostGroupsForUser接口查询指定堡垒机用户已授权或未授权的主机组列表。|
|[ListHostGroupAccountNamesForUser](/cn.zh-CN/API参考/主机授权/ListHostGroupAccountNamesForUser.md)|调用ListHostGroupAccountNamesForUser接口查询指定用户在指定主机组中已授权的主机账户名称。|
|[DetachHostGroupAccountsFromUser](/cn.zh-CN/API参考/主机授权/DetachHostGroupAccountsFromUser.md)|调用DetachHostGroupAccountsFromUser接口移除用户已授权的主机组及主机账户。|
|[AttachHostGroupAccountsToUserGroup](/cn.zh-CN/API参考/主机授权/AttachHostGroupAccountsToUserGroup.md)|调用AttachHostGroupAccountsToUserGroup接口为用户组授权主机组和主机账号。|
|[ListHostGroupsForUserGroup](/cn.zh-CN/API参考/主机授权/ListHostGroupsForUserGroup.md)|调用ListHostGroupsForUserGroup接口查询指定堡垒机用户组已授权或未授权的主机组列表。|
|[ListHostGroupAccountNamesForUserGroup](/cn.zh-CN/API参考/主机授权/ListHostGroupAccountNamesForUserGroup.md)|调用ListHostGroupAccountNamesForUserGroup接口查询指定用户组在指定主机组中已授权的主机账户名称。|
|[DetachHostGroupAccountsFromUserGroup](/cn.zh-CN/API参考/主机授权/DetachHostGroupAccountsFromUserGroup.md)|调用DetachHostGroupAccountsFromUserGroup接口移除用户组已授权的主机组及主机账户。|

