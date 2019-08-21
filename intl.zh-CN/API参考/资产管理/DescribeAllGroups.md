# DescribeAllGroups {#doc_api_Sas_DescribeAllGroups .reference}

调用该接口获取所有的分组信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Sas&api=DescribeAllGroups&type=RPC&version=2018-12-03)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAllGroups|系统规定参数。取值：DescribeAllGroups。

 |
|Lang|String|否|zh|指定返回结果语言环境。

 -   **zh**：中文
-   **en**：英文

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Count|Integer|2|返回结果中显示的当前页码。

 |
|Groups| | |返回的分组信息列表。

 |
|GroupFlag|Integer|1|返回结果中分组类型。0为默认分组，1为其他分组。

 |
|GroupId|Integer|100|返回结果中的分组ID。

 |
|GroupName|String|xx|返回结果中的分组名称。

 |
|RequestId|String|"requestId": "7E0618A9-D5EF-4220-9471-C42B5E92719F",|返回结果的请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeAllGroups
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeAllGroups>
	  <code>200</code>
	  <requestId>7E0618A9-D5EF-4220-9471-C42B5E92719F</requestId>
	  <success>true</success>
	  <data>
		    <Groups>
			      <GroupId>100</GroupId>
			      <GroupName>xx</GroupName>
		    </Groups>
	  </data>
    </DescribeAllGroups>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"requestId":"7E0618A9-D5EF-4220-9471-C42B5E92719F",
	"data":{
		"Groups":{
			"GroupName":"xx",
			"GroupId":100
		}
	},
	"code":200,
	"success":true
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/Sas)查看更多错误码。

