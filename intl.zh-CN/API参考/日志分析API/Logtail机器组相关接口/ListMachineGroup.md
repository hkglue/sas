# ListMachineGroup {#reference_nkz_c5q_12b .reference}

查看机器组名称列表。

示例：

```
GET /machinegroups?offset=1&size=100
```

## 请求语法 {#section_j5v_14t_12b .section}

```
GET /machinegroups?offset=1&size=100 HTTP/1.1
Authorization: <AuthorizationString> 
Date: <GMT Date>
Host: <Project Endpoint>
x-log-apiversion: 0.6.0
x-log-signaturemethod: hmac-sha1
```

## 请求参数 {#section_mx5_b4t_12b .section}

URL 参数：

|参数名称|类型|是否必须|描述|
|:---|:-|:---|:-|
|offset|int|否|返回记录的起始位置，默认为 0|
|size|int|否|每页返回最大条目，默认 500（最大值）|
|groupName|string|否|用于过滤的机器组名称（支持部分匹配）|

**请求头**

无特有请求头。关于 Log Service API 的公共请求头，请参考 [公共请求头](intl.zh-CN/API 参考/公共请求头.md)。

**响应头**

无特有响应头。请参考 [公共响应头](intl.zh-CN/API 参考/公共响应头.md)。

**响应元素**

请求成功，其响应 Body 会包括指定 Project 下的所有 machinegroup 名称列表。具体格式如下：

|名称|类型|描述|
|:-|:-|:-|
|count|int|返回的 machinegroup 数目|
|total|int|返回 machinegroup 总数|
|machinegroups|json array|返回的 machinegroup 名称列表|

```
{
    "machinegroups":     [
        "test-machine-group",
        "test-machine-group-2"
    ],
    "count": 2,
    "total": 2
}
```

**错误码**

除了返回 Log Service API 的 [通用错误码](intl.zh-CN/API 参考/通用错误码.md)，还可能返回如下特有错误码：

|HTTP 状态码|ErrorCode|ErrorMessage|
|:-------|:--------|:-----------|
|500|InternalServerError|internal server error|

## 示例 {#section_e5p_d4t_12b .section}

**请求示例：**

```
GET /machinegroups?groupName=test-machine-group&offset=0&size=3 HTTP/1.1
Header :
{
    "x-log-apiversion": "0.6.0",
    "Authorization": "LOG <yourAccessKeyId>:<yourSignature>",
    "Host": "ali-test-project.cn-hangzhou-devcommon-intranet.sls.aliyuncs.com",
    "Date": "Tue, 10 Nov 2015 18:34:44 GMT",
    "Content-Length": "0",
    "x-log-signaturemethod": "hmac-sha1",
    "User-Agent": "sls-java-sdk-v-0.6.0",
    "Content-Type": "application/x-protobuf",
    "x-log-bodyrawsize": "0"
}
```

**响应示例：**

```
HTTP/1.1 200 OK
Header :
{
    "Date": "Tue, 10 Nov 2015 18:34:44 GMT",
    "Content-Length": "83",
    "x-log-requestid": "564238C499248C8F7B0001DE",
    "Connection": "close",
    "Content-Type": "application/json",
    "Server": "nginx/1.6.1"
}
Body :
{
    "machinegroups":     [
        "test-machine-group",
        "test-machine-group-2"
    ],
    "count": 2,
    "total": 2
}
```

