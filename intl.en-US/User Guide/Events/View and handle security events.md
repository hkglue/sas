# View and handle security events {#concept_rlc_rts_sfb .concept}

You can view and handle security events in TDS console. TDS allows you to handle multiple events at a time.

## Procedure {#section_wxs_bsj_zdb .section}

1.  Log on to [Threat Detection Service console](partners-intl.console.aliyun.com/#/sas).
2.  In the left-side navigation pane, click **Events** to go to the **Events** page.
3.  On the **Events** page, view or search for the detected intrusion or threat events, and check their details.

    You can find a certain event based on specified search conditions. For example, you can search for events by event or asset name, severity level, event status, or event type.

4.  You can handle different events with the following operations.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/61174/155367182933907_en-US.png)

    -   **Quarantine**: Quarantine only the **Webshell** and **Malicious Process** events. You can click Quarantine in the **Actions** column corresponding to a Webshell event to quarantine the relevant webshell file. Quarantined files no longer pose threats to the host.

        **Note:** The system keeps a quarantined file for only 30 days. You can restore any quarantined file before the system deletes the file.

    -   **Handle Offline**: After handling an event offline, you can click **Handle Offline** in the **Actions** column. The event status then changes to **Handled**.
    -   **Ignore Once**: You can click **More** in the **Actions** column corresponding to an event and choose **Ignore Once** from the shortcut menu to ignore the event. The event status then changes to **Handled**. The event will no longer be reported in TDS console.
    -   **Label as False Positive**: You can click **More** in the **Actions** column corresponding to an event and choose **Label as False Positive** from the shortcut menu to label the event as a false positive. The event status then changes to **Handled**. The event will no longer be reported in TDS console. You can find the event that you labeled as a false positive in the **Handled** event list, and click **Cancel Labeling as False Positive** in the **Actions** column to unlabel the event.

        **Note:** False positives are alerts generated for normal processes. The Unusual TCP Packets event is a common false positive. It is reported when a process on your server initiated a suspected scan on other devices.


## Handle security events in batches {#section_tdf_q2n_bgb .section}

You can use the batch-handling toolbar in the lower-left corner of the **Events** page to handle security events in batches.

**Note:** Check the details of each event before you handle the events in batches.

