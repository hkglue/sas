# Asset fingerprints {#concept_lyd_4zc_zdb .concept}

The asset fingerprint feature periodically collects the following information on your servers: processes, system accounts, listener ports, software, and website backgrounds. You can view the status of your assets and perform retrospective analysis using this information. This document describes how to view different asset fingerprints.

## Function description {#section_vxt_wrk_zdb .section}

The asset fingerprint feature contains the following modules:

-   Processes: Periodically collects information about processes on the server. Scenarios: to check which server is running a specific process, and to check which processes are initiated by a specific server.
-   Accounts: Periodically collects system account information on the server. Scenarios: to check which server has created a specific account, and to check which accounts are created by a specific server.
-   Listener ports: Periodically collects information about listener ports on the server. Scenarios: to check which server is listening on a specified port, and to check which ports are enabled on a specified server.
-   Software: Periodically collects software version information on the server. Scenarios: to check for illegal software installations, to check for obsolete software versions, and to quickly find the affected assets when vulnerabilities are exploited.
-   Website backgrounds: Periodically collects logon information at website backgrounds, detects weak passwords and user enumeration attempts, and monitors background security. Scenarios: to view logon records at backgrounds, to check whether weak passwords exist, and to view user enumeration attempts.

Additionally, for information about processes, system accounts, listener ports, and software, you can specify the frequency of data collection.

## View asset fingerprints for an individual asset {#section_hpm_mfg_f2b .section}

You can access the asset details of a specific asset through the Assets page and view the asset fingerprints of this asset. The individual asset fingerprints include processes, accounts, listener ports, and software.

1.  Log on to the [Security Center console](partners-intl.console.aliyun.com/#/sas).
2.  Go to the Assets page, select the asset you want to view, and click its **Asset IP/Name**.
3.  On the asset details page, click **Asset Fingerprints**.
    -   **View processes** 
        1.  Go to the Processes page to view all the running processes on the asset. You can search by process name or user.
        2.  Set **Data Type** to **Historical** to view the process changes, including **New Process** and **Stopped Process**.

            ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13642/15603170146445_en-US.jpg)

        3.  Click a process name to view the details.
    -   **View accounts** 
        1.  Go to the Accounts page to view all the logged-on system accounts on the asset. You can search by account name.
        2.  Set **Data Type** to **Historical** to view the system account changes, including **New**, **Modified**, and **Deleted**.

            ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13642/15603170146447_en-US.jpg)

        3.  Click an account name to view account details.
    -   **View listener ports** 
        1.  Go to the Listener Ports page to view all the enabled ports and the network protocols on the asset. You can search by port number or process name.
        2.  Set **Data Type** to **Historical** to view the listener port changes, including **New Listener** and **Disabled Listener**.

            ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13642/15603170146446_en-US.jpg)

        3.  Click a port number to view the details.
    -   **View software** 
        1.  Go to the Software page to view all the software on the asset. You can search by process, version, or installation directory.
        2.  Set **Data Type** to **Historical** to view the software changes, including **Install**, **Uninstall**, and **Update Version**.

            ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13642/15603170156448_en-US.jpg)

        3.  Click a software name to view the details.

## View asset fingerprints for all assets {#section_yxt_wrk_zdb .section}

You can view the asset fingerprints for all assets on the Asset Fingerprints page. The Asset Fingerprints page displays the real-time information for processes, accounts, listener ports, software, and website backgrounds.

Follow these steps to view asset fingerprints for all assets:

1.  Log on to the [Security Center console](partners-intl.console.aliyun.com/#/sas).
2.  In the left-side navigation pane, click **More**.
3.  Click **Asset Fingerprints**.
    -   **View processes** 
        1.  Go to the Processes page to view all the processes and servers that are running them. You can search by process name or user.
        2.  Click a process name to view the details.

            ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13642/15603170154944_en-US.png)

    -   **View system accounts** 
        1.  Go to the System Accounts page to view all the logged-on accounts and servers that are using them. You can search by account name.
        2.  Click an account name to view account details.

            ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13642/15603170154945_en-US.png)

    -   **View listener ports** 
        1.  Go to the Listener Ports page to view all the enabled ports, protocols, and servers that are using them. You can search by port number or process name.
        2.  Click a port number to view the details.

            ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13642/15603170154946_en-US.png)

    -   **View software** 
        1.  Go to the Software page to view all the software and servers that are using them. You can search by process, version, or by installation directory.
        2.  Click a software name to view the details.

            ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13642/15603170164947_en-US.png)

    -   **View website background logon records**: Go to the Website Background page to view the background logon records, weak logon passwords, and user enumerations attempts.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13642/15603170164948_en-US.png)


## Settings {#section_vyt_wrk_zdb .section}

On the Asset Fingerprints Settings page, you can specify the frequency of data collection for processes, system accounts, listener ports, and software.

You can specify the frequency of data collection by following these steps:

1.  Log on to the [Security Center console](partners-intl.console.aliyun.com/#/sas).
2.  In the left-side navigation pane, click **More**.
3.  Click **Asset Fingerprints**.
4.  In the upper right corner of the page, click **Settings**.
5.  Complete the following settings:

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13642/15603170166444_en-US.jpg)

    -   Select **Auto-Collect Listener Ports** and choose from the following: Disabled, Once an Hour, Once Every 3 Hours, Once Every 12 Hours, Once a Day, or Once a Week.
    -   Select **Auto-Collect Processes** and choose from the following: Disabled, Once an Hour, Once Every 3 Hours, Once Every 12 Hours, Once a Day, or Once a Week.
    -   Select **Auto-Collect System Accounts** and choose from the following: Disabled, Once an Hour, Once Every 3 Hours, Once Every 12 Hours, Once a Day, or Once a Week.
    -   Select **Auto-Collect Software** and choose from the following: Disabled, Once an Hour, Once Every 3 Hours, Once Every 12 Hours, Once a Day, or Once a Week.
6.  Click **OK** to apply the settings.

