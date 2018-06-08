# 为何安全组或者防火墙规则已经屏蔽了 RDP 服务的3389端口还出现 RDP 被暴力破解记录？ {#concept_ejt_r2c_b2b .concept}

由于 Windows 登录审核机制原因， $IPC 、RDP、SAMBA 服务登录审核过程均会记录在同一个日志里面，且未区分具体登录方式，故已经屏蔽了 RDP 服务端口还出现 RDP 被暴力破解记录的情况需检查是否还开启了其它两个服务。对应检查方法为查看 ECS 是否有监听 135、139、445 等端口并且外网 IP 均可访问，并且查看 Windwows 安全类日志是否在该时段有对应的登录记录：

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13701/5996_zh-CN.png)

