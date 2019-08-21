# DescribePropertyProcDetail {#doc_api_Sas_DescribePropertyProcDetail .reference}

调用该接口获取进程列表中一个进程的详细信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Sas&api=DescribePropertyProcDetail&type=RPC&version=2018-12-03)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribePropertyProcDetail|系统规定参数。取值：DescribePropertyProcDetail。

 |
|Cmdline|String|否|./8888|指定待查询启动参数。

 |
|CurrentPage|Integer|否|1|指定返回结果的当前页码。

 |
|Name|String|否|8888|指定待查询进程名称。

 |
|PageSize|Integer|否|5|指定列表每页显示数据条数。

 |
|Remark|String|否|0.0.0.0|服务器名称或IP。

 |
|User|String|否|root|指定待查询运行用户信息。

 |
|Uuid|String|否|c4678332-ef35-4ad4-8358-681ebbc0ccab|指定待查询的资产UUID。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|PageInfo| | |返回结果的页面显示信息。

 |
|Count|Integer|1|返回结果的当前页显示数据条数。

 |
|CurrentPage|Integer|1|返回结果中显示的当前页码。

 |
|PageSize|Integer|5|返回结果中每页显示数据条数。

 |
|TotalCount|Integer|1|返回数据的总条数。

 |
|Propertys| | |返回进程信息的列表。

 |
|Cmdline|String|./8888|返回结果中进程对应启动参数。

 |
|Create|String|1565686951000|返回结果中的最新采集时间。

 |
|CreateTimestamp|Long|1565686951000|返回结果中的采集时间戳。

 |
|EuidName|String|root|返回结果中进程对应运行权限。

 |
|InstanceId|String|c4678332-ef35-4ad4-8358-681ebbc0ccab|返回结果中的资产ID。

 |
|InstanceName|String|null|返回结果中的资产名称。

 |
|InternetIp|String|0.0.0.0|返回结果中资产对应公网IP地址。

 |
|IntranetIp|String|0.0.0.0|返回结果中资产对应私网IP地址。

 |
|Md5|String|N/A|返回结果中进程对应文件MD5信息。

 |
|Name|String|8888|返回结果中进程名称。

 |
|Path|String|/root/Oracle/Middleware/user\_projects/domains/base\_domain/8888|返回结果中进程路径。

 |
|Pid|String|12826|返回结果中进程PID。

 |
|Pname|String|startWebLogic.s|返回结果中父进程名称。

 |
|StartTime|String|2019-08-07 10:09:05|返回结果中进程启动时间。

 |
|User|String|root|返回结果中进程的运行用户。

 |
|Uuid|String|c4678332-ef35-4ad4-8358-681ebbc0ccab|返回结果中的资产UUID。

 |
|RequestId|String|null|返回结果的请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribePropertyProcDetail
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribePropertyProcDetail>
	  <code>200</code>
	  <data>
		    <PageInfo>
			      <Count>1</Count>
			      <PageSize>5</PageSize>
			      <TotalCount>1</TotalCount>
			      <CurrentPage>1</CurrentPage>
		    </PageInfo>
		    <Propertys>
			      <InstanceName></InstanceName>
			      <Pname>startWebLogic.s</Pname>
			      <Euidname>root</Euidname>
			      <Ip></Ip>
			      <Pid>12826</Pid>
			      <Uuid>c4678332-ef35-4ad4-8358-681ebbc0ccab</Uuid>
			      <Path>/root/Oracle/Middleware/user_projects/domains/base_domain/8888</Path>
			      <Cmdline>./8888</Cmdline>
			      <Name>8888</Name>
			      <Create>1565686951000</Create>
			      <StartTime>2019-08-07 10:09:05</StartTime>
			      <User>root</User>
			      <Md5>N/A</Md5>
		    </Propertys>
	  </data>
	  <success>true</success>
	  <requestId></requestId>
	  <message>successful</message>
</DescribePropertyProcDetail>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"message":"successful",
	"data":{
		"PageInfo":{
			"Count":1,
			"TotalCount":1,
			"PageSize":5,
			"CurrentPage":1
		},
		"Propertys":[
			{
				"Uuid":"c4678332-ef35-4ad4-8358-681ebbc0ccab",
				"User":"root",
				"Md5":"N/A",
				"Euidname":"root",
				"Path":"/root/Oracle/Middleware/user_projects/domains/base_domain/8888",
				"Name":"8888",
				"Create":1565686951000,
				"Pname":"startWebLogic.s",
				"StartTime":"2019-08-07 10:09:05",
				"Pid":"12826",
				"Cmdline":"./8888"
			}
		]
	},
	"code":"200",
	"success":true
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/Sas)查看更多错误码。

