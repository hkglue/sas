# Agent说明 {#concept_rbw_fzc_zdb .concept}

## 工作原理 {#section_oqs_fdd_zdb .section}

态势感知Agent每隔五个小时会主动向态势感知服务器端上报一次在线数据信息。

如果态势感知Agent没有按时上报在线信息，态势感知服务器端则在12小时后判定该服务器不在线，并在态势感知控制台中将此服务器的保护状态更新为离线。

## 相关进程 {#section_pqs_fdd_zdb .section}

态势感知Agent包含以下两个主要进程：

**Note:** 态势感知Agent的进程在Linux系统的服务器上以root账号运行，在Windows系统的服务器上以system账号运行。

-   AliYunDun

    此进程用于与态势感知服务器建立连接。

    进程文件所在路径如下：

    -   Windows 32位系统：C:\\Program Files\\Alibaba\\aegis\\aegis\_client
    -   Windows 64位系统：C:\\Program Files \(x86\)\\Alibaba\\aegis\\aegis\_client
    -   Linux 系统：/usr/local/aegis/aegis\_client
-   AliYunDunUpdate

    此进程用于定期检测态势感知Agent是否需要升级。

    进程文件所在路径如下：

    -   Windows 32 位系统：C:\\Program Files\\Alibaba\\aegis\\aegis\_update
    -   Windows 64 位系统：C:\\Program Files \(x86\)\\Alibaba\\aegis\\aegis\_update
    -   Linux 系统：/usr/local/aegis/aegis\_update

