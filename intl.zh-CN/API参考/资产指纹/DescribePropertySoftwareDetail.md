# DescribePropertySoftwareDetail {#doc_api_Sas_DescribePropertySoftwareDetail .reference}

调用该接口获取软件列表中一个软件的详细信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Sas&api=DescribePropertySoftwareDetail&type=RPC&version=2018-12-03)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribePropertySoftwareDetail|系统规定参数。取值：DescribePropertySoftwareDetail。

 |
|CurrentPage|Integer|否|1|指定返回结果的当前页码。

 |
|Name|String|否|xxxx|指定待查询的软件名称。

 |
|PageSize|Integer|否|5|指定列表每页显示数据条数 。

 |
|Path|String|否|/etc/test|指定待查询的软件安装路径。

 |
|Remark|String|否|0.0.0.0|服务器名称或IP。

 |
|SoftwareVersion|String|否|11|指定待查询的软件版本信息。

 |
|Uuid|String|否|50d213b4-3a35-427a-b8a5-04b0c7e1f4d2"|指定待查询的资产UUID。

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
|TotalCount|Integer|23|返回数据的总条数。

 |
|Propertys| | |返回的软件详情列表。

 |
|Create|Long|1565539587000|返回结果中的最新采集时间。

 |
|CreateTimestamp|Long|1565539587000|返回结果中的采集时间戳。

 |
|InstallTime|String|2017-09-07 10:54:49|返回的软件安装时间。

 |
|InstanceId|String|4ef1115b-e423-4b4b-b930-a8be682df6ec|返回结果中的资产ID。

 |
|InstanceName|String|null|返回结果中的资产名称。

 |
|InternetIp|String|0.0.0.0|返回结果中资产对应公网IP地址。

 |
|IntranetIp|String|0.0.0.0|返回结果中资产对应私网IP地址。

 |
|Ip|String|null|返回IP地址信息。

 |
|Name|String|aaa\_base|返回的软件名称。

 |
|Path|String|/etc/test|返回软件资产的安装目录信息。

 |
|Uuid|String|4ef1115b-e423-4b4b-b930-a8be682df6ec|返回的软件版本信息。

 |
|Version|String|11|返回软件资产对应的版本信息。

 |
|RequestId|String|null|返回结果的请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribePropertySoftwareDetail
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribePropertySoftwareDetail>
	  <code>200</code>
	  <data>
		    <Propertys>
			      <Path>/etc/DIR_COLORS</Path>
			      <InstanceName></InstanceName>
			      <Ip></Ip>
			      <Name>aaa_base</Name>
			      <Create>1565539587000</Create>
			      <InstallTime>2017-09-07 10:54:49</InstallTime>
			      <Version>11</Version>
			      <Uuid>4ef1115b-e423-4b4b-b930-a8be682df6ec</Uuid>
		    </Propertys>
		    <Propertys>
			      <Path>/etc/bash.bashrc</Path>
			      <InstanceName></InstanceName>
			      <Ip></Ip>
			      <Name>aaa_base</Name>
			      <Create>1565544175000</Create>
			      <InstallTime>2017-09-07 10:56:38</InstallTime>
			      <Version>13.2+git20140911.61c1681</Version>
			      <Uuid>d276e6d9-72e5-477a-b4f8-6affcbdad858</Uuid>
		    </Propertys>
		    <pageInfo>
			      <Count>2</Count>
			      <PageSize>2</PageSize>
			      <TotalCount>23</TotalCount>
			      <CurrentPage>1</CurrentPage>
		    </pageInfo>
	  </data>
	  <success>true</success>
	  <requestId></requestId>
	  <message>successful</message>
</DescribePropertySoftwareDetail>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"message":"successful",
	"data":{
		"pageInfo":{
			"Count":2,
			"TotalCount":23,
			"PageSize":2,
			"CurrentPage":1
		},
		"Propertys":[
			{
				"Uuid":"4ef1115b-e423-4b4b-b930-a8be682df6ec",
				"Name":"aaa_base",
				"Create":1565539587000,
				"InstallTime":"2017-09-07 10:54:49",
				"Version":"11",
				"Path":"/etc/DIR_COLORS"
			},
			{
				"Uuid":"d276e6d9-72e5-477a-b4f8-6affcbdad858",
				"Name":"aaa_base",
				"Create":1565544175000,
				"InstallTime":"2017-09-07 10:56:38",
				"Version":"13.2+git20140911.61c1681",
				"Path":"/etc/bash.bashrc"
			}
		]
	},
	"code":"200",
	"success":true
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/Sas)查看更多错误码。

