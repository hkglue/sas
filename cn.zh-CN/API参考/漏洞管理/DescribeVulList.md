# DescribeVulList {#doc_api_Sas_DescribeVulList .reference}

查询漏洞列表。

调用本接口查询漏洞列表。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Sas&api=DescribeVulList&type=RPC&version=2018-12-03)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeVulList|要执行的操作。

 取值：DescribeVulList

 |
|AliasName|String|否|RHSA-2019:0230-Important: polkit security update|漏洞别名。

 |
|CurrentPage|Integer|否|1|漏洞列表分页页码。

 起始值：1

 默认值：1

 |
|Dealed|String|否|n|漏洞是否处理。

 取值：

 -   y：已处理
-   n：未处理

 |
|Lang|String|否|zh|语言。

 取值：

 -   zh：中文
-   en：英文

 |
|Necessity|String|否|asap,later,nntf|漏洞修复必要性等级。多个等级用英文逗号分隔。

 取值：

 -   asap：高
-   later：中
-   nntf：低

 |
|PageSize|Integer|否|20|漏洞列表分页大小。

 默认值：20

 |
|Remark|String|否|192.168.1.1|查询标记，可以为资产内网IP、外网IP或资产名称。

 |
|Type|String|否|cve|漏洞类型，包括以下几类：

 -   cve：Linux软件漏洞
-   sys：Windows系统漏洞
-   cms：Web-CMS漏洞
-   app：应用漏洞
-   emg：应急漏洞

 |
|Uuids|String|否|1587bedb-fdb4-48c4-9330-\*\*\*\*\*\*\*\*\*\*\*\*|服务器UUID列表，多个用英文逗号分隔。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|ECDE6715-6286-40E6-A32D-3094051FD74D|请求ID。

 |
|CurrentPage|Integer|1|漏洞列表分页页码。

 |
|PageSize|Integer|20|分页大小。

 |
|TotalCount|Integer|2|查询结果总数。

 |
|VulRecords| | |漏洞列表。

 |
|AliasName|String|RHSA-2017:0574: gnutls security, bug fix, and enhancement update|漏洞别名。

 |
|ExtendContentJson| | |扩展信息。

 |
|AbsolutePath|String|/roo/www/web|绝对路径。

 |
|AliasName|String|RHSA-2017:0574: gnutls security, bug fix, and enhancement update|漏洞别名。

 |
|LastTs|Long|1554189334000|最后发现时间。

 |
|Necessity| | |漏洞修复必要性。

 |
|Assets\_factor|String|1|资产因子。

 |
|Cvss\_factor|String|7.8|CVSS因子。

 |
|Enviroment\_factor|String|1.0|环境因子。

 |
|Gmt\_create|String|20190331|创建时间。

 |
|Is\_calc|String|1|是否计算出分数。

 -   0：未计算
-   1：已计算

 |
|Status|String|normal|状态。

 取值：

 -   none：未生成分数
-   pending：等待计算中
-   miss：未计算出分数
-   normal：正常

 |
|Time\_factor|String|1.0|时间因子。

 |
|Total\_score|String|7.8|总分。

 |
|Os|String|centos|操作系统。

 |
|OsRelease|String|7|操作系统release。

 |
|PrimaryId|Long|111|漏洞ID。

 |
|RpmEntityList| | |RPM包列表。

 |
|FullVersion|String|3.10.0-693.2.2.el7|完整版本号。

 |
|MatchDetail|String|python-perf version less than 0:3.10.0-693.21.1.el7|匹配细节

 |
|Name|String|python-perf|RPM名称。

 |
|Path|String|/usr/lib64/python2.7/site-packages|路径。

 |
|UpdateCmd|String|yum update python-perf|修复命令。

 |
|Version|String|3.10.0|版本号。

 |
|Status|Integer|1|漏洞状态。

 取值：

 -   1：未修复
-   2：修复失败
-   3：回滚失败
-   4：修复中
-   5：回滚中
-   6：验证中
-   7：修复成功
-   8：修复成功待重启
-   9：回滚成功
-   10：已忽略
-   11：回滚成功待重启
-   12：漏洞不存在
-   20：已失效

 |
|Tag|String|oval|漏洞标签。

 |
|cveList| |\["CVE-2016-8610", "CVE-2017-5335" \]|CVE列表。

 |
