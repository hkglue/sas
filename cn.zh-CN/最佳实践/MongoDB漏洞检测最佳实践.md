# MongoDB漏洞检测最佳实践 {#concept_ufj_wrs_2hb .concept}

云安全中心应急漏洞已发布MongoDB未授权漏洞，该漏洞可直接被黑客远程利用，可能导致您的业务数据被泄露或勒索。建议您立即进行漏洞检测并按照提供的修复建议尽快修复漏洞。

## 前提条件 { .section}

-   用户已同意**应急漏洞检测协议**，授权云安全中心进行应急漏洞检测。若您已授权请忽略。
-   漏洞检测需要安装云安全中心Agent， 详见[安装Agent](../../../../../intl.zh-CN/接入云安全中心/接入云安全中心.md#)。

## 操作步骤 { .section}

1.  登录[云安全中心控制台](https://yundun.console.aliyun.com/?p=sas)。
2.  定位到 **漏洞管理** \> **应急漏洞** 。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/118680/155340455339938_zh-CN.png)

3.  单击应急漏洞页面右侧的**立即检测**，开始检测漏洞。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/118680/155340455339960_zh-CN.png)

    触发检测功能后检测引擎开始工作，该漏洞状态会转为**检测中**。需要等待一段时间才可完成漏洞检测，请您耐心等待。

    ![](images/41416_zh-CN.png "漏洞检测中")

4.  判断是否有风险。

    待检查完成后，可以在页面上直接看到检查结果，通过返回可以知道是否存在风险：

    -   有风险检测结果如下：

        ![](images/41418_zh-CN.png "有MongoDB漏洞风险")

    -   无风险检测结果如下：

        ![](images/41417_zh-CN.png "无MongoDB漏洞风险")

5.  查看结果详情。

    ![](images/41419_zh-CN.png "漏洞结果详情")

    ![](images/41420_zh-CN.png "漏洞详情页")

6.  修复漏洞。

    如果检测结果显示您的服务器存在风险，请参考[MongoDB漏洞修复方案](https://helpcdn.aliyun.com/knowledge_detail/112025.html)进行修复。

7.  验证修复。

    漏洞修复完成后，点击**验证**进行复查，确定漏洞是否已经修复成功。

    ![](images/41423_zh-CN.png "验证漏洞修复")


