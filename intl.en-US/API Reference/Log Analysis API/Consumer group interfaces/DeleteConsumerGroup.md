# DeleteConsumerGroup {#reference_tsj_2gh_f2b .reference}

Delete a specified consumer group.

Example:

```
DELETE /logstores/{logstoreName}/consumergroups/{consumerGroupName}
```

## Request syntax {#section_o54_dhh_f2b .section}

```
DELETE /logstores/<logstoreName>/consumergroups/<consumerGroupName> HTTP/1.1
Authorization: <AuthorizationString>
x-log-bodyrawsize: 0
User-Agent: <UserAgent>
x-log-apiversion: 0.6.0
Host: <Project Endpoint>
x-log-signaturemethod: hmac-sha1
Date: <GMT Date>
Content-Type: application/x-protobuf
Content-MD5: F58544E4D022CC28A93D0B7CC208A5AA
```

## Request parameters {#section_lvh_2hh_f2b .section}

|Attribute name|Type |Required|Description|
|:-------------|:----|:-------|:----------|
|logstoreName|string|Yes|Name of the Logstore of the consumer group.|
|consumerGroup|string|Yes|Name of the deleted consumer group.|

**Request header**

The DeleteConsumerGroup interface does not have a specific request header. For details about public request headers of Log Service APIs, see [Public request header](intl.en-US/API Reference/Public request header.md).

**Response header**

The DeleteConsumerGroup interface does not have a specific response header. For details about  public response headers of Log Service APIs, see [Public response header](intl.en-US/API Reference/Public response header.md).

**Response element **

The returned HTTP status code is 200.

**Error code**

The interface may return the following error codes in addition to Log Service API [Common error codes](intl.en-US/API Reference/Common error codes.md):

|HTTP status code|ErrorCode|ErrorMessage|
|:---------------|:--------|:-----------|
|404|ProjectNotExist|The Project does not exist : \{Project\}|
|404|LogStoreNotExist|logstore \{logstoreName\} dose not exist|
|500|InternalServerError|Specified Server Error Message|

**Detailed description**

If you have deleted a consumer group that does not exist, success is returned.

## Example {#section_p5z_ghh_f2b .section}

**Request example:**

```
DELETE /logstores/logstore-test/consumergroups/consumer-group-1 HTTP/1.1
Header:
Authorization: LOG :<yourAccessKeyId>:<yourSignature>
x-log-bodyrawsize: 0
User-Agent: sls-java-sdk-v-0.6.1
x-log-apiversion: 0.6.0
Host: my-project.cn-shanghai.log.aliyuncs.com
x-log-signaturemethod: hmac-sha1
Date: Fri, 04 May 2018 08:02:22 GMT
Content-Type: application/json
Content-MD5: F58544E4D022CC28A93D0B7CC208A5AA
Content-Length: 65
Connection: Keep-Alive
```

**Response example:**

```
HTTP/1.1 200
Server: nginx/1.12.1
Content-Length: 0
Connection: close
Access-Control-Allow-Origin: *
Date: Fri, 04 May 2018 08:15:11 GMT
x-log-requestid: 5AEC168FA796F4195BF404CB
```

