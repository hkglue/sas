# DescribeCheckWarningSummary {#doc_api_Sas_DescribeCheckWarningSummary .reference}

查看基线检查结果统计。

调用DescribeCheckWarningSummary接口，可查看基线检查的结果统计情况，包含检查的服务器数量、基线检查项数量、最近检查通过率等。

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Sas&api=DescribeCheckWarningSummary)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeCheckWarningSummary|系统规定参数。

 取值：DescribeCheckWarningSummary

 |
|CurrentPage|Integer|否|1|分页页码。

 |
|Lang|String|否|zh|语言。

 |
|PageSize|Integer|否|10|分页大小。

 |
|RiskName|String|否|Redis安全基线检查|基线检查风险项名称。

 |
|RiskStatus|Integer|否|1|基线检查的状态。

 -   1：未通过
-   3：已通过

 |
|SourceIp|String|否|127.0.0.1|来源IP。

 |
|Status|String|否|1|检查项状态。

 -   1：未通过
-   2：验证中
-   3：已通过
-   5：已失效
-   6：已忽略

 |
|StrategyId|Long|否|1|策略ID。

 |
|TypeName|String|否|database|基线一级类型。

 |
|Uuids|String|否|f03259d8-1e81-4fae-bcbb-275fb5\*\*\*\*\*\*|机器ID。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Count|Integer|10|当前检测项条数。

 |
|CurrentPage|Integer|1|当前页。

 |
|PageSize|Integer|10|每页条数。

 |
|RequestId|String|00BD7CE2-284A-4534-BD09-FB69836DD750|请求ID。

 |
|TotalCount|Integer|100|基线检查项的总数。

 |
|WarningSummarys| | |检查项统计明细。

 |
|CheckCount|Integer|10|基线检查项个数。

 |
|HighWarningCount|Integer|1|高危检查项个数。

 |
|LastFoundTime|String|2019-01-01 12:23:00|最近执行基线检查的时间。

 |
|Level|String|high|基线检查风险项的危险等级。

 包含以下等级：

 -高危

 -中危

 -低危

 |
|LowWarningCount|Integer|3|低危检查项的个数。

 |
|MediumWarningCount|Integer|2|中危检查项的个数。

 |
|RiskId|Long|1|风险项ID。

 |
|RiskName|String|Redis密码检查|基线检查风险项名称。

 |
|SubTypeAlias|String|Redis检查|风险项二级分类。

 |
|TypeAlias|String|数据库|基线检查项的分类，例如：数据库、系统、弱密码检测和中间件。

 |
