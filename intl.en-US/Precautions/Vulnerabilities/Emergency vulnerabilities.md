# Emergency vulnerabilities {#concept_kw1_y11_4gb .concept}

Security Center can detect and fix emergency vulnerabilities.

The Emergency Vulnerabilities page displays the latest critical vulnerabilities and allows you to check if your assets are affected by these vulnerabilities.

## Procedure {#section_l5r_ynl_zgb .section}

1.  Choose **Vulnerabilities** \> **Emergency**.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/118680/156775977539938_en-US.png)

2.  On the **Emergency** page, you can view a list of the latest security vulnerabilities and their detailed records.
    -   You can click **Check Now**/**Inspect Again** on the right side of the **Emergency**Vulnerabilities page to see if your assets are affected by the selected vulnerability.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/118680/156775977639960_en-US.png)

        **Note:** 

        -   Currently, Security Center does not show the **progress of the check**. If threats are detected, you will be notified of the **assets with urgent vulnerabilities**. You can click an asset name to go to the vulnerability details page and take action.
        -   If you have a large number of assets, it may take up to 20 minutes to complete the checkup, during which the following message is displayed: **No Risk**.
    -   Click a vulnerability name to go to the vulnerability details page. You can find details of this vulnerability, its priority \(urgency level\), assets affected by this vulnerability, and recommended fixes on this page.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/118680/156775977649823_en-US.png)

        -   You can view information about the assets that are affected by this vulnerability.
        -   You can view the vulnerability status, which can be one of the following:
            -   **Handled** 

                -   Fixed: The vulnerability is already fixed.
                -   Fix Failed: An error occurred while fixing the vulnerability. The vulnerable file is already modified or does not exist.
                -   Ignored: The vulnerability is **ignored**. Security Center no longer sends alarms when this vulnerability is detected.
                -   Invalid Vulnerability: The vulnerability has not been detected in the last seven days.
                -   Fix Undoing Failed: An error occurred while undoing the fix. The vulnerable file may not exist.
                **Note:** For **handled** vulnerabilities, you can choose to **undo** fixes. When a fix is undone, the vulnerability status is changed to **Unhandled**.

            -   **Unhandled**: Unfixed, the vulnerability is yet to be fixed.
        -   View vulnerability **priorities \(urgency levels\)**.

            The priority \(urgency level\) of a vulnerability is determined based on multiple factors, such as the severity of the vulnerability, the time of discovery, and the server's environment.

            Vulnerability priorities \(urgency levels\) are divided into three types: high, medium, and low.

            **Note:** We recommend that you immediately fix **high** priority vulnerabilities.

        -   Handle emergency vulnerabilities.
            -   **Verify**: You can verify if a vulnerability is already fixed.
            -   **Ignore**: You can ignore a vulnerability so that Security Center does not send alarms when this vulnerability is detected.

                **Note:** After you **ignore** a vulnerability, the vulnerability status is changed to **Handled**. If you want Security Center to notify you of this vulnerability again, select this vulnerability in the **Handled** vulnerability list and click **Unignore**.


