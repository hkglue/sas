# RDS SQL注入威胁检测 {#concept_h15_mvd_rfb .task}

云安全中心企业版支持RDS SQL注入威胁检测功能，帮助您及时发现资产中是否存在RDS SQL注入隐患。

RDS SQL注入是数据库攻击的常见方式之一。SQL注入会导致数据泄露、篡改或对敏感数据的非法操作，威胁您资产的数据安全。

**说明：** 云安全中心基础版和高级版不支持云产品威胁检测-RDS SQL注入功能。

## 步骤一：开通RDS SQL洞察 {#section_ntp_gem_koc .section}

1.  登录[RDS管理控制台](https://rds.console.aliyun.com/)。
2.  在左侧导航栏单击**实例列表** \> **基本信息**。

    ![RDS实例](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/41684/156566694354828_zh-CN.png)

3.  在实例列表页面中单击需要开通RDS SQL洞察功能的数据库实例。
4.  在左侧导航栏单击**SQL洞察** \> **立即开通**。

    ![立即开通RDS SQL洞察](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/41684/156566694454830_zh-CN.png)

5.  选择您所需要的RDS日志**存储时长**。

    SQL洞察试用版只能查询当天的日志数据，建议选择非试用版。

    ![选择日志存储时长](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/41684/156566694454831_zh-CN.png)

    **说明：** 开通非试用版SQL洞察功能会收取RDS相关使用费用，选择30天或以上，按小时扣费，每小时每GB 0.008元。无需使用SQL洞察时，可关闭该功能。RDS SQL洞察详细说明参见[SQL洞察](../../intl.zh-CN/用户指南/SQL洞察.md#)。


## 步骤二：开启RDS SLS日志投递 {#section_s6o_cqd_5gf .section}

1.  登录SLS管理控制台。
2.  在**接入数据**模块单击**RDS审计-云产品**，进行RDS审计数据接入。

    ![RDS审计](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/41684/156566694454833_zh-CN.png)

3.  在**RDS审计**页面新建或选择您想存放SQL洞察数据相关的项目Project和日志库Logstore。

    ![选择项目和logstore](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/41684/156566694554832_zh-CN.png)

4.  在RDS审计实例列表中，定位到需要开启SQL注入检测的SQL实例，单击**开通投递**。
5.  单击**下一步**完成数据接入配置，将RDS相关日志数据同步到SLS日志服务中。

## 步骤三：开启云安全中心RDS SQL注入威胁检测 {#section_r9r_qvu_pk0 .section}

1.  登录[云安全中心控制台](https://yundun.console.aliyun.com/?p=sas)。
2.  单击左侧导航栏**威胁检测** \> **安全告警处理**。
3.  在**安全告警处理**页面右上角单击**安全告警设置**。

    ![安全告警设置按钮](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/41684/156566694554834_zh-CN.png)

4.  在**安全告警设置**页面开启RDS SQL注入威胁检测功能总开关，对您的所有资产开启该功能。

    **说明：** 如只需对部分资产开启SQL注入威胁检测，可在**资产中心**页面单击该资产名称，跳转到资产详情页面，单独为该资产开启/关闭RDS SQL注入功能。


## 步骤四（可选步骤）：查看SQL注入告警 {#section_aec_7i2_bsl .section}

您的资产开启了RDS SQL注入威胁检测功能后，您可在云安全中心**安全告警处理**页面，查看和处理云安全中心为您检测到的RDS SQL注入告警事件。

![云产品威胁检测RDS SQL注入告警](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/41684/156566694554835_zh-CN.png)

