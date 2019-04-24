# DescribeStratety {#doc_api_Sas_DescribeStratety .reference}

获取基线设置详情。

调用DescribeStratety接口可获取基线扫描策略的设置详情。

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Sas&api=DescribeStratety)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeStratety|系统规定参数。

 取值：DescribeStratety

 |
|Lang|String|否|zh|语言。

 |
|SourceIp|String|否|127.0.0.1|来源。

 |
|StrategyIds|String|否|1,2,3|指定策略ID，多个用逗号分隔。

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|16B9826C-B99F-4F8A-8048-EA81D6D3DE8B|请求ID。

 |
|Strategies| | |策略列表。

 |
|└ConfigTargets| | |关联分组。

 |
|└Flag|String|add|关联标识

 |
|└Target|String|3259405|关联分组id

 |
|└TargetType|String|groupId|关联类型

 |
|└CycleDays|Integer|1|检测周期。

 |
|└CycleStartTime|Integer|6|检测开始时间，可在0:00、06:00、12:00、18:00四个时间点开始执行基线检测。

 |
|└EcsCount|Integer|5|执行基线检测的服务器数量。

 |
|└ExecStatus|Integer|1|执行状态。

 -   1：未执行
-   2：执行中

 |
|└Id|Integer|212635|策略ID。

 |
|└Name|String|测试|策略名称。

 |
|└PassRate|Integer|80|上一次检测通过率。

 |
|└ProcessRate|Integer|80|检测进度。

 |
|└RiskCount|Integer|5|基线个数。

 |
|└Type|Integer|1|策略的类型。

 -   1：默认策略
-   2：用户添加的策略

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeStratety
?Lang=zh
&SourceIp=127.0.0.1
&StrategyIds=1,2,3
&<公共请求参数>

```

正常返回示例

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"ACAFE09B-3346-433B-BDA8-369AB3D9B4F9",
	"Strategies":[
		{
			"Name":"test",
			"RiskCount":1,
			"CycleDays":3,
			"Type":2,
			"CycleStartTime":6,
			"ConfigTargets":[
				{
					"Flag":"add",
					"Target":"4361221",
					"TargetType":"groupId"
				}
			],
			"ProcessRate":0,
			"Id":15161,
			"ExecStatus":1,
			"EcsCount":0
		},
		{
			"Name":"默认策略",
			"RiskCount":13,
			"PassRate":81,
			"CycleDays":1,
			"Type":1,
			"CycleStartTime":0,
			"ConfigTargets":[
				{
					"Flag":"del",
					"Target":"281801",
					"TargetType":"groupId"
				},
				{
					"Flag":"del",
					"Target":"4790960",
					"TargetType":"groupId"
				}
			],
			"ProcessRate":0,
			"Id":20,
			"ExecStatus":1,
			"EcsCount":17
		}
	]
}
```

## 错误码 { .section}

[查看本产品错误码](https://error-center.aliyun.com/status/product/Sas)

