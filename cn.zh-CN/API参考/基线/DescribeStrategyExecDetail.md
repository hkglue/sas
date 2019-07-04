# DescribeStrategyExecDetail {#doc_api_Sas_DescribeStrategyExecDetail .reference}

查询最近一次基线检查的结果详情。

调用DescribeStrategyExecDetail接口可查询某个基线检测策略执行最近一次检查的结果详情，包括最近一次执行检查的时间、

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Sas&api=DescribeStrategyExecDetail)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeStrategyExecDetail|需要执行的操作。

 取值：DescribeStrategyExecDetail

 |
|StrategyId|Integer|是|1|基线检测策略ID。

 |
|SourceIp|String|否|127.0.0.1|来源IP。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|EndTime|String|2019-01-08 20:11:20|基线检查执行结束时间。

 |
|FailCount|Integer|94|基线检查未通过的风险项数量。

 |
|FailedEcsList| | |检测出基线风险项的服务器列表。

 |
|IP|String|1.1.1.1|执行基线检查的服务器实例IP地址。

 |
|InstanceName|String|测试-20180703|实例名。

 |
|IntranetIp|String|1.1.1.1|内网IP。

 |
|Reason|String|Detect timeout|基线检查未通过的原因。

 |
|InProcessCount|Integer|0|状态为执行中的基线检查任务的个数。

 |
|Percent|String|100%|执行进度。

 |
|RequestId|String|09322632-4668-4AD9-BD0D-32757DEFBBA6|请求ID。

 |
|Source|String|Manual|执行来源。

 |
|StartTime|String|2019-01-08 19:41:12|开始时间。

 |
|SuccessCount|Integer|81|基线检查状态为**已通过**的风险项数量。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeStrategyExecDetail
&StrategyId=1
&<公共请求参数>

```

正常返回示例

`JSON` 格式

``` {#json_return_success_demo}
{
	"Source":"Schedule",
	"InProcessCount":0,
	"SuccessCount":1,
	"RequestId":"6489FA6A-D241-4380-9D8C-A8804484CA40",
	"Percent":"100%",
	"FailedEcsList":[
		{
			"IntranetIp":"172.1.1.1",
			"IP":"1.1.1.1",
			"InstanceName":"health-check002",
			"Reason":"Agent offline"
		}
	],
	"EndTime":"2019-04-10 00:58:30",
	"StartTime":"2019-04-10 00:19:01",
	"FailCount":1
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/Sas)查看更多错误码。

