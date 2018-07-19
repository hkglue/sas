# Quick start {#task_rgj_rcc_zdb .task}

Situation Awareness Service \(SAS\) provides multiple features, including alerts, vulnerability detection, baseline check, asset fingerprints, and log queries. SAS allows you to implement complete detection and protection for your servers and web applications. You can also view asset statistics and security information.

1.   Log on to the [SAS console](https://yundun.console.aliyun.com/?p=sas).
2.  Install the SAS agent on your server. 

    **Note:** The SAS agent is a security plug-in running on your servers. It has been integrated into Alibaba Cloud public images. When you create an ECS instance, you can select a public image and enable **Security Enhancement** to automatically install the SAS agent on your instance. For more information about how to manually install the SAS agent on an external server, see [Install the Situation Awareness Service agent](../../../../intl.en-US/User Guide/Access Threat Detection/Install Situation Awareness Service agent.md#).

3.   After the SAS agent has been installed, you can go to the SAS Overview page to view the security status of the servers under your Alibaba Cloud account. Security status includes alerts, server vulnerability and web vulnerability scan results, vulnerable configurations in server and cloud service baselines, and status of the agent.  

    **Note:** The SAS agent detects and collects the security status of the servers that SAS protects. You can determine the status of your server protected by SAS by verifying the status of the SAS agent. Your server is online only if the status of the agent appears online. To resolve the issue of a server going offline, see [Troubleshoot the problem of Situation Awareness Service agent going offline](../../../../intl.en-US/User Guide/Access Threat Detection/Troubleshoot the problem of SAS agent going offline.md#).

4.   In the SAS console, you can view and manage flaws and security events on your server and perform the following operations to enhance the security of your server: 
    -   Go to the Assets page to view detailed information about the security status of the servers under your Alibaba Cloud account. This page also allows you to add tags to assets and create asset groups. For more information about this page, see [Asset list](../../../../intl.en-US/User Guide/Assets.md#).
    -   Go to the Events page to view unusual activities and attacks that have been detected on your servers, such as unusual logon activities, brute force cracking, web shells, suspicious processes,suspicious network connections, sensitive file tampering, and malicious processes. For more information, see [Events](../../../../intl.en-US/User Guide/Security Warning.md#).
    -   Go to the**Vulnerability Management** \> **Server Vulnerabilities**page to view web content management system \(WCMS\) vulnerabilities and system software vulnerabilities. For more information, see Server threat management.
    -   Go to the**Baseline Check** \> **Servers**page to view and manage vulnerable configurations that have been detected on your servers. For more information, see [Server baseline check](../../../../intl.en-US//Server baseline check.md#).
    -   Go to the**Baseline Check** \> **Cloud Services**page to view and manage vulnerable configurations that have been detected in your cloud services. For more information, see [Cloud service baseline check](../../../../intl.en-US//Cloud service baseline check.md#).
    -   Go to the Asset Fingerprints page to view asset summary, including processes running on your servers, enabled system accounts, open ports, software version, and logons to the back end of your website. For more information, see [Asset fingerprints](../../../../intl.en-US/User Guide/Asset fingerprint.md#).
    -   Go to the**Other** \> **Log Search**page to search up to 10 types of logs, such as process logs, network logs, and logon and account logs. You can enable the log shipper function to import these logs to Log Service for analysis. For more information, see [Log retrieval](../../../../intl.en-US/User Guide/Log retrieval.md#).
    -   The SAS console also provides additional settings for you to use the SAS features more efficiently. You can go to the Settings page to perform the following tasks:

        -   Install or uninstall the SAS agent.
        -   Enable or disable daily report.
        -   Configure alert policies.
        For more information about this page, see [Situation Awareness Service settings](../../../../intl.en-US/User Guide/Settings.md#). 


