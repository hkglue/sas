# ListMachineGroup {#reference_nkz_c5q_12b .reference}

View the list of machine group names.

Example:

```
GET /machinegroups? offset=1&size=100
```

## Request syntax {#section_j5v_14t_12b .section}

```
GET /machinegroups? offset=1&size=100 HTTP/1.1
Authorization: <AuthorizationString> 
Date: <GMT Date>
Host: <Project Endpoint>
x-log-apiversion: 0.6.0
x-log-signaturemethod: hmac-sha1
```

## Request Parameters {#section_mx5_b4t_12b .section}

URL parameters:

|Parameter Name|Type|Required|Description|
|:-------------|:---|:-------|:----------|
|offset|int|No|The starting position of the returned records. The default value is 0.|
|size|int|No|The maximum number of entries returned on each page. The default value is 500 \(maximum\).|
|groupName|string|No|The group machine name used for filtering \(partial matching is supported\).|

**Request Header**

The ListMachineGroup API does not have a special request header.  For more information about the public request headers of Log Service APIs, see [Public request header](intl.en-US/API Reference/Public request header.md).

**Response header**

The ListMachineGroup API does not have a special response header.  For more information about the public response headers of Log Service APIs, see [Public response header](intl.en-US/API Reference/Public response header.md).

**Response element**

After the successful request, the response body contains a list of all machine groups in a specific project. The specific formats are as follows. Name The specific formats are as follows.

|Name|Type|Description|
|:---|:---|:----------|
|count|int|Number of machineggroup returned|
|total|int|The total number of returned machine groups.|
|machinegroups|json array|The name list of returned machine groups.|

```
{
    "machinegroups": [
        "test-machine-group",
        "test-machine-group-2"
    ],
    "count": 2,
    "total": 2
}
```

**Error code**

Besides the common error codes of Log Service APIs, the ListMachineGroup API  may return the following [special error codes](intl.en-US/API Reference/Common error codes.md).

|HTTP status code|ErrorCode|ErrorMessage|
|:---------------|:--------|:-----------|
|500|InternalServerError|internal server error|

## Example {#section_e5p_d4t_12b .section}

**Request example:**

```
GET /machinegroups? groupName=test-machine-group&offset=0&size=3 HTTP/1.1
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

**Response example:**

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
    "machinegroups": [
        "test-machine-group",
        "test-machine-group-2"
    ],
    "count": 2,
    "total": 2
}
```

