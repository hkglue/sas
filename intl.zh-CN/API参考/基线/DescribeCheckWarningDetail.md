# DescribeCheckWarningDetail {#doc_api_Sas_DescribeCheckWarningDetail .reference}

查询指定检查项明细信息。

调用DescribeCheckWarningDetail接口可查询指定检查项的明细信息。

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Sas&api=DescribeCheckWarningDetail)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeCheckWarningDetail|系统规定参数。

 取值：DescribeCheckWarningDetail

 |
|CheckWarningId|Long|是|1|检查项告警ID。

 |
|Lang|String|否|zh|请求的语言类型。

 -   zh：中文
-   en：英文

 |
|SourceIp|String|否|127.0.0.1|来源IP。

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Advice|String|立即修复|基线检查结果的建议。

 |
|CheckId|Long|1|检查项ID。

 |
|Description|String|密码即将过期|描述。

 |
|Item|String|密码到期警告|检查项名称。

 |
|Level|String|high|风险等级。

 |
|Prompt|String|密码到期警告|检测提示。

 |
|RequestId|String|09969D2C-4FAD-429E-BFBF-9A60DEF8BF6F|请求ID。

 |
|Type|String|身份鉴别|基线检查项的类型。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeCheckWarningDetail
&CheckWarningId=1
&SourceIp=127.0.0.1
&Lang=zh
&<公共请求参数>

```

正常返回示例

`JSON` 格式

``` {#json_return_success_demo}
{
	"Prompt":"",
	"Description":"设置用户权限配置文件的权限",
	"Item":"设置用户权限配置文件的权限",
	"Type":"文件权限",
	"RequestId":"9F2361B3-B7C3-4189-8DB5-C6D1F67BC225",
	"Advice":"执行以下5条命令\r\nchown root:root /etc/passwd /etc/shadow /etc/group /etc/gshadow\r\nchmod 0644 /etc/group  \r\nchmod 0644 /etc/passwd  \r\nchmod 0400 /etc/shadow  \r\nchmod 0400 /etc/gshadow  ",
	"Level":"high",
	"CheckId":13
}
```

## 错误码 { .section}

[查看本产品错误码](https://error-center.aliyun.com/status/product/Sas)

