# HeartBeat {#reference_mrz_kgh_f2b .reference}

为指定消费者发送心跳到服务端。

示例：

```
POST /logstores/{logstoreName}/consumergroups/{consumerGroupName}?type=heartbeat&consumer={consumer}
```

## 请求语法 {#section_o54_dhh_f2b .section}

```
POST /logstores/<logstoreName>/consumergroups/<consumerGroup>?type=heartbeat&consumer=<consumer> HTTP/1.1
Authorization: <AuthorizationString>
x-log-bodyrawsize: 0
User-Agent: <UserAgent>
x-log-apiversion: 0.6.0
Host: <Project Endpoint>
x-log-signaturemethod: hmac-sha1
Date: <GMT Date>
Content-Type: application/json
Content-MD5: F58544E4D022CC28A93D0B7CC208A5AA
Content-Length: <ContentLength>
<shard ID list>
```

## 请求参数 {#section_lvh_2hh_f2b .section}

|属性名称|类型|是否必须|描述|
|:---|:-|:---|:-|
|logstoreName|string|是|Logstore 的名称，在 Project 下必须唯一。|
|consumerGroup|string|是|消费组名称，在Project 下必须唯一。|
|consumer|string|是|消费者。|
|\{Shard ID List\}|array|是|正在消费的Shard Id列表。|

**请求头**

HeartBeat接口无特有请求头，关于 Log Service API 的公共请求头请参考[公共请求头](intl.zh-CN/API 参考/公共请求头.md)。

**响应头**

HeartBeat接口无特有响应头，关于 Log Service API 的公共响应头请参考[公共响应头](intl.zh-CN/API 参考/公共响应头.md)。

**响应元素**

HeartBeat请求成功，HTTP 状态码返回 200，同时返回消费者负责消费的所有Shard ID列表。

**错误码**

除了返回 Log Service API 的[通用错误码](intl.zh-CN/API 参考/通用错误码.md)，还可能返回如下特有错误码：

|HTTP状态码|ErrorCode|ErrorMessage|
|:------|:--------|:-----------|
|400|NotExistConsumerWithBody|non-exist consumer with non-empty body of heartbeat message|
|404|ProjectNotExist|The Project does not exist : \{Project\}|
|404|LogStoreNotExist|logstore \{logstoreName\} dose not exist|
|404|ConsumerGroupNotExist|consumer group not exist|
|500|InternalServerError|Specified Server Error Message|

**细节描述**

只有消费者和服务端建立连接之后才能发送心跳。

## 示例 {#section_p5z_ghh_f2b .section}

**请求示例：**

```
POST /logstores/my-logstore/consumergroups/consumer_group_test?type=heartbeat&consumer=consumer_1 HTTP/1.1
Authorization: LOG <yourAccessKeyId>:<yourSignature>
x-log-bodyrawsize: 0
User-Agent: sls-java-sdk-v-0.6.1
x-log-apiversion: 0.6.0
Host: my-project.cn-shanghai.log.aliyuncs.com
x-log-signaturemethod: hmac-sha1
Date: Sun, 06 May 2018 09:44:10 GMT
Content-Type: application/json
Content-MD5: 8D5162CA104FA7E79FE80FD92BB657FB
Content-Length: 3
Connection: Keep-Alive
[0]
```

**响应示例：**

```
HTTP/1.1 200
Server: nginx/1.12.1
Content-Type: application/json
Content-Length: 5
Connection: close
Access-Control-Allow-Origin: *
Date: Sun, 06 May 2018 09:44:11 GMT
x-log-requestid: 5AEECE6B1FFC0366B2553FB5
[0,1]
```

