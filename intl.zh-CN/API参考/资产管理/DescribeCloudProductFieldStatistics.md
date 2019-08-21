# DescribeCloudProductFieldStatistics {#doc_api_Sas_DescribeCloudProductFieldStatistics .reference}

调用该接口获取云产品统计信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Sas&api=DescribeCloudProductFieldStatistics&type=RPC&version=2018-12-03)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeCloudProductFieldStatistics|系统规定参数。取值：DescribeCloudProductFieldStatistics。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|GroupedFields| | |返回云产品信息列表。

 |
|CategoryCount|String|\[\{"MachineType":1,"Count":11\}\]|返回的不同种类资产数量的列表。

 |
|InstanceCount|Integer|100|返回的所有资产数量。

 |
|RiskInstanceCount|Integer|90|返回的存在风险的资产的数量。

 |
|RequestId|String|"requestId": "7E0618A9-D5EF-4220-9471-C42B5E92719F",|返回结果的请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeCloudProductFieldStatistics
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeCloudProductFieldStatistics>
	  <code>200</code>
	  <data>
		    <GroupedFields>
			      <InstanceCount>100</InstanceCount>
			      <RiskInstanceCount>90</RiskInstanceCount>
			      <categoryCount>
				        <MachineType>1</MachineType>
				        <Count>11</Count>
			      </categoryCount>
		    </GroupedFields>
	  </data>
	  <requestId>7E0618A9-D5EF-4220-9471-C42B5E92719F</requestId>
	  <success>true</success>
</DescribeCloudProductFieldStatistics>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"requestId":"7E0618A9-D5EF-4220-9471-C42B5E92719F",
	"data":{
		"GroupedFields":{
			"InstanceCount":100,
			"categoryCount":[
				{
					"MachineType":1,
					"Count":11
				}
			],
			"RiskInstanceCount":90
		}
	},
	"code":200,
	"success":true
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/Sas)查看更多错误码。

