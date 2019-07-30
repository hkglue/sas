# Attack analysis {#concept_w4b_xxp_bgb .concept}

Security Center **Enterprise Edition** provides the attack analysis feature. This feature displays the attacks on your assets and analyzes these attacks.

Based on the protection capabilities of Alibaba Cloud, the attack analysis feature provides basic attack detection and prevention. We recommend that you develop a more refined and in-depth protection system by optimizing firewalls and enhancing business security.

**Note:** The **Attacks, Visits, Threats** feature has been removed.

Log on to the Security Center console, click **Attack Analysis** in the left-side navigation pane, and you can view the attack details.

![](images/33918_en-US.png)

**Note:** After you purchase a cloud service, you must wait for the data synchronization to complete before you can view the attack data.

The **Attack Analysis** page displays the following information:

-   **Time Range**: You can specify the time range to view the corresponding attack information.
-   **Number of Attacks**: The total number of attacks on your assets within the specified time range.
-   **Attack Type Distribution**: The attack types and the number of each attack type.
-   **Top 5 Attack Sources**: The top five attack source IP addresses that have launched the most attacks.
-   **Top 5 Attacked Assets**: The top five assets that have encountered the most attacks.
-   **Attack details list**: Lists the details of each attack, including the attack time, attack source IP address, attacked asset, attack type, and attack status.

## Attack time range {#section_dq5_myp_bgb .section}

On the **Attack Analysis** page, you can specify the attack time range to view the corresponding attack information.

You can specify the time range to **Today**,**Last 7 Days**, or **Last 30 Days**.

![](images/33920_en-US.png)

## Number of attacks {#section_bp1_bzp_bgb .section}

In the **Number of Attacks** area, a graph displays the trend in attacks within the specified range of time. You can find the the maximum and minimum numbers of attacks on the graph. You can hover your mouse pointer over the graph to view the number of attacks at a specific time.

![](images/33921_en-US.png)

## Attack type distribution {#section_ijj_zyp_bgb .section}

In the **Attack Type Distribution** area, you can view the number of attacks by type.

![](images/33922_en-US.png)

## Top 5 attack sources {#section_ehk_zyp_bgb .section}

In the **Top 5 Attack Sources** area, you can view the top five IP addresses that have launched the most attacks and the number of attacks launched by each of them.

![](images/33923_en-US.png)

## Top 5 attacked assets {#section_rdl_zyp_bgb .section}

In the **Top 5 Attacked Assets** area, you can view the public IP addresses of the five assets that have encountered the most attacks and the number of attacks on each of these assets.

![](images/33925_en-US.png)

## Attack details list {#section_u1m_zyp_bgb .section}

In the attack details list, you can view the details of each attack, including the attack time, attack source IP address, attacked asset information, attack type, and attack status.

![](images/33926_en-US.png)

**Note:** This list displays the details of a maximum of 10,000 attacks. You can specify **Time Range** to view all attacks within a specific time range.

Attack details

|Item|Description|
|----|-----------|
|Attack time|The time when an attack occurs.|
|Attack source|The source IP address of an attack.|
|Attacked asset|The name, public IP address, and internal IP address of an attacked asset.|
|Attack type|The type of an attack, such as an SSH brute-force attack or a remote code execution attack.|
|Attack status|The status of an attack. Security Center uses the protection capabilities of Alibaba Cloud to block common attacks. The status of a blocked attack is **Blocked**. The intrusions are displayed on the **Events** page.|

To view the details of a specific attack, you can search for this attack by attack type, attacked asset or attack source in the search box above the attack details list.

![](images/33927_en-US.png)

You can click the name of an **Attacked Asset** to open the asset details page. This page displays the basic asset information, vulnerability information, baseline risks, alert events, asset fingerprints, and security configurations.

![](images/33928_en-US.png)

