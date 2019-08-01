# DescribeSuspEventDetail {#doc_api_Sas_DescribeSuspEventDetail .reference}

获取异常事件详情。

告警事件分为告警与异常两个维度，一个告警事件包含多个异常事件。该API可以获取异常事件的详情。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Sas&api=DescribeSuspEventDetail&type=RPC&version=2018-12-03)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeSuspEventDetail|系统规定参数。取值：DescribeSuspEventDetail。

 |
|From|String|是|sas|请求来源，固定为sas。

 |
|Lang|String|否|zh|异常事件的语言类型。

 -   zh：中文
-   cn：英文

 |
|SourceIp|String|否|1.1.1.1|接口访问者源IP。

 |
|SuspiciousEventId|Integer|否|1|要查询的异常告警ID。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|CanBeDealOnLine|Boolean|true|是否支持在线处理（隔离）。

 |
|DataSource|String|aegis\_suspicious\_file\_v2|数据来源。

 |
|Details| | |异常事件的详情。

 |
|InfoType|String|download\_url|图标展示的类型。

 |
|Name|String|更新时间|文案的标题。

 |
|Type|String|html|文案展示的方式。

 -   text：文本方式
-   html：富文本的方式

 |
|Value|String|2018-12-12 12:00:00|文案的内容。

 |
|EventDesc|String|该文件极有可能是黑客成功入侵网站后种植的，建议您先确认文件合法性并处理。|异常事件描述。

 |
|EventName|String|WEBSHELL|异常事件的名称。

 |
|EventStatus|String|1|异常事件状态, 取值有：

 -   PENDING（1，待处理）
-   IGNORE（2，已忽略）
-   HANDLED（4，已确认）
-   FAULT（8，已标记误报）
-   DEALING（16，处理中）
-   DONE（32，处理完毕）
-   EXPIRE（64，已经过期）

 |
|EventTypeDesc|String|网站后门-发现后门\(Webshell\)文件|异常事件类型说明。

 |
|Id|Integer|1991|异常事件ID。

 |
|InstanceName|String|ca\_cpm\_test1|关联实例的名称。

 |
|InternetIp|String|10.0.0.0|关联实例的公网IP。

 |
|IntranetIp|String|10.0.0.10|关联实例的私网IP。

 |
|LastTime|String|2018-10-30 11:43:46|上次发生该事件的时间。

 |
|Level|String|serious|告警事件的危险等级（严重性依次递减）：

 -   serious：紧急
-   suspicious：可疑
-   remind：提醒

 |
|OperateMsg|String|success|操作的扩展信息。

 |
|RequestId|String|1|请求ID。

 |
|SaleVersion|String|17F3C8C2-0504-48D5-8B8F-9CF000000000|态势感知服务的版本信息。

 -   0：基础版本
-   1：企业版本

 |
|SasId|String|1|态势感知系统ID。

 |
|Type|String|text|区分是否为DDoS事件。

 |
