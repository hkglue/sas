# DescribePropertySoftwareItem {#doc_api_Sas_DescribePropertySoftwareItem .reference}

调用该接口获取软件列表.。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Sas&api=DescribePropertySoftwareItem&type=RPC&version=2018-12-03)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribePropertySoftwareItem|系统规定参数。取值：DescribePropertySoftwareItem。

 |
|CurrentPage|Integer|否|1|指定返回结果的当前页码。

 |
|ForceFlush|Boolean|否|true|是否强制刷新待查询数据。

 |
|Name|String|否|xxx|指定待查询的软件名称。

 |
|PageSize|Integer|否|10|指定列表每页显示数据条数 。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|PageInfo| | |返回结果的页面显示信息。

 |
|Count|Integer|2|返回结果的当前页显示数据条数。

 |
|CurrentPage|Integer|1|返回结果中显示的当前页码。

 |
|PageSize|Integer|2|返回结果中每页显示数据条数。

 |
|TotalCount|Integer|5037|返回数据的总条数。

 |
|PropertyItems| | |返回的软件列表。

 |
|Count|Integer|23|返回结果中软件资产对应的服务器数量。

 |
|Name|String|aaa\_base|返回的软件资产名称。

 |
|RequestId|String|null|返回结果的请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribePropertySoftwareItem
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribePropertySoftwareItem>
	  <code>200</code>
	  <data>
		    <PropertyItems>
			      <Name>a11y-profile-manager-indicator</Name>
			      <Count>1</Count>
		    </PropertyItems>
		    <PropertyItems>
			      <Name>aaa_base</Name>
			      <Count>23</Count>
		    </PropertyItems>
		    <PageInfo>
			      <Count>2</Count>
			      <PageSize>2</PageSize>
			      <TotalCount>5037</TotalCount>
			      <CurrentPage>1</CurrentPage>
		    </PageInfo>
	  </data>
	  <success>true</success>
	  <requestId></requestId>
	  <message>successful</message>
</DescribePropertySoftwareItem>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"message":"successful",
	"data":{
		"PropertyItems":[
			{
				"Name":"a11y-profile-manager-indicator",
				"Count":1
			},
			{
				"Name":"aaa_base",
				"Count":23
			}
		],
		"PageInfo":{
			"Count":2,
			"TotalCount":5037,
			"PageSize":2,
			"CurrentPage":1
		}
	},
	"code":"200",
	"success":true
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/Sas)查看更多错误码。

