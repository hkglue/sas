# ModifyRiskCheckStatus {#doc_api_Sas_ModifyRiskCheckStatus .reference}

修改检查项的检测结果状态。

调用ModifyRiskCheckStatus可修改检查项检测结果状态，进行忽略或标记误报。

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Sas&api=ModifyRiskCheckStatus)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ModifyRiskCheckStatus|系统规定参数。取值：ModifyRiskCheckStatus。

 |
|ItemId|Long|否|1|检查项id

 |
|Lang|String|否|cn|语种

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
|RequestId|String|48D2E9A9-A1B0-4295-B727-0995757C47E9|请求id

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=ModifyRiskCheckStatus
&ItemId=1
&TaskId=57
&Status=ignored
&<公共请求参数>

```

正常返回示例

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"48D2E9A9-A1B0-4295-B727-0995757C47E9"
}
```

## 错误码 { .section}

[查看本产品错误码](https://error-center.aliyun.com/status/product/Sas)

