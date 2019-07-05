# DescribeWarningMachines {#doc_api_Sas_DescribeWarningMachines .reference}

查询执行了基线检查策略的服务器的信息。

调用DescribeWarningMachines接口可查询执行了基线检查的服务器的信息，包含服务器的ID、服务器名称、检测到的风险项统计数据和风险项状态等信息。

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Sas&api=DescribeWarningMachines)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeWarningMachines|系统规定参数。取值：DescribeWarningMachines。

 |
|RiskId|Long|是|1|风险项ID。

 |
|CurrentPage|Integer|否|1|执行了基线检查的服务器的风险项页面。

 |
|Lang|String|否|zh|请求内容的语言类型。

 -   zh：中文
-   en：英文

 |
|MachineName|String|否|基线测试服务器|执行基线检查的服务器的名称。

 |
|PageSize|Integer|否|10|风险项页面中，每页包含的风险项条数。

 |
|SourceIp|String|否|127.0.0.1|来源IP。

 |
|StrategyId|Long|否|1|基线检查策略的ID。

 |
|Uuids|String|否|xxx-aaa-bbb-ccc|执行基线检查的服务器ID。多个ID用英文逗号分隔。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Count|Integer|10|当前条数

 |
|CurrentPage|Integer|1|基线检查风险项当前页的编号。

 |
|PageSize|Integer|10|基线检查风险项页面每页的条数。

 |
|RequestId|String|00BD7CE2-284A-4534-BD09-FB69836DD750|请求ID。

 |
|TotalCount|Integer|100|执行了基线检查的服务器所检测出的风险项总数。

 |
|WarningMachines| | |产生告警的服务器的信息。

 |
|HighWarningCount|Integer|10|高危检查项的个数。

 |
|InternetIp|String|47.39.120.22|外网IP。

 |
|IntranetIp|String|127.0.0.1|内网IP。

 |
|LowWarningCount|Integer|3|低危检查项的个数。

 |
|MachineName|String|基线测试服务器|服务器的名称。

 |
|MediumWarningCount|Integer|2|中危检查项的个数。

 |
|PassCount|Integer|10|通过检测的检查项个数。

 |
|Status|Integer|1|基线检查风险项修复完成后，风险项验证的状态。

 -   1：已完成
-   2：验证中

 |
|Uuid|String|xxx-aaa-bbb-ccc|用户ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeWarningMachines
&RiskId=1
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeWarningMachines>
  <TotalCount>47</TotalCount>
  <PageSize>20</PageSize>
  <RequestId>7E6F0031-6D83-4FEC-9077-FF87F9D9887C</RequestId>
  <CurrentPage>1</CurrentPage>
  <WarningMachines>
    <Status>1</Status>
    <MediumWarningCount>0</MediumWarningCount>
    <Uuid>6b36bd63-1848-47dd-8b5a-************</Uuid>
    <InternetIp>47.97.192.205</InternetIp>
    <MachineName>测试</MachineName>
    <HighWarningCount>8</HighWarningCount>
    <PassCount>8</PassCount>
    <IntranetIp>192.1.1.1</IntranetIp>
    <LowWarningCount>0</LowWarningCount>
  </WarningMachines>
  <WarningMachines>
    <Status>1</Status>
    <MediumWarningCount>0</MediumWarningCount>
    <Uuid>f03259d8-1e81-4fae-bcbb-************</Uuid>
    <InternetIp>1.1.1.1</InternetIp>
    <MachineName>health-check002</MachineName>
    <HighWarningCount>8</HighWarningCount>
    <PassCount>8</PassCount>
    <IntranetIp>172.1.1.1</IntranetIp>
    <LowWarningCount>0</LowWarningCount>
  </WarningMachines>
  <WarningMachines>
    <Status>1</Status>
    <MediumWarningCount>0</MediumWarningCount>
    <Uuid>f87e146b-c704-4845-a187-05c37743a614</Uuid>
    <InternetIp>1.1.1.1</InternetIp>
    <MachineName>hht测试白名单数据准确性</MachineName>
    <HighWarningCount>8</HighWarningCount>
    <PassCount>8</PassCount>
    <IntranetIp>172.1.1.1</IntranetIp>
    <LowWarningCount>0</LowWarningCount>
  </WarningMachines>
  <Count>20</Count>
</DescribeWarningMachines>

```

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

访问[错误中心](https://error-center.alibabacloud.com/status/product/Sas)查看更多错误码。

