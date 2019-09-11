# DeleteMachineGroup {#reference_sbw_b5q_12b .reference}

删除机器组，如果机器组上有配置，则 Logtail 上对应的配置也会被删除。

示例：

``` {#codeblock_fy4_a4j_kcs}
DELETE /machinegroups/{groupName}
```

## 请求语法 {#section_j5v_14t_12b .section}

``` {#codeblock_hf7_iuo_500}
DELETE /machinegroups/{groupName} HTTP/1.1
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
|groupName|string|是|机器分组名称|

 **请求头** 

DeleteMachineGroup接口无特有请求头。关于 Log Service API 的公共请求头，请参考 [公共请求头](intl.zh-CN/API 参考/公共请求头.md)。

 **响应头** 

DeleteMachineGroup接口无特有响应头。关于 Log Service API 的公共响应头，请参考 [公共响应头](intl.zh-CN/API 参考/公共响应头.md)。

 **响应元素** 

HTTP 状态码返回 200。

 **错误码** 

除了返回 Log Service API 的 [通用错误码](intl.zh-CN/API 参考/通用错误码.md)，还可能返回如下特有错误码：

|HTTP 状态码|ErrorCode|ErrorMessage|
|--------|---------|------------|
|404|GroupNotExist|group \{GroupName\} does not exist|
|500|InternalServerError|internal server error|

## 示例 {#section_e5p_d4t_12b .section}

**请求示例：** 

``` {#codeblock_oi5_kbf_485}
DELETE /machinegroups/test-machine-group-4 HTTP/1.1
Header :
{
    "x-log-apiversion": "0.6.0",
    "Authorization": "LOG <yourAccessKeyId>:<yourSignature>",
    "Host": "ali-test-project.cn-hangzhou-devcommon-intranet.sls.aliyuncs.com",
    "Date": "Tue, 10 Nov 2015 19:13:28 GMT",
    "Content-Length": "0",
    "x-log-signaturemethod": "hmac-sha1",
    "User-Agent": "sls-java-sdk-v-0.6.0",
    "Content-Type": "application/x-protobuf",
    "x-log-bodyrawsize": "0"
}
```

 **响应示例：** 

``` {#codeblock_avo_n1z_5dr}
HTTP/1.1 200 OK
Header :
{
    "Date": "Tue, 10 Nov 2015 19:13:28 GMT",
    "Content-Length": "0",
    "x-log-requestid": "564241D899248C827B000CFE",
    "Connection": "close",
    "Server": "nginx/1.6.1"
}
```

