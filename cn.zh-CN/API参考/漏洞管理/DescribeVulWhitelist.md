# DescribeVulWhitelist {#doc_api_Sas_DescribeVulWhitelist .reference}

分页获取漏洞白名单。

调用DescribeVulWhitelist分页获取漏洞白名单

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Sas&api=DescribeVulWhitelist)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeVulWhitelist|需要执行的操作。

 取值：DescribeVulWhitelist

 |
|CurrentPage|Integer|否|1|分页页码。

 起始值：1

 默认值：1

 |
|PageSize|Integer|否|10|分页大小。

 默认值：20

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|CurrentPage|Integer|1|分页页码。

 |
|PageSize|Integer|10|分页大小。

 |
|RequestId|String|74F97EF7-B543-43FD-A4E9-18456731F9C5|请求ID。

 |
|TotalCount|Integer|1|数据总数。

 |
|VulWhitelists| | |漏洞白名单列表。

 |
|└AliasName|String|RHSA-2017:3263: curl security update|漏洞别名

 |
|└Name|String|oval:com.redhat.rhsa:def:20173263|漏洞名称

 |
|└Reason|String|暂不修复|加白原因

 |
|└Type|String|cve|漏洞类型

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeVulWhitelist
&<公共请求参数>

```

正常返回示例

`JSON` 格式

``` {#json_return_success_demo}
{
	"TotalCount":1,
	"PageSize":3,
	"VulWhitelists":[
		{
			"Name":"oval:com.redhat.rhsa:def:20173263",
			"AliasName":"RHSA-2017:3263: curl security update",
			"Type":"cve",
			"Reason":"暂不修复"
		}
	],
	"RequestId":"74F97EF7-B543-43FD-A4E9-18456731F9C5",
	"CurrentPage":1
}
```

## 错误码 { .section}

[查看本产品错误码](https://error-center.aliyun.com/status/product/Sas)

