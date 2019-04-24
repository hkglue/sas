# DescribeWarningMachines {#doc_api_Sas_DescribeWarningMachines .reference}

查询指定基线检查服务器列表。

调用DescribeWarningMachines接口可查询基线检查机器列表

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Sas&api=DescribeWarningMachines)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeWarningMachines|系统规定参数。取值：DescribeWarningMachines。

 |
|RiskId|Long|是|1|风险项ID。

 |
|CurrentPage|Integer|否|1|当前页。

 |
|Lang|String|否|zh|请求内容的语言类型。

 -   zh：中文
-   en：英文

 |
|MachineName|String|否|基线测试服务器|服务器名称。

 |
|PageSize|Integer|否|10|每页条数。

 |
|SourceIp|String|否|127.0.0.1|来源IP。

 |
|StrategyId|Long|否|1|策略ID。

 |
|Uuids|String|否|xxx-aaa-bbb-ccc|服务器ID。多个ID用英文逗号分隔。

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Count|Integer|10|当前条数

 |
|CurrentPage|Integer|1|当前页

 |
|PageSize|Integer|10|每页条数

 |
|RequestId|String|00BD7CE2-284A-4534-BD09-FB69836DD750|请求id

 |
|TotalCount|Integer|100|总数

 |
|WarningMachines| | |产生告警的服务器的信息。

 |
|└HighWarningCount|Integer|10|高危检查项的个数。

 |
|└InternetIp|String|47.39.120.22|外网IP。

 |
|└IntranetIp|String|127.0.0.1|内网IP。

 |
|└LowWarningCount|Integer|3|低危检查项的个数。

 |
|└MachineName|String|基线测试服务器|服务器的名称。

 |
|└MediumWarningCount|Integer|2|中危检查项的个数。

 |
|└PassCount|Integer|10|通过检测的检查项个数。

 |
|└Status|Integer|1|检测执行的状态。

 -   1：已完成
-   2：验证中

 |
|└Uuid|String|xxx-aaa-bbb-ccc|用户ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeWarningMachines
&RiskId=1
&Lang=zh
&SourceIp=127.0.0.1
&MachineName=基线测试服务器
&Uuids=xxx-aaa-bbb-ccc
&StrategyId=1
&CurrentPage=1
&PageSize=20
&<公共请求参数>

```

正常返回示例

`JSON` 格式

``` {#json_return_success_demo}
{
	"Count":20,
	"TotalCount":47,
	"PageSize":20,
	"RequestId":"7E6F0031-6D83-4FEC-9077-FF87F9D9887C",
	"WarningMachines":[
		{
			"Uuid":"6b36bd63-1848-47dd-8b5a-************",
			"Status":1,
			"HighWarningCount":8,
			"LowWarningCount":0,
			"IntranetIp":"192.1.1.1",
			"InternetIp":"47.97.192.205",
			"MachineName":"测试",
			"MediumWarningCount":0,
			"PassCount":8
		},
		{
			"Uuid":"f03259d8-1e81-4fae-bcbb-************",
			"Status":1,
			"HighWarningCount":8,
			"LowWarningCount":0,
			"IntranetIp":"172.1.1.1",
			"InternetIp":"1.1.1.1",
			"MachineName":"health-check002",
			"MediumWarningCount":0,
			"PassCount":8
		},
		{
			"Uuid":"f87e146b-c704-4845-a187-05c37743a614",
			"Status":1,
			"HighWarningCount":8,
			"LowWarningCount":0,
			"IntranetIp":"172.1.1.1",
			"InternetIp":"1.1.1.1",
			"MachineName":"hht测试白名单数据准确性",
			"MediumWarningCount":0,
			"PassCount":8
		}
	],
	"CurrentPage":1
}
```

## 错误码 { .section}

[查看本产品错误码](https://error-center.aliyun.com/status/product/Sas)

