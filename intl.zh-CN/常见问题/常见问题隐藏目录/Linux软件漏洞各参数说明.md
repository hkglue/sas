# Linux软件漏洞各参数说明 {#concept_56586_zh .concept}

您通过本文档可以了解Linux软件漏洞各项参数的含义及相关说明，帮助您对云安全中心发现的Linux软件漏洞有更深的认知。

您可以登录[云安全中心管理控制台](https://yundunnext.console.aliyun.com/?p=sas)，前往**漏洞修复**页面，在Linux软件漏洞页签下查看到云安全中心在您的服务器上检测到的Linux软件漏洞。

## 漏洞名称 {#section_54i_ii7_7f5 .section}

在Linux软件漏洞页面单击需要查看的漏洞，进入该漏洞的详情页面。

该Linux软件漏洞的名称，一般以 CVE 及 RHSA 开头。例如，RHSA-2016:2972: vim security update。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/163490/155963001245593_zh-CN.png)

## CVSS分值 {#section_o9c_tir_83n .section}

CVSS 分值是依据行业公开标准，通用漏洞评分系统（Common Vulnerability Scoring System），对该漏洞判定的一个分值，主要用于评测漏洞的严重程度，可以帮助您确定所需反应的紧急度和重要度。

## CVEID {#section_c7n_nf6_tvx .section}

该漏洞对应的 CVE 漏洞号，通过 CVEID，如 CVE-2016-1248。Common Vulnerabilities & Exposures （CVE）是已被广泛认同的信息安全漏洞或者已经暴露的弱点的公共名称。您可以快速地在任何其它 CVE 兼容的数据库中找到相应漏洞修复的信息，帮助您解决安全问题。

## 漏洞等级 {#section_5fi_m0t_s8i .section}

漏洞等级分为严重、高危、中危和低危。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/163490/155963001345596_zh-CN.png)

-   **严重**等级的漏洞包括：
    -   可直接获取服务器系统权限的漏洞。
    -   可直接获取重要的敏感信息导致数据泄漏。
    -   可直接导致敏感信息越权访问的漏洞。
    -   可造成大范围影响的其他漏洞。
-   **高危**等级的漏洞包括：
    -   可间接获取服务器和应用系统的普通权限的漏洞。
    -   可导致任意文件读取、下载、写入、或删除的漏洞。
    -   可导致敏感信息泄漏的漏洞。
    -   可直接导致业务中断、或远程拒绝服务的漏洞。
-   **中危**等级的漏洞包括：
    -   需要进行交互才能影响用户的漏洞。
    -   可导致普通越权操作的漏洞。
    -   通过本地修改配置或获取信息之后，可进一步的利用漏洞。
-   **低危**等级漏洞包括：
    -   可导致本地拒绝服务的漏洞。
    -   其他危害较低的漏洞。

本例中的漏洞为高危等级漏洞，通过此漏洞可以间接获取服务器和应用系统的用户权限。

## 说明 {#section_x4d_333_x3p .section}

漏洞说明包含软件及命中两个说明内容。

-   **软件**：显示云安全中心收集到的当前服务器系统中的软件版本信息。
-   **命中**：显示该漏洞的匹配命中原因，一般是由于当前软件版本不满足或者小于某个版本（以小于某个版本为主），因此存在该漏洞。

单击**说明**内容右侧的**更多**，可查看详细说明信息。例如：

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/163490/155963001345598_zh-CN.png)

-   **软件**：`5.5.44-2.el7.centos` 

    云安全中心检查到的您服务器上的软件版本，即当前检测到服务器上的mariadb-libs的版本是 5.5.44-2.el7.centos。

-   **命中**：`mariadb-libs version less than 1:5.5.52-1.el7` 

    该软件漏洞的匹配命中原因，即当前 mariadb-libs 软件版本小于1:5.5.52-1.el7。

-   **路径**：`/etc/virc` 

    云安全中心检查到的该软件在您服务器上的路径，即 mariadb-libs 所在路径为 /etc/ld.so.conf.d/mariadb-x86\_64.conf。


## 首次/最后发现时间 {#section_6we_iu1_amy .section}

该Linux软件漏洞第一次被发现的时间，及最近一次进行云安全中心漏洞检测发现的时间。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/163490/155963001345599_zh-CN.png)

## 操作 {#section_7gc_uxw_099 .section}

您可对检测到的Linux漏洞执行以下操作：

-   生成修复命令：生成可执行的漏洞修复命令。
-   一键修复：一键修复Linux漏洞。
-   验证：对漏洞进行验证。
-   忽略：忽略该漏洞。