|Uuid|String|bffb12c3-590a-4db2-b538-XXXXXXXXXXXX|关联实例的唯一标识。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeSuspEventDetail
&From=sas
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeSuspEventDetailResponse>
	  <RequestId>43F670F3-AB40-4E91-BC7D-C57468834F67</RequestId>
	  <HostId>aegis.cn-hangzhou.aliyuncs.com</HostId>
	  <Code>200</Code>
	  <Message>
		illegal parameter, xxxx
	</Message>
	  <EventDesc>该文件极有可能是黑客成功入侵网站后种植的，建议您先确认文件合法性并处理。</EventDesc>
	  <EventTypeDesc>网站后门-发现后门(Webshell)文件</EventTypeDesc>
	  <EventStatus>1</EventStatus>
	  <EventName>WEBSHELL</EventName>
	  <SaleVersion>1</SaleVersion>
	  <IntranetIp>10.0.0.0</IntranetIp>
	  <DataSource>aegis_suspicious_file_v2</DataSource>
	  <InstanceName>ca_cpm_test1</InstanceName>
	  <Type>normal</Type>
	  <CanBeDealOnLine>true</CanBeDealOnLine>
	  <OperateMsg></OperateMsg>
	  <Uuid>bffb12c3-590a-4db2-b538-XXXXXXXXXXXX</Uuid>
	  <Details>
		    <Type>text</Type>
		    <Value>/data/ftpUser/pub/f12cd3bc5b484b0326309b48afb463fb</Value>
		    <InfoType>trojan_path</InfoType>
		    <Name>木马文件路径</Name>
	  </Details>
	  <Details>
		    <Type>text</Type>
		    <Value>--</Value>
		    <Name>影响域名</Name>
	  </Details>
	  <Details>
		    <Type>text</Type>
		    <Value>2018-10-30 05:00:56</Value>
		    <InfoType>frist_found_time</InfoType>
		    <Name>首次发现时间</Name>
	  </Details>
	  <Details>
		    <Type>text</Type>
		    <Value>2018-10-30 11:43:45</Value>
		    <InfoType>update_time</InfoType>
		    <Name>更新时间</Name>
	  </Details>
	  <Details>
		    <Type>text</Type>
		    <Value>Webshell</Value>
		    <InfoType>trojan_type</InfoType>
		    <Name>木马类型</Name>
	  </Details>
	  <Details>
		    <Type>html</Type>
		    <Value>&lt;a href="http://yundun-aegis-webshell-file.oss-cn-shanghai.aliyuncs.com/XXXXXXXXXXX?Expires=1540899863&amp;OSSAccessKeyId=XXXXXX&amp;Signature=XXXXXX;response-content-disposition=attachment%3Bfilename%3Df12cd3bc5b484b0326309b48afb463fb"&gt;下载&lt;/a&gt;</Value>
		    <InfoType>download_url</InfoType>
		    <Name>源文件下载</Name>
	  </Details>
	  <InternetIp>39.105.41.176</InternetIp>
	  <Level>serious</Level>
	  <Id>129636</Id>
	  <LastTime>2018-10-30 11:43:46</LastTime>
	  <SasId>39938056</SasId>
         </DescribeSuspEventDetailResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"Uuid":"bffb12c3-590a-4db2-b538-XXXXXXXXXXXX",
	"EventName":"WEBSHELL",
	"EventStatus":1,
	"Message":"illegal parameter, xxxx\n",
	"LastTime":"2018-10-30 11:43:46",
	"Details":[
		{
			"Name":"木马文件路径",
			"Value":"/data/ftpUser/pub/f12cd3bc5b484b0326309b48afb463fb",
			"Type":"text",
			"InfoType":"trojan_path"
		},
		{
			"Name":"影响域名",
			"Value":"--",
			"Type":"text"
		},
		{
			"Name":"首次发现时间",
			"Value":"2018-10-30 05:00:56",
			"Type":"text",
			"InfoType":"frist_found_time"
		},
		{
			"Name":"更新时间",
			"Value":"2018-10-30 11:43:45",
			"Type":"text",
			"InfoType":"update_time"
		},
		{
			"Name":"木马类型",
			"Value":"Webshell",
			"Type":"text",
			"InfoType":"trojan_type"
		},
		{
			"Name":"源文件下载",
			"Value":"<a href=\"http://yundun-aegis-webshell-file.oss-cn-shanghai.aliyuncs.com/XXXXXXXXXX?Expires=1540899863&OSSAccessKeyId=XXXXXX&Signature=XXXXXX&response-content-disposition=attachment%3Bfilename%3Df12cd3bc5b484b0326309b48afb463fb\">下载</a>",
			"Type":"html",
			"InfoType":"download_url"
		}
	],
	"Type":"normal",
	"InternetIp":"39.105.41.176",
	"HostId":"aegis.cn-hangzhou.aliyuncs.com",
	"EventTypeDesc":"网站后门-发现后门(Webshell)文件",
	"Code":"200",
	"DataSource":"aegis_suspicious_file_v2",
	"SasId":"39938056",
	"RequestId":"43F670F3-AB40-4E91-BC7D-C57468834F67",
	"IntranetIp":"10.0.0.0",
	"Id":129636,
	"Level":"serious",
	"EventDesc":"该文件极有可能是黑客成功入侵网站后种植的，建议您先确认文件合法性并处理。",
	"OperateMsg":"",
	"CanBeDealOnLine":true,
	"SaleVersion":"1",
	"InstanceName":"ca_cpm_test1"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/Sas)查看更多错误码。

