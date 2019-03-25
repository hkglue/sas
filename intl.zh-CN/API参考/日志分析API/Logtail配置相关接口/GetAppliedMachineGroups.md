# GetAppliedMachineGroups {#reference_cld_35q_12b .reference}

列出 config 应用的机器列表。

示例：

```
GET /configs/{configName}/machinegroups
```

## 请求语法 {#section_j5v_14t_12b .section}

```
GET /configs/{configName}/machinegroups HTTP/1.1
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
|ConfigName|string|是|配置名称|

**请求头**

无特有请求头。关于 Log Service API 的公共请求头，请参考 [公共请求头](intl.zh-CN/API 参考/公共请求头.md)。

**响应头**

无特有响应头。请参考 [公共响应头](intl.zh-CN/API 参考/公共响应头.md)。

**响应元素**

请求成功，其响应 Body 会包括指定 machinegroup 下的所有 machine 列表，具体格式如下：

|名称|类型|描述|
|:-|:-|:-|
|count|整型|返回的 machineGroup 数目。|
|machinegroups|字符串数组|返回的 machineGroup 名称列表。|

```
{
    "count":2,
    "machinegroups":
    ["group1","group2"]
}
```

**错误码**

除了返回 Log Service API 的 [通用错误码](intl.zh-CN/API 参考/通用错误码.md)，还可能返回如下特有错误码：

|HTTP 状态码|ErrorCode|ErrorMessage|
|:-------|:--------|:-----------|
|404|GroupNotExist|group \{GroupName\} does not exist|
|500|InternalServerError|internal server error|

## 示例 {#section_e5p_d4t_12b .section}

**请求示例：**

```
GET /configs/logtail-config-sample/machinegroups
Header:
{
    "Content-Length": 0, 
    "x-log-signaturemethod": "hmac-sha1", 
    "x-log-bodyrawsize": 0, 
    "User-Agent": "log-python-sdk-v-0.6.0", 
    "Host": "ali-test-project.cn-hangzhou-devcommon-intranet.sls.aliyuncs.com", 
    "Date": "Mon, 09 Nov 2015 09:51:38 GMT", 
    "x-log-apiversion": "0.6.0", 
    "Authorization": "LOG <yourAccessKeyId>:<yourSignature>"
}
```

**响应示例：**

```
Header : 
{
    "content-length": "44", 
    "server": "nginx/1.6.1", 
    "connection": "close", 
    "date": "Mon, 09 Nov 2015 09:51:38 GMT", 
    "content-type": "application/json", 
    "x-log-requestid": "56406CAA99248CAA230BE828"
}
Body:
{
    "count": 1, 
    "machinegroups": 
    [
        "sample-group"
    ]
}
```

