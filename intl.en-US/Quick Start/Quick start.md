# Quick start {#task_rgj_rcc_zdb .task}

Security Center provides multiple features, including security events, vulnerability detection, baseline check, asset fingerprints, and log retrieval. Security Center allows you to implement complete detection and protection for your servers and web applications. You can also view asset statistics and security information.

1.  Log on to the [Security Center console](partners-intl.console.aliyun.com/#/sas).
2.  Install the Cloud Security Center agent plug-in for your server. 

    **Note:** The Security Center agent is a security plug-in running on your servers. It has been integrated into Alibaba Cloud public images. When you create an ECS instance, you can select a public image and enable **Security enhancement** to automatically install the Security Center agent on your instance. For more information about how to manually install the Security Center agent on an external server, see [Install the Security Center agent](../../../../reseller.en-US/Access Cloud Security Center/Install the Security Center agent.md#).

3.  After the Security Center agent has been installed, you can go to the Assets page in the Security Center console to view the security status of the servers under your Alibaba Cloud account. 

    **Note:** The Security Center agent detects and collects the security status of the servers that Security Center protects. You can determine the status of the installed Security Center agent by verifying the security status of your server. If the security status of your server is protected, the installed agent is online and working properly. If the security status is unprotected, the installed agent is offline. For more information, see [Troubleshoot the problem of Cloud Security Center agent going offline](../../../../reseller.en-US/Access Cloud Security Center/Troubleshoot the problem of Security Center agent going offline.md#).

4.  In the Security Center console, you can view and manage flaws and security events on your server and perform the following operations to enhance the security of your server: 
    -   Go to the Assets page to view detailed information about the security status of the servers under your Alibaba Cloud account. This page also allows you to add tags to assets and create asset groups. For more information about this page, see [Assets](../../../../reseller.en-US/User Guide/Assets.md#).
    -   Go to the Events page to view unusual activities and attacks that have been detected on your servers, such as unusual logon activities, brute force cracking, webshells, suspicious processes, suspicious network connections, sensitive file tampering, and malicious processes. For more information, see [Security events](../../../../reseller.en-US/User Guide/Events/Security events.md#).
    -   Go to the **Vulnerabilities** \> **Server Vulnerabilities** page to view system software vulnerabilities and web content management system \(WCMS\) vulnerabilities. For more information, see [Server vulnerability management](../../../../reseller.en-US/User Guide/Server vulnerability management.md#).
    -   Go to the **Baseline Check** \> **Servers** page to view and manage vulnerable configurations that have been detected on your servers. For more information, see [Server baseline check](../../../../reseller.en-US/User Guide/Baseline check/Baseline Check overview.md#).
    -   Go to the **More** \> **Asset Fingerprints** page to view asset summary, including processes running on your servers, enabled system accounts, open ports, software version, and logons to the back end of your website. For more information, see [Asset fingerprints](../../../../reseller.en-US/User Guide/Asset fingerprints.md#).
    -   The Security Center console also provides additional settings for you to use the Security Center features more efficiently. You can go to the Settings page to perform the following tasks:

        -   Install or uninstall the Security Center agent.
        -   Configure alert policies.
        For more information about this page, see [Security Center settings](../../../../reseller.en-US/User Guide/Settings.md#).


