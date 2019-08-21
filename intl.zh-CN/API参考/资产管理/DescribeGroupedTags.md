# DescribeGroupedTags {#doc_api_Sas_DescribeGroupedTags .reference}

调用该接口获取标签的统计信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Sas&api=DescribeGroupedTags&type=RPC&version=2018-12-03)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeGroupedTags|系统规定参数。取值：DescribeGroupedTags。

 |
|MachineTypes|String|否|ecs|指定待查询的资产类型。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Count|Integer|2|返回结果的当前页显示数据条数。

 |
|GroupedFileds| | |返回的标签统计信息列表。

 |
|Count|String|2|返回结果中标签对应资产数量。

 |
|Name|String|xxx|返回结果中标签名称。

 |
|TagId|Integer|111|返回结果中的标签ID。

 |
|HttpStatusCode|Integer|200|返回请求数据结果的状态码。

 |
|RequestId|String|7E0618A9-D5EF-4220-9471-C42B5E92719F|返回结果的请求ID。

 |
|Success|Boolean|true|返回数据请求是否成功。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeGroupedTags
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeGroupedTags>
	  <code>200</code>
	  <data>
		    <GroupedFileds>
			      <Name>xxx</Name>
			      <Count>2</Count>
			      <TagId>111</TagId>
		    </GroupedFileds>
	  </data>
	  <requestId>7E0618A9-D5EF-4220-9471-C42B5E92719F</requestId>
	  <success>true</success>
</DescribeGroupedTags>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"requestId":"7E0618A9-D5EF-4220-9471-C42B5E92719F",
	"data":{
		"GroupedFileds":[
			{
				"Name":"xxx",
				"Count":2,
				"TagId":111
			}
		]
	},
	"code":200,
	"success":true
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/Sas)查看更多错误码。