|FirstTs|Long|1554189334000|首次发现时间，时间戳。

 |
|GroupId|Integer|281801|资产分组ID。

 |
|InstanceId|String|i-bp18tnigcymjvmc2fw9e|资产实例ID。

 |
|InstanceName|String|测试ECS|资产实例名称。

 |
|InternetIp|String|47.99.0.0|资产外网IP。

 |
|IntranetIp|String|192.1.1.1|资产内网IP。

 |
|Ip|String|47.99.0.0|资产IP，优先显示外网IP。

 |
|LastTs|Long|1541207563000|最后发现时间，时间戳。

 |
|ModifyTs|Long|1541207563000|修改时间，时间戳。

 |
|Name|String|oval:com.redhat.rhsa:def:20170574|漏洞名称。

 |
|Necessity|String|asap|漏洞修复必要性。

 -   asap：高
-   later：中
-   nntf：低

 |
|NeedReboot|String|yes|是否需要重启。

 -   yes：是
-   no：否

 |
|OsVersion|String|linux|操作系统版本。

 |
|PrimaryId|Long|101162078|漏洞ID。

 |
|Related|String|CVE-2017-7518,CVE-2017-12188|漏洞关联CVE列表，多个用英文逗号分隔。

 |
|RepairTs|Long|1541207563000|修复时间，时间戳。

 |
|ResultCode|String|0|修复返回码。

 |
|ResultMessage|String|timeout|修复返回消息。

 |
|Status|Integer|1|漏洞状态。

 -   1：未修复
-   2：修复失败
-   3：回滚失败
-   4：修复中
-   5：回滚中
-   6：验证中
-   7：修复成功
-   8：修复成功待重启
-   9：回滚成功
-   10：已忽略
-   11：回滚成功待重启
-   12：漏洞不存在
-   20：已失效

 |
|Tag|String|oval|漏洞标签。

 |
|Type|String|cve|漏洞类型，包含以下类型：

 -   cve：Linux漏洞
-   sys：Windows漏洞
-   cms：WebCMS漏洞
-   emg：应急漏洞
-   app：应用漏洞

 |
|Uuid|String|04c56617-23fc-43a5-ab9b-\*\*\*\*\*\*\*\*\*\*\*\*|资产UUID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeVulList
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeVulList>
	  <TotalCount>6430</TotalCount>
	  <PageSize>2</PageSize>
	  <RequestId>ECDE6715-6286-40E6-A32D-3094051FD74D</RequestId>
	  <CurrentPage>1</CurrentPage>
	  <VulRecords>
		    <Necessity>asap</Necessity>
		    <Uuid>04c56617-23fc-43a5-ab9b-755da574ffe8</Uuid>
		    <Ip>47.99.63.178</Ip>
		    <ModifyTs>1541347310000</ModifyTs>
		    <Type>cve</Type>
		    <FirstTs>1541207563000</FirstTs>
		    <InstanceId>i-bp18tnigcymjvmc2fw9e</InstanceId>
		    <InternetIp>47.99.63.178</InternetIp>
		    <ResultMessage>
			out:Loaded plugins: security
			Setting up Update Process
			Resolving Dependencies
			--&gt; Running transaction check
			---&gt; Package gnutls.x86_64 0:2.8.5-14.el6_5 will be updated
			---&gt; Package gnutls.x86_64 0:2.12.23-22.el6 will be an update
			--&gt; Finished Dependency Resolution
			
			Dependencies Resolved
			
			================================================================================
			 Package         Arch            Version                    Repository     Size
			================================================================================
			Updating:
			 gnutls          x86_64          2.12.23-22.el6             base          389 k
			
			Transaction Summary
			================================================================================
			Upgrade       1 Package(s)
			
			Total download size: 389 k
			Downloading Packages:
			Running rpm_check_debug
			Running Transaction Test
			Transaction Test Succeeded
			Running Transaction
			
Updating   : gnutls-2.12.23-22.el6.x86_64                                 1/2
			
Cleanup    : gnutls-2.8.5-14.el6_5.x86_64                                 2/2
			
Verifying  : gnutls-2.12.23-22.el6.x86_64                                 1/2
			
