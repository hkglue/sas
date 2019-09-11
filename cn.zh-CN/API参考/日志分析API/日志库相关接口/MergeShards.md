# MergeShards {#reference_tyv_xtq_12b .reference}

合并两个相邻的 readwrite 状态的 Shards。在参数中指定一个 shardid，服务端自动找相邻的下一个 Shard。

## 请求语法 {#section_j5v_14t_12b .section}

``` {#codeblock_gmb_866_smo}
POST /logstores/<logstorename>/shards/<shardid>?action=merge HTTP/1.1
Authorization: <AuthorizationString>
Date: <GMT Date>
Host: <Project Endpoint>
x-log-apiversion: 0.6.0
x-log-signaturemethod: hmac-sha1
```

## 请求参数 {#section_mx5_b4t_12b .section}

|参数名称|类型|是否必须|描述|
|:---|:-|:---|:-|
|logstoreName|string|是|日志库名称|
|shardid|int|是|shard ID|

 **请求头** 

MergeShards接口无特有请求头。关于 Log Service API 的公共请求头，请参考 [公共请求头](intl.zh-CN/API 参考/公共请求头.md)。

 **响应头** 

Content-Type: application/json

MergeShards接口无特有响应头。关于 Log Service API 的公共响应头，请参考 [公共响应头](intl.zh-CN/API 参考/公共响应头.md)。

 **响应元素** 

3 个 Shard 元素组成的数组，第一个 shard 为 merge 之后的 Shard，后两个为 merge 之前的 Shard。

``` {#codeblock_fmk_m8x_934}
[
    {
        'shardID': 167, 
        'status': 'readwrite', 
        'inclusiveBeginKey': 'e0000000000000000000000000000000',
        'createTime': 1453953105,
        'exclusiveEndKey': 'ffffffffffffffffffffffffffffffff'
    }, 
    {
        'shardID': 30, 
        'status': 'readonly', 
        'inclusiveBeginKey': 'e0000000000000000000000000000000', 
        'createTime': 0, 
        'exclusiveEndKey': 
        'e7000000000000000000000000000000'
    },
    {
        'shardID': 166, 
        'status': 'readonly', 
        'inclusiveBeginKey': 'e7000000000000000000000000000000', 
        'createTime': 1453953073, 
        'exclusiveEndKey': 'ffffffffffffffffffffffffffffffff'
    }
]
```

 **错误码** 

除了返回 Log Service API 的 [通用错误码](intl.zh-CN/API 参考/通用错误码.md)，还可能返回如下特有错误码：

|HTTP 状态码|ErrorCode|ErrorMessage|
|:-------|:--------|:-----------|
|404|LogStoreNotExist|logstore \{logstoreName\} does not exist|
|400|ParameterInvalid|invalid shard id|
|400|ParameterInvalid|can not merge the last shard|
|500|InternalServerError|Specified Server Error Message|
|400|LogStoreWithoutShard|logstore has no shard|

**说明：** 上表错误消息中 \{name\} 表示该部分会被具体的 LogstoreName 来替换。

## 示例 {#section_e5p_d4t_12b .section}

**请求示例：** 

``` {#codeblock_0l6_0sx_g7x}
POST /logstores/logstorename/shards/30?action=merge
Header :
{
    "Content-Length": 0, 
    "x-log-signaturemethod": "hmac-sha1", 
    "x-log-bodyrawsize": 0, 
    "User-Agent": "log-python-sdk-v-0.6.0", 
    "Host": "ali-test-project.cn-hangzhou.sls.aliyuncs.com", 
    "Date": "Thu, 12 Nov 2015 03:40:31 GMT", 
    "x-log-apiversion": "0.6.0", 
    "Authorization": "LOG <yourAccessKeyId>:<yourSignature>"
}
```

 **响应示例：** 

``` {#codeblock_49v_1kb_zg2}
Header:
{
    "content-length": "57", 
    "server": "nginx/1.6.1", 
    "connection": "close", 
    "date": "Thu, 12 Nov 2015 03:40:31 GMT", 
    "content-type": "application/json", 
    "x-log-requestid": "56440A2F99248C050600C74C"
}
Body :
[
    {
        'shardID': 167, 
        'status': 'readwrite', 
        'inclusiveBeginKey': 'e0000000000000000000000000000000',
        'createTime': 1453953105,
        'exclusiveEndKey': 'ffffffffffffffffffffffffffffffff'
    }, 
    {
        'shardID': 30, 
        'status': 'readonly', 
        'inclusiveBeginKey': 'e0000000000000000000000000000000', 
        'createTime': 0, 
        'exclusiveEndKey': 
        'e7000000000000000000000000000000'
    },
    {
        'shardID': 166, 
        'status': 'readonly', 
        'inclusiveBeginKey': 'e7000000000000000000000000000000', 
        'createTime': 1453953073, 
        'exclusiveEndKey': 'ffffffffffffffffffffffffffffffff'
    }
]
```

