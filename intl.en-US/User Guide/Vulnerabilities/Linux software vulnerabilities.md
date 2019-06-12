# Linux software vulnerabilities {#concept_akr_grq_32b .concept}

This topic describes how to view and manage Linux software vulnerabilities in Security Center.

**Note:** Security Center **Basic** only supports vulnerability detection. To fix vulnerabilities, you need to activate **Security Center Enterprise**. For more information about the features provided by Security Center Basic and Enterprise, see [Features](../../../../reseller.en-US/Product Introduction/Features.md#).

## Procedure {#section_lst_wsc_ygb .section}

1.  Choose **Vulnerabilities** \> **Linux Software Vulnerabilities**.

    On the **Linux Software Vulnerabilities** page, you can view security bulletins about the Linux vulnerabilities detected by Security Center. Each security bulletin has a title that starts with USN, RHSA, or CVE.

    You can click a security bulletin to view details of the corresponding vulnerabilities.

    ![](images/39856_en-US.png)

2.  On the Linux Software Vulnerabilities page, you can perform the following operations: view security bulletins about the vulnerabilities detected by Security Center, view vulnerability details, fix vulnerabilities, verify whether a vulnerability has been fixed, search vulnerabilities by severity level and status, add vulnerabilities to the whitelist, and ignore vulnerabilities.
    -   **View vulnerability details** 

        Click a vulnerability name to view details. On the vulnerability details page, you can view a description of this vulnerability, its severity level, assets affected by this vulnerability, and the vulnerability status. You can also choose to fix this vulnerability, verify whether it has been fixed, or ignore it.

        ![](images/39857_en-US.png)

        The vulnerability details page also displays information about **correlated vulnerabilities** and assets that are affected by these vulnerabilities. You can easily analyze and handle these vulnerabilities on this page.

        ![](images/39858_en-US.png)

        On the vulnerability details page, click an **affected asset** to view all vulnerabilities that are correlated with the asset. You can also choose **Assets** \> **Vulnerabilities** to open this page. ![](images/39876_en-US.png)

    -   **Vulnerability priorities \(urgency levels\)** 

        Vulnerability priorities are color coded for easy identification.

        -   Red indicates **high** priority.
        -   Orange indicates **medium** priority.
        -   Gray indicates **low** priority.
        ![](images/39814_en-US.png)

        **Note:** We recommend that you immediately fix high priority vulnerabilities.

    -   **Alibaba Cloud vulnerability library** 

        On the vulnerability details page, select a vulnerability and click its **Vulnerability Number** to go to the Alibaba Cloud vulnerability library.

        ![](images/39873_en-US.png)

        On the Alibaba Cloud vulnerability library page, you can view more details about this vulnerability, including the detailed description, severity level, time of discovery, and mitigations.

        ![](images/39874_en-US.png)

    -   **Vulnerability severity levels \(emergency degrees\)** 

        Severity levels are color coded for easy identification. Red indicates **important \(high severity\)**. Orange indicates **moderate \(medium severity\)**. Gray indicates **low \(low severity\)**.

    -   **Verify vulnerabilities** 

        On the vulnerability details page, you can select one or multiple vulnerabilities and click **Verify** to verify whether the selected vulnerabilities have been fixed.

        After you click **Verify**, the vulnerability **status** is changed to **Verifying**. It takes several seconds to verify vulnerabilities.

        ![](images/39859_en-US.png)

    -   **Fix vulnerabilities** 

        On the vulnerability details page, you can select one or multiple vulnerabilities and click **Fix** to fix the selected vulnerabilities.

    -   **Search vulnerabilities** 

        On the Linux Software Vulnerabilities page, you can search vulnerabilities by vulnerability name, severity level \(high, medium, and low\), or vulnerability status \(handled, unhandled\).

        ![](images/39860_en-US.png)

        **Note:** You can also fuzzy search vulnerabilities by name.

    -   **Add vulnerabilities to the whitelist** 

        On the Linux Software Vulnerabilities page, you can select one or multiple vulnerabilities and click **Add to Whitelist** to add the selected vulnerabilities to the whitelist. After a vulnerability is added to the whitelist, Security Center does not send alarms when this vulnerability is detected.

        ![](images/39861_en-US.png)

        Whitelisted vulnerabilities are removed from the vulnerability list on the Linux Software Vulnerabilities page. You can click [Settings](reseller.en-US/User Guide/Vulnerabilities/Vulnerability management settings and whitelist configuration.md#) in the upper-right corner and view these vulnerabilities in the **Whitelisted Vulnerabilities** table.

        If you want Security Center to detect and send alarms on whitelisted vulnerabilities again, select a vulnerability and click **Remove** to remove this vulnerability from the whitelist on the Settings page.

         ![](images/39827_en-US.png)

    -   **Ignore vulnerabilities** 

        On the Linux Software Vulnerabilities page, you can select one or more vulnerabilities and click **Ignore** to ignore the selected vulnerabilities.

        **Note:** After you **ignore** a vulnerability, the vulnerability status is changed to **Handled**. If you want Security Center to notify you of this vulnerability again, select this vulnerability in the **Handled** vulnerability list and click **Unignore**.

    -   **Export vulnerabilities** 

        On the Linux Software Vulnerabilities page, you can click the **Export** icon to export records of all vulnerabilities to your local computer. The exported file is in Excel format.

        **Note:** It may take a few minutes to export the records of vulnerabilities depending on the data size.

    -   On the vulnerability details page, you can click ![](images/39821_en-US.png) to save multiple vulnerabilities to a group. This allows you to track vulnerabilities by group.

        ![](images/39862_en-US.png)


## Vulnerability details {#section_dhc_1vq_32b .section}

|Item|Description|
|----|-----------|
|Vulnerability number|The Common Vulnerabilities and Exposures \(CVE\) ID of the vulnerability. The Common Vulnerabilities and Exposures \(CVE\) system provides a reference-method for publicly known information-security vulnerabilities and exposures. You can use CVE IDs, such as CVE-2018-1123, to quickly search for information about vulnerability fixes in any CVE-compatible databases to resolve security issues.|
|Severity score \(CVSS score\)|The CVSS score follows the widely accepted industry standard, Common Vulnerability Scoring System, and is calculated based on multiple attributes of the vulnerability. This score is used to quantify the severity of vulnerabilities. In the CVSS v3.0 rating system, the severity level indicated by each score is as follows:

-   0.0: None.
-   0.1-3.9: Low
    -   Vulnerabilities that can cause denial of service.
    -   Vulnerabilities that have minor impacts.
-   4.0-6.9: Medium
    -   Vulnerabilities that can impact users during system and user interactions.
    -   Vulnerabilities that can be exploited to perform unauthorized activities.
    -   Vulnerabilities that can be exploited after attackers change local configurations or obtain important information.
-   7.0-8.9: High
    -   Vulnerabilities that can be exploited to indirectly obtain user permissions to your server and application systems.
    -   Vulnerabilities that can be exploited to read, download, write, or delete arbitrary files.
    -   Vulnerabilities that can cause sensitive data leaks.
    -   Vulnerabilities that can cause business disruption or remote denial of service.
-   9.0-10.0: Critical
    -   Vulnerabilities that can be exploited to directly obtain permissions to the operating system of your server.
    -   Vulnerabilities that can be exploited to directly obtain sensitive data and cause data leaks.
    -   Vulnerabilities that can cause unauthorized access to sensitive information.
    -   Vulnerabilities that can cause large-scale impacts.

 |
|Vulnerability name|The name of the vulnerability, which typically starts with CVE. For example, CVE-2018-1123 on Ubuntu 14.04 LTS \(trustly\).|
|Affected assets|The server assets that are exposed to this vulnerability, including the servers' public and internal IP addresses.|
|Priority \(Urgency level\)|The priority of the vulnerability, including -   **High**:

We recommend that you fix high priority vulnerabilities as soon as possible.

-   **Medium**:

You can fix medium priority vulnerabilities based on your business needs.

-   **Low**:

You may fix low priority vulnerabilities based on your needs.


 For more information about fixing vulnerabilities, see [Prioritize vulnerabilities](../../../../reseller.en-US/FAQ/Frequently Asked Questions (Hidden directory)/Prioritize vulnerabilities to be fixed.md#).

 |
|Details|You can select a vulnerability and click **Details** under the Actions column to view details of this vulnerability. -   **Commands**: The commands you can use to fix this vulnerability.
-   **Impact description**:
    -   **Software**: Version information about the software in the current server.
    -   **Cause**: The reason why the software is exposed to this vulnerability. Typically, the reason is that the current version is outdated.
    -   **Path**: The path of the software on the server.
-   **Caution**: Important notes, prevention tips, and links to reference documents about this vulnerability.

 |

