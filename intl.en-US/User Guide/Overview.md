# Overview {#concept_jxf_z34_k2b .concept}

The Threat Detection Service \(TDS\) overview page allows you to view brief information about threats that have been detected on all assets. You can upgrade and renew services, scale up the number of assets, and modify notification reception rules.

To view security issues and perform operations, follow these steps:

1.  Log on to the [TDS console](https://yundun.console.aliyun.com/?p=sas).
2.  Go to the Overview page. You can view asset security information and perform the following tasks on this page:
    -   **Upgrade TDS, scale up assets, and renew services**
        -   To upgrade TDS from Basic Edition to Enterprise Edition, click **Upgrade** in the upper-right corner. If you want to use baseline check, asset fingerprint, and more functions, you can click **Upgrade** and purchase the enterprise service. For more information, see [Purchasing Threat Detection Service](../../../../intl.en-US/Pricing/Purchase Threat Detection Service.md#).
        -   The Enterprise Edition shows the service expiration date and total number of assets in the upper-right corner of the overview page. You can click **Renew** to renew your TDS service.

            **Note:** The **Asset Scaling** button is available only if the current number of assets has reached 120% of the asset count that you have specified when purchasing TDS. To guarantee the availability of all features, we recommend that you scale up the number of assets.

    -   **View threat statistics**

        Statistics about events, vulnerabilities, and baseline risks are displayed in the upper area of the overview page. You can click the corresponding number to view related details. On the right side, you can view statistics about the security status of all assets, that is, how many assets are protected and how many are not protected. Click the number under **Uninspected Assets**, and you can go directly to the Install/Uninstall TDS Agent page where you can install the TDS agent to your server. For more information, see [Install the TDS agent](intl.en-US/User Guide/Access Threat Detection Service/Install the TDS agent.md#).

        You can click the **Alert Settings** button to select the alerts that you want to receive based on the severity levels of events, vulnerabilities, and baseline risks.

    -   **View recently unhandled alerts and top 5 vulnerable assets**

        The middle-left area of the overview page displays the recently unhandled alerts. The middle-right area of the overview page displays the top 5 vulnerable assets. You can click a record to go to the corresponding detail page.

    -   **View security events**

        The bottom area of the overview page displays the Security Issues chart. This chart shows the changes of the number of events, vulnerabilities, and baseline risks in the last 7 or 30 days.


