# GetCursor {#concept_ffg_3dm_12b .concept}

You can call this operation to query a cursor based on the server time. The following figure shows the relationships among the project, Logstore, shard, and cursor.

![](images/6710_en-US.png "Relationships among the project, Logstore, shard, and cursor")

-   A project has multiple Logstores.
-   A Logstore has multiple shards.
-   You can use a cursor to obtain the location of a specific log.

## Request syntax {#section_j5v_14t_12b .section}

```
GET /logstores/ay42/shards/2? type=cursor&from=1402341900 HTTP/1.1
Authorization: <AuthorizationString>
Date: <GMT Date>
Host: <Project Endpoint>
x-log-apiversion: 0.6.0
```

## Request parameters {#section_mx5_b4t_12b .section}

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|shard|String|Yes| |
|type|String|Yes|The type of data to be queried. Set this parameter to cursor.|
|from|String|Yes|The time used to query a cursor. Set this parameter to a Unix timestamp or a string such as begin or end.|

**Logstore lifecycle**

The lifecycle of a Logstore is specified by the ttl parameter in the Logstore attributes. For example, the current time is 2018-11-11 09:00:00 and the ttl parameter is set to 5. The time interval of consumable data in each shard is \[2018-11-05 09:00:00, 2018-11-11 09:00:00\). The server time is used.

Using the from parameter, you can locate the logs within the lifecycle of a shard. Assume that the Logstore lifecycle is \[begin\_time, end\_time\) and the from parameter is set to from\_time, then:

-   `from_time ≤ begin_time or from_time = "begin"`: returns the cursor corresponding to the log whose timestamp is at begin\_time.
-   `from_time ≥ end_time or from_time = "end"`: returns the cursor corresponding to the next log to be written at the current time \(there is no data in the current cursor location\).
-   `from_time > begin_time and from_time < end_time`: returns the cursor corresponding to the first data packet that the server receives later than or at from\_time.

**Request header fields**

This operation does not require special request header fields. For more information about the common request header fields of Log Service operations, see [Common request header fields](intl.en-US/API Reference/Public request header.md).

**Response header fields**

This operation does not return special response header fields. For more information about the common response header fields of Log Service operations, see [Common response header fields](intl.en-US/API Reference/Public response header.md).

**Response parameters**

```
{
    "cursor": "MTQ0NzI5OTYwNjg5NjYzMjM1Ng=="
}
```

**Error codes**

In addition to the [common errors](intl.en-US/API Reference/Common error codes.md) of Log Service operations, this operation also returns some specific errors, as listed in the following table.

|HTTP status code|Error code|Error message|
|:---------------|:---------|:------------|
|404|LogStoreNotExist|Logstore \{Name\} does not exist|
|400|ParameterInvalid|Parameter From is not valid|
|400|ShardNotExist|Shard \{ShardID\} does not exist|
|500|InternalServerError|Specified Server Error Message|
|400|LogStoreWithoutShard|the logstore has no shard|

## Examples {#section_e5p_d4t_12b .section}

**Sample request**

```
GET /logstores/sls-test-logstore/shards/0? type=cursor&from=begin
Header:
{
    "Content-Length": 0, 
    "x-log-signaturemethod": "hmac-sha1", 
    "x-log-bodyrawsize": 0, 
    "User-Agent": "log-python-sdk-v-0.6.0", 
    "Host": "ali-test-project.cn-hangzhou-devcommon-intranet.sls.aliyuncs.com", 
    "Date": "Thu, 12 Nov 2015 03:56:57 GMT", 
    "x-log-apiversion": "0.6.0", 
    "Content-Type": "application/json", 
    "Authorization": "LOG <yourAccessKeyId>:<yourSignature>"
}
```

**Sample success response**

```
Header:
{
    "content-length": "41", 
    "server": "nginx/1.6.1", 
    "connection": "close", 
    "date": "Thu, 12 Nov 2015 03:56:57 GMT", 
    "content-type": "application/json", 
    "x-log-requestid": "56440E0999248C070600C6AA"
}
Body:
{
    "cursor": "MTQ0NzI5OTYwNjg5NjYzMjM1Ng=="
}
```

