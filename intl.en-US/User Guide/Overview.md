# Overview {#concept_jxf_z34_k2b .concept}

As the security operation center of Alibaba Cloud, the **Overview** page of the Threat Detection Service \(TDS\) console displays the threats to, and the safety score of all your assets, and all the Alibaba Cloud Security services you have bought. You can upgrade TDS, renew your TDS service, scale up your assets, and modify the notification method.

On the **Overview** page, you can view important security information of your assets and execute related operations.

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/15448/155229653137206_en-US.png)

The **Overview** page includes the following modules:

-   TDS edition: Click **Upgrade to Enterprise Edition**/**Renew**on the top right of the Overview page, you can upgrade to your TDS to the Enterprise Edition, scale up your assets, or renew your TDS service.

    **Basic Edition**：

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/15448/155229653137208_en-US.png)

    **Enterprise Edition**：

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/15448/155229653137207_en-US.png)

-   **Safety score**: Safety score displays your assest's security score evaluated by TDS, and the number of protected and unprotected assets. For specific score descriptions, see the Safety score table below.

    To add unprotected assets under the protection of TDS, click the number under **Unprotected Assets** and on the displayed Install/Uninstall TDS Agent page, install the TDS agent. For more information, see [Install the TDS agent](reseller.en-US/User Guide/Access Threat Detection Service/Install the TDS agent.md#).

-   **Urgent Vulnerabilities**: Urgent Vulnerabilities displays the latest discovered urgent vulnerabilities of your assets.
-   **Threat statistics**: Threat statistics includes the number of security events, attacks, vulnerabilities, and vulnerable baseline configurations.
-   **Cloud platform best security practices**: This module displays the detected baseline risks of your cloud products.
-   **Safe operation**: This module displays the number of events, vulnerabilities, and vulnerable baseline configurations handled during the week in the form of column charts.
-   Information on the Alibaba Cloud Security products you have bought.

## Upgrade to the Enterprise Edition, scale up assets, and renew your TDS service {#section_wqz_1zk_wfb .section}

TDS provides a Basic Edition and an Enterprise Edition. You can view information on your specific edition in the upper-right corner of the **Overview** page. For more information on the differences in features of the Basic Edition and the Enterprise Edition, see [Features](https://www.alibabacloud.com/help/doc-detail/42306.htm).

-   **Basic Edition**: The edition of TDS is shown in the upper-right corner of the page. An **Upgrade to Enterprise Edition** button is also displayed. If you upgrade your TDS Basic Edition to the Enterprise Edition, you are able to use such advanced functions as baseline checks, asset fingerprints, malicious processes \(malware checking\), and log analysis.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/15448/15522965316876_en-US.png)

-   **Enterprise Edition**: The expiration date of your TDS service, and the size of your assets \(the number of servers\) are displayed in the upper-right corner of the page. A **Renew** button is also displayed.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/15448/155229653137207_en-US.png)

    **Note:** If your current number of servers exceeds the number that you specified when purchasing TDS, an **Asset Scaling** button is displayed in the upper-right corner of the page. To guarantee the availability of all features, we recommend that you scale up your assets.


## Security score table {#section_jxm_rrk_wfb .section}

|Security score|Description|
|--------------|-----------|
|95–100|Your assets are fully secured.|
|85–94|There are some security risks to your assets. We recommend that you strengthen the security of your servers and your system as soon as possible.|
|70–84|There are many security risks in your assets detected by TDS. We highly recommend that you strengthen the security and protection of your system as soon as possible.|
|69 and lower|Your assets are exposed to security risks and may be easily compromised. We recommend that you immediately strengthen the security and protection of your system.|

|Impact|Strengthening suggestion|
|------|------------------------|
|Lack of a security operation center|Establish an in-depth defense system. If you have any queries, submit a ticket for technical support.|
|Unfixed vulnerabilities|Fix the vulnerabilities. For more information, see Vulnerabilities.|
|Unhandled security events|Handle the security events in a timely manner.|
|Lack of host protection|Enable the enterprise edition of Server Guard.|
|The protection status is offline \(the TDS agent is not installed or offline\).|Install the TDS agent. For more information.|
|Web-CMS vulnerabilities|Fix the Web-CMS vulnerabilities.|
|System software vulnerabilities|Fix the software vulnerabilities.|
|Risks detected by baseline checks|Fix the vulnerabilities of baseline.|
|Unexpected logons|Check and handle the unexpected logons.|
|Webshell threats|Check and handle the webshell files.|
|Host exceptions|Handle the host exception events.|

## Threat statistics {#section_wt4_szk_wfb .section}

The **Overview** page displays the statistics of the threats that TDS detects in all your assets, and the corresponding trend diagrams, including:

-   **Events**: Number of unhandled security events.
-   **Times of attacks**: Number of attacks today.
-   **Vulnerabilities**: Number of unhandled vulnerabilities.
-   **Baseline check**: Number of vulnerable baseline configurations.

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/15448/155229653137209_en-US.png)

