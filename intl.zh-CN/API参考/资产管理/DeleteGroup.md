# DeleteGroup {#doc_api_Sas_DeleteGroup .reference}

调用该接口删除服务器分组。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Sas&api=DeleteGroup&type=RPC&version=2018-12-03)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteGroup|系统规定参数。取值：DeleteGroup。

 |
|GroupId|Long|是|11111|指定待删除的服务器分组ID。

 |
|SourceIp|String|否|127.1.1.1|指定访问源IP地址。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|11111|返回结果的请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DeleteGroup
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DeleteGroup>
	  <code>200</code>
	  <requestId>7E0618A9-D5EF-4220-9471-C42B5E92719F</requestId>
	  <success>true</success>
    </DeleteGroup>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"requestId":"7E0618A9-D5EF-4220-9471-C42B5E92719F",
	"code":200,
	"success":true
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/Sas)查看更多错误码。

