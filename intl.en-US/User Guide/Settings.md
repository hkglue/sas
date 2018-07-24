# Settings {#concept_cxc_qzc_zdb .concept}

On the Threat Detection Service \(TDS\) settings page, you can perform the following tasks: Install/Uninstall TDS agent, and Configure alert policies. This document introduces how to configure TDS settings.

## Install/Uninstall TDS agent {#section_r1f_45k_zdb .section}

**Note:** The TDS agent is a security plug-in that runs on servers. To use TDS to protect your servers, you must first install the TDS agent to the operation system of your servers.

1.  Log on to the [Threat Detection Service console](https://yundun.console.aliyun.com/?p=sas).
2.  In the left-side navigation pane, click **Settings**.
3.  Go to the **Install/Uninstall TDS Agent** page.
4.  If the server is in the Unprotected status, follow the instructions on the page to download and install the latest version of the TDS agent. For more information, see [Install the Threat Detection Service agent](intl.en-US/User Guide/SAS agent/Install the TDS agent.md#).
5.  To disable TDS protection, click **Uninstall** in the upper-right corner to uninstall the agent. For more information about uninstalling the TDS agent, see [Uninstall the Threat Detection Service agent](intl.en-US/User Guide/SAS agent/Uninstall the TDS agent.md#).

## Configure alert settings {#section_w1f_45k_zdb .section}

Alert settings allow you to modify the alert policies for TDS. The operation is as follows:

**Note:** By default, the alarm message recipient is your account contact, you can also go to the [Message Center](https://notifications.console.aliyun.com/#/subscribeMsg), and add more message recipients in **Basic Receive Management** \> **Security Message** \> **Cloud Shield Security Information notification**.

1.  Log on to the [Threat Detection Service console](https://yundun.console.aliyun.com/?p=sas).
2.  In the left-side navigation pane, click **Settings**.
3.  Go to the **Alert Settings** page.
4.  Specify the alert **Severity** level and **Notification Method** for **Events**, **Vulnerabilities**, and **Baseline Check**.

    **Note:** Changes made on this page are applied immediately.


You can also modify the alert policy on the Overview page. The operation is as follows:

1.  Log on to the [Threat Detection Service console](https://yundun.console.aliyun.com/?p=sas).
2.  In the left-side navigation pane, click **Overview**.
3.  Click the **Alert Settings** button at the top of the page.
4.  In the Alert Settings dialog box, select a alert policy: **Critical**, **Not Critical**, **All**, or **Customize**. We recommend that you use the first three policies.

    **Note:** Click **Save** for the changes to take effect.