|WarningMachineCount|Integer|11|检测出基线风险项的资产的数量。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeCheckWarningSummary
&Lang=zh
&TypeName=database
&Status=1
&RiskStatus=1
&RiskName=Redis安全基线检查
&StrategyId=1
&Uuids=f03259d8-1e81-4fae-bcbb-275fb55efb34
&CurrentPage=1
&PageSize=20
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeCheckWarningSummary>
  <TotalCount>25</TotalCount>
  <PageSize>20</PageSize>
  <RequestId>DFA6CDC5-E826-4D18-A499-BEF9DA31F1AD</RequestId>
  <CurrentPage>1</CurrentPage>
  <Count>20</Count>
  <WarningSummarys>
    <RiskId>43</RiskId>
    <LastFoundTime>2019-04-10 00:33:00</LastFoundTime>
    <MediumWarningCount>0</MediumWarningCount>
    <WarningMachineCount>3</WarningMachineCount>
    <CheckCount>16</CheckCount>
    <HighWarningCount>8</HighWarningCount>
    <Level>high</Level>
    <TypeAlias>系统</TypeAlias>
    <SubTypeAlias>
			CentOS Linux 7安全基线检查
			
		                            </SubTypeAlias>
    <LowWarningCount>0</LowWarningCount>
    <RiskName>
			CentOS Linux 7安全基线检查
			
		                            </RiskName>
  </WarningSummarys>
  <WarningSummarys>
    <RiskId>47</RiskId>
    <LastFoundTime>2019-04-10 00:58:11</LastFoundTime>
    <MediumWarningCount>0</MediumWarningCount>
    <WarningMachineCount>2</WarningMachineCount>
    <CheckCount>15</CheckCount>
    <HighWarningCount>7</HighWarningCount>
    <Level>medium</Level>
    <TypeAlias>系统</TypeAlias>
    <SubTypeAlias>CentOS Linux 7合规基线检查-等保三级</SubTypeAlias>
    <LowWarningCount>0</LowWarningCount>
    <RiskName>CentOS Linux 7合规基线检查-等保三级</RiskName>
  </WarningSummarys>
  <WarningSummarys>
    <RiskId>48</RiskId>
    <LastFoundTime>2019-04-10 00:58:11</LastFoundTime>
    <MediumWarningCount>0</MediumWarningCount>
    <WarningMachineCount>2</WarningMachineCount>
    <CheckCount>12</CheckCount>
    <HighWarningCount>6</HighWarningCount>
    <Level>medium</Level>
    <TypeAlias>系统</TypeAlias>
    <SubTypeAlias>CentOS Linux 7合规基线检查-等保二级</SubTypeAlias>
    <LowWarningCount>0</LowWarningCount>
    <RiskName>CentOS Linux 7合规基线检查-等保二级</RiskName>
  </WarningSummarys>
  <WarningSummarys>
    <RiskId>3</RiskId>
    <LastFoundTime>2019-04-10 08:31:32</LastFoundTime>
    <MediumWarningCount>0</MediumWarningCount>
    <WarningMachineCount>1</WarningMachineCount>
    <CheckCount>1</CheckCount>
    <HighWarningCount>1</HighWarningCount>
    <Level>high</Level>
    <TypeAlias>数据库</TypeAlias>
    <SubTypeAlias>Redis安全基线检查</SubTypeAlias>
    <LowWarningCount>0</LowWarningCount>
    <RiskName>Redis安全基线检查</RiskName>
  </WarningSummarys>
  <WarningSummarys>
    <RiskId>19</RiskId>
    <LastFoundTime>2019-04-10 08:31:32</LastFoundTime>
    <MediumWarningCount>0</MediumWarningCount>
    <WarningMachineCount>1</WarningMachineCount>
    <CheckCount>1</CheckCount>
    <HighWarningCount>1</HighWarningCount>
    <Level>high</Level>
    <TypeAlias>弱密码检测</TypeAlias>
    <SubTypeAlias>Linux系统登录弱口令检测</SubTypeAlias>
    <LowWarningCount>0</LowWarningCount>
    <RiskName>Linux系统登录弱口令检测</RiskName>
  </WarningSummarys>
  <WarningSummarys>
    <RiskId>12</RiskId>
    <LastFoundTime>2019-04-10 08:31:32</LastFoundTime>
    <MediumWarningCount>0</MediumWarningCount>
    <WarningMachineCount>1</WarningMachineCount>
    <CheckCount>1</CheckCount>
    <HighWarningCount>1</HighWarningCount>
    <Level>high</Level>
    <TypeAlias>弱密码检测</TypeAlias>
    <SubTypeAlias>FTP匿名登录配置检测</SubTypeAlias>
    <LowWarningCount>0</LowWarningCount>
    <RiskName>FTP匿名登录配置检测</RiskName>
  </WarningSummarys>
  <WarningSummarys>
    <RiskId>13</RiskId>
    <LastFoundTime>2019-04-10 06:58:58</LastFoundTime>
    <MediumWarningCount>0</MediumWarningCount>
    <WarningMachineCount>1</WarningMachineCount>
    <CheckCount>1</CheckCount>
    <HighWarningCount>1</HighWarningCount>
    <Level>high</Level>
    <TypeAlias>弱密码检测</TypeAlias>
    <SubTypeAlias>Windows系统登录弱口令检测</SubTypeAlias>
    <LowWarningCount>0</LowWarningCount>
    <RiskName>Windows系统登录弱口令检测</RiskName>
  </WarningSummarys>
  <WarningSummarys>
    <RiskId>23</RiskId>
    <LastFoundTime>2019-04-10 14:00:17</LastFoundTime>
    <MediumWarningCount>0</MediumWarningCount>
    <WarningMachineCount>0</WarningMachineCount>
    <CheckCount>8</CheckCount>
    <HighWarningCount>0</HighWarningCount>
    <Level>medium</Level>
    <TypeAlias>中间件</TypeAlias>
    <SubTypeAlias>Apache Tomcat 安全基线检查</SubTypeAlias>
    <LowWarningCount>0</LowWarningCount>
    <RiskName>Apache Tomcat 安全基线检查</RiskName>
  </WarningSummarys>
  <WarningSummarys>
    <RiskId>2</RiskId>
    <LastFoundTime>2019-04-10 08:31:32</LastFoundTime>
    <MediumWarningCount>0</MediumWarningCount>
    <WarningMachineCount>0</WarningMachineCount>
    <CheckCount>1</CheckCount>
    <HighWarningCount>0</HighWarningCount>
    <Level>high</Level>
    <TypeAlias>弱密码检测</TypeAlias>
    <SubTypeAlias>PostgreSQL弱密码检测</SubTypeAlias>
    <LowWarningCount>0</LowWarningCount>
    <RiskName>PostgreSql登录弱口令检测</RiskName>
  </WarningSummarys>
  <WarningSummarys>
    <RiskId>11</RiskId>
    <LastFoundTime>2019-04-10 08:31:32</LastFoundTime>
    <MediumWarningCount>0</MediumWarningCount>
    <WarningMachineCount>0</WarningMachineCount>
    <CheckCount>1</CheckCount>
    <HighWarningCount>0</HighWarningCount>
    <Level>high</Level>
    <TypeAlias>弱密码检测</TypeAlias>
    <SubTypeAlias>MySQL弱密码检测</SubTypeAlias>
    <LowWarningCount>0</LowWarningCount>
    <RiskName>MySQL弱密码检测</RiskName>
  </WarningSummarys>
  <WarningSummarys>
    <RiskId>20</RiskId>
    <LastFoundTime>2019-04-10 08:31:32</LastFoundTime>
    <MediumWarningCount>0</MediumWarningCount>
    <WarningMachineCount>0</WarningMachineCount>
    <CheckCount>1</CheckCount>
    <HighWarningCount>0</HighWarningCount>
    <Level>high</Level>
    <TypeAlias>弱密码检测</TypeAlias>
    <SubTypeAlias>FTP登陆弱口令检测</SubTypeAlias>
    <LowWarningCount>0</LowWarningCount>
    <RiskName>FTP登陆弱口令检测</RiskName>
  </WarningSummarys>
  <WarningSummarys>
    <RiskId>17</RiskId>
    <LastFoundTime>2019-04-10 06:58:58</LastFoundTime>
    <MediumWarningCount>0</MediumWarningCount>
    <WarningMachineCount>0</WarningMachineCount>
    <CheckCount>1</CheckCount>
    <HighWarningCount>0</HighWarningCount>
    <Level>high</Level>
    <TypeAlias>弱密码检测</TypeAlias>
    <SubTypeAlias>Microsoft SQL Server弱密码检测</SubTypeAlias>
    <LowWarningCount>0</LowWarningCount>
    <RiskName>Microsoft SQL Server登录弱口令检测</RiskName>
  </WarningSummarys>
  <WarningSummarys>
    <RiskId>24</RiskId>
    <LastFoundTime>2019-04-10 06:52:05</LastFoundTime>
    <MediumWarningCount>0</MediumWarningCount>
    <WarningMachineCount>0</WarningMachineCount>
    <CheckCount>2</CheckCount>
    <HighWarningCount>0</HighWarningCount>
    <Level>medium</Level>
    <TypeAlias>数据库</TypeAlias>
    <SubTypeAlias>Memcached安全基线检查</SubTypeAlias>
    <LowWarningCount>0</LowWarningCount>
    <RiskName>Memcached安全基线检查</RiskName>
  </WarningSummarys>
  <WarningSummarys>
    <RiskId>42</RiskId>
    <LastFoundTime>2019-02-19 14:59:17</LastFoundTime>
    <MediumWarningCount>0</MediumWarningCount>
    <WarningMachineCount>0</WarningMachineCount>
    <CheckCount>16</CheckCount>
    <HighWarningCount>0</HighWarningCount>
    <Level>high</Level>
    <TypeAlias>系统</TypeAlias>
    <SubTypeAlias>CentOS Linux 6安全基线检查</SubTypeAlias>
    <LowWarningCount>0</LowWarningCount>
    <RiskName>CentOS Linux 6安全基线检查</RiskName>
  </WarningSummarys>
  <WarningSummarys>
    <RiskId>49</RiskId>
    <LastFoundTime>2019-02-19 14:59:17</LastFoundTime>
    <MediumWarningCount>0</MediumWarningCount>
    <WarningMachineCount>0</WarningMachineCount>
    <CheckCount>12</CheckCount>
    <HighWarningCount>0</HighWarningCount>
    <Level>medium</Level>
    <TypeAlias>系统</TypeAlias>
    <SubTypeAlias>CentOS Linux 6合规基线检查-等保二级</SubTypeAlias>
    <LowWarningCount>0</LowWarningCount>
    <RiskName>CentOS Linux 6合规基线检查-等保二级</RiskName>
  </WarningSummarys>
  <WarningSummarys>
    <RiskId>50</RiskId>
    <LastFoundTime>2019-02-19 14:59:17</LastFoundTime>
    <MediumWarningCount>0</MediumWarningCount>
    <WarningMachineCount>0</WarningMachineCount>
    <CheckCount>15</CheckCount>
    <HighWarningCount>0</HighWarningCount>
    <Level>medium</Level>
    <TypeAlias>系统</TypeAlias>
    <SubTypeAlias>CentOS Linux 6合规基线检查-等保三级</SubTypeAlias>
    <LowWarningCount>0</LowWarningCount>
    <RiskName>CentOS Linux 6合规基线检查-等保三级</RiskName>
  </WarningSummarys>
  <WarningSummarys>
    <RiskId>55</RiskId>
    <LastFoundTime>2019-02-19 12:57:23</LastFoundTime>
    <MediumWarningCount>0</MediumWarningCount>
    <WarningMachineCount>0</WarningMachineCount>
    <CheckCount>14</CheckCount>
    <HighWarningCount>0</HighWarningCount>
    <Level>medium</Level>
    <TypeAlias>系统</TypeAlias>
    <SubTypeAlias>Linux Ubuntu合规基线检查-等保二级</SubTypeAlias>
    <LowWarningCount>0</LowWarningCount>
    <RiskName>Linux Ubuntu合规基线检查-等保二级</RiskName>
  </WarningSummarys>
  <WarningSummarys>
    <RiskId>56</RiskId>
    <LastFoundTime>2019-02-19 12:57:23</LastFoundTime>
    <MediumWarningCount>0</MediumWarningCount>
    <WarningMachineCount>0</WarningMachineCount>
    <CheckCount>15</CheckCount>
    <HighWarningCount>0</HighWarningCount>
    <Level>medium</Level>
    <TypeAlias>系统</TypeAlias>
    <SubTypeAlias>Linux Ubuntu合规基线检查-等保三级</SubTypeAlias>
    <LowWarningCount>0</LowWarningCount>
    <RiskName>Linux Ubuntu合规基线检查-等保三级</RiskName>
  </WarningSummarys>
  <WarningSummarys>
    <RiskId>54</RiskId>
    <LastFoundTime>2019-02-19 12:57:23</LastFoundTime>
    <MediumWarningCount>0</MediumWarningCount>
    <WarningMachineCount>0</WarningMachineCount>
    <CheckCount>16</CheckCount>
    <HighWarningCount>0</HighWarningCount>
    <Level>high</Level>
    <TypeAlias>系统</TypeAlias>
    <SubTypeAlias>Linux Ubuntu 安全基线检查</SubTypeAlias>
    <LowWarningCount>0</LowWarningCount>
    <RiskName>Linux Ubuntu 安全基线检查</RiskName>
  </WarningSummarys>
  <WarningSummarys>
    <RiskId>51</RiskId>
    <LastFoundTime>2019-02-19 12:44:58</LastFoundTime>
    <MediumWarningCount>0</MediumWarningCount>
    <WarningMachineCount>0</WarningMachineCount>
    <CheckCount>12</CheckCount>
    <HighWarningCount>0</HighWarningCount>
    <Level>high</Level>
    <TypeAlias>系统</TypeAlias>
    <SubTypeAlias>Windows 2012 R2安全基线检查</SubTypeAlias>
    <LowWarningCount>0</LowWarningCount>
    <RiskName>Windows 2012 R2安全基线检查</RiskName>
  </WarningSummarys>
