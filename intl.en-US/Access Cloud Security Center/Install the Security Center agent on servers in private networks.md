# Install the Security Center agent on servers in private networks {#concept_vth_3zc_zdb .concept}

The following sections describe how to install the Security Center agent to connect instances in private networks \(such as instances used in Alibaba Cloud’s Financial Service Solutions, or instances in Alibaba Cloud VPC\) to the Security Center server.

## Procedure {#section_qqt_mcd_zdb .section}

Follow these steps to install the Security Center agent on servers in private networks:

**Note:** If security software such as Fortinet FortiGate has been installed on your server, the system may fail to install the Security Center agent correctly. We recommend that you check whether security software already exists on your server before installing the Security Center agent. If security software is already installed on your instances, we recommend that you temporarily disable or uninstall the software before you install the Security Center agent.

1.  Log on to the [Security Center console](partners-intl.console.aliyun.com/#/sas).
2.  Go to the **Settings** page.
3.  Click **Install/Uninstall Security Center Agent**.
4.  Depending on the operating system running on your instance, select the applicable installation method.
    -   **Windows** 
        1.  Click **Download** on the Install/Uninstall Security Center Agent page to download the latest version of Security Center agent package to your PC.
        2.  Upload the Security Center agent package to your instance. For example, you can use an FTP client to upload the package to the instance.
        3.  Run the package on your instance as an administrator.

            **Note:** The installation of the Security Center agent requires a verification key. The verification key is used to associate the Security Center agent with your Alibaba Cloud account. You can view the verification key on the Install/Uninstall Security Center Agent page.

    -   **Linux** 
        1.  Depending on your system requirements, click one of the following links to download the Security Center agent package to your PC.
            -   32-bit Linux: [Security Center agent package](https://aegis.alicdn.com/download/AliAqsInstall_32.sh)
            -   64-bit Linux: [Security Center agent package](https://aegis.alicdn.com/download/AliAqsInstall_64.sh)
        2.  Upload the Security Center agent package to your instance. For example, you can use an FTP client to upload the package to the instance.
        3.  Log on to your Linux instance as an administrator.
        4.  Locate the directory that stores the uploaded Security Center agent package, depending on your system requirements, run one of the following commands to install the Security Center agent:

            -   32-bits Linux: `chmod +x AliAqsInstall_32.sh && . /AliAqsInstall_32.sh xxxxxx`
            -   64-bits Linux: `chmod +x AliAqsInstall_64.sh && . /AliAqsInstall_64.sh xxxxxx`
            **Note:** Replace `xxxxxx` at the end of each command with the verification key that is provided on the Install/Uninstall Security Center Agent page. This verification key is the same as that used to install the Security Center agent to a Windows running instance. The verification key is used to associate the Security Center agent with your Alibaba Cloud account.

5.  Once the Security Center agent is installed and synced with your instances \(this process may take up to 5 minutes\), you can log on to the Security Center console and view the Security Status of your instances on the Assets page. The Security Status of your instances will change from **Unprotected** to **Protected**.

## Verify Security Center agent installation {#section_art_mcd_zdb .section}

To verify your Security Center agent installation, follow these steps:

1.  Verify that the AliYunDun and AliYunDunUpdate processes of the Security Center agent are running normally. For more information about the Security Center agent processes, see [Security Center agent](reseller.en-US/Access Cloud Security Center/Security Center agent.md#).
2.  Verify that your instance can communicate with Security Center servers by running the following telnet commands on your instance:

    **Note:** Make sure that your instance can communicate with the following two Security Center servers properly:

    -   `telnet jsrv3.aegis.aliyun.com 80`
    -   `telnet update3.aegis.aliyun.com 80`

If your instance cannot communicate with the Security Center servers properly, see [Troubleshoot the problem of Security Center agent going offline](reseller.en-US/Access Cloud Security Center/Troubleshoot the problem of Security Center agent going offline.md#) to resolve the issue.

