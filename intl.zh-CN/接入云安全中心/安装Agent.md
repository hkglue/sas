# 安装Agent {#concept_dl4_ykc_zdb .concept}

云安全中心Agent是云安全中心提供的本地插件，您必须在服务器操作系统上安装云安全中心Agent插件才能使用云安全中心提供的安全防护服务。

未安装Agent插件的服务器将不受云安全中心保护，控制台页面也不会显示该资产的任何漏洞、告警、基线漏洞和资产指纹等数据。

## 如何查看哪些资产需要安装Agent插件？ {#section_wzt_66o_xsp .section}

每台资产都需安装Agent插件，您可以在云安全中心控制台**总览**页面资产保护模块，查看未安装Agent插件（即**未保护资产**）的服务器数量。单击**安装Agent**跳转到**设置** \> **安装/卸载插件**页面。

![1](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13631/156413363248934_zh-CN.png)

**说明：** 您也可以在**资产管理**页面确认服务器Agent安装状态。

-   保护状态为**开启**：表示Agent已安装且处于正常运行状态。
-   保护状态为**关闭**：表示Agent未安装或处于离线状态。

**安装/卸载插件**页面会展示出您所有**未安装Agent插件**（包含已关机的服务器）的服务器列表。您可在该页面对未安装Agent的服务器执行一键自动安装或手动下载、执行命令安装。一键安装功能无需您单独下载插件。

![2](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13631/156413363353451_zh-CN.png)

该页面下方还会展示出对于不支持一键安装功能的服务器，您需手动安装Agent插件的操作指引。

![3](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13631/156413363353460_zh-CN.png)

## 注意事项 {#section_ort_h99_hi3 .section}

非阿里云服务器必须通过安装程序（Windows）或脚本命令（Linux）安装云安全中心Agent。

如果您的非阿里云服务器通过以下方式安装了Agent，则您需要删除云安全中心Agent目录后，按照下述手动安装步骤重新安装Agent。

-   通过已安装云安全中心Agent的镜像批量安装服务器。
-   从已安装云安全中心Agent的服务器上，直接复制云安全中心Agent文件。

**云安全中心Agent文件目录**

-   Windows：C:\\Program Files \(x86\)\\Alibaba\\Aegis
-   Linux：/usr/local/aegis

## 一键自动安装Agent {#section_6zm_lum_3t3 .section}

执行一键安装前，需确定您的服务器已满足以下条件：

