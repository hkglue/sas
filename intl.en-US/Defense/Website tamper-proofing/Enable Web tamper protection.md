# Enable Web tamper protection {#concept_drl_cg3_dhb .concept}

Security Center Enterprise Edition and Pro Edition provide the Web tamper protection feature to protect your websites.

To use this feature, purchase Web tamper protection licenses, and then add servers and directories for protection.

**Note:** After you add a server on the Tamper Protection page, the protection is disabled for this server by default. To enable protection, you must turn on the toggle in the Protection column for the specific server. For more information about this operation, see step 9 in **Procedure**.

## Prerequisites {#section_f8p_dke_8kz .section}

Before using Web tamper protection, make sure that your account has sufficient licenses. On the Tamper Protection page in the Security Center console, you can view the total licenses, used licenses, and license expiration date in the upper-right corner.

![Tamper Protection](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/141310/156878712248735_en-US.png)

**Note:** 

-   One license can be used to protect one server. If you disable protection for one server, the license is released.
-   Make sure that you use the licenses before the expiration date. After the expiration date, the licenses become invalid.

If you need more licenses, click **Buy Licenses** in the upper-right corner of the Tamper Protection page, and purchase licenses in the **Web Tamper Protection** area on the purchasing page.

![Configuration Upgrade](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/141310/156878712248733_en-US.png)

## Limits {#section_yxo_3zs_r87 .section}

-   You can add a maximum of 10 directories of a server for protection.
-   The protected directories of a Windows server must meet the following requirements: The maximum size of each directory is 20 GB. Each directory contains a maximum of 20,000 folders. The maximum directory level is 20. The maximum size of each file is 3 MB.
-   The protected directories of a Linux server must meet the following requirements: The maximum size of each directory is 20 GB. Each directory contains a maximum of 3,000 folders. The maximum directory level is 20. The maximum size of each file is 3 MB.
-   Before you add a directory for protection, make sure that the directory level, the number of folders, and the directory size meet the preceding requirements.
-   We recommend that you exclude file formats that do not require protection, such as LOG, PNG, JPG, MP4, AVI, and MP3 files. Separate multiple file formats with semicolons \(;\).
-   You cannot add servers for protection if you do not have licenses. If a server does not require protection, turn off the toggle in the **Protection** column for this server. After this operation, the license used by this server is released, and you can add another server for protection.

## Procedure {#section_osb_2h3_3gb .section}

1.  Log on to the [Security Center console](https://yundun.console.aliyun.com/?p=sas).
2.  In the left pane, choose **Extensions** \> **Tamper Protection** to activate the Web Tamper Protection feature.

    **Note:** Only Enterprise Edition and Pro Edition provide this feature.

3.  In the upper-left corner of the Tamper Protection page, click **Add Server**.

    ![Add Server](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/141310/156878712242140_en-US.png)

4.  In the Add Servers for Protection dialog box, select servers.

    ![Add Servers for Protection](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/141310/156878712242149_en-US.png)

    **Note:** You cannot add servers for protection if you do not have licenses. If a server does not require protection, turn off the toggle in the **Protection** column for this server. After this operation, the license used by this server is released, and you can add another server for protection.

5.  Click **Next**.
6.  On the Add Protected Directories page, configure the following parameters:

    ![Add Protected Directories](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/141310/156878712242157_en-US.png)

    Select the protection mode. Whitelist mode and blacklist mode are available. In whitelist mode, specify the directories and file formats to be protected. In blacklist mode, specify the sub-directories, file formats, and files that do not require protection, and all the other files in the specified directory are protected. The whitelist mode is used by default.

    -   In whitelist mode, configure the following parameters:
        -   **Protected Directory**: Enter a directory to be protected.

            **Note:** The format of a directory varies with the server OS. Enter a directory in the right format.

        -   **Protected File Formats**: In the drop-down list, select the file formats to be protected, for example, JS, HTML, XML, and JPG.
        -   **Local Backup Directory**: The default backup directory is displayed. Security Center assigns the following default backup directories: /usr/local/aegis/bak for Linux servers and C:\\Program Files \(x86\)\\Alibaba\\Aegis\\bak for Windows servers. You can modify this directory.
    -   In blacklist mode, configure the following parameters:
        -   **Protected Directory**: Enter a directory to be protected.
        -   **Excluded Sub-Directories**: The sub-directories that do not require protection. Enter sub-directories. Separate multiple sub-directories with semicolons \(;\). Security Center does not protect the files in the excluded sub-directories.
        -   **Excluded File Formats**: The file formats that do not require protection. Enter file formats. Separate multiple file formats with semicolons \(;\). Security Center does not protect the files of the excluded file formats.
        -   **Local Backup Directory**: The default backup directory is displayed. Security Center assigns the following default backup directories: /usr/local/aegis/bak for Linux servers and C:\\Program Files \(x86\)\\Alibaba\\Aegis\\bak for Windows servers. You can modify this directory.
7.  Click **Enable Protection**.

    After you add a server, it is displayed on the server list on the Tamper Protection page.

    ![server list](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/141310/156878712248747_en-US.png)

    **Note:** Web Tamper Protection is **disabled by default** for a newly added server. To enable protection, you must turn on the toggle in the Protection column for this server on the Tamper Protection page.

8.  On the server list on the Tamper Protection page, turn on the toggle in the **Protection** column for this server.

    ![Protection](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/141310/156878712248754_en-US.png)

    After you enable protection for a server for the first time, the service status is changed to **Initializing**, and a progress bar is displayed. After several seconds, the service status is changed to **Running**.

    ![Running](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/141310/156878712348755_en-US.png)

    **Note:** If the service status of a server is Exception, click **Exception**. The details of the exception are displayed. click **Retry**. For more information, see [Handle protection service exceptions](#).


## Subsequent operations {#section_tk1_0sl_szt .section}

After you enable Web Tamper Protection, you can go to the Alerts page, and select Tamper Protection in the event type drop-down list to view the alerts on Web tampering events.

![Alerts](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/141310/156878712348739_en-US.png)

## Handle protection service exceptions {#abnormal .section}

|Service status|Description|Resolution|
|--------------|-----------|----------|
|Initializing|Web Tamper Protection is being initialized.|After you enable protection for a server for the first time, the service status is changed to **Initializing**. It takes several seconds to start the service.|
|Running|The protection is enabled.|-|
|Exception|An error occurred while starting the service.|Click **Exception** in the Status column. The details of the exception are displayed. Click **Retry**. For more information, see [Handle protection service exceptions](#).|
|Not initialized|The protection service is disabled.|Set the toggle in the Protection column to **On**.|

