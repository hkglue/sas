# Application whitelist {#concept_187376 .concept}

Security Center provides an application whitelist feature to prevent unauthorized programs from running on your servers and maintain a trusted running environment for your assets.

The application whitelist feature allows you to add the servers that require protection and programs that are allowed to run on them to a whitelist. Security Center then identifies programs on the servers as trusted, suspicious, or malicious based on the whitelist and generates alerts when non-whitelisted programs start. This prevents your servers from being compromised by untrusted or malicious programs, which consume server resources.

You can create a whitelist policy and apply it to a server to detect suspicious or malicious programs, and get alerted about non-whitelisted programs.

**Note:** When a non-whitelisted program starts, an alert is generated. A non-whitelisted program may be a newly started normal program, or a malicious program placed by an intruder. We recommend that you add normal programs, commonly used programs, and third-party programs that you installed to the whitelist to avoid false alerts. If the alert identifies a malicious program, we recommend that you remove the program as soon as possible, and check whether it has tampered any configuration files.

## Instructions {#section_bar_jif_sdc .section}

The application whitelist feature is in the trial phase. You can log on to Security Center console and navigate to the Application Market page to apply for a trial.

## Step 1: Configure an application whitelist policy {#section_9hx_vmf_gz1 .section}

1.  Log on to the [Cloud Security Center console](http://partners-intl.console.aliyun.com/#/sas).
2.  In the left-side navigation pane, click **Application whitelist** \> ****. On the Application whitelist page, click Policies.
3.  On the Policies tab, click **Create Policy**.
4.  In the Create Whitelist Policy pane, set the following parameters:
    -   **Policy Name**: Enter a whitelist policy name.
    -   **Intelligent Learning Duration**: Select a duration for Cloud Security Center to perform intelligent learning of the policy. You can select 1, 3, 7, or 15 days. The intelligent learning function uses machine learning to automatically collect and categorize large amounts of alert data. Cloud Security Center can learn to identify suspicious or malicious programs based on the collected data.
    -   **Servers for Intelligent Learning**: Select servers to add to the whitelist.
5.  Click **Next** to create the whitelist policy.

After the whitelist policy is created, its details are automatically displayed in the policy list on the **Policies** tab.

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/161240/155807307545356_en-US.png)

The policy list contains the following information about the policy:

-   **Policy Name**: the whitelist policy name.
-   **Servers**: the number of servers to which the whitelist policy is applied.

    Click the number in the **Servers** column corresponding to the policy. In the pane that appears on the right, you can select servers from the server list and click **Add Server** to add the selected servers to the policy.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/161240/155807307545363_en-US.png)

-   **Status**: the policy status. Valid values:
    -   **Applied**: Intelligent learning is complete. The policy has been applied to the servers.
    -   **Pending Confirmation**: Intelligent learning is complete. The policy needs to be confirmed and enabled.

        After intelligent learning is complete, Security Center automatically identifies the programs on the corresponding servers as trusted, suspicious, or malicious. To enable the policy, click **Apply**. The policy takes effect only after it is enabled.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/161240/155807307545364_en-US.png)

    -   **Paused**: Intelligent learning has been manually paused. You can click **Continue** to resume intelligent learning.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/161240/155807307547357_en-US.png)

    -   **Learning**: Intelligent learning is in progress.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/161240/155807307545365_en-US.png)

        After a whitelist policy is created, Cloud Security Center performs intelligent learning to learn the policy. The status of each newly created policy is **Learning**.

-   **Applications**: the numbers of programs, including **Trusted**, **Suspicious**, and **Malicious** programs, on all servers to which the policy is applied.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/161240/155807307547358_en-US.png)

-   **Actions**: the actions that can be taken on the policy.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/161240/155807307547359_en-US.png)

    -   **Apply**: Click **Apply** to add or remove servers to which the policy is applied in the **Apply Whitelist Policy** pane.
    -   **Confirm**: Click **Confirm** to view the program list of the policy. In the pane that appears on the right, confirm the identified programs and their risks and enable the policy. The policy takes effect on the servers only after it is enabled.
    -   **Modify**: Click **Modify** to modify the policy in the **Modify Whitelist Policy** pane. You can modify the **Intelligent Learning Duration** and Servers for Intelligent Learning parameters of the policy.
    -   **Pause Learning**: Click **Pause Learning** to pause intelligent learning.
    -   **Continue**: Click **Continue** to resume intelligent learning.

        After you click **Continue**, the status of the policy changes to **Learning**. You can view the learning progress of the policy in the **Status** column.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/161240/155807307545365_en-US.png)

    -   **Delete**: Click Delete to delete the policy.

        After the policy is deleted, the corresponding servers and programs are no longer protected by the policy.


