# Create and configure a baseline check policy {#concept_h1z_m3b_rfb .concept}

This topic describes how to create, modify, or delete a baseline check policy.

Baseline check is a value-added service of Security Center. Only **Enterprise Edition** users can activate and use this service. A Basic Edition or Pro Edition user must upgrade to Enterprise Edition to use this service.

After you activate this service, Security Center automatically scans all assets based on the **default policy**. The details of this check are as follows:

Time: From 06:00 to 12:00 every day.

Object: All assets under your Alibaba Cloud account.

![默认策略](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/41642/156887646341077_en-US.png)

You can also customize a baseline check policy that covers the baseline items that are not covered by the default policy.

## Procedure {#section_hxf_n4k_zdb .section}

1.  Log on to the [Security Center console](https://yundun.console.aliyun.com/?p=sas).
2.  In the left-side navigation pane, click **Baseline Check**.
3.  In the upper-right corner, click **Manage Policies** to customize a policy or modify the default policy.
    -   In the upper-right corner of the Manage Policies page, click **Create Policy**.

        ![新增策略](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/41642/156887646341084_en-US.png)

        |Configuration item|Description|
        |------------------|-----------|
        |**Policy Name**|Enter a policy name.|
        |**Cycle**|Set the cycle to 1 day, 3 days, 7 days, or 30 days. Set the time to 00:00-06:00, 06:00-12:00, 12:00-18:00, or 18:00-24:00.|
        |**Check Items**|Select check items under the categories including database, system, weak password, and middleware baseline. For more information about baseline check items, see [Baseline check items](intl.en-US/Precautions/Baseline check/Baseline Check overview.md#table_brz_4q1_f2b).

 |
        |**Servers**|Select the asset groups to which you want to apply this policy. **Note:** New servers belong to **Asset Groups** \> **Default** by default. To apply this policy to new servers, select **Default**.

 |

    -   On the Manage Policies page, click **Edit** or **Delete** to modify or delete a specified policy.

        **Note:** You cannot restore a deleted policy.

    -   Click **Edit** next to the **Default** policy. You can select the asset groups to which the default policy is applied.

        **Note:** You cannot delete the default policy or modify the check items in the default policy.

        ![编辑默认策略](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/41642/156887646541078_en-US.png)

    -   Below the Manage Policies page, you can set the level range \(high, medium, low\) for the baseline check.

        ![基线检查等级](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/41642/156887646558548_en-US.png)


