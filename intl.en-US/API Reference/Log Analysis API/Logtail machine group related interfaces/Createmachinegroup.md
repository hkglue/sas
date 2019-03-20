# Createmachinegroup {#reference_xnh_b5q_12b .reference}

You can create a group of machines to collect logs and deliver configuration.

## Request syntax {#section_j5v_14t_12b .section}

```
POST /machinegroups HTTP/1.1
Authorization: <AuthorizationString> 
Content-Type:application/json
Content-Length:<Content Length>
Content-MD5<:<Content MD5>
Date: <GMT Date>
Host: <Project Endpoint>
x-log-apiversion: 0.6.0
x-log-signaturemethod: hmac-sha1
{
    "groupName" : "testgroup",
    "groupType" : "",
    "groupAttribute" : {
        "externalName" : "testgroup",
        "groupTopic": "testgrouptopic"
    },
    "machineIdentifyType" : "ip",
    "machineList" : [
        "test-ip1",
        "test-ip2"
    ]
}
```

## Request parameters {#section_mx5_b4t_12b .section}

Body parameters

|Parameter name|Type|Required|Description|
|:-------------|:---|:-------|:----------|
|groupName|string|Yes|The machine group name, which is unique in the same project.|
|groupType|string|No|The machine group type, which is empty by default.|
|machineIdentifyType|string|Yes|The machine identification type, including IP and user-defined identity.|
|groupAttribute|object|Yes|The machine group attribute, which is empty by default.|
|machineList|array|Yes|The specific machine identification, which can be an IP address or user-defined identity.|

groupAttribute description

|Attribute name|Type|Required|Description|
|:-------------|:---|:-------|:----------|
|groupTopic|string|No|The topic of a machine group, which is empty by default.|
|externalName|string|No|The external identification that the machine group depends, which is empty by default.|

**Request header**

The CreateMachineGroup API does not have a special request header. For more information about the public request headers of Log Service APIs, see [Public request header](intl.en-US/API Reference/Public request header.md).

**Response header**

The CreateMachineGroup API does not have a special response header. For more information about the public response headers of Log Service APIs, see [Public response header](intl.en-US/API Reference/Public response header.md).

**Response element**

The returned HTTP status code is 200.

**Error code**

Besides the [common error codes](intl.en-US/API Reference/Common error codes.md) of Log Service APIs, the CreateMachineGroup API may return the following special error codes.

|HTTP status code|ErrorCode|ErrorMessage|
|:---------------|:--------|:-----------|
|400|MachineGroupAlreadyExist|group \{GroupName\} already exists|
|400|InvalidParameter|invalid group resource json|
|500|InternalServerError|Internal server error|

## Example {#section_e5p_d4t_12b .section}

**Request example**

```
POST /machinegroups HTTP/1.1
Header :
{
    "x-log-apiversion": "0.6.0",
    "Authorization": "LOG <yourAccessKeyId>:<yourSignature>",
    "Host": "ali-test-project.cn-hangzhou-devcommon-intranet.sls.aliyuncs.com",
    "Date": "Tue, 10 Nov 2015 17:57:33 GMT",
    "Content-Length": "187",
    "x-log-signaturemethod": "hmac-sha1",
    "Content-MD5": "82033D507DEAAD72067BB58DFDCB590D",
    "User-Agent": "sls-java-sdk-v-0.6.0",
    "Content-Type": "application/json",
    "x-log-bodyrawsize": "0"
}
Body :
{
    "groupName": "test-machine-group",
    "groupType": "",
    "machineIdentifyType": "ip",
    "groupAttribute": {
        "groupTopic": "testtopic",
        "externalName": "testgroup"
    },
    "machineList": [
        \"127.0.0.1\
        \"127.0.0.2\"
    ]
}
```

**Response example**

```
HTTP/1.1 200 OK
Header :
{
    "Date": "Tue, 10 Nov 2015 17:57:33 GMT",
    "Content-Length": "0",
    "x-log-requestid": "5642300D99248CB76D005D36",
    "Connection": "close",
    "Server": "nginx/1.6.1"
}
```

