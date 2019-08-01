# DescribeRiskItemType {#doc_api_Sas_DescribeRiskItemType .reference}

查看所有云产品配置检测项的类型。

每个检测项都对应一个类型，调用DescribeRiskItemType接口查看所有云产品配置检测项的类型。

检测项类型包含：

-   身份认证及权限
-   网络访问控制
-   日志审计
-   数据安全

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Sas&api=DescribeRiskItemType&type=RPC&version=2018-12-03)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeRiskItemType|要执行的操作。

 取值：DescribeRiskItemType。

 |
|Lang|String|否|cn|调用该接口返回的内容的语言种类。支持中文（CN）和英文（EN）。

 |
|SourceIp|String|否|1.1.1.1|请求源IP。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|List| | |云产品配置检测项类型的列。

 |
|Id|Long|1|云产品配置检测项的ID。

 |
|Title|String|身份认证及权限|检测类型名称。如“身份认证及权限”。

 |
|RequestId|String|3B3F3A90-46A5-4023-A2D8-D68B14262F96|调用接口的请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeRiskItemType
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeRiskItemTypeResponse>
	  <RequestId>3B3F3A90-46A5-4023-A2D8-D68B14262F96</RequestId>
	  <List>
		    <Title>zh-身份认证及权限</Title>
		    <Id>1</Id>
	  </List>
	  <List>
		    <Title>网络访问控制</Title>
		    <Id>2</Id>
	  </List>
	  <List>
		    <Title>日志审计</Title>
		    <Id>3</Id>
	  </List>
	  <List>
		    <Title>数据安全</Title>
		    <Id>4</Id>
	  </List>
	  <List>
		    <Title>基础安全防护</Title>
		    <Id>6</Id>
	  </List>
    </DescribeRiskItemTypeResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"3B3F3A90-46A5-4023-A2D8-D68B14262F96",
	"List":[
		{
			"Id":1,
			"Title":"zh-身份认证及权限"
		},
		{
			"Id":2,
			"Title":"网络访问控制"
		},
		{
			"Id":3,
			"Title":"日志审计"
		},
		{
			"Id":4,
			"Title":"数据安全"
		},
		{
			"Id":6,
			"Title":"基础安全防护"
		}
	]
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/Sas)查看更多错误码。

