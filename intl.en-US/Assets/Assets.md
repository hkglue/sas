# Assets {#concept_mvx_jlc_zdb .concept}

The Assets page in the Security Center console allows you to view the security status of the assets that have been protected by Security Center. You can use the asset group and tag functions on the Assets page to manage the security of specific assets. You can view security events by asset group. You can also use tags to filter and view assets that have the same attributes.

## View the security status of assets {#section_w2f_khj_zdb .section}

To view the security status of your assets, follow these steps:

1.  Log on to the [Security Center console](https://yundun.console.aliyun.com/?p=sas).
2.  In the left-side navigation pane, click **Assets** to view the security status of the assets that have been protected by Security Center.
3.  You can show the filter pane, and use the search and filtering functions in the pane to quickly find your expected assets.
    -   Enter the IP address of a server in the search box to view the security status of the server.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13636/15687729354854_en-US.png)

    -   You can use the filtering items to filter assets, including **Category**, **Tag**, **Region**, **Security Issue Type**, **Agent**, **OS**, and **All Groups**.

        **Note:** When a filtering item contains too many criteria, you can click the sort button next to the filtering item to sort these criteria. You can sort the criteria in the alphabetical ascending order \(A to Z\), alphabetical descending order \(Z to A\), numerical ascending order \(1 to 9\), and numerical descending order \(9 to 1\).

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13636/15687729354855_en-US.png)

        -   You can select a criterion under a filtering item to view assets that match the specified criterion. For example, you can select **Malaysia \(Kuala Lumpur\)** under the **Region** item to view servers in the Malaysia \(Kuala Lumpur\) region.
        -   You can also select multiple criteria under a filtering item, and then click **Apply** to view assets that match all these criteria. For example, you can select **Baseline Check** and **Vulnerability** for the **Security Issue Type** item, and then click **Apply** to view servers that have baseline risks or vulnerabilities.
        -   You can select multiple filtering items to filter assets. For example, you can select **Malaysia \(Kuala Lumpur\)** for the **Region** item and select **linux** for the **OS** item to only view Linux servers in the Malaysia \(Kuala Lumpur\) region.
        **Note:** You can save filtering items that have been applied as a filtering condition. To perform this task, click **Save**, and enter a filtering condition name \(for example, malay-li\). You can then select the condition from the filtering condition list in the upper-right corner of the asset list page.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13636/15687729364857_en-US.png)

4.  You can click **Select Columns** in the upper-right corner of the Assets page to customize the columns to be shown in the asset list.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13636/15687729374858_en-US.png)

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13636/15687729374859_en-US.png)


## Disable/Enable Security Center protection {#section_gff_khj_zdb .section}

If you want the Security Center agent to stop consuming resources on your assets for a specific period of time, follow these steps to disable Security Center protection for your assets:

1.  Select one or more assets whose **Security Status** is **Protected** from the Assets page.
2.  Click **More** \> **Disable Protection** under Assets.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13636/15687729374860_en-US.png)


After Security Center protection has been disabled, the Security Center agent no longer collects security information on your servers, reports security information, or occupies system resources. You can select **More** \> **Enable Protection** to enable Security Center protection for your assets.

## Quick security check {#section_jff_khj_zdb .section}

You can use the **Security Check** function on the Assets page to perform a security scan for specific assets and update information about vulnerabilities, baseline configuration risks, and asset summary.

Follow these steps to perform a quick security check:

1.  Select one or more assets from the Assets page.
2.  Click **Security Check** under Assets.
3.  Select security check entries in the Security Check dialog box.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13636/15687729374861_en-US.png)

4.  Click **OK** to perform a quick security check.

The security check results will be automatically updated to the relevant page in the Security Center console.

## Asset group management {#section_mff_khj_zdb .section}

If the Assets page contains multiple assets under your account, we recommend that you use the asset group function to create an asset group for these assets so that you can search and manage these assets by group.

Follow these steps to create and manage asset groups:

1.  Show the filter pane. At the bottom of the filter pane, click **Manage** under **All Groups** to open the Manage Asset Groups dialog box.
2.  Create an asset group.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13636/15687729386423_en-US.jpg)

    **Note:** The **Default** group contains assets that have not been added to any asset group. If you delete an asset group, all assets in that group will be moved to the **Default** group.

    1.  Click **Add Group**.
    2.  Enter a group name, and click **OK**.
    3.  You can click the **+** button on the right side of a group to create a sub group. You can also rename or delete a group.

        **Note:** The system supports up to three levels of sub groups.

3.  Sort asset groups. When there are multiple groups with the same level, you can click the **↑** or **↓** button next to a group to sort the groups.
4.  Delete an asset group. You can click the **×** button on the right side of a group to delete the group.

    **Note:** When you delete an asset group that contains sub groups, all of the assets in this group and sub groups will be moved to the Default group.


## Add assets to a specific asset group {#section_qff_khj_zdb .section}

You can add assets to an asset group to operate multiple assets at one time. We recommend that you add the same type of assets to an asset group. For example, when you configure an asset baseline check policy, you can specify an asset group to apply the policy to all assets in the group. You can also filter assets on the Assets page by asset group.

To add assets to a specific asset group, follow these steps:

1.  Select one or more assets on the Assets page and click **Change Group** under the asset list.
2.  Select an asset group to add these assets to the specified group.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13636/15687729384863_en-US.png)

    **Note:** You cannot add both assets and sub groups to the same asset group. For example, asset group A contains sub group B. In this case, you cannot add asset C to asset group A.

3.  Click **OK**.

## Add/Modify tags {#section_tff_khj_zdb .section}

You can use tags to label your assets and filter assets on the Assets page by tag.

Follow these steps to add a tag to an asset:

1.  Select an asset on the Assets page.
2.  Hover your cursor over the tag icon in the **Tag** column, and click **Add**. \(If the asset already has tags, click **Edit**.\)

    **Note:** You can select one or more assets, and click **Modify Tag** under the asset list to modify tags for these assets at the same time.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13636/15687729386424_en-US.jpg)

3.  Enter a tag name or select one or more existing tags.

    **Note:** You can add multiple tags to an asset.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13636/15687729386427_en-US.jpg)

4.  Click **OK**.

## Remove external server {#section_vff_khj_zdb .section}

You can remove external servers from the asset list to completely disable Security Center protection for these servers.

**Note:** Uninstalling the Security Center agent on an ECS instance does not remove the instance from the asset list. In this case, the security status of the ECS instance appears unprotected.

Follow these steps to remove external servers from the asset list:

1.  Select one or more external servers from the Assets page.
2.  Click **More** \> **Delete External Servers** under Assets.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13636/15687729384864_en-US.png)

3.  Click **OK**. The system will automatically uninstall the Security Center agent on your servers and then remove the servers from the asset list.

