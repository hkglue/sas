# DescribePropertyUserDetail {#doc_api_Sas_DescribePropertyUserDetail .reference}

调用该接口获取账号列表中一个账号的详细信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Sas&api=DescribePropertyUserDetail&type=RPC&version=2018-12-03)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribePropertyUserDetail|系统规定参数。取值：DescribePropertyUserDetail。

 |
|CurrentPage|Integer|否|1|指定返回结果的当前页码。

 |
|IsRoot|String|否|0|是否ROOT权限。

 -   **0**：否
-   **1**：是

 |
|PageSize|Integer|否|2|指定列表每页显示数据条数 。

 |
|Remark|String|否|0.0.0.0|服务器名称或IP。

 |
|User|String|否|test|指定待查询的账户名称。

 |
|Uuid|String|否|50d213b4-3a35-427a-b8a5-04b0c7e1f4d2|指定待查询的资产UUID。

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
|TotalCount|Integer|384|返回数据的总条数。

 |
|Propertys| | |返回的账号详情列表。

 |
|AccountsExpirationDate|String|never|返回账号的到期时间。

 |
|Create|String|1565644643000|返回结果中的最新采集时间。

 |
|CreateTimestamp|Long|1565644643000|返回结果中的采集时间戳。

 |
|GroupNames| |adm|用户组。

 |
|InstanceId|String|02c4a5dc-c2d2-483a-9015-f972b44d2cd9|返回结果中的资产ID。

 |
|InstanceName|String|null|返回结果中的资产名称。

 |
|InternetIp|String|0.0.0.0|返回结果中资产对应公网IP地址。

 |
|IntranetIp|String|0.0.0.0|返回结果中资产对应私网IP地址。

 |
|Ip|String|null|返回结果中的IP地址。

 |
|IsRoot|String|0|返回账号是否为ROOT权限。

 -   **0**：否
-   **1**：是

 |
|LastLoginIp|String|N/A|上次登录来源。

 |
|LastLoginTime|String|xxxx|上次登录时间。

 |
|PasswordExpirationDate|String|never|返回账号密码的到期时间。

 |
|User|String|adm|账户名称。

 |
|Uuid|String|02c4a5dc-c2d2-483a-9015-f972b44d2cd9|返回结果中的资产UUID。

 |
|RequestId|String|null|返回结果的请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribePropertyUserDetail
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribePropertyUserDetail>
	  <code>200</code>
	  <data>
		    <PageInfo>
			      <Count>2</Count>
			      <PageSize>2</PageSize>
			      <TotalCount>384</TotalCount>
			      <CurrentPage>1</CurrentPage>
		    </PageInfo>
		    <Propertys>
			      <LastLoginTime>N/A</LastLoginTime>
			      <GroupName>adm</GroupName>
			      <IsRoot>0</IsRoot>
			      <InstanceName></InstanceName>
			      <AccountsExpirationDate>never</AccountsExpirationDate>
			      <PasswordExpirationDate>never</PasswordExpirationDate>
			      <Ip></Ip>
			      <Create>1565644643000</Create>
			      <User>adm</User>
			      <Uuid>00ea0155-548e-4f32-bb53-3a000110b30d</Uuid>
			      <LastLoginIp>N/A</LastLoginIp>
		    </Propertys>
		    <Propertys>
			      <LastLoginTime>N/A</LastLoginTime>
			      <GroupName>adm</GroupName>
			      <IsRoot>0</IsRoot>
			      <InstanceName></InstanceName>
			      <AccountsExpirationDate>never</AccountsExpirationDate>
			      <PasswordExpirationDate>never</PasswordExpirationDate>
			      <Ip></Ip>
			      <Create>1565652008000</Create>
			      <User>adm</User>
			      <Uuid>02c4a5dc-c2d2-483a-9015-f972b44d2cd9</Uuid>
			      <LastLoginIp>N/A</LastLoginIp>
		    </Propertys>
	  </data>
	  <success>true</success>
	  <requestId></requestId>
	  <message>successful</message>
	</DescribePropertyUserDetail>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"message":"successful",
	"data":{
		"PageInfo":{
			"Count":2,
			"TotalCount":384,
			"PageSize":2,
			"CurrentPage":1
		},
		"Propertys":[
			{
				"Uuid":"00ea0155-548e-4f32-bb53-3a000110b30d",
				"User":"adm",
				"AccountsExpirationDate":"never",
				"IsRoot":"0",
				"LastLoginTime":"N/A",
				"PasswordExpirationDate":"never",
				"GroupName":[
					"adm"
				],
				"Create":1565644643000,
				"LastLoginIp":"N/A"
			},
			{
				"Uuid":"02c4a5dc-c2d2-483a-9015-f972b44d2cd9",
				"User":"adm",
				"AccountsExpirationDate":"never",
				"IsRoot":"0",
				"LastLoginTime":"N/A",
				"PasswordExpirationDate":"never",
				"GroupName":[
					"adm"
				],
				"Create":1565652008000,
				"LastLoginIp":"N/A"
			}
		]
	},
	"code":"200",
	"success":true
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/Sas)查看更多错误码。

