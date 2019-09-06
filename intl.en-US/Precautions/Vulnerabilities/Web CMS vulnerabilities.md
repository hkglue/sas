# Web CMS vulnerabilities {#concept_y4c_nzc_zdb .concept}

Security Center can detect and fix CMS vulnerabilities. The service can monitor your Web directory, identify common website builders, and detect the vulnerabilities in your system by comparing vulnerable files.

Security Center montiors the latest security vulnerabilities and provides patches and updates in a timely manner. You can download the updates in the console and fix vulnerabilities. The service can help you discover vulnerabilities and provides updates to fix vulnerabilities in batches.

**Note:** Security Center **Basic** only supports vulnerability detection. To fix vulnerabilities, you need to activate **Security Center Enterprise**. For more information about the features provided by Security Center Basic and Enterprise, see [Features](../../../../reseller.en-US/Product Introduction/Features.md#).

**Note:** Once fixed, CMS vulnerabilities are removed from the console and cannot be detected.

## Procedure {#section_lst_wsc_ygb .section}

1.  Choose **Vulnerabilities** \> **Web CMS Vulnerabilities**.

    ![](images/39865_en-US.png)

2.  On the Web CMS Vulnerabilities page, you can perform the following operations: view all CMS vulnerabilities detected by Security Center, fix vulnerabilities, search vulnerabilities by severity level and status, add vulnerabilities to the whitelist, and ignore vulnerabilities.
    -   **View vulnerability details** 

        Click a vulnerability name to view details. On the vulnerability details page, you can view a description of this vulnerability, its severity level, assets affected by this vulnerability, and the status of this vulnerability. You can also choose to fix this vulnerability or ignore it.

        ![](images/39899_en-US.png)

        The vulnerability details page also displays information about **correlated vulnerabilities** and assets that are affected by these vulnerabilities. You can easily analyze and handle these vulnerabilities on this page.

        ![](images/39900_en-US.png)

        On the vulnerability details page, click an **affected asset** to view all the vulnerabilities that are correlated with the asset. You can also choose **Assets** \> **Vulnerabilities** to open this page.![](images/39908_en-US.png)

    -   **Vulnerability priorities \(urgency levels\)** 

        CMS vulnerabilities can cause serious damage. Therefore, CMS vulnerabilities have **high** priority and are marked in red.

        ![](images/39911_en-US.png)

        **Note:** We recommend that you fix CMS vulnerabilities as soon as possible.

    -   **Search vulnerabilities** 

        On the Web CMS Vulnerabilities page, you can search vulnerabilities by vulnerability name, severity level \(high, medium, and low\), or vulnerability status \(handled, unhandled\).

        ![](images/39904_en-US.png)

        **Note:** You can also fuzzy search vulnerabilities by name.

    -   **View vulnerability status**

        -   **Handled** 

            -   Fixed: The vulnerability is already fixed.
            -   Fix Failed: An error occurred while fixing the vulnerability. The vulnerable file is already modified or does not exist.
            -   Ignored: The vulnerability is **ignored**. Security Center no longer sends alarms when this vulnerability is detected.
            -   Invalid Vulnerability: The vulnerability has not been detected in the last seven days.
            -   Fix Undoing Failed: An error occurred while undoing the fix. The vulnerable file may not exist.
            **Note:** For **handled** vulnerabilities, you can choose to **undo** fixes. When a fix is undone, the vulnerability status is changed to **Unhandled**.

        -   **Unhandled** 
            -   Unfixed: The vulnerability is yet to be fixed.
    -   **Fix vulnerabilities** 

        On the vulnerability details page, you can select one or multiple vulnerabilities and click **Fix** to fix the selected vulnerabilities.

    -   **Ignore vulnerabilities** 

        On the Web CMS Vulnerabilities page, you can select one or more vulnerabilities and click **Ignore** to ignore the selected vulnerabilities.

        **Note:** After you **ignore** a vulnerability, the vulnerability status is changed to **Handled**. If you want Security Center to notify you of this vulnerability again, select this vulnerability in the **Handled** vulnerability list and click **Unignore**.

    -   **Undo fixes** 

        For **handled** vulnerabilities, you can choose to undo fixes. When a fix is undone, the vulnerability status is changed to **Unhandled**.

    -   **Add vulnerabilities to the whitelist** 

        On the Web CMS Vulnerabilities page, you can select one or multiple vulnerabilities and click **Add to Whitelist** to add the selected vulnerabilities to the whitelist. After a vulnerability is added to the whitelist, Security Center does not send alarms when this vulnerability is detected.

        ![](images/39905_en-US.png)

        Whitelisted vulnerabilities are removed from the vulnerability list. You can click [Settings](reseller.en-US/Precautions/Vulnerabilities/Vulnerability management settings and whitelist configuration.md#) in the upper-right corner and view these vulnerabilities in the **Whitelisted Vulnerabilities** table.

        If you want Security Center to detect and send alarms on whitelisted vulnerabilities again, select the vulnerability and click **Remove** to remove this vulnerability from the whitelist on the Settings page.

        ![](images/39906_en-US.png)

    -   **Export vulnerabilities** 

        On the Web CMS Vulnerabilities page, you can click the **Export** icon to export records of all vulnerabilities to your local computer. The exported file is in Excel format.

        **Note:** It may take a few minutes to export vulnerability records depending on the data size.

    -   On the vulnerability details page, you can click ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/118684/156774776139821_en-US.png) to save multiple vulnerabilities to a group. This allows you to track vulnerabilities by group.

        ![](images/39907_en-US.png)