Verifying  : gnutls-2.8.5-14.el6_5.x86_64                                 2/2
			
			Updated:
			gnutls.x86_64 0:2.12.23-22.el6                                               
			
			Complete!
			
		err:</ResultMessage>
		    <Related>CVE-2016-8610,CVE-2017-5335,CVE-2017-5336,CVE-2017-5337</Related>
		    <GroupId>281801</GroupId>
		    <OsVersion>linux</OsVersion>
		    <ExtendContentJson>
			      <Necessity>
				        <Status>pending</Status>
			      </Necessity>
			      <Os>centos</Os>
			      <cveList>CVE-2016-8610</cveList>
			      <cveList>CVE-2017-5335</cveList>
			      <cveList>CVE-2017-5336</cveList>
			      <cveList>CVE-2017-5337</cveList>
			      <RpmEntityList>
				        <Name>gnutls</Name>
				        <Version>2.8.5</Version>
				        <FullVersion>2.8.5-14.el6_5</FullVersion>
				        <MatchDetail>gnutls version less than 0:2.12.23-21.el6</MatchDetail>
				        <UpdateCmd>yum update gnutls</UpdateCmd>
				        <Path>/usr/lib64/libgnutls-extra.so.26</Path>
			      </RpmEntityList>
			      <OsRelease>6</OsRelease>
		    </ExtendContentJson>
		    <Name>oval:com.redhat.rhsa:def:20170574</Name>
		    <Status>7</Status>
		    <LastTs>1541207563000</LastTs>
		    <NeedReboot>no</NeedReboot>
		    <AliasName>RHSA-2017:0574: gnutls security, bug fix, and enhancement update</AliasName>
		    <Tag>oval</Tag>
		    <IntranetIp>10.0.0.173</IntranetIp>
		    <PrimaryId>101162078</PrimaryId>
		    <ResultCode>0</ResultCode>
		    <Level>serious</Level>
		    <InstanceName>雷鹰测试-Aegis123456789</InstanceName>
	  </VulRecords>
	  <VulRecords>
		    <Necessity>later</Necessity>
		    <Uuid>1bfac26f-0301-435e-bcfd-2cdbd271c8a1</Uuid>
		    <Ip>172.19.220.94</Ip>
		    <ModifyTs>1554096622000</ModifyTs>
		    <Type>cve</Type>
		    <FirstTs>1550891785000</FirstTs>
		    <InstanceId>i-uf6iywlcvu7n0v8er15l</InstanceId>
		    <InternetIp></InternetIp>
		    <Related>CVE-2017-7518,CVE-2017-12188</Related>
		    <GroupId>281801</GroupId>
		    <OsVersion>linux</OsVersion>
		    <ExtendContentJson>
			      <Necessity>
				        <Cvss_factor>7.8</Cvss_factor>
				        <Total_score>7.8</Total_score>
				        <Status>normal</Status>
				        <Enviroment_factor>1.0</Enviroment_factor>
				        <Time_factor>1.0</Time_factor>
				        <Assets_factor>1</Assets_factor>
				        <Gmt_create>20190331</Gmt_create>
				        <Is_calc>1</Is_calc>
			      </Necessity>
			      <Os>centos</Os>
			      <cveList>CVE-2017-7518</cveList>
			      <cveList>CVE-2017-12188</cveList>
			      <RpmEntityList>
				        <Name>kernel</Name>
				        <Version>3.10.0</Version>
				        <FullVersion>3.10.0-693.2.2.el7</FullVersion>
				        <MatchDetail>kernel version less than 0:3.10.0-693.21.1.el7</MatchDetail>
				        <UpdateCmd>yum update kernel</UpdateCmd>
				        <Path>/boot/.vmlinuz-3.10.0-693.2.2.el7.x86_64.hmac</Path>
			      </RpmEntityList>
			      <RpmEntityList>
				        <Name>kernel-headers</Name>
				        <Version>3.10.0</Version>
				        <FullVersion>3.10.0-693.2.2.el7</FullVersion>
				        <MatchDetail>kernel-headers version less than 0:3.10.0-693.21.1.el7</MatchDetail>
				        <UpdateCmd>yum update kernel-headers</UpdateCmd>
				        <Path>/usr/include/asm</Path>
			      </RpmEntityList>
			      <RpmEntityList>
				        <Name>kernel-tools</Name>
				        <Version>3.10.0</Version>
				        <FullVersion>3.10.0-693.2.2.el7</FullVersion>
				        <MatchDetail>kernel-tools version less than 0:3.10.0-693.21.1.el7</MatchDetail>
				        <UpdateCmd>yum update kernel-tools</UpdateCmd>
				        <Path>/etc/sysconfig/cpupower</Path>
			      </RpmEntityList>
			      <RpmEntityList>
				        <Name>kernel-tools-libs</Name>
				        <Version>3.10.0</Version>
				        <FullVersion>3.10.0-693.2.2.el7</FullVersion>
				        <MatchDetail>kernel-tools-libs version less than 0:3.10.0-693.21.1.el7</MatchDetail>
				        <UpdateCmd>yum update kernel-tools-libs</UpdateCmd>
				        <Path>/usr/lib64/libcpupower.so.0</Path>
			      </RpmEntityList>
			      <RpmEntityList>
				        <Name>python-perf</Name>
				        <Version>3.10.0</Version>
				        <FullVersion>3.10.0-693.2.2.el7</FullVersion>
				        <MatchDetail>python-perf version less than 0:3.10.0-693.21.1.el7</MatchDetail>
				        <UpdateCmd>yum update python-perf</UpdateCmd>
				        <Path>/usr/lib64/python2.7/site-packages</Path>
			      </RpmEntityList>
			      <OsRelease>7</OsRelease>
		    </ExtendContentJson>
		    <Name>oval:com.redhat.rhsa:def:20180395</Name>
		    <Status>1</Status>
		    <LastTs>1554096622000</LastTs>
		    <NeedReboot>yes</NeedReboot>
		    <AliasName>RHSA-2018:0395-Important: kernel security and bug fix update</AliasName>
		    <Tag>oval</Tag>
		    <IntranetIp>172.19.0.0</IntranetIp>
		    <PrimaryId>160191232</PrimaryId>
		    <Level>low</Level>
		    <InstanceName>master-03-k8s-for-cs-cce881ec0ec77435e8e21bb52d1178e2a</InstanceName>
	  </VulRecords>
    </DescribeVulList>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"TotalCount":6430,
	"PageSize":2,
	"RequestId":"ECDE6715-6286-40E6-A32D-3094051FD74D",
	"CurrentPage":1,
	"VulRecords":[
		{
			"Necessity":"asap",
			"Uuid":"04c56617-23fc-43a5-ab9b-755da574ffe8",
			"Ip":"47.99.63.178",
			"ModifyTs":1541347310000,
			"Type":"cve",
			"FirstTs":1541207563000,
			"InstanceId":"i-bp18tnigcymjvmc2fw9e",
			"InternetIp":"47.99.63.178",
			"ResultMessage":"out:Loaded plugins: security\nSetting up Update Process\nResolving Dependencies\n--> Running transaction check\n---> Package gnutls.x86_64 0:2.8.5-14.el6_5 will be updated\n---> Package gnutls.x86_64 0:2.12.23-22.el6 will be an update\n--> Finished Dependency Resolution\n\nDependencies Resolved\n\n================================================================================\n Package         Arch            Version                    Repository     Size\n================================================================================\nUpdating:\n gnutls          x86_64          2.12.23-22.el6             base          389 k\n\nTransaction Summary\n================================================================================\nUpgrade       1 Package(s)\n\nTotal download size: 389 k\nDownloading Packages:\nRunning rpm_check_debug\nRunning Transaction Test\nTransaction Test Succeeded\nRunning Transaction\n\r  Updating   : gnutls-2.12.23-22.el6.x86_64                                 1/2 \n\r  Cleanup    : gnutls-2.8.5-14.el6_5.x86_64                                 2/2 \n\r  Verifying  : gnutls-2.12.23-22.el6.x86_64                                 1/2 \n\r  Verifying  : gnutls-2.8.5-14.el6_5.x86_64                                 2/2 \n\nUpdated:\n  gnutls.x86_64 0:2.12.23-22.el6                                                \n\nComplete!\n\nerr:",
			"Related":"CVE-2016-8610,CVE-2017-5335,CVE-2017-5336,CVE-2017-5337",
			"GroupId":281801,
			"OsVersion":"linux",
			"Name":"oval:com.redhat.rhsa:def:20170574",
			"ExtendContentJson":{
				"Os":"centos",
				"Necessity":{
					"Status":"pending"
				},
				"cveList":[
					"CVE-2016-8610",
					"CVE-2017-5335",
					"CVE-2017-5336",
					"CVE-2017-5337"
				],
				"RpmEntityList":[
					{
						"Name":"gnutls",
						"FullVersion":"2.8.5-14.el6_5",
						"Version":"2.8.5",
						"MatchDetail":"gnutls version less than 0:2.12.23-21.el6",
						"Path":"/usr/lib64/libgnutls-extra.so.26",
						"UpdateCmd":"yum update gnutls"
					}
				],
				"OsRelease":"6"
			},
			"Status":7,
			"LastTs":1541207563000,
			"NeedReboot":"no",
			"AliasName":"RHSA-2017:0574: gnutls security, bug fix, and enhancement update",
			"Tag":"oval",
			"PrimaryId":101162078,
			"IntranetIp":"10.0.0.173",
			"ResultCode":"0",
			"Level":"serious",
			"InstanceName":"雷鹰测试-Aegis123456789"
		},
		{
			"Necessity":"later",
			"Uuid":"1bfac26f-0301-435e-bcfd-2cdbd271c8a1",
			"Ip":"172.19.220.94",
			"ModifyTs":1554096622000,
			"Type":"cve",
			"FirstTs":1550891785000,
			"InstanceId":"i-uf6iywlcvu7n0v8er15l",
			"InternetIp":"",
			"Related":"CVE-2017-7518,CVE-2017-12188",
			"GroupId":281801,
			"OsVersion":"linux",
			"ExtendContentJson":{
				"Os":"centos",
				"Necessity":{
					"Cvss_factor":"7.8",
					"Status":"normal",
					"Total_score":"7.8",
					"Enviroment_factor":"1.0",
					"Assets_factor":"1",
					"Time_factor":"1.0",
					"Gmt_create":"20190331",
					"Is_calc":"1"
				},
				"cveList":[
					"CVE-2017-7518",
					"CVE-2017-12188"
				],
				"RpmEntityList":[
					{
						"Name":"kernel",
						"FullVersion":"3.10.0-693.2.2.el7",
						"Version":"3.10.0",
						"MatchDetail":"kernel version less than 0:3.10.0-693.21.1.el7",
						"Path":"/boot/.vmlinuz-3.10.0-693.2.2.el7.x86_64.hmac",
						"UpdateCmd":"yum update kernel"
					},
					{
						"Name":"kernel-headers",
						"FullVersion":"3.10.0-693.2.2.el7",
						"Version":"3.10.0",
						"MatchDetail":"kernel-headers version less than 0:3.10.0-693.21.1.el7",
						"Path":"/usr/include/asm",
						"UpdateCmd":"yum update kernel-headers"
					},
					{
						"Name":"kernel-tools",
						"FullVersion":"3.10.0-693.2.2.el7",
						"Version":"3.10.0",
						"MatchDetail":"kernel-tools version less than 0:3.10.0-693.21.1.el7",
						"Path":"/etc/sysconfig/cpupower",
						"UpdateCmd":"yum update kernel-tools"
					},
					{
						"Name":"kernel-tools-libs",
						"FullVersion":"3.10.0-693.2.2.el7",
						"Version":"3.10.0",
						"MatchDetail":"kernel-tools-libs version less than 0:3.10.0-693.21.1.el7",
						"Path":"/usr/lib64/libcpupower.so.0",
						"UpdateCmd":"yum update kernel-tools-libs"
					},
					{
						"Name":"python-perf",
						"FullVersion":"3.10.0-693.2.2.el7",
						"Version":"3.10.0",
						"MatchDetail":"python-perf version less than 0:3.10.0-693.21.1.el7",
						"Path":"/usr/lib64/python2.7/site-packages",
						"UpdateCmd":"yum update python-perf"
					}
				],
				"OsRelease":"7"
			},
			"Name":"oval:com.redhat.rhsa:def:20180395",
			"Status":1,
			"LastTs":1554096622000,
			"NeedReboot":"yes",
			"AliasName":"RHSA-2018:0395-Important: kernel security and bug fix update",
			"Tag":"oval",
			"PrimaryId":160191232,
			"IntranetIp":"172.19.0.0",
			"Level":"low",
			"InstanceName":"master-03-k8s-for-cs-cce881ec0ec77435e8e21bb52d1178e2a"
		}
	]
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/Sas)查看更多错误码。