-   服务器为阿里云服务器，非阿里云服务器需进行手动安装
-   ECS在支持[一键安装功能支持的地域](#section_frg_dlh_ghb)内
-   服务器已在运行中
-   网络已正常连接
-   该服务器已安装云助手

    **说明：** 云助手安装相关内容参见文档[云助手](../../../../intl.zh-CN/运维与监控/云助手/云助手概述.md#)。

-   如果您已在服务器上安装了安全软件（如安全狗、云锁等），可能会导致Agent插件无法正常安装。建议您在安装Agent插件前确认您的服务器上是否存在这类安全软件。如果存在，建议您先关闭或卸载该安全软件之后再安装Agent插件。

**操作步骤** 

1.  登录[云安全中心管理控制台](https://yundunnext.console.aliyun.com/?p=sas)。
2.  单击**安全运营** \> **设置** \> **安装/卸载插件**。
3.  单击**操作**栏的**安装客户端**，勾选单个服务器安装Agent，或单击左下角**一键安装**对多台服务器执行批量安装Agent。

    ![2](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13631/156413363353451_zh-CN.png)


Agent插件安装完成约五分钟后，您即可在**资产管理**中查看您服务器的在线情况：阿里云服务器将会从**关闭**变成**开启**。

**说明：** 一键安装后如果客户端状态显示为**安装失败**并提示**未安装云助手**，请先安装云助手。云助手安装相关内容参见文档[云助手](../../../../intl.zh-CN/运维与监控/云助手/云助手概述.md#)。

## 手动安装Agent {#section_qxq_hkv_ghb .section}

以下情况不支持一键自动安装、必须执行手动安装Agent：

-   您的服务器为非阿里云服务器
-   网络类型为经典网络
-   ECS不在[支持的区域](#table_ec1_2lh_ghb)内
-   服务器操作系统为Windows 2019、Windows 2016、Windows 2012、Windows 2008、Windows 2003
-   未安装[云助手](../../../../intl.zh-CN/运维与监控/云助手/云助手概述.md#)
-   通过专线连接、内网通信的非阿里云服务器，需要修改服务器的DNS配置，指定以下任意一个云安全中心服务端DNS解析地址：

    `106.11.248.209/106.11.248.51 jsrv.aegis.aliyun.com`

    `106.11.248.90/106.11.250.224 update.aegis.aliyun.com`


**说明：** 手动安装Agent前，请确认该服务器已正常运行，并且网络已连通。

**操作步骤** 

1.  登录[云安全中心控制台](https://yundun.console.aliyun.com/?p=sas)。
2.  单击**安全运营** \> **设置** \> **安装/卸载插件**。
3.  根据您的服务器操作系统选择安装步骤，获取最新版本Agent插件。

    ![3](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13631/156413363353460_zh-CN.png)

    -   **Windows 系统**

        1.  在安装Agent页面，单击**点击下载**下载最新版本Agent安装文件到本地计算机。
        2.  将安装文件上传至您的Windows服务器，例如通过FTP工具将安装文件上传到服务器。
        3.  在您的Windows服务器上以管理员权限运行Agent插件安装程序。
        4.  非阿里云服务器输入安装验证Key关联您的阿里云账号。您可在Agent安装页面找到您的安装验证Key。

            ![4](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13631/156413363448994_zh-CN.png)

            **说明：** 每个安装验证KEY有效期为1小时，超过该时间将无法正确安装Agent插件。安装插件前请及时刷新安装验证KEY。

    -   **Linux 系统**

        1.  根据您的实际情况，在安装Agent页面选择**阿里云服务器**或**非阿里云服务器**。
        2.  以管理员身份登录您的Linux服务器。
        3.  根据您的服务器，选择32位或64位的安装命令并复制至您的Linux服务器上。
        4.  执行安装命令即可完成Agent插件的下载及安装。
        **说明：** 该安装命令包含从阿里云站点下载最新的Agent插件，如您使用的是非阿里云服务器请确认您的服务器已连接公网。


Agent插件安装完成约五分钟后，您即可在云安全中心管理控制台中查看您服务器的在线情况：

-   阿里云服务器会从**关闭**变成**开启**。
-   非阿里云服务器将会被添加至您的服务器列表中。

**说明：** 请不要对无需保护的机器（例如：线下测试机器、您自己的工作电脑等）安装Agent。

## 后续步骤 {#section_csp_z1d_zdb .section}

安装Agent后，建议您参照以下步骤进行验证Agent是否已成功安装：

1.  检查您服务器上云安全中心Agent的AliYunDun和AliYunDunUpdate进程是否正常运行。关于云安全中心Agent进程说明，请参考[Agent说明](intl.zh-CN/接入云安全中心/Agent说明.md#)。
2.  在您的服务器上执行以下telnet命令，检查您的服务器是否能正常连通云安全中心服务器：

    **说明：** 确保您的服务器能够连通至少一个jsrv和一个update服务域名。

    -   `telnet jsrv.aegis.aliyun.com 80`
    -   `telnet jsrv2.aegis.aliyun.com 80`
    -   `telnet jsrv3.aegis.aliyun.com 80`
    -   `telnet update.aegis.aliyun.com 80`
    -   `telnet update2.aegis.aliyun.com 80`
    -   `telnet update3.aegis.aliyun.com 80`

如果云安全中心Agent安装验证失败，请参考[Agent离线排查](intl.zh-CN/接入云安全中心/Agent离线排查.md#)。

## 一键安装功能支持的地域 {#section_frg_dlh_ghb .section}

|支持的地域|地域名称|
|-----|----|
|亚太|华东 1（杭州）|
|华东 2（上海）|
|华东 2 金融云|
|华北 1（青岛）|
|华北 2（北京）|
|华北 3（张家口）|
|华北 5（呼和浩特）|
|华南 1（深圳）|
|香港|
|新加坡|
|澳大利亚（悉尼）|
|马来西亚（吉隆坡）|
|印度尼西亚（雅加达）|
|日本（东京）|
|欧洲与美洲|德国（法兰克福）|
|英国（伦敦）|
|美国（硅谷）|
|美国（弗吉尼亚）|
|中东与印度|印度（孟买）|
|阿联酋（迪拜）|

## 相关文档 {#section_iph_k3p_57w .section}

[安装、卸载相关问题](../../../../intl.zh-CN/常见问题/云安全中心常见问题概览.md#section_ymh_u9c_vbp)

