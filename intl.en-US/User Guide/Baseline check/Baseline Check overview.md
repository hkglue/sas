# Baseline Check overview {#concept_xpl_nzc_zdb .concept}

This topic describes how to use the Baseline Check feature and handle the configuration risks on your servers.

## Features {#section_gxf_n4k_zdb .section}

After you activate Baseline Check, Security Center automatically detects risks related to the systems, accounts, databases, passwords, and security compliance configurations of your servers, and provides resolutions. For more information on the check items, see [Baseline Check items](reseller.en-US/User Guide/Baseline check/Baseline Check overview.md#table_brz_4q1_f2b).

Security Center automatically checks your baseline configurations from 00:00 to 06:00 every day. You can create the check policies and manage the policies. When you create or modify a policy, you can customize the items, the cycle, and the time of a baseline check, and select the servers to which you want to apply this policy.

## Restrictions {#section_sng_3xk_dhb .section}

Baseline Check is a value-added service of Security Center. Only **Enterprise Edition** or users can activate and use this service. A Basic Edition or Pro Edition user must upgrade to **Enterprise Edition** to use this service.

Logon attempts may be required to check for weak passwords on applications such as MySQL and SQL Server. This leads to server resource consumption and many logon failure records. Therefore, Security Center disables the check for weak passwords on specific applications and system compliance with classified protection standards by default. To check these items, make sure that you are aware of the risks mentioned above, and select these items when you customize a scan policy.

## Baseline Check items {#section_zgh_y6u_vnj .section}

|Category|Check item|
|--------|----------|
|Database|Risks in the port listening configuration of Redis or Memcached and risks in the configuration of the permission to start Redis or Memcached.|
|System|The classified protection standard compliance check covers check items in the level 2 and level 3 security requirements stated in China Classified Protection Standard 2.0. The security baseline check follows the security standards of Alibaba Cloud and Center for Internet Security \(CIS\). Security Center checks these items on the following systems: -   CentOS Linux 6 and Linux 7
-   Linux Ubuntu
-   Debian Linux
-   Windows 2008 R2 and 2012 R2

 |
|Weak password|PostgreSQL weak password|
|SSH weak password|
|Anonymous FTP logon|
|SQL Server weak password|
|MySQL weak password|
|RDP weak password|
|FTP weak password|
|Middleware|Apache Tomcat security baseline|

