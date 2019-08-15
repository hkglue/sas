# 子账户登录提示当前操作未授权FAQ {#concept_878560 .concept}

云安全中心支持RAM子账号功能。RAM 允许在一个云账号下创建并管理多个身份，并允许给单个身份或一组身份分配不同的权限，从而实现不同用户拥有不同的云资源访问权限。

RAM用户新创建的时候默认无任何权限。

## 问题描述 {#section_yr1_vif_e5s .section}

使用RAM子账号登录云安全中心并进行操作时，提示“当前操作未被授权”。这种情况下，可能是由于您使用了未经过主账号授权的子账号。

![子账号授权](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/711042/156585593650404_zh-CN.png)

## 解决方法 {#section_6nd_dr1_9xw .section}

为可信的RAM子账号授予AliyunYundunSASFullAccess（管理云安全中心）权限。

1.  联系主账号管理员登录主账号。
2.  主账号为子账号授予管理云安全中心的系统权限。子账号授权详细内容参见[为RAM角色授权](../../../../intl.zh-CN/用户指南/角色/为RAM角色授权.md#)。

    ![子账号授权](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/711042/156585593655689_zh-CN.png)

    **说明：** 授权前，请确认要授权的子账号是否正确。


授权完成后，使用该子账号[登录云安全中心](https://signin.alibabacloud.com/login.htm)，进行相应的操作。

