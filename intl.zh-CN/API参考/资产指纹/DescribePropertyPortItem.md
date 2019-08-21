# DescribePropertyPortItem {#doc_api_Sas_DescribePropertyPortItem .reference}

调用该接口获取端口信息列表。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Sas&api=DescribePropertyPortItem&type=RPC&version=2018-12-03)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribePropertyPortItem|系统规定参数。取值：DescribePropertyPortItem。

 |
|CurrentPage|Integer|否|1|指定返回结果的当前页码。

 |
|ForceFlush|Boolean|否|true|是否强制刷新待查询数据。

 |
|PageSize|Integer|否|5|指定列表每页显示数据条数。

 |
|Port|String|否|22|指定待查询端口。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|PageInfo| | |返回结果的页面显示信息。

 |
|Count|Integer|5|返回结果的当前页显示数据条数。

 |
|CurrentPage|Integer|1|返回结果中显示的当前页码。

 |
|PageSize|Integer|5|返回结果中每页显示数据条数。

 |
|TotalCount|Integer|163|返回数据的总条数。

 |
|PropertyItems| | |返回的端口列表。

 |
|Count|Integer|495|返回结果中端口对应的服务器数量。

 |
|Port|String|22|返回结果中监听端口号。

 |
|Proto|String|tcp|返回结果中端口对应的网络协议。

 |
|RequestId|String|7E0618A9-D5EF-4220-9471-C42B5E92719F|返回结果的请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribePropertyPortItem
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribePropertyPortItem>
	  <code>200</code>
	  <data>
		    <PageInfo>
			      <Count>5</Count>
			      <PageSize>5</PageSize>
			      <TotalCount>163</TotalCount>
			      <CurrentPage>1</CurrentPage>
		    </PageInfo>
		    <PropertyItems>
			      <Port>22</Port>
			      <Proto>tcp</Proto>
			      <Count>495</Count>
		    </PropertyItems>
		    <PropertyItems>
			      <Port>111</Port>
			      <Proto>tcp</Proto>
			      <Count>43</Count>
		    </PropertyItems>
		    <PropertyItems>
			      <Port>6000</Port>
			      <Proto>tcp</Proto>
			      <Count>2</Count>
		    </PropertyItems>
		    <PropertyItems>
			      <Port>53</Port>
			      <Proto>tcp</Proto>
			      <Count>1</Count>
		    </PropertyItems>
		    <PropertyItems>
			      <Port>80</Port>
			      <Proto>tcp</Proto>
			      <Count>38</Count>
		    </PropertyItems>
	  </data>
	  <success>true</success>
	  <requestId></requestId>
	  <message>successful</message>
    </DescribePropertyPortItem>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"message":"successful",
	"data":{
		"PropertyItems":[
			{
				"Port":"22",
				"Count":495,
				"Proto":"tcp"
			},
			{
				"Port":"111",
				"Count":43,
				"Proto":"tcp"
			},
			{
				"Port":"6000",
				"Count":2,
				"Proto":"tcp"
			},
			{
				"Port":"53",
				"Count":1,
				"Proto":"tcp"
			},
			{
				"Port":"80",
				"Count":38,
				"Proto":"tcp"
			}
		],
		"PageInfo":{
			"Count":5,
			"TotalCount":163,
			"PageSize":5,
			"CurrentPage":1
		}
	},
	"code":"200",
	"success":true
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/Sas)查看更多错误码。

