# DeleteMachineGroup {#reference_sbw_b5q_12b .reference}

Delete a machine group and the Logtail configuration applied to this machine group.

Example:

```
DELETE /machinegroups/{groupName}
```

## Request syntax {#section_j5v_14t_12b .section}

```
DELETE /machinegroups/{groupName} HTTP/1.1
Authorization: <AuthorizationString> 
Date: <GMT Date>
Host: <Project Endpoint>
x-log-apiversion: 0.6.0
x-log-signaturemethod: hmac-sha1
```

## Request parameters {#section_mx5_b4t_12b .section}

URL parameters

|Parameter name|Type |Required|Description |
|:-------------|:----|:-------|:-----------|
|groupName|string |Yes |The machine group name.|

**Request header**

The DeleteMachineGroup API does not have a special request header. For more information about the public request headers of Log Service APIs, see [Public request header](intl.en-US/API Reference/Public request header.md).

**Response header**

The DeleteMachineGroup API does not have a special response header. For more information about the public response headers of Log Service APIs, see [Public response header](intl.en-US/API Reference/Public response header.md).

**Response element**

The returned HTTP status code is 200.

**Error Code**

Besides the common error codes of Log Service APIs, the DeleteMachineGroup API may return the following special error codes

|HTTP status code |ErrorCode|ErrorMessage|
|-----------------|---------|------------|
|404|GroupNotExist|group \{GroupName\} does not exist|
|500|InternalServerError|internal server error|

## Example  {#section_e5p_d4t_12b .section}

**Request example**

```
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

**Response example**

```
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

