# Automatic alert correlation analysis {#concept_slf_kbx_bgb .concept}

Security Center **Advanced Edition** and **Enterprise Edition** provides automatic alert correlation analysis. On the Events page, you can click an event name to enter the automatic correlation analysis page. On this page, you can view and handle all related exceptions and view the diagnosis results of the attacks.

## Benefits {#section_ash_2fn_bgb .section}

-   This feature automatically correlates exceptions with this event in real time to find out potential threats.
-   This feature lists the related exceptions by time. This allows you to easily analyze and handle the exceptions to improve the emergency response mechanism.

## Procedure {#section_g2v_wdx_bgb .section}

1.  Log on to the [Security Center console](partners-intl.console.aliyun.com/#/sas).
2.  In the left-side navigation pane, click **Detection** \> **Alerts**. The **Alerts** page is displayed.
3.  On the **Alerts** page, click an event name to enter the event details page.
4.  View the details of the event and the related exceptions. Handle the exceptions.
    -   View event details: You can view the assets affected by this event, the time when the event started or ended, and the details about the related exceptions.
    -   View affected assets: Click an asset in the **Affected Assets** column. The details page of this asset is displayed. You can view all the events, vulnerabilities, baseline risks, and asset fingerprints.
    -   View and handle **Related Exceptions**: In the **Related Exceptions** area, you can view the details of the related exceptions and the corresponding solutions.
        -   **Handle Offline**: After you handle an event offline, you can click this button to change the event status to **Handled**.
        -   **Ignore Once**: If you ignore an event, the event status is changed to **Handled**. Security Center does not send alerts on a handled event.
        -   **Whitelist**: If you label an event as a false positive, the event status is changed to **Handled**. Security Center does not send alerts on a handled event. You can locate a handled event by filtering the events by **Handled** on the Events page, and click **Cancel Whitelist**.

            **Note:** A false positive indicates that the system sends alerts on a normal program. A common false positive is unusual TCP packets. It indicates that a program on your server is performing suspicious scanning on other devices.


