# UpdateIndex {#reference_cmx_pdh_f2b .reference}

更新指定Logstore的索引。

示例：

``` {#codeblock_c8u_ruy_q22}
PUT /logstores/{logstoreName}/index
```

## 请求语法 {#section_qwn_nch_f2b .section}

``` {#codeblock_ncn_ya6_nfd}
PUT /logstores/<logstoreName>/index HTTP/1.1
Authorization: <AuthorizationString>
x-log-bodyrawsize: 0
User-Agent: <UserAgent>
x-log-apiversion: 0.6.0
Host: <Project Endpoint>
x-log-signaturemethod: hmac-sha1
Date: <GMT Date>
Content-Type: application/json
Content-MD5: <Content-MD5>
Content-Length: <ContentLength>
{
  "line": <full text index>,
  "keys": <key-value index>,
}
```

## 请求参数 {#section_m3m_vch_f2b .section}

|属性名称|类型|是否必须|描述|
|:---|:-|:---|:-|
|logstoreName|string|是|Logstore 的名称。|
|keys|object|否|字段索引配置，key为字段名称，value为字段索引配置。|
|line|object|否|全文索引配置。|

属性keys和line必须至少指定一个。全文索引配置包含如下属性：

|属性名称|类型|是否必须|描述|
|:---|:-|:---|:-|
|token|array|是|分词符列表。|
|caseSensitive|bool|否|是否大小写敏感。|
|chn|bool|否|是否包含中文。|
|include\_keys|array|否|包含的字段列表，不能与exclude\_keys同时指定。|
|exclude\_keys|array|否|排除的字段列表，不能与include\_keys同时指定。|

字段索引配置包含如下属性：

|属性名称|类型|是否必须|描述|
|:---|:-|:---|:-|
|type|string|是|字段类型。|
|alias|string|否|别名。|
|chn|bool|否|是否包含中文，只有type为text时才有意义。|
|token|array|否，当type为text时必须|分词符列表，只有type为text时才有意义。|
|caseSensitive|bool|否|是否大小写敏感，只有type为text时有意义。|
|doc\_value|bool|否|是否开启统计。|

 **请求头** 

UpdateIndex 接口无特有请求头，关于 Log Service API 的公共请求头，请参考 [公共请求头](intl.zh-CN/API 参考/公共请求头.md)。

 **响应头** 

UpdateIndex 接口无特有响应头，关于 Log Service API 的公共响应头，请参考[公共响应头](intl.zh-CN/API 参考/公共响应头.md)。

 **响应元素** 

HTTP 状态码返回 200。

 **错误码** 

除了返回 Log Service API 的[通用错误码](intl.zh-CN/API 参考/通用错误码.md)，还可能返回如下特有错误码：

|HTTP状态码|ErrorCode|ErrorMessage|
|:------|:--------|:-----------|
|400|ParameterInvalid|log store index is not created|
|400|ParameterInvalid|key config must has type|
|400|IndexInfoInvalid|required field token is lacking or of error format|
|400|IndexInfoInvalid|required fields line/keys are lacking or of error format|
|404|ProjectNotExist|The Project does not exist : \{Project\}|
|404|LogStoreNotExist|logstore \{logstoreName\} dose not exist|
|500|InternalServerError|Specified Server Error Message|

## 示例 {#section_t3z_rfh_f2b .section}

-   请求示例

    ``` {#codeblock_zb7_bgf_e7j}
    PUT /logstores/logstore-4/index HTTP/1.1
    Header:
    Authorization: LOG <yourAccessKeyId>:<yourSignature>
    x-log-bodyrawsize: 0
    User-Agent: sls-java-sdk-v-0.6.1
    x-log-apiversion: 0.6.0
    Host: my-project.cn-shanghai.log.aliyuncs.com
    x-log-signaturemethod: hmac-sha1
    Date: Mon, 07 May 2018 09:47:20 GMT
    Content-Type: application/json
    Content-MD5: 1860B805A6AA5288B97B32CF3B519112
    Content-Length: 316
    Connection: Keep-Alive
    Body:
    {
      "line": {
        "token": [
          ",",
          " ",
          "'",
          "\"",
          ";",
          "=",
          "(",
          ")",
          "[",
          "]",
          "{",
          "}",
          "?",
          "@",
          "&",
          "<",
          ">",
          "/",
          ":",
          "\n",
          "\t",
          "\r"
        ]
      },
      "keys": {
        "agent": {
          "doc_value": true,
          "caseSensitive": true,
          "alias": "agent_alias",
          "type": "text",
          "token": [
            ",",
            " ",
            "'",
            "\"",
            ";",
            "=",
            "(",
            ")",
            "[",
            "]",
            "{",
            "}",
            "?",
            "@",
            "&",
            "<",
            ">",
            "/",
            ":",
            "\n",
            "\t",
            "\r"
          ]
        }
      }
    }
    ```

-   响应示例

    ``` {#codeblock_r0f_qeb_dat}
    HTTP/1.1 200
    Server: nginx/1.12.1
    Content-Length: 0
    Connection: close
    Access-Control-Allow-Origin: *
    Date: Mon, 07 May 2018 09:47:21 GMT
    x-log-requestid: 5AF020A98CBAA2EF52AB66C9
    ```


