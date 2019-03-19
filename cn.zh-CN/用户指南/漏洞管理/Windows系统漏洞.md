# Windows系统漏洞 {#concept_qbb_xb1_4gb .concept}

云安全中心支持Windows系统漏洞检测和修复的功能。

通过实时同步微软官网补丁源，对高危及有影响的漏洞进行有效的检测和告警，避免攻击者通过Windows系统漏洞对您的服务器进行攻击或威胁您服务器的数据安全。

**说明：** 云安全中心**基础版**只提供漏洞检测，不提供漏洞修复的服务；如需一键修复漏洞，请开通云安全中心**企业版**。基础版和企业版详细功能介绍参见[功能特性](../../../../../cn.zh-CN/产品简介/功能特性.md#)。

## 操作步骤 {#section_lst_wsc_ygb .section}

1.  登录[云安全中心控制台](https://yundun.console.aliyun.com/?p=sas)。
2.  定位到**漏洞管理** \> **Windows系统漏洞**。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/118684/155301437139812_zh-CN.png)

3.  您可以在Windows系统漏洞页面查看云安全中心检测到的所有Windows系统漏洞的详细信息、执行验证和修复漏洞、根据漏洞的严重程度和状态对特定漏洞进行定位、将漏洞加入白名单或忽略漏洞。
    -   **查看漏洞详情**

        单击漏洞列表中的漏洞名称打开漏洞详情页面。您可在漏洞详情页面查看该漏洞的描述、漏洞紧急程度、漏洞影响的所有资产信息、漏洞的状态，并可对漏洞执行验证、修复或忽略的操作。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/118684/155301437139813_zh-CN.png)

        漏洞详情页面可展示该漏洞所有**关联漏洞**，即该漏洞影响的所有资产信息，方便您对所有相关的漏洞进行分析和批量处理。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/118684/155301437139815_zh-CN.png)

        漏洞紧急程度用不同颜色的图标表示。红色图标表示**高危**漏洞、橙色图标表示**中危**漏洞、灰色图标表示**低危**漏洞。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/118684/155301437139814_zh-CN.png)

        **说明：** 建议立即修复高危漏洞（紧急程度高）。

    -   **验证漏洞**

        您可在漏洞详情页面**验证**单个漏洞或对多个关联漏洞进行批量验证，检测该漏洞是否已修复成功。

        单击**验证**后，该漏洞的**状态**转为**验证中**。需要等待数秒后漏洞验证才可完成。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/118684/155301437139816_zh-CN.png)

    -   **修复漏洞**

        您可在漏洞详情页面单击**立即修复**对单个漏洞进行修复或对多个关联漏洞进行批量修复。

    -   **搜索漏洞**

        您可在Windows系统漏洞页面通过筛选漏洞危险等级（高、中、低）、漏洞处理状态（已处理、未处理）或输入漏洞名称定位到相关的漏洞。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/118684/155301437139817_zh-CN.png)

        **说明：** 搜索漏洞名称支持模糊查询。

    -   **将漏洞加入白名单**

        您可在Windows系统漏洞页面勾选漏洞列表左侧的复选框后单击**加入白名单**，将该漏洞加入白名单中。加入白名单后，云安全中心将不再对白名单中的漏洞进行告警。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/118684/155301437239818_zh-CN.png)

        加入白名单的漏洞将从Windows系统漏洞的漏洞列表中移除，并记录在[漏洞管理设置](cn.zh-CN/用户指南/漏洞管理/漏洞管理设置与加白名单.md#)页面的**漏洞白名单配置**列表中。

        如需恢复云安全中心对白名单中的漏洞进行检测和告警提示，可在漏洞管理设置页面**移除**该漏洞。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/118684/155301437239827_zh-CN.png)

    -   **忽略漏洞**

        您可在Windows系统漏洞页面勾选漏洞列表左侧的复选框后单击**忽略**，云安全中心将不再提示该漏洞。

        **说明：** 被**忽略**的漏洞状态将转为**已处理**。如需云安全中心继续对该漏洞进行告警提示，可在**已处理**的漏洞列表中找到该漏洞并对其**取消忽略**。

    -   **导出漏洞**

        您可在Windows系统漏洞页面单击**导出**将云安全中心检测到的所有Windows系统漏洞统一导出并保存到本地。导出的文件为Excel格式。

        **说明：** 根据您资产中漏洞数据的大小，导出漏洞列表可能需要耗费一定时间，请耐心等待。

    -   您可在漏洞详情页面单击![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/118684/155301437239821_zh-CN.png)按钮保存筛选出的所有漏洞为一个漏洞修复批次，方便您对该批次漏洞的状态进行持续跟踪。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/118684/155301437239820_zh-CN.png)


