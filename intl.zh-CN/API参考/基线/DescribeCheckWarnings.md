# DescribeCheckWarnings {#doc_api_Sas_DescribeCheckWarnings .reference}

查询指定风险项和指定服务器下的检查项列表。

调用DescribeCheckWarnings接口可查询指定风险项信息和指定的服务器下的检查项列表。

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Sas&api=DescribeCheckWarnings)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeCheckWarnings|系统规定参数。取值：DescribeCheckWarnings。

 |
|RiskId|Long|是|1|风险项ID。

 |
|Uuid|String|是|d42f938c-d962-48a0-90f9-05\*\*\*\*\*\*\*\*\*\*|机器id

 |
|CurrentPage|Integer|否|1|分页页码。

 起始值为1，表示第1个分页。默认值为1，表示默认展示第1个分页。

 |
|Lang|String|否|zh|语言。

 -   zh：中文
-   en：英文

 |
|PageSize|Integer|否|20|分页的数量。

 默认值为20，代表系统默认创建20个分页。

 |
|SourceIp|String|否|127.0.0.1|来源ID。

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|CheckWarnings| | |检查项列表。

 |
|└CheckId|Long|1|检查项ID。

 |
|└CheckWarningId|Long|10|告警数据ID。

 |
|└Item|String|密码到期警告|检查项名称。

 |
|└Level|String|high|检查项级别。

 |
|└Status|Integer|1|检查项状态。

 -   1：未通过
-   2：验证中
-   3：已通过
-   5：已失效
-   6：已忽略

 |
|└Type|String|身份鉴别|检查项类型。

 |
|└Uuid|String|d42f938c-d962-48a0-90f9-\*\*\*\*\*\*\*\*\*\*\*|服务器ID。

 |
|Count|Integer|10|当前条数。

 |
|CurrentPage|Integer|1|分页页码。

 |
|PageSize|Integer|20|分页的数量。

 |
|RequestId|String|0DFCADBA-7065-42DA-AF17-6868B9C2A8CF|请求ID。

 |
|TotalCount|Integer|100|总数。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeCheckWarnings
&RiskId=1
&Uuid=d42f938c-d962-48a0-90f9-05e4eaf92e34
&Lang=zh
&SourceIp=127.0.0.1
&CurrentPage=1
&PageSize=20
&<公共请求参数>

```

正常返回示例

`JSON` 格式

``` {#json_return_success_demo}
{
	"Count":16,
	"TotalCount":16,
	"PageSize":20,
	"RequestId":"C1E6C4FE-DE00-4B75-A01E-FCAB55A36449",
	"CurrentPage":1,
	"CheckWarnings":[
		{
			"Uuid":"974af549-3248-44dd-9180-************",
			"Status":6,
			"CheckWarningId":1393768,
			"Item":"检查系统空密码账户\r\n                                \r\n                            ",
			"Type":"身份鉴别",
			"Level":"high",
			"CheckId":1
		},
		{
			"Uuid":"974af549-3248-44dd-9180-************",
			"Status":6,
			"CheckWarningId":1393774,
			"Item":"密码复杂度检查",
			"Type":"身份鉴别",
			"Level":"high",
			"CheckId":52
		},
		{
			"Uuid":"974af549-3248-44dd-9180-1bd7c9f60bd5",
			"Status":6,
			"CheckWarningId":1393773,
			"Item":"确保root是唯一的UID为0的帐户",
			"Type":"身份鉴别",
			"Level":"high",
			"CheckId":15
		},
		{
			"Uuid":"974af549-3248-44dd-9180-1bd7c9f60bd5",
			"Status":6,
			"CheckWarningId":1393772,
			"Item":"开启地址空间布局随机化",
			"Type":"入侵防范",
			"Level":"high",
			"CheckId":14
		},
		{
			"Uuid":"974af549-3248-44dd-9180-1bd7c9f60bd5",
			"Status":6,
			"CheckWarningId":1393767,
			"Item":"设置用户权限配置文件的权限",
			"Type":"文件权限",
			"Level":"high",
			"CheckId":13
		},
		{
			"Uuid":"974af549-3248-44dd-9180-1bd7c9f60bd5",
			"Status":6,
			"CheckWarningId":1393771,
			"Item":"访问控制配置文件的权限设置",
			"Type":"文件权限",
			"Level":"high",
			"CheckId":12
		},
		{
			"Uuid":"974af549-3248-44dd-9180-1bd7c9f60bd5",
			"Status":6,
			"CheckWarningId":1393766,
			"Item":"确保SSH LogLevel设置为INFO",
			"Type":"服务配置",
			"Level":"high",
			"CheckId":11
		},
		{
			"Uuid":"974af549-3248-44dd-9180-1bd7c9f60bd5",
			"Status":6,
			"CheckWarningId":1393770,
			"Item":"确保rsyslog服务已启用",
			"Type":"安全审计",
			"Level":"high",
			"CheckId":10
		},
		{
			"Uuid":"974af549-3248-44dd-9180-1bd7c9f60bd5",
			"Status":6,
			"CheckWarningId":1393765,
			"Item":"设置SSH空闲超时退出时间",
			"Type":"服务配置",
			"Level":"high",
			"CheckId":8
		},
		{
			"Uuid":"974af549-3248-44dd-9180-1bd7c9f60bd5",
			"Status":6,
			"CheckWarningId":1393764,
			"Item":"SSHD强制使用V2安全协议",
			"Type":"服务配置",
			"Level":"high",
			"CheckId":7
		},
		{
			"Uuid":"974af549-3248-44dd-9180-1bd7c9f60bd5",
			"Status":6,
			"CheckWarningId":1393763,
			"Item":"确保SSH MaxAuthTries设置为3到6之间",
			"Type":"服务配置",
			"Level":"high",
			"CheckId":6
		},
		{
			"Uuid":"974af549-3248-44dd-9180-1bd7c9f60bd5",
			"Status":6,
			"CheckWarningId":1393769,
			"Item":"确保密码到期警告天数为7或更多",
			"Type":"身份鉴别",
			"Level":"high",
			"CheckId":5
		},
		{
			"Uuid":"974af549-3248-44dd-9180-1bd7c9f60bd5",
			"Status":6,
			"CheckWarningId":1393761,
			"Item":"设置密码修改最小间隔时间",
			"Type":"身份鉴别",
			"Level":"high",
			"CheckId":4
		},
		{
			"Uuid":"974af549-3248-44dd-9180-1bd7c9f60bd5",
			"Status":6,
			"CheckWarningId":1393760,
			"Item":"设置密码失效时间",
			"Type":"身份鉴别",
			"Level":"high",
			"CheckId":3
		},
		{
			"Uuid":"974af549-3248-44dd-9180-1bd7c9f60bd5",
			"Status":6,
			"CheckWarningId":1393762,
			"Item":"禁止SSH空密码用户登录                                \r\n                            \r\n                                \r\n                            ",
			"Type":"服务配置",
			"Level":"high",
			"CheckId":2
		},
		{
			"Uuid":"974af549-3248-44dd-9180-1bd7c9f60bd5",
			"Status":6,
			"CheckWarningId":1393775,
			"Item":"检查密码重用是否受限制",
			"Type":"身份鉴别",
			"Level":"high",
			"CheckId":58
		}
	]
}
```

## 错误码 { .section}

[查看本产品错误码](https://error-center.aliyun.com/status/product/Sas)

