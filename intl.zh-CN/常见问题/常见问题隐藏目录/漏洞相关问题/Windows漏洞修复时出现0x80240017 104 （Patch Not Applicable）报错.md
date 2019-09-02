# Windows漏洞修复时出现0x80240017 104 （Patch Not Applicable）报错 {#concept_1958027 .concept}

## 问题原因 {#section_k4r_4ky_iv8 .section}

Windows漏洞修复时，可能会出现0x80240017 104 （Patch Not Applicable）的报错， 原因是没有安装前置补丁。

## 解决方案 {#section_t6t_8su_jww .section}

该补丁安装前需要安装前置补丁：KB4490628和KB4474419（在云安全中心已覆盖检测前置补丁，可直接搜索补丁号查找）。建议根据云安全中心漏洞管理检测提示，按KB号从小到大依次安装补丁。

![漏洞详情](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/1553748/156739209558582_zh-CN.png)

