# ModifyRiskSingleResultStatus {#doc_api_Sas_ModifyRiskSingleResultStatus .reference}

修改检查项影响资产的状态。

调用ModifyRiskSingleResultStatus对检查项影响的资产进行操作：可忽略或标记为误报。

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Sas&api=ModifyRiskSingleResultStatus)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ModifyRiskSingleResultStatus|系统规定参数。取值：ModifyRiskSingleResultStatus。

 |
|Ids.N|RepeatList|否|1|影响资产id

 |
|SourceIp|String|否|1.1.1.1|请求源ip

 |
|Status|String|否|ignored|新状态

 |
|TaskId|Long|否|57|任务id

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|3B3F3A90-46A5-4023-A2D8-D68B14262F96|请求id

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=ModifyRiskSingleResultStatus
&Ids.1=4
&Status=ignored
&TaskId=57
&<公共请求参数>

```

正常返回示例

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"3B3F3A90-46A5-4023-A2D8-D68B14262F96"
}
```

## 错误码 { .section}

[查看本产品错误码](https://error-center.aliyun.com/status/product/Sas)