</DescribeCheckWarningSummary>

```

`JSON` 格式

``` {#json_return_success_demo}
{
	"Count":20,
	"TotalCount":25,
	"WarningSummarys":[
		{
			"SubTypeAlias":"CentOS Linux 7安全基线检查\n                                \n                            ",
			"HighWarningCount":8,
			"WarningMachineCount":3,
			"RiskName":"CentOS Linux 7安全基线检查\n                                \n                            ",
			"LowWarningCount":0,
			"CheckCount":16,
			"RiskId":43,
			"Level":"high",
			"MediumWarningCount":0,
			"TypeAlias":"系统",
			"LastFoundTime":"2019-04-10 00:33:00"
		},
		{
			"SubTypeAlias":"CentOS Linux 7合规基线检查-等保三级",
			"HighWarningCount":7,
			"WarningMachineCount":2,
			"RiskName":"CentOS Linux 7合规基线检查-等保三级",
			"LowWarningCount":0,
			"CheckCount":15,
			"RiskId":47,
			"Level":"medium",
			"MediumWarningCount":0,
			"TypeAlias":"系统",
			"LastFoundTime":"2019-04-10 00:58:11"
		},
		{
			"SubTypeAlias":"CentOS Linux 7合规基线检查-等保二级",
			"HighWarningCount":6,
			"WarningMachineCount":2,
			"RiskName":"CentOS Linux 7合规基线检查-等保二级",
			"LowWarningCount":0,
			"CheckCount":12,
			"RiskId":48,
			"Level":"medium",
			"MediumWarningCount":0,
			"TypeAlias":"系统",
			"LastFoundTime":"2019-04-10 00:58:11"
		},
		{
			"SubTypeAlias":"Redis安全基线检查",
			"HighWarningCount":1,
			"WarningMachineCount":1,
			"RiskName":"Redis安全基线检查",
			"LowWarningCount":0,
			"CheckCount":1,
			"RiskId":3,
			"Level":"high",
			"MediumWarningCount":0,
			"TypeAlias":"数据库",
			"LastFoundTime":"2019-04-10 08:31:32"
		},
		{
			"SubTypeAlias":"Linux系统登录弱口令检测",
			"HighWarningCount":1,
			"WarningMachineCount":1,
			"RiskName":"Linux系统登录弱口令检测",
			"LowWarningCount":0,
			"CheckCount":1,
			"RiskId":19,
			"Level":"high",
			"MediumWarningCount":0,
			"TypeAlias":"弱密码检测",
			"LastFoundTime":"2019-04-10 08:31:32"
		},
		{
			"SubTypeAlias":"FTP匿名登录配置检测",
			"HighWarningCount":1,
			"WarningMachineCount":1,
			"RiskName":"FTP匿名登录配置检测",
			"LowWarningCount":0,
			"CheckCount":1,
			"RiskId":12,
			"Level":"high",
			"MediumWarningCount":0,
			"TypeAlias":"弱密码检测",
			"LastFoundTime":"2019-04-10 08:31:32"
		},
		{
			"SubTypeAlias":"Windows系统登录弱口令检测",
			"HighWarningCount":1,
			"WarningMachineCount":1,
			"RiskName":"Windows系统登录弱口令检测",
			"LowWarningCount":0,
			"CheckCount":1,
			"RiskId":13,
			"Level":"high",
			"MediumWarningCount":0,
			"TypeAlias":"弱密码检测",
			"LastFoundTime":"2019-04-10 06:58:58"
		},
		{
			"SubTypeAlias":"Apache Tomcat 安全基线检查",
			"HighWarningCount":0,
			"WarningMachineCount":0,
			"RiskName":"Apache Tomcat 安全基线检查",
			"LowWarningCount":0,
			"CheckCount":8,
			"RiskId":23,
			"Level":"medium",
			"MediumWarningCount":0,
			"TypeAlias":"中间件",
			"LastFoundTime":"2019-04-10 14:00:17"
		},
		{
			"SubTypeAlias":"PostgreSQL弱密码检测",
			"HighWarningCount":0,
			"WarningMachineCount":0,
			"RiskName":"PostgreSql登录弱口令检测",
			"LowWarningCount":0,
			"CheckCount":1,
			"RiskId":2,
			"Level":"high",
			"MediumWarningCount":0,
			"TypeAlias":"弱密码检测",
			"LastFoundTime":"2019-04-10 08:31:32"
		},
		{
			"SubTypeAlias":"MySQL弱密码检测",
			"HighWarningCount":0,
			"WarningMachineCount":0,
			"RiskName":"MySQL弱密码检测",
			"LowWarningCount":0,
			"CheckCount":1,
			"RiskId":11,
			"Level":"high",
			"MediumWarningCount":0,
			"TypeAlias":"弱密码检测",
			"LastFoundTime":"2019-04-10 08:31:32"
		},
		{
			"SubTypeAlias":"FTP登陆弱口令检测",
			"HighWarningCount":0,
			"WarningMachineCount":0,
			"RiskName":"FTP登陆弱口令检测",
			"LowWarningCount":0,
			"CheckCount":1,
			"RiskId":20,
			"Level":"high",
			"MediumWarningCount":0,
			"TypeAlias":"弱密码检测",
			"LastFoundTime":"2019-04-10 08:31:32"
		},
		{
			"SubTypeAlias":"Microsoft SQL Server弱密码检测",
			"HighWarningCount":0,
			"WarningMachineCount":0,
			"RiskName":"Microsoft SQL Server登录弱口令检测",
			"LowWarningCount":0,
			"CheckCount":1,
			"RiskId":17,
			"Level":"high",
			"MediumWarningCount":0,
			"TypeAlias":"弱密码检测",
			"LastFoundTime":"2019-04-10 06:58:58"
		},
		{
			"SubTypeAlias":"Memcached安全基线检查",
			"HighWarningCount":0,
			"WarningMachineCount":0,
			"RiskName":"Memcached安全基线检查",
			"LowWarningCount":0,
			"CheckCount":2,
			"RiskId":24,
			"Level":"medium",
			"MediumWarningCount":0,
			"TypeAlias":"数据库",
			"LastFoundTime":"2019-04-10 06:52:05"
		},
		{
			"SubTypeAlias":"CentOS Linux 6安全基线检查",
			"HighWarningCount":0,
			"WarningMachineCount":0,
			"RiskName":"CentOS Linux 6安全基线检查",
			"LowWarningCount":0,
			"CheckCount":16,
			"RiskId":42,
			"Level":"high",
			"MediumWarningCount":0,
			"TypeAlias":"系统",
			"LastFoundTime":"2019-02-19 14:59:17"
		},
		{
			"SubTypeAlias":"CentOS Linux 6合规基线检查-等保二级",
			"HighWarningCount":0,
			"WarningMachineCount":0,
			"RiskName":"CentOS Linux 6合规基线检查-等保二级",
			"LowWarningCount":0,
			"CheckCount":12,
			"RiskId":49,
			"Level":"medium",
			"MediumWarningCount":0,
			"TypeAlias":"系统",
			"LastFoundTime":"2019-02-19 14:59:17"
		},
		{
			"SubTypeAlias":"CentOS Linux 6合规基线检查-等保三级",
			"HighWarningCount":0,
			"WarningMachineCount":0,
			"RiskName":"CentOS Linux 6合规基线检查-等保三级",
			"LowWarningCount":0,
			"CheckCount":15,
			"RiskId":50,
			"Level":"medium",
			"MediumWarningCount":0,
			"TypeAlias":"系统",
			"LastFoundTime":"2019-02-19 14:59:17"
		},
		{
			"SubTypeAlias":"Linux Ubuntu合规基线检查-等保二级",
			"HighWarningCount":0,
			"WarningMachineCount":0,
			"RiskName":"Linux Ubuntu合规基线检查-等保二级",
			"LowWarningCount":0,
			"CheckCount":14,
			"RiskId":55,
			"Level":"medium",
			"MediumWarningCount":0,
			"TypeAlias":"系统",
			"LastFoundTime":"2019-02-19 12:57:23"
		},
		{
			"SubTypeAlias":"Linux Ubuntu合规基线检查-等保三级",
			"HighWarningCount":0,
			"WarningMachineCount":0,
			"RiskName":"Linux Ubuntu合规基线检查-等保三级",
			"LowWarningCount":0,
			"CheckCount":15,
			"RiskId":56,
			"Level":"medium",
			"MediumWarningCount":0,
			"TypeAlias":"系统",
			"LastFoundTime":"2019-02-19 12:57:23"
		},
		{
			"SubTypeAlias":"Linux Ubuntu 安全基线检查",
			"HighWarningCount":0,
			"WarningMachineCount":0,
			"RiskName":"Linux Ubuntu 安全基线检查",
			"LowWarningCount":0,
			"CheckCount":16,
			"RiskId":54,
			"Level":"high",
			"MediumWarningCount":0,
			"TypeAlias":"系统",
			"LastFoundTime":"2019-02-19 12:57:23"
		},
		{
			"SubTypeAlias":"Windows 2012 R2安全基线检查",
			"HighWarningCount":0,
			"WarningMachineCount":0,
			"RiskName":"Windows 2012 R2安全基线检查",
			"LowWarningCount":0,
			"CheckCount":12,
			"RiskId":51,
			"Level":"high",
			"MediumWarningCount":0,
			"TypeAlias":"系统",
			"LastFoundTime":"2019-02-19 12:44:58"
		}
	],
	"PageSize":20,
	"RequestId":"DFA6CDC5-E826-4D18-A499-BEF9DA31F1AD",
	"CurrentPage":1
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/Sas)查看更多错误码。

