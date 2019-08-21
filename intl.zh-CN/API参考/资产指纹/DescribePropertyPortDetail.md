# DescribePropertyPortDetail {#doc_api_Sas_DescribePropertyPortDetail .reference}

调用该接口查询端口列表中一个端口的详细信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Sas&api=DescribePropertyPortDetail&type=RPC&version=2018-12-03)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribePropertyPortDetail|系统规定参数。取值：DescribePropertyPortDetail。

 |
|CurrentPage|Integer|否|1|指定返回结果的当前页码。

 |
|PageSize|Integer|否|6|指定列表每页显示数据条数。

 |
|Port|String|否|22|指定待查询的端口信息。

 |
|ProcName|String|否|sshd|指定待查询的进程名称。

 |
|Remark|String|否|0.0.0.0|服务器名称或IP。

 |
|Uuid|String|否|50d213b4-3a35-427a-b8a5-04b0c7e1f4d2|指定待查询的资产UUID。

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
|TotalCount|Integer|762|返回数据的总条数。

 |
|Propertys| | |返回的端口信息列表。

 |
|BindIp|String|0.0.0.0|返回结果中绑定IP地址信息。

 |
|Create|String|1552632559000|返回结果中的最新采集时间。

 |
|CreateTimestamp|Long|1552632559000|返回结果中的采集时间戳。

 |
|InstanceId|String|50d213b4-3a35-427a-b8a5-04b0c7e1f4d2"|返回结果中的资产ID。

 |
|InstanceName|String|null|返回结果中的资产名称。

 |
|InternetIp|String|127.1.1.1|返回结果中资产对应公网IP地址。

 |
|IntranetIp|String|0.0.0.0|返回结果中资产对应私网IP地址。

 |
|Ip|String|null|返回结果中的IP地址。

 |
|Port|String|22|返回的端口信息。

 |
|ProcName|String|sshd|返回端口对应的进程名称。

 |
|Proto|String|tcp|返回的端口对应网络协议。

 |
|Uuid|String|50d213b4-3a35-427a-b8a5-04b0c7e1f4d2"|返回结果中的资产UUID。

 |
|RequestId|String|null|返回结果的请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribePropertyPortDetail
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribePropertyPortDetail>
	  <code>200</code>
	  <data>
		    <Propertys>
			      <BindIp>0.0.0.0</BindIp>
			      <Port>22</Port>
			      <InstanceName></InstanceName>
			      <Proto>tcp</Proto>
			      <Ip></Ip>
			      <Create>1552285726000</Create>
			      <ProcName>sshd</ProcName>
			      <Uuid>36bde5fc-a09e-4028-a278-594091c36c74</Uuid>
		    </Propertys>
		    <Propertys>
			      <BindIp>0.0.0.0</BindIp>
			      <Port>22</Port>
			      <InstanceName></InstanceName>
			      <Proto>tcp</Proto>
			      <Ip></Ip>
			      <Create>1552520423000</Create>
			      <ProcName>sshd</ProcName>
			      <Uuid>27e7d065-4788-4d0e-8f88-22d7f2a2ccaf</Uuid>
		    </Propertys>
		    <Propertys>
			      <BindIp>0.0.0.0</BindIp>
			      <Port>22</Port>
			      <InstanceName></InstanceName>
			      <Proto>tcp</Proto>
			      <Ip></Ip>
			      <Create>1552630937000</Create>
			      <ProcName>sshd</ProcName>
			      <Uuid>inet-f7e35eaa-e112-40c5-af83-58cea026afe7</Uuid>
		    </Propertys>
		    <Propertys>
			      <BindIp>::</BindIp>
			      <Port>22</Port>
			      <InstanceName></InstanceName>
			      <Proto>tcp</Proto>
			      <Ip></Ip>
			      <Create>1552630937000</Create>
			      <ProcName>sshd</ProcName>
			      <Uuid>inet-f7e35eaa-e112-40c5-af83-58cea026afe7</Uuid>
		    </Propertys>
		    <Propertys>
			      <BindIp>0.0.0.0</BindIp>
			      <Port>22</Port>
			      <InstanceName></InstanceName>
			      <Proto>tcp</Proto>
			      <Ip></Ip>
			      <Create>1552632559000</Create>
			      <ProcName>sshd</ProcName>
			      <Uuid>50d213b4-3a35-427a-b8a5-04b0c7e1f4d2</Uuid>
		    </Propertys>
		    <PageInfo>
			      <Count>5</Count>
			      <PageSize>5</PageSize>
			      <TotalCount>762</TotalCount>
			      <CurrentPage>1</CurrentPage>
		    </PageInfo>
	  </data>
	  <success>true</success>
	  <requestId></requestId>
	  <message>successful</message>
</DescribePropertyPortDetail>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"message":"successful",
	"data":{
		"PageInfo":{
			"Count":5,
			"TotalCount":762,
			"PageSize":5,
			"CurrentPage":1
		},
		"Propertys":[
			{
				"Uuid":"36bde5fc-a09e-4028-a278-594091c36c74",
				"Port":"22",
				"Create":1552285726000,
				"Proto":"tcp",
				"BindIp":"0.0.0.0",
				"ProcName":"sshd"
			},
			{
				"Uuid":"27e7d065-4788-4d0e-8f88-22d7f2a2ccaf",
				"Port":"22",
				"Create":1552520423000,
				"Proto":"tcp",
				"BindIp":"0.0.0.0",
				"ProcName":"sshd"
			},
			{
				"Uuid":"inet-f7e35eaa-e112-40c5-af83-58cea026afe7",
				"Port":"22",
				"Create":1552630937000,
				"Proto":"tcp",
				"BindIp":"0.0.0.0",
				"ProcName":"sshd"
			},
			{
				"Uuid":"inet-f7e35eaa-e112-40c5-af83-58cea026afe7",
				"Port":"22",
				"Create":1552630937000,
				"Proto":"tcp",
				"BindIp":"::",
				"ProcName":"sshd"
			},
			{
				"Uuid":"50d213b4-3a35-427a-b8a5-04b0c7e1f4d2",
				"Port":"22",
				"Create":1552632559000,
				"Proto":"tcp",
				"BindIp":"0.0.0.0",
				"ProcName":"sshd"
			}
		]
	},
	"code":"200",
	"success":true
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/Sas)查看更多错误码。

