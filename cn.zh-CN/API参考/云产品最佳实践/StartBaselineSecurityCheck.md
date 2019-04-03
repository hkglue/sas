# StartBaselineSecurityCheck {#doc_api_Sas_StartBaselineSecurityCheck .reference}

调用本接口执行检测任务。

执行检测任务，进行全量检测或对某个检查项进行检测或验证。

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Sas&api=StartBaselineSecurityCheck)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|StartBaselineSecurityCheck|要执行的操作。

 取值：StartBaselineSecurityCheck。

 |
|SourceIp|String|否|1.1.1.1|访问者源IP。

 |
|Lang|String|否|cn|调用参数返回的内容的语言种类。支持中文（CN）和英文（EN）。

 |
|ItemIds.N|RepeatList|否|1|检查项ID。

 |
|Assets.N|RepeatList|否|1|资产ID。

 |
|Type|String|否|check|任务类型。

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|48D2E9A9-A1B0-4295-B727-0995757C47E9|请求id

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=StartBaselineSecurityCheck
&Type=check
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<StartBaselineSecurityCheckResponse>
  <RequestId>48D2E9A9-A1B0-4295-B727-0995757C47E9</RequestId>
</StartBaselineSecurityCheckResponse>

```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"48D2E9A9-A1B0-4295-B727-0995757C47E9"
}
```

## 错误码 { .section}

[查看本产品错误码](https://error-center.aliyun.com/status/product/Sas)

