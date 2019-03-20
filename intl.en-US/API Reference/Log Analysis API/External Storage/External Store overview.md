# External Store overview {#concept_ecg_55q_12b .concept}

## Differences between External Store and Logstore {#section_ggv_y45_12b .section}

The Logstore stores logs and continuously receives incremental data.

The External Store stores static metadata associated with logs, and is called the external data source.  Log Service usually performs join query between logs and other related data.

## Scenarios {#section_gcy_x45_12b .section}

-   Logstore and External Store perform join query and analysis.
-   Log Service writes the query and analysis results of Logstore to External Store.

## Supported storage types {#section_gvd_x45_12b .section}

Currently, only RDS instances in the Virtual Private Cloud \(VPC\) environment in cn-beijing, cn-qingdao, and cn-hangzhou regions can be used as External Stores. To use RDS instances in other regions as External Stores, open a ticket.

## Procedure {#section_ghs_545_12b .section}

1.  Create an External Store and specify the corresponding metadata.
2.  When querying and analyzing logs, reference the External Store name to query and write logs.

For more information about creating, updating, and deleting External Stores, see [External Store related APIs](intl.en-US/API Reference/External Storage/External Store related APIs.md) related APIs or Python SDK [Python SDK](../../../../../intl.en-US/SDK Reference/Python SDK.md).

