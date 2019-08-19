# AK泄露检测 {#concept_vb5_3jw_f2b .task}

云安全中心可以检测在Github等第三方代码托管网站上的公开代码中可能包含的您资产的登录账号和密码信息。

阿里云云安全中心企业版支持AK泄露检测功能，基础版和高级版不支持该功能。基础版和高级版用户需先升级至企业版，才可使用AK泄露检测服务。

## 功能说明 {#section_al5_jrq_zdb .section}

因企业制度不规范或管理困难，企业员工有权限（或无意识地）将公司源码上传至Github等代码托管平台，导致企业的数据库连接地址和密码以及服务器登录密码等在代码中直接外泄。

云安全中心使用搭建在网络空间中的威胁情报采集系统，通过网络爬虫对Github等第三方代码托管网站进行实时监控，捕获并判定被公开的源代码（多为企业员工私自上传并不小心公开）中是否含有ECS、RDS、Redis、MySQL等用户资产的登录名和密码等信息，帮助企业规避数据外泄。

云安全中心AK和账密泄露检测功能支持检测AK（AccessKey）信息。

**说明：** 如果用户在云安全中心控制台的**安全运营** \> **设置** \> **通知**页面，设置**AccessKey泄露情报**的**通知时间**是`8:00-20:00`，这种情况下，`8:00-20:00`以外时间检测到的AK泄露情报，只能在以后的这个时间段通知。

## 操作步骤 {#section_dtj_ss4_f2b .section}

1.  登录[云安全中心控制台](https://yundun.console.aliyun.com/?p=sas)。
2.  在左侧导航栏，单击**威胁检测** \> **AK泄露检测**。
3.  您可以在AK泄露检测页面，进行以下操作。 
    -   **查看AccessKey泄露情报列表** 

        您可以查看云安全中心检测到的所有信息泄露情报：AccessKey泄露次数及检测列表、检测平台、最近一次检测时间。

        ![查看AccessKey泄露情报列表](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/15125/15661810306504_zh-CN.jpg)

    -   **搜索指定AccessKey泄露情报** 

        在搜索框输入AccessKey ID可以快速定位到想要查看的记录。

        ![搜索特定AccessKey泄露情报](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/15125/156618103154200_zh-CN.png)

    -   **执行立即检测** 

        您可以在**AccessKey泄露检测**页，单击**立即检测**，检测最新的AccessKey泄露情报。

        ![执行立即检测](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/15125/156618103154201_zh-CN.png)

    -   **查看AccessKey泄露检测详情** 

        您可以选择一个记录，单击其操作列下的**详情**，查看详细的情报信息。

        ![查看AccessKey泄露检测详情](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/15125/15661810316505_zh-CN.jpg)

    -   **处理检测出的AK泄露事件** 

        您可以根据AccessKey泄露详情页面的**相关推荐**，尽快确认数据泄露事件以及参考建议方案对AK泄露进行处理。

        -   您可以前往[日志检索平台](https://sls.console.aliyun.com)，搜索对应的服务器访问日志（例如，检索日志源Web访问日志，指定URI字段为包含AK应用文件的文件路径），确认数据是否泄漏。
        -   处理方式包含**手动删除**、**手动禁用AK**、**加白名单**三种，您可根据实际情况选择合适的处理方式。

            您可以在**AccessKey泄露检测**列表，单击一个检测记录右侧操作列下的**处理**，选择处理方式。

            ![处理检测结果](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/15125/156618103154185_zh-CN.png)

            如果选择加入白名单处理，该检测项处理状态变为**已加白名单**，并进入**已处理**列表。需要回复检测时，可以从**已处理**列表，进入AccessKey泄露详情页进行**取消白名单**操作。

            ![取消白名单](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/15125/156618103254188_zh-CN.png)

        **说明：** 建议您禁止员工将公司源代码托管在GitHub等代码平台，或使用**私有的**Github代码托管来管理代码，搭建企业内部的代码托管系统，防止源代码和敏感信息泄露。

    -   **导出AccessKey泄露检测报表** 

        您可以单击**AccessKey泄露检测**列表右上角的导出按钮。报表导出完成后，安全告警页面右上角会提示导出完成。单击右上角导出完成提示对话框中的**下载**，将excel格式的报表下载到本地。

        ![下载](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/15125/156618103254205_zh-CN.png)


