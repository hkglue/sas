# DescribeDomainCount {#doc_api_Sas_DescribeDomainCount .reference}

调用该接口获取域名资产数量。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Sas&api=DescribeDomainCount&type=RPC&version=2018-12-03)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeDomainCount|系统规定参数。取值：DescribeDomainCount。

 |
|SourceIp|String|否|127.1.1.1|指定的访问源IP地址。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|6FAFB857-FE24-4226-A09F-52EA5023C987|返回结果的请求ID。

 |
|RootDomainsCount|Integer|27|返回的根网站数量。

 |
|TotalDomainsCount|Integer|1|返回的所有网站数量。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeDomainCount
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeDomainCount>
	  <code>200</code>
	  <data>
		    <TotalDomainsCount>27</TotalDomainsCount>
		    <RootDomainsCount>1</RootDomainsCount>
	  </data>
	  <requestId>6FAFB857-FE24-4226-A09F-52EA5023C987</requestId>
	  <success>true</success>
    </DescribeDomainCount>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"requestId":"6FAFB857-FE24-4226-A09F-52EA5023C987",
	"data":{
		"TotalDomainsCount":27,
		"RootDomainsCount":1
	},
	"code":200,
	"success":true
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/Sas)查看更多错误码。

