# Log retrieval {#concept_ljs_fxb_zdb .concept}

Threat Detection Service \(TDS\) provides the log retrieval feature to help you manage logs on your Alibaba Cloud systems. You can easily identify the causes of problems that occur on your servers.

**Note:** You must upgrade to the Threat Detection Service Enterprise Edition to use the log retrieval feature. TDS records your logs and supports retrieval only when the Log retrieval feature is enabled. Currently, TDS retains logs for 180 days and allows you to retrieve the logs of the last 30 days.

## Benefits {#section_tpl_ptq_zdb .section}

The log retrieval feature provides the following benefits:

-   One-stop log retrieval platform. You can retrieve all logs on your Alibaba Cloud systems and trace problems easily.
-   Web-based log retrieval. Without the need for additional deployment, you can log on to the TDS console using a browser and use the log retrieval feature directly.
-   Supports TB sized data retrieval. You can add multiple operators in a search condition and get full-text search results within several seconds.
-   Supports various kinds of server logs and Web logs.

## Scenarios  {#section_wpl_ptq_zdb .section}

You can use log retrieval to achieve the following scenarios:

-   Security incident analysis: When a security incident occurs on your server, you can retrieve the logs to investigate the cause, and evaluate the damage and affected assets.
-   Operation review: You can review operation logs on your server, and troubleshoot high-risk operations or serious problems with fine granularity.
-   Business traffic statistics: You can analyze Web access logs to track your visitors and their requests, and evaluate your service responses.

## Supported logs {#section_ypl_ptq_zdb .section}

You can retrieve the following types of logs:

|Type| Log|Description|
|Server log|Logon history|Logs of successful logons|
|Brute force cracking|Logs of brute force cracking attacks|
|Process snapshot|Logs of processes on the server at a specific time|
|Port snapshot|Logs of listener ports on the server at a specific time|
|Account snapshot|Account logon information on the server at a specific time|
|Process initiation log|Logs of process initiation on the server|
|Network connection log|Logs of outgoing connections from the server|
|Web log|Web access log|HTTP logs of the cloud services|
|Network session log|Logs of the 5-tuples of the cloud services|
|DNS log|Domain name resolution logs|

**Note:** For more information, see [Supported logs and fields](intl.en-US/User Guide/Log retrieval/Supported logs and fields.md#).

## Procedure {#section_dql_ptq_zdb .section}

You can use the log retrieval feature by following these steps:

1.  Log on to the [Threat Detection Service console](https://yundun.console.aliyun.com/?p=sas).
2.  In the left-side navigation pane, click **More**.
3.  Select **Log Retrieval**.
4.  Select a **Log Source** and **Field**, specify a **keyword** and Duration, and then click **Search**. The duration can be the last 24 hours, the last 7 days, or a specified time period within the last 30 days.

    **Note:** You can click **+** on the right-side of the page to add multiple operators to a search condition, or click **Add Conditions** to add multiple search conditions. You can delete an operator by clicking **-**. For more information, see [Query operators and keywords](intl.en-US/User Guide/Log retrieval/Grammar logic instructions.md#).

5.  Detailed log records are retrieved based on your search conditions. You can modify the fields in search results for further analysis, or click **Save Search** to save the current search conditions for future use. You can click **Saved Searches** to use saved search conditions.
6.  You can view the search results based on different time granularities and export the results.

