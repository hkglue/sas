# 如何在Windows2012中查看登录失败的用户名？ {#concept_53698_zh .concept}

由于Windows 2012 远程桌面服务开启了SSL安全层，安全日志无法记录登录失败的源IP和用户名。因此，云安全中心异常登录拦截功能也无法获取对方用户名。但是您可以通过人工分析并获取登录失败的用户名。

## 前提条件 {#section_jkv_fnc_3gb .section}

人工分析获取登录失败用户名的前提条件是：Windows 2012已经打开审核登录事件日志。您可以通过：

-   在 **控制面板** \> **系统和安全** \> **管理工具** \> **事件查看器**中，查看日志功能是否启用并记录。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/163482/155792503545539_zh-CN.jpg)

-   在 **控制面板** \> **系统和安全** \> **管理工具**中，开启审核登录事件、审核账户登录事件。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/163482/155792503545540_zh-CN.jpg)


## 操作步骤 { .section}

参照以下步骤执行手动分析，并获取登录失败的用户名。

1.  登录[云安全中心管理控制台](https://yundunnext.console.aliyun.com/?p=sas)。
2.  单击左侧导航栏**安全告警处理**。
3.  筛选**异常登录**类型的告警。
4.  找到**异常登录-ECS被暴力破解登录**告警记录，查看其**发生时间**。
5.  登录Windows 2012服务器，打开 **控制面板** \> **系统和安全** \> **管理工具** \> **事件查看器**，并查找 **Windows日志** \> **安全**。
6.  查找云安全中心提示爆破登录时刻的明细日志。根据关键字**审核失败**、任务类别**登录**定位到具体暴力破解登录事件。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/163482/155792503545546_zh-CN.png)

7.  在常规页面中查看登录失败原因：未知用户名或密码错误。其中，**账户名**为登录失败的用户。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/163482/155792503545547_zh-CN.png)


