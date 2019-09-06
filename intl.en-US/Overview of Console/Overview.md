# Overview {#concept_jxf_z34_k2b .concept}

As the security operation center of Alibaba Cloud, the **Overview** page of the Security Center console displays the threats to, and the safety score of all your assets, and all the Alibaba Cloud Security services you have bought. You can upgrade Security Center, renew your Security Center service, scale up your assets, and modify the notification method.

On the **Overview** page, you can view important security information of your assets and execute related operations.

![Overview](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/15448/156775416749838_en-US.png)

The **Overview** page includes the following modules:

-   **Upgrade、Renew**: Click **Upgrade**/**Renew**on the top right of the Overview page, you can upgrade to your Security Center to the Enterprise Edition, scale up your assets, or renew your Security Center service.

    ![升级续费](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/15448/156775416748508_en-US.png)

-   **Secure score**: Safety score displays your assest's security score evaluated by Security Center, and the number of protected and unprotected assets. For specific score descriptions, see [Safety score table](#section_jxm_rrk_wfb).

    Click **Fix Now** to expand the **Security Risk** page. You can refer to the corresponding help documentation or directly address the risk immediately, based on the prompts on the page.

    Security Risk Handling contains all the security risks and threats that you need to address as quickly as possible, including the following categories:

    -   Unhandled alerts
    -   Unfixed vulnerability
    -   Baseline risks
    -   Cloud platform configuration risks
    -   Other risks or threats such as attack events
    ![安全评分](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/15448/156775416759402_en-US.png)

-   **Asset status**: View the number of assets for which you have installed and not installed the Agent plug-in, that is, assets that are already within the scope of Security Center and the number of assets that have not been protected by Security Center. And View the total number of risk assets present; view the number of servers, websites, and cloud products that are at risk.

    ![资产状态](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/15448/156775416848509_en-US.png)

    To add unprotected assets under the protection of Security Center, click the number under **Unprotected Assets** and on the displayed Install/Uninstall Security Center Agent page, install the Security Center agent. For more information, see [Install Security Center agent](reseller.en-US/Access Cloud Security Center/Install the Security Center agent.md#).

-   **Threat Statistics**: Threat statistics includes the number of unhandled alerts, unfixed vulnerabilities, baseline risks and attacks.
-   **Cloud Platform Configuration Risks**: This module displays the detected baseline risks of your cloud products.
-   **Issues Resolved**: This module displays the number of events, vulnerabilities, and vulnerable baseline configurations handled during the week in the form of column charts.

## Upgrade to the Enterprise Edition, scale up assets, and renew your Security Center service {#section_wqz_1zk_wfb .section}

Security Center provides a Basic Edition, Advanced and an Enterprise Edition. You can view information on your specific edition in the upper-right corner of the **Overview** page. For more information on the differences in features of the Basic Edition and the Enterprise Edition, see [Features](https://www.alibabacloud.com/help/doc-detail/42306.htm).

-   **Basic Edition**: The edition of Security Center is shown in the upper-right corner of the page. An **Upgrade** button is also displayed. If you upgrade your Security Center Basic Edition to the Advanced or Enterprise Edition, you are able to use such advanced functions as baseline checks, asset fingerprints, malicious processes \(malware checking\), and log analysis \(needs to be purchased additionally\).
-   **Advanced/Enterprise Edition**: The expiration date of your Security Center service, and the size of your assets \(the number of servers\) are displayed in the upper-right corner of the page. A **Renew** button is also displayed.

    **Note:** If your current number of servers exceeds the number that you specified when purchasing Security Center, an **Asset Scaling** button is displayed in the upper-right corner of the page. To guarantee the availability of all features, we recommend that you scale up your assets.


## Safety score table {#section_jxm_rrk_wfb .section}

|Safety score|Description|
|------------|-----------|
|95–100|Your assets are fully secured.|
|85–94|There are some security risks to your assets. We recommend that you strengthen the security of your servers and your system as soon as possible.|
|70–84|There are many security risks in your assets detected by Security Center. We highly recommend that you strengthen the security and protection of your system as soon as possible.|
|69 and lower|Your assets are exposed to security risks and may be easily compromised. We recommend that you immediately strengthen the security and protection of your system.|

|Impact|Strengthening suggestion|
|------|------------------------|
|Lack of a security operation center|Establish an in-depth defense system. If you have any queries, submit a ticket for technical support.|
|Unfixed vulnerabilities|Fix the vulnerabilities. For more information, see [Linux software vulnerabilities](reseller.en-US/Precautions/Vulnerabilities/Linux software vulnerabilities.md#).|
|Unhandled security events|Handle the security events in a timely manner.|
|Lack of host protection|Enable the enterprise edition of Server Guard.|
|The protection status is offline \(the Security Center agent is not installed or offline\).|Install the Security Center agent.|
|Web-CMS vulnerabilities|Fix the Web-CMS vulnerabilities.|
|System software vulnerabilities|Fix the software vulnerabilities.|
|Risks detected by baseline checks|Fix the vulnerabilities of baseline.|
|Unexpected logons|Check and handle the unexpected logons.|
|Webshell threats|Check and handle the webshell files.|
|Host exceptions|Handle the host exception events.|

## Threat statistics {#section_wt4_szk_wfb .section}

The **Overview** page displays the statistics of the threats that Security Center detects in all your assets, and the corresponding trend diagrams, including:

-   **Events**: Number of unhandled security events.
-   **Times of attacks**: Number of attacks today.
-   **Vulnerabilities**: Number of unhandled vulnerabilities.
-   **Baseline check**: Number of vulnerable baseline configurations.

