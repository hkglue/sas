# DescribeDomainDetail {#doc_api_Sas_DescribeDomainDetail .reference}

调用该接口获取域名资产详情。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Sas&api=DescribeDomainDetail&type=RPC&version=2018-12-03)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeDomainDetail|系统规定参数。取值：DescribeDomainDetail。

 |
|DomainName|String|是|0.0.0.0|指定待查询的域名名称或网站名称。

 |
|SourceIp|String|否|127.1.1.1|指定访问源IP地址。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Domain|String|b.tst.com|返回的域名名称。

 |
|DomainDetailItems| | |返回的域名相关的资产列表。

 |
|AssetType|String|0|返回结果中域名下资产的资产类型。

 -   **0**：ECS
-   **1**：负载均衡
-   **2**：NAT网关
-   **3**：RDS数据库
-   **4**：MongoDb数据库

 |
|InstanceId|String|i-m5e6w7dzsktt6mz4yime|返回结果中的资产ID。

 |
|InstanceName|String|iZm5e6w7dzsktt6mz4yimeZ-60288|返回结果中的资产名称。

 |
|InternetIp|String|0.0.0.0|返回结果中资产对应的公网IP地址。

 |
|IntranetIp|String|0.0.0.0|返回结果中资产对应的私网IP地址。

 |
|MachineIp|String|0.0..0.0|返回的资产IP。

 |
|Uuid|String|lb-bp1g9dohoyin9cjhn6itt|返回结果中的资产UUID。

 |
|RequestId|String|3A85CFCF-05C8-451A-9E41-C0D5E96BA407|返回结果的请求ID。

 |
|RootDomain|String|tst.com|返回结果中域名对应的根域名名称。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeDomainDetail
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeDomainDetail>
	  <code>200</code>
	  <data>
		    <DomainDetailItems>
			      <InstanceName>iZm5e6w7dzsktt6mz4yimeZ-602888</InstanceName>
			      <AssetType>0</AssetType>
			      <Uuid>d664e15e-488b-4f3c-a80f-25e3560d6085</Uuid>
			      <InternetIp>139.129.103.215</InternetIp>
			      <InstanceId>i-m5e6w7dzsktt6mz4yime</InstanceId>
			      <IntranetIp>172.31.13.43</IntranetIp>
		    </DomainDetailItems>
		    <DomainDetailItems>
			      <InstanceName>iZm5ehn8ugwvsp2k4xdzokZ</InstanceName>
			      <AssetType>0</AssetType>
			      <Uuid>0d804403-8d36-4642-a5f1-a22905491c94</Uuid>
			      <InternetIp>120.27.11.134</InternetIp>
			      <InstanceId>i-m5ehn8ugwvsp2k4xdzok</InstanceId>
			      <IntranetIp>10.30.183.121</IntranetIp>
		    </DomainDetailItems>
		    <DomainDetailItems>
			      <AssetType>2</AssetType>
			      <Uuid>eip-wz98lk3q06mhqvbhcuvb5</Uuid>
			      <InternetIp>120.79.72.16</InternetIp>
			      <InstanceId>eip-wz98lk3q06mhqvbhcuvb5</InstanceId>
		    </DomainDetailItems>
		    <DomainDetailItems>
			      <InstanceName>郝浩天测试</InstanceName>
			      <AssetType>1</AssetType>
			      <Uuid>lb-bp1g9dohoyin9cjhn6itt</Uuid>
			      <InternetIp>47.111.33.130</InternetIp>
			      <InstanceId>lb-bp1g9dohoyin9cjhn6itt</InstanceId>
		    </DomainDetailItems>
		    <RootDomain>sastst.com</RootDomain>
		    <Domain>b.sastst.com</Domain>
	  </data>
	  <requestId>3A85CFCF-05C8-451A-9E41-C0D5E96BA407</requestId>
	  <success>true</success>
    </DescribeDomainDetail>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"requestId":"3A85CFCF-05C8-451A-9E41-C0D5E96BA407",
	"data":{
		"RootDomain":"sastst.com",
		"Domain":"b.sastst.com",
		"DomainDetailItems":[
			{
				"Uuid":"d664e15e-488b-4f3c-a80f-25e3560d6085",
				"AssetType":"0",
				"IntranetIp":"172.31.13.43",
				"InstanceId":"i-m5e6w7dzsktt6mz4yime",
				"InternetIp":"139.129.103.215",
				"InstanceName":"iZm5e6w7dzsktt6mz4yimeZ-602888"
			},
			{
				"Uuid":"0d804403-8d36-4642-a5f1-a22905491c94",
				"AssetType":"0",
				"IntranetIp":"10.30.183.121",
				"InstanceId":"i-m5ehn8ugwvsp2k4xdzok",
				"InternetIp":"120.27.11.134",
				"InstanceName":"iZm5ehn8ugwvsp2k4xdzokZ"
			},
			{
				"Uuid":"eip-wz98lk3q06mhqvbhcuvb5",
				"AssetType":"2",
				"InstanceId":"eip-wz98lk3q06mhqvbhcuvb5",
				"InternetIp":"120.79.72.16"
			},
			{
				"Uuid":"lb-bp1g9dohoyin9cjhn6itt",
				"AssetType":"1",
				"InstanceId":"lb-bp1g9dohoyin9cjhn6itt",
				"InternetIp":"47.111.33.130",
				"InstanceName":"郝浩天测试"
			}
		]
	},
	"code":200,
	"success":true
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/Sas)查看更多错误码。

