# DescribeFieldStatistics {#doc_api_Sas_DescribeFieldStatistics .reference}

调用该接口检索资产实例列表。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Sas&api=DescribeFieldStatistics&type=RPC&version=2018-12-03)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeFieldStatistics|系统规定参数。取值：DescribeFieldStatistics。

 |
|MachineTypes|String|否|ecs|指定待检索的资产类型。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|GroupedFields| | |返回的资产信息列表。

 |
|GroupCount|Integer|20|返回的服务器组数量。

 |
|InstanceCount|Integer|100|返回的所有资产数量。

 |
|NewInstanceCount|Integer|10|返回的新增资产数量。

 |
|NotRunningStatusCount|Integer|10|返回的未启动的服务器数量。

 |
|RegionCount|Integer|11|返回的服务器地域数量。

 |
|RiskInstanceCount|Integer|90|返回的存在风险的资产数量。

 |
|UnprotectedInstanceCount|Integer|10|返回的未受保护的资产数量。

 |
|VpcCount|Integer|5|返回的专有网络VPC数量。

 |
|RequestId|String|7E0618A9-D5EF-4220-9471-C42B5E92719F|返回数据请求是否成功。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeFieldStatistics
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeFieldStatistics>
	  <code>200</code>
	  <data>
		    <GroupedFields>
			      <InstanceCount>100</InstanceCount>
			      <RiskInstanceCount>90</RiskInstanceCount>
			      <UnProtectedInstanceCount>10</UnProtectedInstanceCount>
			      <GroupCount>20</GroupCount>
			      <RegionCount>11</RegionCount>
			      <VpcCount>5</VpcCount>
		    </GroupedFields>
	  </data>
	  <requestId>7E0618A9-D5EF-4220-9471-C42B5E92719F</requestId>
	  <success>true</success>
    </DescribeFieldStatistics>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"requestId":"7E0618A9-D5EF-4220-9471-C42B5E92719F",
	"data":{
		"GroupedFields":{
			"InstanceCount":100,
			"GroupCount":20,
			"VpcCount":5,
			"UnProtectedInstanceCount":10,
			"RiskInstanceCount":90,
			"RegionCount":11
		}
	},
	"code":200,
	"success":true
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/Sas)查看更多错误码。