## Step 2: Add servers to the application whitelist {#section_dej_7o8_26s .section}

Before applying the whitelist policy to servers, you must purchase a sufficient authorization quota for application whitelist.

1.  Log on to the [Security Center console](http://partners-intl.console.aliyun.com/#/sas).
2.  In the left-side navigation pane, click **Application whitelist** \> ****. On the Application whitelist page, click Servers.
3.  On the Servers tab, click **Add Server**.
4.  In the Add Server pane, set the following parameters:

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/161240/155807307545319_en-US.png)

    -   **Whitelist Policy**: Select the whitelist policy you created from the drop-down list.
    -   **Event Handling**: indicates how Security Center handles suspicious events. The default value is **Alert**, which indicates that Security Center generates an alert when detecting a suspicious program.

        When a non-whitelisted program starts on a server protected by the whitelist, an alert is automatically triggered. You can click the number of alerts in the **Suspicious Events** column corresponding to a server. On the **Assets** \> **Events** page that appears, you can view the alert details.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/161240/155807307647360_en-US.png)

    -   **Servers**: Select the servers to add to the whitelist. You can select multiple servers.

        To search for servers, enter the server name in the search box on the **Servers** tab. You can enter part of a server name to search for similar servers on the **Servers** tab.

5.  Click **OK** to create the application whitelist.

After the application whitelist is created, you can view the protected servers and the name of the whitelist policy applied to the servers in the server list on the Servers tab.

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/161240/155807307647361_en-US.png)

The following information about each protected server is available on the Servers tab:

-   **Server Name/IP**: the name and IP address of the server to which the whitelist policy is applied.
-   **Whitelist Policy**: the whitelist policy that is applied to the server.
-   **Suspicious Events**: the number of non-whitelisted programs that are running on the server. The Cloud Security Center generates an alert in real time when it detects the startup of a non-whitelisted program.
-   **Event Handling**: indicates how the Cloud Security Center handles suspicious events. The default value is **Alert**, which indicates that the Cloud Security Center generates an alert when detecting a suspicious program.

    When a non-whitelisted program starts on a server protected by the whitelist, an alert is automatically triggered. You can click the number of alerts in the **Suspicious Events** column corresponding to the server. On the **Assets** \> **Events** page that appears, view the alert details.

-   **Actions**: Click **Delete** in the **Actions** column corresponding to a server to delete the server from the application whitelist.

    After the server is deleted from the application whitelist, the application whitelist policy will no longer take effect on the server. The Cloud Security Center will no longer generate alerts when any programs start on that server.


## Add a program to or remove it from the application whitelist {#section_rie_e3k_sye .section}

After you create an application whitelist, you can view the protected servers and the name of the whitelist policy applied to the servers in the server list on the Servers tab. You can click the policy name in the **Whitelist Policy** column corresponding to a server. The list of programs running on the server is displayed. View the trusted, suspicious, and malicious programs that have been detected and their details.

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/161240/155807307647362_en-US.png)

The following information about each program on the server is available in the program list:

-   **Type**: the type of the program. Programs are classified into trusted, suspicious, and malicious programs.
-   **Process Name**: the name of the program.
-   **hash**: the hash function of the program. The hash function is used to ensure that the program has not been forged.
-   **Path**: the file path of the program on the server.
-   **Degree of Trustability**: the degree of trustability for the program determined by the Cloud Security Center. Valid values: 0%, 60%, and 100%. 0% indicates that the program is malicious. 60% indicates that the program is suspicious. 100% indicates that the program is trusted.

    We recommend that you focus on the programs whose degree of trustability is 0%.

-   **Actions**: the actions that can be taken on the program.

    -   **Add to Whitelist**: If a program is trusted, add it to the whitelist.
    -   **Remove from Whitelist**: After a program is removed from the whitelist, the Cloud Security Center will identify the program as untrusted and generate an alert when this program starts.
    You can determine whether to add the program to the whitelist based on the services deployed on your server.


