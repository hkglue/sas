# DescribeSecurityCheckScheduleConfig {#doc_api_Sas_DescribeSecurityCheckScheduleConfig .reference}

查看用户自定义设置的检测周期以及时间段。

调用DescribeSecurityCheckScheduleConfig查看用户自定义设置的检测周期以及时间段。

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Sas&api=DescribeSecurityCheckScheduleConfig)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeSecurityCheckScheduleConfig|系统规定参数。取值：DescribeSecurityCheckScheduleConfig。

 |
|Lang|String|否|cn|语种

 |
|SourceIp|String|否|1.1.1.1|请求源ip

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|48D2E9A9-A1B0-4295-B727-0995757C47E9|请求id

 |
|RiskCheckJobConfig| | |周期检测任务设置

 |
|└DaysOfWeek|String|1，2，3|每周检测时间

 |
|└EndTime|Integer|12|结束时间

 |
|└StartTime|Integer|6|开始时间

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeSecurityCheckScheduleConfig
&<公共请求参数>

```

正常返回示例

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"C17F3C01-0AFD-4898-A950-AA0129025B41",
	"RiskCheckJobConfig":{
		"DaysOfWeek":"1,2,3",
		"EndTime":12,
		"StartTime":6
	}
}
```

## 错误码 { .section}

[查看本产品错误码](https://error-center.aliyun.com/status/product/Sas)

