# Baseline check {#concept_hmp_h5d_rfb .task}

This topic describes how to check the baselines by using customized policies, and how to view the check results and suggestions on handling baseline risks.

Baseline check is a value-added service of Security Center. Only **Enterprise Edition** users can activate and use this service. A Basic Edition or Pro Edition user must upgrade to Enterprise Edition to use this service.

## View the summary data for the check result {#section_wkt_knl_dhb .section}

In the upper part of the Baseline Risk page, you can view the summary data for the baseline check result.

![](images/21603_en-US.png)

-   Checked Servers: The number of servers on which baseline check is performed.

    **Checked Servers** indicates the number of servers that you select when [configuring a check policy](intl.en-US/Precautions/Baseline check/Create and configure a baseline check policy.md#ul_xwj_qzk_dhb).

-   Check Items: The number of **check items** that you select when [configuring a scan policy](intl.en-US/Precautions/Baseline check/Create and configure a baseline check policy.md#ul_xwj_qzk_dhb).
-   Last Check Pass Rate: The pass rate of the last baseline check.

    If the number in the **Last Check Pass Rate** area is green, the pass rate of the checked servers is high. If this number is red, a large number of baseline risks have been detected. We recommend that you view the check result details and deal with the **failed** items.

    ![](images/41096_en-US.png)


## Manually perform a baseline check {#section_pq1_3ql_dhb .section}

Both automatic periodical check and manual check are supported. To schedule a periodical check, set **Cycle** and **Time** when [configuring a scan policy](intl.en-US/Precautions/Baseline check/Create and configure a baseline check policy.md#ul_xwj_qzk_dhb). To manually begin a check, click **Check Now**.

1.  Log on to the [Security Center console](https://yundun.console.aliyun.com/?p=sas).
2.  In the left-side navigation pane, click **Baseline Check**.
3.  In the **Select Policy** drop-down list, select a policy for a manual check.

    ![](images/41095_en-US.png)

    **Note:** If any number in the **Failed Items/Affected Servers** column is not 0, baseline risks have been detected on your servers.

4.  Click **Check Now**.![](images/41092_en-US.png) 

    After you click **Check Now**, the progress of the check is displayed.

    ![](images/41093_en-US.png)

    You can click **View Progress** to view the number of servers that have passed or failed the check and the causes of the failures. Click **View Solution** to learn how to handle the failures.

    ![](images/41094_en-US.png)

    Click **Refresh** to view the latest check result.


## View detailed check results {#section_uw5_djv_k2b .section}

After a baseline check is complete, you can click a **baseline** in the list to enter the details page of this baseline. This page displays the assets affected by this baseline, the failed and passed items of each asset, and the suggestions on risk handling. You can also **ignore****failed** items or **verify** fixed risks.

1.  Log on to the [Security Center console](https://yundun.console.aliyun.com/?p=sas).
2.  In the left-side navigation pane, click **Baseline Check**.
3.  In the baseline list, click a **baseline**.

    ![](images/41097_en-US.png)

4.  On the details page of the selected baseline, you can:
    -   View the information about all assets affected by this baseline.

        ![](images/41098_en-US.png)

    -   Click ![](images/41099_en-US.png) next to an asset to view the at-risk baseline items on this asset and the check result of each item. The check result can be **failed** or **passed**.

        **Note:** We recommend that you handle the **failed** items immediately.

    -   If you do not want to receive alerts for risks on an item, select this item and click **Ignore** to remove it from the alert list. An ignored item no longer triggers alerts.

        ![](images/41100_en-US.png)

        **Note:** To ignore multiple items, select the items, and click **Ignore** below the item list of the asset.

    -   Click **Details** next to an item to view the item description, check result, and suggestions.

        We recommend that you enhance the baseline configurations based on the **suggestions**.

        ![](images/41101_en-US.png)

        **Note:** We recommend that you handle the failed items of high severity immediately.

    -   After you handle a failed item, click **Verify** to check whether the risk has been cleared. After you begin verifying an item, the item status becomes **Verifying**.

        ![](images/41102_en-US.png)

        If you have not verified an item, Security Center automatically verifies this item during the next periodical check.


