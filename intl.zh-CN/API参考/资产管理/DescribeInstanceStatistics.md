# DescribeInstanceStatistics {#doc_api_Sas_DescribeInstanceStatistics .reference}

调用该接口获取机器的统计信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Sas&api=DescribeInstanceStatistics&type=RPC&version=2018-12-03)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeInstanceStatistics|系统规定参数。取值：DescribeInstanceStatistics。

 |
|From|String|是|sas|指定数据请求来源。固定为sas。

 |
|Uuid|String|是|\["ff675afd-703e-40dc-809b-0fad8b0ded28"\]|指定待查询的机器列表。

 |
|Lang|String|否|zh|指定返回结果语言环境。

 -   **zh**：中文
-   **en**：英文

 |
|SourceIp|String|否|127.1.1.1|指定访问源IP地址。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Data| | |返回机器的检测结果项列表。

 |
|Account|Integer|1|返回结果中的分组类型。

 -   **0**：默认分组
-   **1**：其他分组

 |
|AppNum|Integer|0|返回结果中的应用漏洞数量。

 |
|CmsNum|Integer|2|返回结果中的Web-CMS漏洞数量。

 |
|CveNum|Integer|1|返回结果中的通用漏洞数量。

 |
|EmgNum|Integer|0|返回结果中的应急漏洞数量。

 |
|Health|Integer|1|返回结果中的基线检查问题数量。

 |
|Suspicious|Integer|2|返回结果中的安全告警数量。

 |
|SysNum|Integer|1|返回结果中的系统漏洞数量。

 |
|Trojan|Integer|1|返回结果中的木马数量。

 |
|Uuid|String|xxx|返回结果中的机器UUID。

 |
|Vul|Integer|4|返回结果中所有漏洞数量总和：CveNum+EmgNum+SysNum+CmsNum+AppNum。

 |
|RequestId|String|"requestId": "7E0618A9-D5EF-4220-9471-C42B5E92719F",|返回结果的请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeInstanceStatistics
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeInstanceStatistics>
	  <code>200</code>
	  <requestId>7E0618A9-D5EF-4220-9471-C42B5E92719F</requestId>
	  <success>true</success>
	  <data>
		    <EntEntityListity>
			      <Uuid>xxx</Uuid>
			      <Health>1</Health>
			      <Suspicious>2</Suspicious>
			      <Vul>3</Vul>
		    </EntEntityListity>
	  </data>
    </DescribeInstanceStatistics>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"requestId":"7E0618A9-D5EF-4220-9471-C42B5E92719F",
	"data":{
		"EntEntityListity":[
			{
				"Uuid":"xxx",
				"Suspicious":2,
				"Health":1,
				"Vul":3
			}
		]
	},
	"code":200,
	"success":true
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/Sas)查看更多错误码。

