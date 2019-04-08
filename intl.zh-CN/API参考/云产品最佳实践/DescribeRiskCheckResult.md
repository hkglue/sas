# DescribeRiskCheckResult {#doc_api_Sas_DescribeRiskCheckResult .reference}

查询检查项的检测结果。

调用DescribeRiskCheckResult可查询检查项的检测结果，可按类别或名称进行筛选。

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Sas&api=DescribeRiskCheckResult)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeRiskCheckResult|系统规定参数。取值：DescribeRiskCheckResult。

 |
|CurrentPage|Integer|否|1|当前页

 |
|GroupId|Long|否|2|检测项类别id

 |
|Lang|String|否|cn|语种

 |
|Name|String|否|云平台-主账号双因素认证配置检查|检查项名称

 |
|PageSize|Integer|否|10|每页行数

 |
|RiskLevel|String|否|high|风险级别

 |
|SourceIp|String|否|1.1.1.1|请求源ip

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Count|Integer|10|数量

 |
|CurrentPage|Integer|1|当前页

 |
|List| | |检查项列表

 |
|└AffectedCount|Integer|0|受影响资产数

 |
|└CheckTime|Long|1543991525000|检测时间

 |
|└ItemId|Long|1|检查项id

 |
|└RemainingTime|Integer|0|预计检查时间

 |
|└RiskItemResources| | |详情数据

 |
|└ContentResource|Json|\{ "type": "link", "value": "未开启多因素认证，存在风险\\n", "url": "https://account.console.aliyun.com/\#/secure\\n" \}|详情json

 |
|└ResourceName|String|bestPractice|详情条目 bestPractice检查描述 ， influence威胁影响，suggestion指导方案，helpResource帮助资源

 |
|└RiskLevel|String|high|风险等级 high medium low

 |
|└Sort|Integer|1|顺序

 |
|└Status|String|pass|检查项检查状态 pass通过 failed失败 running运行中 waiting等待运行 ignored已忽略 falsePositive已标记误报

 |
|└TaskId|Long|5|任务id

 |
|└Title|String|云平台-主账号双因素认证配置检查|检查项标题

 |
|└Type|String|身份认证及权限|类型

 |
|PageCount|Integer|2|页数

 |
|PageSize|Integer|10|页大小

 |
|RequestId|String|AD271C07-4ACE-413D-AA9B-F14FD3B7717F|请求id

 |
|TotalCount|Integer|12|总数

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeRiskCheckResult
&CurrentPage=1
&PageSize=20
&<公共请求参数>

```

正常返回示例

`JSON` 格式

``` {#json_return_success_demo}
{
	"PageCount":2,
	"Count":10,
	"TotalCount":12,
	"PageSize":10,
	"RequestId":"AD271C07-4ACE-413D-AA9B-F14FD3B7717F",
	"List":[
		{
			"Sort":3,
			"Status":"pass",
			"ItemId":5,
			"RiskItemResources":[
				{
					"ContentResource":{
						"value":"未开启多因素认证，存在风险\n",
						"type":"link",
						"url":"https://account.console.aliyun.com/#/secure\n"
					},
					"ResourceName":"bestPractice"
				},
				{
					"ContentResource":{
						"value":"在只使用单一密码认证的情况下，黑客可能通过暴力破解等手段获取您的云平台管理密码。建议对云平台管理员账号开启密码加手机短信双重身份认证，防止密码泄露带来的安全隐患。",
						"type":"text"
					},
					"ResourceName":"influence"
				},
				{
					"ContentResource":{
						"value":"进入阿里云后台，顺序操作：管理控制台-账号管理-安全设置-虚拟MFA-设置 ",
						"type":"link",
						"url":"https://account.console.aliyun.com/#/selectVerificationMethod"
					},
					"ResourceName":"suggestion"
				},
				{
					"ContentResource":{
						"value":"1、使用多重机制保护主账户安全原理：\nhttps://help.aliyun.com/document_detail/28643.html\n2、设置MFA方法：\nhttps://help.aliyun.com/document_detail/28635.html",
						"type":"text"
					},
					"ResourceName":"helpResource"
				}
			],
			"RiskLevel":"high",
			"Type":"zh-身份认证及权限",
			"CheckTime":1543991525000,
			"AffectedCount":0,
			"TaskId":58,
			"Title":"云平台-主账号双因素认证配置检查",
			"RemainingTime":0
		},
		{
			"Sort":13,
			"Status":"pass",
			"ItemId":25,
			"RiskItemResources":[
				{
					"ContentResource":{
						"emptyGridValue":{
							"value":"无影响",
							"type":"text"
						},
						"type":"grid"
					},
					"ResourceName":"bestPractice"
				},
				{
					"ContentResource":{
						"value":"超长时间未登陆的子用户可能存在数据泄露隐患，当子用户被非法登陆后，登陆者可以直接控制您的云产品。",
						"type":"text"
					},
					"ResourceName":"influence"
				},
				{
					"ContentResource":{
						"value":"进入管理控制台-访问控制 RAM， 删除暂不使用的子用户。",
						"type":"link",
						"url":"https://ram.console.aliyun.com/?#/user/list"
					},
					"ResourceName":"suggestion"
				},
				{
					"ContentResource":{
						"emptyGridValue":{
							"value":"暂无风险",
							"type":"text"
						},
						"values":[],
						"columns":[
							{
								"title":"所在可用区",
								"key":"RegionId"
							},
							{
								"title":"Bucket 名",
								"key":"RiskInstance"
							},
							{
								"title":"风险描述",
								"key":"RiskDescribe"
							}
						],
						"resultStatus":[
							{
								"id":1,
								"status":"failed"
							}
						],
						"type":"grid"
					},
					"ResourceName":"helpResource"
				}
			],
			"RiskLevel":"medium",
			"Type":"zh-身份认证及权限",
			"CheckTime":1543991523000,
			"AffectedCount":0,
			"TaskId":57,
			"Title":"子账号安全-长时间未使用账户",
			"RemainingTime":0
		}
	],
	"CurrentPage":1
}
```

## 错误码 { .section}

[查看本产品错误码](https://error-center.aliyun.com/status/product/Sas)

