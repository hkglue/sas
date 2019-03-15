# Install the TDS agent {#concept_dl4_ykc_zdb .concept}

The Threat Detection Service \(TDS\) agent is a security plug-in running on servers. To use TDS to protect your servers, you must first install the TDS agent in the guest operating system of your servers.

## Automatically install the TDS agent through Alibaba Cloud public images {#section_prp_z1d_zdb .section}

The TDS agent has been integrated into Alibaba Cloud public images. When you create an ECS instance, select a public image and enable **Security enhancement** to automatically install the TDS agent on your instance.

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13631/15526334304557_en-US.png)

## View the security status of your instance {#section_izq_114_k2b .section}

The security status of an instance indicates whether or not the TDS agent is installed or working properly on the instance.

Log on to the [Threat Detection Service console](https://yundun.console.aliyun.com/?p=sas), and view the **Security Status** of all your instances on the Assets page.

-   **Protected** indicates that the TDS agent is installed on the instance and is online.
-   **Unprotected** indicates that the TDS agent is not installed on the instance or is offline.

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13631/15526334306339_en-US.jpg)

If the security status of your servers appears unprotected, use the following method to manually download and install the TDS agent on your servers.

## Manually install the TDS agent on a server \(including external servers\) {#section_rrp_z1d_zdb .section}

**Note:** If security software such as Fortinet FortiGate has been installed on your server, the system may fail to install the TDS agent correctly. We recommend that you check whether security software already exists on your server before installing the TDS agent. If you have already installed security software to your server, disable or uninstall the software before you install the TDS agent.

**Prerequisites**

Before you install the TDS agent, make sure that your server meets the following requirements:

-   If the server has been deployed in Alibaba Cloud, you can directly install the TDS agent on the server.
-   If the server is not in Alibaba Cloud and communicates with Alibaba Cloud over the Internet, make sure that your server has access to the Internet.
-   If the server is not in Alibaba Cloud and communicates with Alibaba Cloud through a leased line, add the following lines to the host file in the operating system of your server for TDS host names to be resolved.
    -   `100.100.25.3 jsrv.aegis.aliyun.com`
    -   `100.100.25.4 update.aegis.aliyun.com`

**Procedure**

Follow these steps to manually install the TDS agent:

1.  Log on to the [Threat Detection Service console](https://yundun.console.aliyun.com/?p=sas).
2.  In the left-side navigation pane, click **Settings**.
3.  Click **Install/Uninstall TDS Agent**.
4.  Select the installation method that is applicable to the operating system of your server to download and install the latest TDS agent version:
    -   **Windows**
        1.  Click **Download** to download the latest version of TDS agent package to your PC.
        2.  Upload the TDS agent package to your server. For example, you can use an FTP client to upload the package to the server.
        3.  Run the package on your server as an administrator.

            **Note:** The installation of the TDS agent requires a verification key. The verification key is used to associate the TDS agent with your Alibaba Cloud account. You can view the verification key on the Install/Uninstall TDS Agent page.

    -   **Linux**
        1.  Depending on the type of your server, select **Alibaba Cloud Servers** or **External Servers**.
        2.  Log on to your Linux instance as an administrator.
        3.  Upload the TDS agent package to your Linux server, and then select an install command that is applicable to the operating system of your server.
        4.  Run the command to download and install the TDS agent.

            **Note:** The install command will download the latest version of TDS agent package from Alibaba Cloud. Before you run the command, make sure that your server has access to the Internet.

5.  The TDS agent installation may take five minutes to complete. After the TDS agent has been installed, log on to the TDS console and verify the server security status on the Assets page:
    -   If the server is an ECS instance, the security status of the server changes from **Unprotected** to **Protected**.
    -   If the server is an external server, the server is added to the asset list.

## Verify TDS agent installation {#section_csp_z1d_zdb .section}

Follow these steps to verify the TDS agent installation:

1.  Verify if the TDS agent processes, including AliYunDun and AliYunDunUpdate, are running correctly. For more information about the TDS agent processes, see [Threat Detection Service agent](intl.en-US/User Guide/Access Threat Detection Service/Threat Detection Service agent.md#).
2.  Verify that your instance can communicate with TDS servers by running the following telnet commands on your instance: 

    **Note:** Make sure that your server can access at least one of the following jsrv domain names and one of the following update domain names.

    -   `telnet jsrv.aegis.aliyun.com 80`
    -   `telnet jsrv2.aegis.aliyun.com 80`
    -   `telnet jsrv3.aegis.aliyun.com 80`
    -   `telnet update.aegis.aliyun.com 80`
    -   `telnet update2.aegis.aliyun.com 80`
    -   `telnet update3.aegis.aliyun.com 80`

If the verification fails, follow the instructions in [Troubleshoot the problem of TDS agent going offline](intl.en-US/User Guide/Access Threat Detection Service/Troubleshoot the problem of TDS agent going offline.md#) to resolve the issue.

## Restrictions and guidelines {#section_fsp_z1d_zdb .section}

For an external server that runs Windows, you must use the TDS agent package to install the agent. For an external server that runs Linux, you must run the relevant command to install the agent.

To make sure that the agent can run correctly in the following situations, delete the TDS agent directory and follow the preceding steps to manually reinstall the agent.

-   You have used an image that includes the TDS agent to install the TDS agent on multiple external servers.
-   You have directly copied the TDS agent files to your external servers.

**TDS agent directory**

-   Windows: C:\\Program Files \(x86\)\\Alibaba\\Aegis
-   Linux: /usr/local/aegis

