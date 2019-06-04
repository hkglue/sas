# Wget缓冲区溢出漏洞检测命中规则说明 {#concept_71525_zh .concept}

2017年10月26日，GNU Wget官方发布Wget缓冲区溢出的漏洞公告。当使用存在漏洞的Wget版本下载特殊HTTP链接时，可能会受到恶意HTTP响应攻击，从而导致拒绝服务和恶意代码执行。 相关漏洞编号为CVE-2017-13089、CVE-2017-13090。

关于该漏洞的详细信息，请查看[【漏洞公告】Wget缓冲区溢出漏洞](https://www.alibabacloud.com/help/zh/faq-detail/62126.htm)。

云安全中心的漏洞管理功能支持检测并修复该漏洞。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/163498/155963000045574_zh-CN.png)

## 受影响版本说明 {#section_ozr_qvc_3gb .section}

GNU官方公布的受影响版本为1.19.2之前的所有版本，即通过官方途径下载编译的Wget必须使用1.19.2之后的版本避免受该漏洞影响。然而，对于部分Linux软件源（如CentOS源）中的Wget工具，由于已通过补丁的方式对部分老版本中的该漏洞进行了修复，因此无需升级至1.19.2以上的版本。

根据阿里云安全专家反复测试验证，对于通过Linux软件源方式安装的Wget仅需高于1.14-15.el7\_4.1版本即不会受到该漏洞影响。因此，在云安全中心漏洞管理检测功能中，对于通过该途径安装的Wget工具使用以下命中规则进行漏洞检测：`wget version less than 1.14-15.el7_4.1`。

