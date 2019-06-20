# Cloud Platform Configuration Assessment {#concept_kn2_wdm_3gb .concept}

The Cloud Platform Configuration Assessment feature of Security Center checks the security configuration of your cloud services. The checks are performed from five perspectives, including identity authentication, network access control, data security, log auditing, and basic security configuration. This feature helps you detect configuration risks in your cloud services and provides suggestions on risk handling.

This feature is available only in Security **Advanced** or **Enterprise** edition. If you are a **Basic Edition** user and want to use this feature, upgrade to Advanced or Enterprise Edition.

## Procedure {#section_w2z_q2m_3gb .section}

1.  Log on to the [Security Center console](https://yundun.console.aliyun.com/?spm=5176.2020520001.1011.3.796f4bd3iakMqe&p=sas#/sas/overviews).
2.  In the left pane, click **Config Assessment**.
3.  On the **Cloud Platform Configuration Assessment** page, click **Authorize Now**. The **Cloud Resource Access Authorization** page is displayed.
4.  Click **Confirm Authorization Policy** to allow Security Center to access your cloud resources.

    After the authorization, you can use the Cloud Platform Configuration Assessment feature to check for configuration risks on your cloud services and handle these risks.

    This feature supports the following operations:

    -   **Settings**: You can set **the days** and **time frame** for configuration checks.

        Select one or multiple days from Monday to Sunday.

        Each day is divided into four time frames. Select one time frame. During the selected time frame on the selected day, Security Center automatically checks all the check items. By default, TDS automatically checks your configurations **from 00:00 to 06:00** once every other day.

    -   **Check Now**: Check for risks on all configuration items of your cloud services and identify the number of affected assets. The check items are listed by risk severity, in the order from the highest severity to the lowest severity.

        Security Center can check the following types of items:

        -   Cloud platform - primary account two-factor authentication configuration
        -   Cloud platform - ActionTrail configuration
        -   Alibaba Cloud Security - Anti-DDoS Pro back-to-origin configuration
        -   Security group - RDS whitelist configuration
        -   SLB - open vulnerable ports
        -   Alibaba Cloud Security - WAF back-to-origin configuration
        -   OSS sensitive file leaks
        -   RDS - database security policies
        **Note:** Wait until the check is complete to perform other operations.

    -   **Verify**: Verify whether risks exist on a specific item. If you have modified the configuration of a check item, you can click **Verify** to check for risks on this item.
    -   Click the name of a check item to view the details, including the description, risks, and solutions.
    -   **Ignore**: If you confirm that an at-risk item is secure, you can click **Ignore**. This changes the item status to **Ignored**. An **ignored** item is not included in **at-risk items**.

        You can also **Unignore** an **ignored** item.

        **Note:** **Ignored** items are not included in the at-risk items in later checks.

    -   **Label as False Positive**: If you confirm that the alert on a check item is a false positive, click **Label as False Positive**. This changes the item status to **Labelled as False Positive**.

        **Note:** An item that has been **labelled as a false positive** is not included in the at-risk items in later checks.


