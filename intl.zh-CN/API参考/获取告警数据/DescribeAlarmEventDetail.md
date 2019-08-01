# DescribeAlarmEventDetail {#doc_api_Sas_DescribeAlarmEventDetail .reference}

获取告警事件的详细信息。

告警事件分为告警与异常两个维度，一个告警事件包含多个异常事件。该API可以获取一个告警事件的详情。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Sas&api=DescribeAlarmEventDetail&type=RPC&version=2018-12-03)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAlarmEventDetail|系统规定参数。取值：DescribeAlarmEventDetail。

 |
|AlarmUniqueInfo|String|是|8df914418f4211fbf756efe7a6f40cbc|告警事件的唯一标识。

 |
|From|String|是|sas|请求来源标识，固定为sas。

 |
|Lang|String|否|zh|告警事件显示的语言类型。

 -   zh：中文
-   cn：英文

 |
|SourceIp|String|否|1.1.1.1|请求源IP。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Data| | |告警事件详情。

 |
|AlarmEventAliasName|String|进程异常行为-Linux计划任务执行异常指令|告警事件完整名称。

 |
|AlarmEventDesc|String|黑客入侵服务器后，为了让恶意后门程序能持久化运行，黑客常常将恶意SHELL脚本写入crontab、systemd等计划任务。|告警事件描述。

 |
|AlarmUniqueInfo|String|8df914418f4211fbf756efe700000000|告警事件的唯一标识。

 |
|CanBeDealOnLine|Boolean|false|是否能在线处理（隔离）。

 |
|CanCancelFault|Boolean|false|能否取消标记为误报。

 |
|CauseDetails| | |告警事件发生的原因（溯源信息）。

 |
|Key|String|item|文本的展示方式：

 -   text：文本方式
-   html：富文本方式

 |
|Value| | |溯源信息字段值。

 |
|Name|String|排查方案|溯源信息字段的key。

 |
|Type|String|html|溯源信息字段展示的类型。

 |
|Value|String|请根据上述信息排查您的WEB服务被利用的页面及参数是否存在漏洞，并及时修复。|溯源信息字段的值。

 |
|DataSource|String|aegis\_suspicious\_event|数据来源。

 |
|EndTime|Long|1542366542000|告警事件结束时间。

 |
|InstanceName|String|测试服务器|关联实例的名称。

 |
|InternetIp|String|10.0.0.0|关联实例的公网IP。

 |
|IntranetIp|String|10.0.0.0|关联实例的私网IP。

 |
|Level|String|serious|告警事件的危险等级。

 -   serious：紧急
-   suspicious：可疑
-   remind：提醒

 |
|Solution|String|请及时排查告警中提示的恶意URL，以及所下载的目录下的恶意文件。并及时清理已运行的恶意进程。如果该指令是您自己主动执行，您可以在控制台点击标记为误报，并通过工单方式反馈给我们的安全工程师。|告警事件的处理方法。

 |
|StartTime|Long|1542378601000|告警事件的开始时间。

 |
|Type|String|异常网络连接|事件类型。

 |
|Uuid|String|47900178-885d-4fa4-9d77-XXXXXXXXXXXX|关联实例的唯一标识。

 |
|RequestId|String|5A1DDB3C-798C-4A84-BF6E-3DC700000000|请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeAlarmEventDetail
&AlarmUniqueInfo=8df914418f4211fbf756efe7a6f40cbc
&From=sas
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeAlarmEventDetailResponse>
	  <Data>
		    <Uuid>47900178-885d-4fa4-9d77-XXXXXXXXXXXX</Uuid>
		    <AlarmEventAliasName>进程异常行为-Linux计划任务执行异常指令</AlarmEventAliasName>
		    <Type>进程异常行为</Type>
		    <InternetIp>10.0.0.10</InternetIp>
		    <AlarmEventDesc>黑客入侵服务器后，为了让恶意后门程序能持久化运行，黑客常常将恶意SHELL脚本写入crontab、systemd等计划任务。</AlarmEventDesc>
		    <IntranetIp>10.0.0.0</IntranetIp>
		    <CauseDetails>
			      <Value>
				        <Type>text</Type>
				        <Value>黑客登录ECS后通过编辑文件方式 写WEBSHELL</Value>
				        <Name>入侵原因</Name>
			      </Value>
			      <Value>
				        <Type>text</Type>
				        <Value>2018-11-16 19:09:02</Value>
				        <Name>攻击时间</Name>
			      </Value>
			      <Value>
				        <Type>text</Type>
				        <Value>N/A</Value>
				        <Name>攻击源IP</Name>
			      </Value>
			      <Value>
				        <Type>text</Type>
				        <Value>N/A</Value>
				        <Name>漏洞攻击载荷</Name>
			      </Value>
			      <Value>
				        <Type>text</Type>
				        <Value>请根据上述信息排查您的WEB服务被利用的页面及参数是否存在漏洞，并及时修复。</Value>
				        <Name>排查方案</Name>
			      </Value>
			      <Key>item</Key>
		    </CauseDetails>
		    <Level>serious</Level>
		    <EndTime>1543741201000</EndTime>
		    <StartTime>1543312803000</StartTime>
		    <CanBeDealOnLine>false</CanBeDealOnLine>
		    <InstanceName>server01</InstanceName>
	  </Data>
	  <RequestId>5A1DDB3C-798C-4A84-BF6E-3DC7F7D7EB4A</RequestId>
    </DescribeAlarmEventDetailResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"Data":{
		"Uuid":"47900178-885d-4fa4-9d77-XXXXXXXXXXXX",
		"AlarmEventDesc":"黑客入侵服务器后，为了让恶意后门程序能持久化运行，黑客常常将恶意SHELL脚本写入crontab、systemd等计划任务。",
		"AlarmEventAliasName":"进程异常行为-Linux计划任务执行异常指令",
		"Type":"进程异常行为",
		"IntranetIp":"10.0.0.0",
		"CauseDetails":[
			{
				"Value":[
					{
						"Name":"入侵原因",
						"Value":"黑客登录ECS后通过编辑文件方式 写WEBSHELL",
						"Type":"text"
					},
					{
						"Name":"攻击时间",
						"Value":"2018-11-16 19:09:02",
						"Type":"text"
					},
					{
						"Name":"攻击源IP",
						"Value":"N/A",
						"Type":"text"
					},
					{
						"Name":"漏洞攻击载荷",
						"Value":"N/A",
						"Type":"text"
					},
					{
						"Name":"排查方案",
						"Value":"请根据上述信息排查您的WEB服务被利用的页面及参数是否存在漏洞，并及时修复。",
						"Type":"text"
					}
				],
				"Key":"item"
			}
		],
		"InternetIp":"10.0.0.10",
		"EndTime":1543741201000,
		"Level":"serious",
		"StartTime":1543312803000,
		"CanBeDealOnLine":false,
		"InstanceName":"server01"
	},
	"RequestId":"5A1DDB3C-798C-4A84-BF6E-3DC7F7D7EB4A"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/Sas)查看更多错误码。

