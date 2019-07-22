# Ubuntu 内核补丁漏洞修复FAQ {#concept_1236951 .concept}

使用Ubuntu内核的服务器执行漏洞一键修复时，安装新内核后系统重启时不会启用最新内核，原因是用户修改过GRUN引导菜单的内核选择顺序导致安装kernel时候会要求用户选择是否保留自己修改的GRUB菜单，这时需要静默安装默认使用更新的内核作为第一启动顺序。

## 问题描述 {#section_2co_75h_45b .section}

在云安全中心控制台对Linux内核漏洞执行一键修复后，需要重启系统，漏洞修复才能成功。重启系统/ECS实例时，如果您的内核引导GRUB菜单曾做过修改，系统将无法自动为最新的内核建立引导菜单，即使重启后，云安全中心控制台仍然会提示**修复成功待重启**。这种情况下，会导致无法验证漏洞是否修复成功。

![修复成功待重启](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/987740/156378367352210_zh-CN.png)

## 解决方法 {#section_ka1_shu_7xb .section}

如果您默认使用新内核默认附带的设置，并丢弃原本的GRUB菜单配置，可在执行漏洞修复命令前设置以下环境变量，使安装系统自动选择默认设置。

``` {#codeblock_ftp_usv_tkt}
export DEBIAN_FRONTEND=noninteractive
```

如果您无需使用新内核的默认设置，可手动修改GRUB引导顺序，相关操作参见[ECS Linux CentOS 修改内核引导顺序](https://www.alibabacloud.com/help/zh/faq-detail/41463.htm)。

