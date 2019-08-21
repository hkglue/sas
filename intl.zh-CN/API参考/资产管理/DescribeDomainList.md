# DescribeDomainList {#doc_api_Sas_DescribeDomainList .reference}

调用该接口域名资产列表。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Sas&api=DescribeDomainList&type=RPC&version=2018-12-03)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeDomainList|系统规定参数。取值：DescribeDomainList。

 |
|CurrentPage|Integer|否|1|指定返回结果的当前页码。

 |
|DomainType|String|否|root|指定待查询的域名类型。

 |
|FuzzyDomain|String|否|sas|指定的域名模糊匹配搜索信息。

 |
|PageSize|Integer|否|1|指定列表每页显示数据条数。

 |
|SourceIp|String|否|127.1.1.1|指定访问源IP地址。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|DomainListResponseList| | |返回的域名列表。

 |
|Domain|String|tst.com|返回的域名名称或网站名称。

 |
|IpList|String|0.0.0.0，0.0.0.0|返回的域名对应域名IP列表信息。

 |
|PageInfo| | |返回结果的页面显示信息。

 |
|Count|Integer|10|返回结果的当前页显示数据条数。

 |
|CurrentPage|Integer|1|返回结果中显示的当前页码。

 |
|PageSize|Integer|10|返回结果中每页显示数据条数。

 |
|TotalCount|Integer|27|返回数据的总条数。

 |
|RequestId|String|0B48AB3C-84FC-424D-A01D-B9270EF46038|返回结果的请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeDomainList
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeDomainList>
	  <code>200</code>
	  <data>
		    <PageInfo>
			      <TotalCount>27</TotalCount>
			      <PageSize>10</PageSize>
			      <CurrentPage>1</CurrentPage>
			      <Count>10</Count>
		    </PageInfo>
		    <DomainListResponseList>
			      <Domain>sastst.com</Domain>
		    </DomainListResponseList>
		    <DomainListResponseList>
			      <Domain>p.sastst.com</Domain>
		    </DomainListResponseList>
		    <DomainListResponseList>
			      <IpList>120.27.11.134,47.111.33.130,120.79.72.16,139.129.103.215</IpList>
			      <Domain>b.sastst.com</Domain>
		    </DomainListResponseList>
		    <DomainListResponseList>
			      <Domain>r.sastst.com</Domain>
		    </DomainListResponseList>
		    <DomainListResponseList>
			      <Domain>t.sastst.com</Domain>
		    </DomainListResponseList>
		    <DomainListResponseList>
			      <Domain>k.sastst.com</Domain>
		    </DomainListResponseList>
		    <DomainListResponseList>
			      <Domain>{.sastst.com</Domain>
		    </DomainListResponseList>
		    <DomainListResponseList>
			      <Domain>w.sastst.com</Domain>
		    </DomainListResponseList>
		    <DomainListResponseList>
			      <Domain>l.sastst.com</Domain>
		    </DomainListResponseList>
		    <DomainListResponseList>
			      <Domain>v.sastst.com</Domain>
		    </DomainListResponseList>
	  </data>
	  <requestId>0B48AB3C-84FC-424D-A01D-B9270EF46038</requestId>
	  <success>true</success>
    </DescribeDomainList>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"requestId":"0B48AB3C-84FC-424D-A01D-B9270EF46038",
	"data":{
		"DomainListResponseList":[
			{
				"Domain":"sastst.com"
			},
			{
				"Domain":"p.sastst.com"
			},
			{
				"Domain":"b.sastst.com",
				"IpList":"120.27.11.134,47.111.33.130,120.79.72.16,139.129.103.215"
			},
			{
				"Domain":"r.sastst.com"
			},
			{
				"Domain":"t.sastst.com"
			},
			{
				"Domain":"k.sastst.com"
			},
			{
				"Domain":"{.sastst.com"
			},
			{
				"Domain":"w.sastst.com"
			},
			{
				"Domain":"l.sastst.com"
			},
			{
				"Domain":"v.sastst.com"
			}
		],
		"PageInfo":{
			"Count":10,
			"TotalCount":27,
			"PageSize":10,
			"CurrentPage":1
		}
	},
	"code":200,
	"success":true
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/Sas)查看更多错误码。

