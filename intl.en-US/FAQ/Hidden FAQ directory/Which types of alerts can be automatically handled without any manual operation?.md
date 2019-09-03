# Which types of alerts can be automatically handled without any manual operation? {#concept_525289 .concept}

After exceptions and threats are detected, Security Center sends you alerts and provides solutions.

On the Alerts page in the Security Center console, you can view the 15 types of alert events that can be detected, as shown in the following figure.

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/422588/156750331348802_en-US.png)

## Three ways of handling alert events {#section_2yq_vup_udd .section}

The 15 types of alert events detected by Security Center can be handled in the following three ways:

-   Security Center automatically handles certain types of events. The **Precise Defense** events are automatically detected and quarantined by the virus detection and removal feature. This feature automatically detects and quarantines mainstream virus files. No manual operations are required in this process. On the Alerts page, you can select **Precision Defense** in the event type filter box to show this type of events only. All of these events are **handled**. This indicates that the viruses have been automatically quarantined by Security Center.

    For more information about virus detection and removal, see [Cloud Threat Detection](../../../../intl.en-US/Threat Detection/Events/Cloud Threat Detection.md#).

-   Manual operations are required to handle all exceptions except for the **Precise Defense** type. The manual operations include the online quarantining of files and the offline handling of exceptions. For example, you can click **Quarantine** in the Security Center console to handle the following events: malicious process-DDoS trojans and webshells.

    For more information about how to quarantine a file, see [Which types of alerts can be handled by the quarantine operation?](intl.en-US/.md#)

-   All the alert events that cannot be handled in the console must be handled on the affected servers. For example, unusual logon activities and suspicious network connections must be handled offline.

    ![告警详情](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/422588/156750331448803_en-US.png)


