# 云安全中心控制台提示“token校验失败” {#concept_66689_zh .concept}

在云盾云安全中心管理控制台中，执行某些操作时，提示“token校验失效”。

## 问题描述 {#section_czk_pnx_jgb .section}

例如，在[云盾服务器安全（云安全中心）管理控制台](https://yundunnext.console.aliyun.com/?p=sas)的漏洞管理页面，选择某个漏洞，单击**一键修复**时，提示**token校验失效**。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/188526/155972460645738_zh-CN.png)

## 问题原因 {#section_wvl_mnx_jgb .section}

由于用户长时间没有在控制台进行任何操作，之前验证的token失效，需重新登录控制台。

## 解决方法 { .section}

刷新当前页面，重新登录云盾云安全中心管理控制台。

**说明：** 您可按Ctrl+F5，强制刷新当前浏览器页面。

