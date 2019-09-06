# Windows software vulnerabilities {#concept_qbb_xb1_4gb .concept}

Security Center can detect and fix Windows software vulnerabilities.

Synchronized with the security updates released on Microsoft's official website, Security Center can effectively detect important vulnerabilities and notify you of potential threats. This prevents attackers from exploiting Windows software vulnerabilities to compromise the security of your server.

**Note:** Security Center **Basic** only supports vulnerability detection. To fix vulnerabilities, you need to activate **Security Center Enterprise**. For more information about the features provided by Security Center Basic and Enterprise, see [Features](../../../../reseller.en-US/Product Introduction/Features.md#).

## Procedure {#section_lst_wsc_ygb .section}

1.  Choose **Vulnerabilities** \> **Windows Software Vulnerabilities**.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/118684/156775863139812_en-US.png)

2.  On the Windows Software Vulnerabilities page, view security bulletins about the vulnerabilities detected by Security Center, view vulnerability details, fix vulnerabilities, verify whether a vulnerability is fixed, search vulnerabilities by severity level and status, add vulnerabilities to the whitelist, and ignore vulnerabilities.
    -   **View vulnerability details** 

        Click a vulnerability name to view details. On the vulnerability details page, you can view a description of the vulnerability, its severity level, assets affected by this vulnerability, and the vulnerability status. You can also choose to fix the vulnerability, verify whether it is fixed, or ignore it.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/118684/156775863139813_en-US.png)

        The vulnerability details page also displays information about **Pending vulnerability** and assets that are affected by these vulnerabilities. You can easily analyze and handle these vulnerabilities.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/118684/156775863139815_en-US.png)

        Vulnerability priorities \(urgency levels\) are color coded for easy identification. Red indicates **high** priority. Orange indicates **medium** priority. Gray indicates **low** priority.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/118684/156775863139814_en-US.png)

        **Note:** We recommend that you immediately fix high priority vulnerabilities.

    -   **Verify vulnerabilities** 

        On the vulnerability details page, you can select one or multiple vulnerabilities and click **Verify** to verify whether the selected vulnerabilities are fixed.

        After you click **Verify**, the vulnerability **status** is changed to **Verifying**. It takes several seconds to verify vulnerabilities.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/118684/156775863139816_en-US.png)

    -   **Fix vulnerabilities** 

        On the vulnerability details page, you can select one or multiple vulnerabilities and click **Fix** to fix the selected vulnerabilities.

    -   **Search vulnerabilities** 

        On the Windows Software Vulnerabilities page, you can search vulnerabilities by vulnerability name, severity level \(high, medium, and low\), or vulnerability status \(handled, unhandled\).

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/118684/156775863139817_en-US.png)

        **Note:** You can also fuzzy search vulnerabilities by name.

    -   **Add vulnerabilities to the whitelist** 

        On the Windows Software Vulnerabilities page, you can select one or multiple vulnerabilities and click **Add to Whitelist** to add the selected vulnerabilities to the whitelist. After a vulnerability is added to the whitelist, Security Center does not send alarms when this vulnerability is detected.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/118684/156775863239818_en-US.png)

        Whitelisted vulnerabilities are removed from the vulnerability list on the Windows Software Vulnerabilities page. You can click [Settings](reseller.en-US/Precautions/Vulnerabilities/Vulnerability management settings and whitelist configuration.md#) in the upper-right corner and view these vulnerabilities in the **Whitelisted Vulnerabilities** table.

        If you want Security Center to detect and send alarms on whitelisted vulnerabilities again, select a vulnerability and click **Remove** to remove this vulnerability from the whitelist on the Settings page.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/118684/156775863239827_en-US.png)

    -   **Ignore vulnerabilities** 

        On the Windows Software Vulnerabilities page, you can select one or more vulnerabilities and click **Ignore** to ignore the selected vulnerabilities.

        **Note:** After you **ignore** a vulnerability, the vulnerability status is changed to **Handled**. If you want Security Center to notify you of this vulnerability again, select this vulnerability in the **Handled** vulnerability list and click **Unignore**.

    -   **Export vulnerabilities** 

        On the Windows Software Vulnerabilities page, you can click the **Export** icon to export records of all vulnerabilities to your local computer. The exported file is in Excel format.

        **Note:** It may take a few minutes to export vulnerability records depending on the data size.

    -   On the vulnerability details page, you can click ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/118684/156775863239821_en-US.png) to save multiple vulnerabilities to a group. This allows you to track vulnerabilities by group.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/118684/156775863239820_en-US.png)


