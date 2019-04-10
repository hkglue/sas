# DescribeEmgVulGroup {#doc_api_Sas_DescribeEmgVulGroup .reference}

分组查询应急漏洞。

调用DescribeEmgVulGroup分组查询应急漏洞。

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Sas&api=DescribeEmgVulGroup)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeEmgVulGroup|需要执行的操作。

 取值：DescribeEmgVulGroup

 |
|Lang|String|否|zh|语言。

 取值：

 -   zh：中文
-   en：英文

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|EmgVulGroupList| | |应急漏洞分组列表。

 |
|└AliasName|String|Jenkins 远程高危安全漏洞\(CVE-2018-1999001和CVE-2018-1999002\)|漏洞别名。

 |
|└Description|String|Jenkins是一个开源软件项目，是基于Java开发的一种持续集成工具，用于监控持续重复的工作，旨在提供一个开放易用的软件平台，使软件的持续集成变成可能。\\n\\nJenkins存在任意文件读取漏洞，攻击者在远程且未经授权的情况下，可以通过构造恶意的HTTP 请求发往Jenkins Web服务端，从请求响应中直接获取攻击者指定读取的文件内容。|漏洞描述。

 |
|└GmtPublish|Long|1532592480000|漏洞发布时间，时间戳。

 |
|└Name|String|scan:ACSV-2018-072601|漏洞名称。

 |
|└PendingCount|Integer|0|待处理漏洞数。

 |
|└Type|String|scan|应急类型。

 -   scan：扫描插件
-   python：扫描脚本

 |
|RequestId|String|E836EDA2-DBFB-489E-8FD3-5B141EB81A9C|请求ID。

 |
|TotalCount|Integer|2|漏洞总数。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeEmgVulGroup
&<公共请求参数>

```

正常返回示例

`JSON` 格式

``` {#json_return_success_demo}
{
	"TotalCount":2,
	"EmgVulGroupList":[
		{
			"Name":"scan:ACSV-2018-072601",
			"Status":30,
			"Description":"Jenkins是一个开源软件项目，是基于Java开发的一种持续集成工具，用于监控持续重复的工作，旨在提供一个开放易用的软件平台，使软件的持续集成变成可能。\n\nJenkins存在任意文件读取漏洞，攻击者在远程且未经授权的情况下，可以通过构造恶意的HTTP 请求发往Jenkins Web服务端，从请求响应中直接获取攻击者指定读取的文件内容。",
			"PendingCount":0,
			"AliasName":"Jenkins 远程高危安全漏洞(CVE-2018-1999001和CVE-2018-1999002)",
			"Type":"scan",
			"GmtPublish":1532592480000
		},
		{
			"Name":"scan:acsv-2018-082001",
			"Status":30,
			"Description":"近日，有安全研究人员披露Metinfo多个高危安全漏洞，包括任意文件读取，XXE，敏感信息泄露等危害严重的漏洞。",
			"PendingCount":0,
			"AliasName":"Metinfo 多个高危漏洞",
			"Type":"scan",
			"GmtPublish":1534767031000
		}
	],
	"RequestId":"E836EDA2-DBFB-489E-8FD3-5B141EB81A9C"
}
```

## 错误码 { .section}

[查看本产品错误码](https://error-center.aliyun.com/status/product/Sas)

