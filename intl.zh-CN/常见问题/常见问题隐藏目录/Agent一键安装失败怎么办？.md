# Agent一键安装失败怎么办？ {#concept_593057 .concept}

云安全中心支持对阿里云服务器进行一键安装Agent。Agent一键安装失败时，请排查是否存在以下不支持一键安装的情况：

-   您的服务器为非阿里云服务器
-   网络类型为经典网络
-   ECS不在[支持的区域](../intl.zh-CN/接入云安全中心/安装Agent.md#table_ec1_2lh_ghb)内
-   服务器操作系统为Windows 2008、Redhat、FreeBSD、Coreos
-   未安装[云助手](../intl.zh-CN/部署与运维/云助手/云助手概述.md#)
-   通过专线连接、内网通信的非阿里云服务器，需要修改服务器的DNS配置，指定以下任意一个云安全中心服务端DNS解析地址：

    `106.11.248.209/106.11.248.51 jsrv.aegis.aliyun.com`

    `106.11.248.90/106.11.250.224 update.aegis.aliyun.com`


对于以上不支持一键安装的情况，您需执行手动安装。有关手动安装Agent的详细操作，参见[手动安装Agent](../intl.zh-CN/接入云安全中心/安装Agent.md#section_qxq_hkv_ghb)。

