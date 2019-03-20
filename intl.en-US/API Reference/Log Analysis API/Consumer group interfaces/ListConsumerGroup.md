# ListConsumerGroup {#reference_ns3_mgh_f2b .reference}

Query all consumer groups of a specified Logstore.

Example:

```
GET /logstores/{logstoreName}/consumergroups
```

## Request syntax {#section_o54_dhh_f2b .section}

```
GET /logstores/<logstoreName>/consumergroups HTTP/1.1
Authorization: <AuthorizationString>
x-log-bodyrawsize: 0
User-Agent: <UserAgent>
x-log-apiversion: 0.6.0
Host: <Project Endpoint>
x-log-signaturemethod: hmac-sha1
Date: <GMT Date>
Content-Type: application/x-protobuf
Connection: Keep-Alive
```

## Request parameters {#section_lvh_2hh_f2b .section}

|Attribute name|Type |Required or not|Description|
|:-------------|:----|:--------------|:----------|
|logstoreName|string|Yes|Logstore name.|

**Request header**

The ListConsumerGroup interface does not have a specific request header. For details about public request headers of Log Service APIs, see [Public request header](intl.en-US/API Reference/Public request header.md).

**Response header**

The ListConsumerGroup interface does not have a specific response header. For details about public response headers of Log Service APIs, see [Public response header](intl.en-US/API Reference/Public response header.md).

**Response element**

If the ListConsumerGroup request is sent successfully, the response body contains a list of all consumer groups under the specified project and Logstore in the following format:

|Attribute name| Type|Description|
|:-------------|:----|:----------|
|Consumergroup|string|Consumer group name.|
|timeout |integer|Timeout period. If no heartbeat is received in the timeout period, the consumer group is deleted.|
|order|bool|Sequential consumption or not.|

**Error code**

The interface may return the following error codes in addition to Log Service API [Common error codes](intl.en-US/API Reference/Common error codes.md):

|HTTP status code|ErrorCode|ErrorMessage|
|:---------------|:--------|:-----------|
|404|ProjectNotExist|The Project does not exist : \{Project\}|
|404|LogStoreNotExist|logstore \{logstoreName\} dose not exist|
|500|InternalServerError|Specified Server Error Message|

## Example {#section_p5z_ghh_f2b .section}

**Request example:**

```
GET /logstores/my-logstore/consumergroups HTTP/1.1
Authorization: LOG <yourAccessKeyId>:<yourSignature>
x-log-bodyrawsize: 0
User-Agent: sls-java-sdk-v-0.6.1
x-log-apiversion: 0.6.0
Host: my-project.cn-shanghai.log.aliyuncs.com
x-log-signaturemethod: hmac-sha1
Date: Fri, 04 May 2018 08:47:30 GMT
Content-Type: application/x-protobuf
Connection: Keep-Alive
```

**Response example:**

```
HTTP/1.1 200
Server: nginx/1.12.1
Content-Type: application/json
Connection: close
Access-Control-Allow-Origin: *
Date: Fri, 04 May 2018 08:47:31 GMT
x-log-requestid: 5AEC1E23048191954B42EAB9
[
  {
    "name": "test-consumer-group",
    "timeout": 30,
    "order": true
  }
]
```

