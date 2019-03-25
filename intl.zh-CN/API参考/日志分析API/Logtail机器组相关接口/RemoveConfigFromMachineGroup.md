# RemoveConfigFromMachineGroup {#reference_p1t_25q_12b .reference}

从机器组中删除配置。

示例：

```
DELETE /machinegroups/{GroupName}/configs/{ConfigName}
```

## 请求语法 {#section_j5v_14t_12b .section}

```
GET /machinegroups/{groupName} HTTP/1.1
Authorization: <AuthorizationString> 
Date: <GMT Date>
Host: <Project Endpoint>
x-log-apiversion: 0.6.0
x-log-signaturemethod: hmac-sha1
```

## 请求参数 {#section_mx5_b4t_12b .section}

|参数名称|类型|是否必须|描述|
|:---|:-|:---|:-|
|GroupName|string|是|机器分组名称|
|ConfigName|string|是|日志配置名称|

**请求头**

无特有请求头。关于 Log Service API 的公共请求头，请参考 [公共请求头](intl.zh-CN/API 参考/公共请求头.md)。

**响应头**

无特有响应头。请参考 [公共响应头](intl.zh-CN/API 参考/公共响应头.md)。

**响应元素**

HTTP 状态码返回 200。

**错误码**

除了返回 Log Service API 的 [通用错误码](intl.zh-CN/API 参考/通用错误码.md)，还可能返回如下特有错误码：

|HTTP 状态码|ErrorCode|ErrorMessage|
|:-------|:--------|:-----------|
|404|GroupNotExist|group \{GroupName\} does not exist|
|404|ConfigNotExist|config \{ConfigName\} does not exist|
|500|InternalServerError|internal server error|

## 示例 {#section_e5p_d4t_12b .section}

**请求示例：**

```
DELETE /machinegroups/sample-group/configs/logtail-config-sample
{
    "Content-Length": 0, 
    "x-log-signaturemethod": "hmac-sha1", 
    "x-log-bodyrawsize": 0, 
    "User-Agent": "log-python-sdk-v-0.6.0", 
    "Host": "ali-test-project.cn-hangzhou-devcommon-intranet.sls.aliyuncs.com", 
    "Date": "Mon, 09 Nov 2015 09:48:48 GMT", 
    "x-log-apiversion": "0.6.0", 
    "Authorization": "LOG <yourAccessKeyId>:<yourSignature>"
}
```

**响应示例：**

```
{
    "date": "Mon, 09 Nov 2015 09:48:48 GMT", 
    "connection": "close", 
    "x-log-requestid": "56406C0099248CAA230BE135", 
    "content-length": "0", 
    "server": "nginx/1.6.1"
}
```

