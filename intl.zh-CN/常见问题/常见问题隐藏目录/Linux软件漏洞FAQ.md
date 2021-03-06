# Linux软件漏洞FAQ {#concept_58649_zh .concept}

本文档列举了Linux软件漏洞功能相关的常见问题，您可以在问题列表中选择您想要了解的问题，并单击该问题查看相关解答。

**说明：** 本文档仅适用于以下操作系统：CentOS、Ubuntu、及 Debian。

-   [如何获取当前软件版本漏洞信息？](#ul_et5_zpb_3gb)
-   [如何将 Ubuntu 14.04 系统的 3.1\\\* 内核升级至 4.4 内核？](#2)
-   [内核漏洞升级修复后，云安全中心仍然提示存在漏洞？](#3)
-   [云安全中心管理控制台中某些漏洞提示无更新？](#4)
-   [如何手动检测服务器上的Linux软件漏洞？](#5)

## 如何获取当前软件版本漏洞信息？ {#1 .section}

一般情况下，系统软件漏洞（CVE 漏洞）是通过软件包版本匹配的方式获取您的服务器当前的软件漏洞信息。

**在云安全中心中查看当前软件漏洞信息**

您可以登录[云盾云安全中心管理控制台](https://yundunnext.console.aliyun.com/?p=sas)，在**弱点** \> **漏洞管理**中的系统软件漏洞页面，查看到云安全中心在您的服务器上检测到的系统软件漏洞信息。关于云安全中心对系统软件漏洞的各项参数说明，请参考[Linux软件漏洞各参数说明](intl.zh-CN/常见问题/常见问题隐藏目录/Linux软件漏洞各参数说明.md#)。

**在您的服务器上查看当前软件版本信息**

您也可以在您的服务器上直接查看当前的软件版本信息：

-   **CentOS 系统** 

    通过`rpm -qa | grep xxx`命令查看软件版本信息，其中`xxx`为软件包名。例如，执行`rpm -qa | grep bind-libs`命令查看服务器上的 bind-libs 软件版本信息。

-   **Ubuntu 和 Debian 系统** 

    通过`dpkg-query -W -f '${Package} -- ${Source}\n' | grep xxx`命令查看软件版本信息，其中`xxx`为软件包名。例如，执行`dpkg-query -W | grep bind-libs`命令查看服务器上的bind-libs软件版本信息。

    **说明：** 如果显示无法找到该软件包，您可以使用`dpkg-query –W`查看服务器上所安装的软件列表进行查看。


您通过以上命令获取您服务器上的软件版本信息后，可将得到软件版本信息与云安全中心系统软件漏洞中检测到的相关漏洞的说明信息进行对比，根据漏洞说明参数中的 “软件”和“命中”信息，确认是否满足漏洞版本信息。

**说明：** 如果升级后老版本软件包还有残留信息，这些老版本信息可能仍会被云安全中心检测收集，并作为漏洞上报。如果确认是由于这种情况产生的漏洞告警，建议您选择忽略该漏洞，或者您可以使用`yum remove`或者`apt-get remove`命令删除老版本的软件包（删除前，请务必确认已经没有在使用该老版本软件的业务或应用）。

## 如何将 Ubuntu 14.04 系统的 3.1\\\* 内核升级至 4.4 内核？ {#2 .section}

**说明：** 系统内核升级有一定风险，强烈建议您参考 [系统软件漏洞修复最佳实践]() 中的方法进行升级。

1.  执行`uname -av`命令，确认当前服务器的系统内核版本是否为3.1\*。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/163489/155972452745567_zh-CN.png)

2.  执行以下命令，查看是否已有最新的内核 Kernel 更新包。

    ``` {#codeblock_xqr_7ml_563}
    apt list | grep linux-image-4.4.0-94-generic
    apt list | grep linux-image-extra-4.4.0-94-generic
    ```

3.  如果没有相关更新，您可执行`apt-get update`命令获取到最新的更新包。
4.  执行以下命令，进行内核升级。

    ``` {#codeblock_iqq_3yw_w9s}
    apt-get update && apt-get install linux-image-4.4.0-94-generic
    apt-get update && apt-get install linux-image-extra-4.4.0-94-generic
    ```

5.  更新包安装完成后，重启服务器完成内核加载。
6.  服务器重启后，执行以下命令验证内核升级是否成功。
    -   执行`uname -av`命令查看当前调用内核。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/163489/155972452745568_zh-CN.png)

    -   执行`dpkg -l | grep linux-image`命令查看当前内核包情况。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/163489/155972452745570_zh-CN.png)


## 内核漏洞升级修复后，云安全中心仍然提示存在漏洞？ {#3 .section}

由于内核升级比较特殊，一般都会有老版本信息残留的问题。确认该漏洞告警是由于老版本信息残留造成后，您可以选择忽略该漏洞告警，或者删除老版本的残留信息。

1.  确认内核升级完成后，通过执行`uname –av`命令和`cat /proc/version`命令查看当前内核版本，确保当前使用的内核版本已符合漏洞说明命中条件中的要求。
2.  执行`cat /etc/grub.conf`命令查看配置文件，确认当前已经调用最新的内核版本。
3.  由于系统软件漏洞检测功能主要是通过针对版本进行匹配检测，如果系统中依然存在老版本的内核 rpm 安装包，仍将会被云安全中心检测到并进行漏洞告警。您需要确认当前系统中已经没有老版本 rpm 安装包残留，如果有，您可以对老版本安装包进行卸载。
4.  卸载老版本安装包前，请务必确认当前系统已经使用新内核。强烈建议您在卸载老版本内核安装包前，为您的系统创建快照以便于发生异常情况后的恢复。

**说明：** 如果由于某些原因不想卸载老版本内核，在您确认系统已经调用新内核后，可以在[云盾云安全中心管理控制台](https://yundunnext.console.aliyun.com/?p=sas)的系统软件漏洞页面对该漏洞进行忽略（在该漏洞的漏洞处理页面，单击操作栏中的**忽略**），暂时忽略该系统漏洞告警提醒。

## 云安全中心管理控制台中某些漏洞提示无更新？ {#4 .section}

-   您在对某些漏洞进行更新修复时，收到以下提示：

    ``` {#codeblock_xyi_nbl_1ip}
    Package xxx already installed and latest version
    Nothing to do
    					
    ```

    或

    ``` {#codeblock_ipr_6fz_4ed}
    No Packages marked for Update
    					
    ```

    这种情况是由于官方更新源暂时还未提供更新，请您等待官方更新源的更新。目前已知未更新的软件包包括：

    -   Gnutls
    -   Libnl
    -   Mariadb
-   您已经更新到了最新的软件包，但仍然无法满足云安全中心管理控制台中报告的软件版本条件。

    请检查您的操作系统版本官方是否已经停止支持。例如，截止到 2017 年 9 月 1 日，官方已经停止对 CentOS 6.2-6.6/7.1 等版本的支持。这种情况下，建议您在云安全中心管理控制台中忽略该漏洞（该漏洞对您服务器的风险可能依然存在），或者升级您的服务器操作系统。


## 如何手动检测服务器上的Linux软件漏洞？ {#5 .section}

如果您需要手动验证您服务器上的系统软件漏洞，您可以参考[如何手动检测系统软件漏洞？](intl.zh-CN/常见问题/如何手动检测系统软件漏洞？.md#)中的操作步骤检测您服务器上的系统软件漏洞。

建议您使用云安全中心的系统软件漏洞功能定期自动检测您服务器上的系统软件漏洞及时发现漏洞。

参考链接

-   [Frequently Asked Questions about CentOS in general](https://wiki.centos.org/FAQ/General)
-   [Ubuntu security notices](https://www.ubuntu.com/usn)

