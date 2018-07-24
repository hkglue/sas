# Quick start {#task_rgj_rcc_zdb .task}

Threat Detection Service \(TDS\) provides multiple features, including security events, vulnerability detection, baseline check, asset fingerprints, and log retrieval. TDS allows you to implement complete detection and protection for your servers and web applications. You can also view asset statistics and security information.

1.  Log on to the [Threat Detection Service console](https://yundun.console.aliyun.com/?p=sas). 
2.  Install the TDS agent plug-in for your server. 

    **Note:** The TDS agent is a security plug-in running on your servers. It has been integrated into Alibaba Cloud public images. When you create an ECS instance, you can select a public image and enable **Security enhancement** to automatically install the TDS agent on your instance. For more information about how to manually install the TDS agent on an external server, see [Install the TDS agent](../../../../intl.en-US/User Guide/SAS agent/Install the TDS agent.md#).

3.  After the TDS agent has been installed, you can go to the Assets page in the TDS console to view the security status of the servers under your Alibaba Cloud account. 

    **Note:** The TDS agent detects and collects the security status of the servers that TDS protects. You can determine the status of the installed TDS agent by verifying the security status of your server. If the security status of your server is protected, the installed agent is online and working properly. If the security status is unprotected, the installed agent is offline. For more information, see [Troubleshoot the problem of TDS agent going offline](../../../../intl.en-US/User Guide/SAS agent/Troubleshoot the problem of TDS agent going offline.md#).

4.  In the TDS console, you can view and manage flaws and security events on your server and perform the following operations to enhance the security of your server: 
    -   Go to the Assets page to view detailed information about the security status of the servers under your Alibaba Cloud account. This page also allows you to add tags to assets and create asset groups. For more information about this page, see [Assets](../../../../intl.en-US/User Guide/Assets.md#).
    -   Go to the Events page to view unusual activities and attacks that have been detected on your servers, such as unusual logon activities, brute force cracking, web shells, suspicious processes, suspicious network connections, sensitive file tampering, and malicious processes. For more information, see [Security events](../../../../intl.en-US/User Guide/Security events.md#).
    -   Go to the **Vulnerabilities** \> **Server** page to view web content management system \(WCMS\) vulnerabilities and system software vulnerabilities. For more information, see [Server vulnerability](../../../../intl.en-US/User Guide/Vulnerabilities/Server vulnerability management.md#).
    -   Go to the **Baseline Check** \> **Servers** page to view and manage vulnerable configurations that have been detected on your servers. For more information, see [Server baseline check](../../../../intl.en-US/User Guide/Baseline check/Server baseline check.md#).
    -   Go to the **More** \> **Asset Fingerprints** page to view asset summary, including processes running on your servers, enabled system accounts, open ports, software version, and logons to the back end of your website. For more information, see [Asset fingerprints](../../../../intl.en-US/User Guide/Asset fingerprints.md#).
    -   Go to the **More** \> **Log Retrieval** page to search up to 10 types of logs, such as process logs, network logs, and logon and account logs. For more information, see [Log retrieval](../../../../intl.en-US/User Guide/Log retrieval/Log retrieval.md#).
    -   The TDS console also provides additional settings for you to use the TDS features more efficiently. You can go to the Settings page to perform the following tasks:

        -   Install or uninstall the TDS agent.
        -   Configure alert policies.
        For more information about this page, see [Threat Detection Service settings](../../../../intl.en-US/User Guide/Settings.md#). 


