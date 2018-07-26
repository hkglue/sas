# Server baseline check {#concept_xpl_nzc_zdb .concept}

Threat Detection Service \(TDS\) supports baseline checks to automatically detect vulnerable configurations on servers and provides resolutions. This article describes how to use the server baseline check to locate and optimize vulnerable configurations on servers.

## Function description {#section_gxf_n4k_zdb .section}

After you enable the server baseline check, TDS automatically detects risks related to systems, accounts, databases, passwords, and compliance configurations of your servers, and provides resolutions. For more information about the check items, see [Details of the server baseline check](#section_e1p_s4k_zdb).

By default, TDS automatically performs the server baseline check once between 00:00 and 06:00 each day. You can add and maintain a scan policy that specifies the check items, target instances, check cycle, and trigger time.

**Note:** For some checked items, such as detecting weak passwords in MySQL and SQL Server services, TDS may use certain instance resources for logon attempts, and generate some logon failure records. Therefore, these checked items are disabled by default.  If you require these items, confirm the preceding risks, customize the server baseline scan policy, and then check these items.

You can configure a whitelist for the server baseline check. TDS skips items that are included in the whitelist. You can also add notes to the items in the whitelist to facilitate tracking.

## Add a scan policy {#section_hxf_n4k_zdb .section}

When you enable the server baseline check, the default policy is used. You cannot change the check items and check cycle of the default policy.

Follow these steps to create a scan policy:

1.  Log on to the [Threat Detection Service console](https://yundun.console.aliyun.com/?p=sas).
2.  In the left-side navigation pane, click **Baseline Check**.
3.  Click **Create Policy** to create a scan policy and follow these configurations:

    1.  Enter a policy name.
    2.  Select the items to check related to compliance configurations, passwords, systems, accounts, and databases. For more information, see [Details of the server baseline check](#section_e1p_s4k_zdb).
    3.  Specify the check cycle \(1, 3, 7, or 30 days\), and trigger time \(00:00-06:00, 06:00-12:00, 12:00-18:00, or 18:00-24:00\).
    4.  Select the target assets.

        **Note:** By default, new instances are sent to **All Groups** \> **default**. To apply this policy to new instances, select **Default**.

    5.  Click **OK**.
    The new policy takes effect immediately, and runs a scan according to the specified cycle and trigger time. You can also click **Check Now** on a target policy on the Servers tab page to run the scan immediately.

4.  Click **Settings** in the upper-right corner on the Baseline Check page. Then, in the dialog box that appears, select a target policy from the list under **Scan Policy**, and click **Edit** to edit this policy, or click **Delete** to delete this policy.

     


## View and fix vulnerable configurations {#section_uw5_djv_k2b .section}

Follow these steps to locate and optimize vulnerable configurations on your instance:

1.  Log on to the [Threat Detection Service console](https://yundun.console.aliyun.com/?p=sas).
2.  In the left-side navigation pane, click **Baseline Check**.
3.  On the Servers tab page, check vulnerable configurations on your instance.
4.  You can quickly locate a vulnerable configuration by specifying its name, category, severity, and status. 

    **Note:** When you specify a category, you can then choose a sub-category.

5.  On the Servers tab page, perform the following actions as needed:
    -   Select risk items and click **Ignore** to ignore them. The ignored items do not trigger alarms any more.
    -   Select risk items and click **Add to Whitelist** to add them to the whitelist. TDS does not check the items in the whitelist.
6.  Click the name of a risk to enter the details page, and view the details of the risk and affected assets.
7.  Refer to the suggestion in **Details** \> **More** to fix the risk on servers.

    **Note:** You can select one or more affected assets and apply the bulk operations at the bottom of the Affected Assets list.

    -   Once you fix the risk, click **Verify** in the **Actions** column to verify if the risk has been fixed successfully. If you do not perform a manual verification, the system automatically verifies the resolution 72 hours after the resolution is applied.
    -   If you do not want to receive an alarm for this risk item, you can click **Ignore** in the **Actions** column to ignore the risk. The ignored risk does not trigger any alarm.
    -   If you do not want to check for the specified risk, click **Add to Whitelist** in the upper-right corner of the page, and add a note to this item. You can remove a risk item from the whitelist in [Settings](#section_nxf_n4k_zdb).

## Settings {#section_nxf_n4k_zdb .section}

Follow these steps to change server baseline check settings:

1.  Log on to the [Threat Detection Service console](https://yundun.console.aliyun.com/?p=sas).
2.  In the left-side navigation pane, click **Baseline check**.
3.  Click **Settings** in the upper right corner of the page. You can perform the following settings:
    -   **Edit** or **Delete** scan policies. For more information, see [Add a scan policy](intl.en-US/User Guide/Baseline check/Server baseline check.md#ol_oxf_n4k_zdb).
    -   Set a time frame for **Retain Invalid Risks** for: 7 days, 30 days, or 90 days. 

        **Note:** If you do not take any actions on the detected risks, the system determines that these risks are invalid. The system deletes them when the retention period expires.

    -   Maintain the **Baseline Check Whitelist**: Click **Remove** under a risk to remove this item from the whitelist. Then, the system performs a new scan and generates the corresponding alarms.

## Details of the server baseline check {#section_e1p_s4k_zdb .section}

|Category|Check item|
|Compliance with Security Standards|httpd2.2|
|Windows 2008 R2|
|Memcached|
|CentOS 7|
|MySQL 5.6 Database|
|SQL Server 2008 R2|
|Tomcat 7|
|MongoDB|
|Ubuntu 14|
|Weak Password|PostgreSQL Weak Password|
|SSH Weak Password|
|Anonymous FTP Logon|
|SQL Server Weak Password|
|MySQL Weak Password|
|RDP Weak Password|
|FTP Weak Password|
|System|Group Policy|
|Baseline Policy|
|System File Changes|
|Registry|
|Account|System Account Security|
|Database|Redis Configurations|

