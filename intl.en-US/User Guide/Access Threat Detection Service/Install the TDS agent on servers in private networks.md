# Install the TDS agent on servers in private networks {#concept_vth_3zc_zdb .concept}

The following sections describe how to install the Threat Detection Service \(TDS\) agent to connect instances in private networks \(such as instances used in Alibaba Cloud’s Financial Service Solutions, or instances in Alibaba Cloud VPC\) to the TDS server.

## Procedure {#section_qqt_mcd_zdb .section}

Follow these steps to install the TDS agent on servers in private networks:

**Note:** If security software such as Fortinet FortiGate has been installed on your server, the system may fail to install the TDS agent correctly. We recommend that you check whether security software already exists on your server before installing the TDS agent. If security software is already installed on your instances, we recommend that you temporarily disable or uninstall the software before you install the TDS agent.

1.  Log on to the [Threat Detection Service console](https://yundun.console.aliyun.com/?p=sas).
2.  Go to the **Settings** page.
3.  Click **Install/Uninstall TDS Agent**.
4.  Depending on the operating system running on your instance, select the applicable installation method.
    -   **Windows**
        1.  Click **Download** on the Install/Uninstall TDS Agent page to download the latest version of TDS agent package to your PC.
        2.  Upload the TDS agent package to your instance. For example, you can use an FTP client to upload the package to the instance.
        3.  Run the package on your instance as an administrator.

            **Note:** The installation of the TDS agent requires a verification key. The verification key is used to associate the TDS agent with your Alibaba Cloud account. You can view the verification key on the Install/Uninstall TDS Agent page.

    -   **Linux**
        1.  Depending on your system requirements, click one of the following links to download the TDS agent package to your PC.
            -   32-bit Linux: [TDS agent package](https://aegis.alicdn.com/download/AliAqsInstall_32.sh)
            -   64-bit Linux: [TDS agent package](https://aegis.alicdn.com/download/AliAqsInstall_64.sh)
        2.  Upload the TDS agent package to your instance. For example, you can use an FTP client to upload the package to the instance.
        3.  Log on to your Linux instance as an administrator.
        4.  Locate the directory that stores the uploaded TDS agent package and, depending on your system requirements, run one of the following commands to install the TDS agent:

            -   32-bits Linux: `chmod +x AliAqsInstall_32.sh && . /AliAqsInstall_32.sh xxxxxx`
            -   64-bits Linux: `chmod +x AliAqsInstall_64.sh && . /AliAqsInstall_64.sh xxxxxx`
            **Note:** Replace `xxxxxx` at the end of each command with the verification key that is provided on the Install/Uninstall TDS Agent page. This verification key is the same as that used to install the TDS agent to a Windows running instance. The verification key is used to associate the TDS agent with your Alibaba Cloud account.

5.  Once the TDS agent is installed and synced with your instances \(this process may take up to 5 minutes\), you can log on to the TDS console and view the Security Status of your instances on the Assets page. The Security Status of your instances will change from **Unprotected** to **Protected**.

## Verify TDS agent installation {#section_art_mcd_zdb .section}

To verify your TDS agent installation, follow these steps:

1.  Verify that the AliYunDun and AliYunDunUpdate processes of the TDS agent are running normally. For more information about the TDS agent processes, see [Threat Detection Service agent](intl.en-US/User Guide/Access Threat Detection Service/Threat Detection Service agent.md#).
2.  Verify that your instance can communicate with TDS servers by running the following telnet commands on your instance: 

    **Note:** Make sure that your instance can communicate with the following two TDS servers properly:

    -   `telnet jsrv3.aegis.aliyun.com 80`
    -   `telnet update3.aegis.aliyun.com 80`

If your instance cannot communicate with the TDS servers properly, see [Troubleshoot the problem of TDS agent going offline](intl.en-US/User Guide/Access Threat Detection Service/Troubleshoot the problem of TDS agent going offline.md#) to resolve the issue. 

