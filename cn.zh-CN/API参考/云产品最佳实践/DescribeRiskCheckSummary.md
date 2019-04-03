# DescribeRiskCheckSummary {#doc_api_Sas_DescribeRiskCheckSummary .reference}

查看云产品检测结果汇总，包括检测到的风险项数量、风险率、影响资产数量、上次检测时间以及检测项各个类型的统计数据

查看云产品检测结果汇总，包括检测到的风险项数量、风险率、影响资产数量、上次检测时间以及检测项各个类型的统计数据。

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Sas&api=DescribeRiskCheckSummary)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeRiskCheckSummary|要执行的操作。

 取值：DescribeRiskCheckSummary。

 |
|Lang|String|否|cn|调用接口返回的内容的语种类型，支持中文和英文。

 |
|SourceIp|String|否|1.1.1.1|请求源IP。

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|291B49F9-1685-4005-9D34-606B6F78740F|调用接口的请求ID。

 |
|RiskCheckSummary| | |云产品检测的结果统计。

 |
|└AffectedAssetCount|Integer|0|检测结果中风险项影响的资产数量。

 |
|└Groups| | |检查项类型的统计信息。

 |
|└CountByStatus| | |检查项结果统计。

 |
|└Count|Integer|2|检测到的风险项数量。

 |
|└Status|String|pass|完成检测后，检测项的状态。

 取值：

 -   pass：检测通过，表示检测项正常。
-   failed：检测不通过，表示检测项存在风险。

 |
|└Id|Long|1|检查项类别ID。

 |
|└RemainingTime|Integer|0|预计检测时间。

 |
|└Sort|Integer|1|检测项类型在控制台**全部类型**下拉列表中的排列顺序。

 |
|└Status|String|finish|检测完成的状态。

 取值：

 -   finish：检测已完成。
-   running：检测中。
-   waiting：检测等待中。
-   notStart：检测未开始。

 |
|└Title|String|身份认证及权限|检测项类别的名称。

 |
|└ItemCount|Integer|4|检查项的数量。

 |
|└PreviousCount|Integer|0|上次检测到的风险项数量。

 |
|└PreviousTime|Long|1545012926000|上次检测时间。

 |
|└RiskCount|Integer|1|检测到的风险项数量。

 |
|└RiskLevelCount| | |检测项每类危险等级的数量。

 危险等级包含：

 -   高危
-   中危
-   低危

 |
|└Count|Integer|1|数量

 |
|└Key|String|medium|检测项的危险等级。

 |
|└RiskRate|Float|0.25|检测出的风险项数量在检测项总数中的占比。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeRiskCheckSummary
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeRiskCheckSummaryResponse>
  <RequestId>291B49F9-1685-4005-9D34-606B6F78740F</RequestId>
  <RiskCheckSummary>
    <RiskCount>1</RiskCount>
    <RiskRate>0.25</RiskRate>
    <PreviousTime>1545012926000</PreviousTime>
    <ItemCount>4</ItemCount>
    <AffectedAssetCount>0</AffectedAssetCount>
    <RiskLevelCount>
      <Count>1</Count>
      <Key>medium</Key>
    </RiskLevelCount>
    <Groups>
      <Status>finish</Status>
      <CountByStatus>
        <Status>exception</Status>
        <Count>2</Count>
      </CountByStatus>
      <RemainingTime>0</RemainingTime>
      <Sort>1</Sort>
      <Title>zh-身份认证及权限</Title>
      <Id>1</Id>
    </Groups>
    <Groups>
      <Status>finish</Status>
      <CountByStatus>
        <Status>exception</Status>
        <Count>5</Count>
      </CountByStatus>
      <RemainingTime>0</RemainingTime>
      <Sort>2</Sort>
      <Title>网络访问控制</Title>
      <Id>2</Id>
    </Groups>
    <Groups>
      <Status>finish</Status>
      <CountByStatus>
        <Status>pass</Status>
        <Count>1</Count>
      </CountByStatus>
      <RemainingTime>0</RemainingTime>
      <Sort>3</Sort>
      <Title>日志审计</Title>
      <Id>3</Id>
    </Groups>
    <Groups>
      <Status>finish</Status>
      <CountByStatus>
        <Status>exception</Status>
        <Count>2</Count>
      </CountByStatus>
      <RemainingTime>0</RemainingTime>
      <Sort>4</Sort>
      <Title>数据安全</Title>
      <Id>4</Id>
    </Groups>
    <Groups>
      <Status>finish</Status>
      <CountByStatus>
        <Status>exception</Status>
        <Count>2</Count>
      </CountByStatus>
      <RemainingTime>0</RemainingTime>
      <Sort>6</Sort>
      <Title>基础安全防护</Title>
      <Id>6</Id>
    </Groups>
    <PreviousCount>0</PreviousCount>
  </RiskCheckSummary>
</DescribeRiskCheckSummaryResponse>

```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"291B49F9-1685-4005-9D34-606B6F78740F",
	"RiskCheckSummary":{
		"Groups":[
			{
				"Sort":1,
				"Status":"finish",
				"CountByStatus":[
					{
						"Status":"exception",
						"Count":2
					}
				],
				"Id":1,
				"Title":"zh-身份认证及权限",
				"RemainingTime":0
			},
			{
				"Sort":2,
				"Status":"finish",
				"CountByStatus":[
					{
						"Status":"exception",
						"Count":5
					}
				],
				"Id":2,
				"Title":"网络访问控制",
				"RemainingTime":0
			},
			{
				"Sort":3,
				"Status":"finish",
				"CountByStatus":[
					{
						"Status":"pass",
						"Count":1
					}
				],
				"Id":3,
				"Title":"日志审计",
				"RemainingTime":0
			},
			{
				"Sort":4,
				"Status":"finish",
				"CountByStatus":[
					{
						"Status":"exception",
						"Count":2
					}
				],
				"Id":4,
				"Title":"数据安全",
				"RemainingTime":0
			},
			{
				"Sort":6,
				"Status":"finish",
				"CountByStatus":[
					{
						"Status":"exception",
						"Count":2
					}
				],
				"Id":6,
				"Title":"基础安全防护",
				"RemainingTime":0
			}
		],
		"PreviousCount":0,
		"RiskCount":1,
		"ItemCount":4,
		"PreviousTime":1545012926000,
		"AffectedAssetCount":0,
		"RiskRate":0.25,
		"RiskLevelCount":[
			{
				"Key":"medium",
				"Count":1
			}
		]
	}
}
```

## 错误码 { .section}

[查看本产品错误码](https://error-center.aliyun.com/status/product/Sas)

