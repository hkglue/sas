# 安装Agent {#concept_dl4_ykc_zdb .concept}

态势感知Agent插件是态势感知提供的本地插件，您需要在您的服务器操作系统上安装态势感知Agent插件，才能使用态势感知提供的安全防护服务。

## 阿里云公共镜像集成插件 {#section_prp_z1d_zdb .section}

态势感知Agent插件已集成于公共镜像中。如果您在购买ECS实例时，选择公共镜像并选择启用**安全加固**选项的话，态势感知Agent插件即默认通过镜像安装。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13631/4557_zh-CN.png)

登录 [云盾服态势感知控制台 \> 资产列表](https://yundun.console.aliyun.com/?p=sas)，可以查看您所有服务器的保护状态，也就是态势感知Agent的在线/离线状态。

若您的服务器保护状态显示为未受保护，请按照以下方式，手动下载并安装态势感知Agent插件。

## 手动安装（支持非阿里云服务器） {#section_rrp_z1d_zdb .section}

**Note:** 如果您已在服务器上安装了安全软件（如安全狗、云锁等），可能会导致态势感知Agent插件无法正常安装。建议您在安装态势感知Agent插件前，确认您的服务器上是否存在这类安全软件。如果存在，建议您暂时关闭或卸载该安全软件，然后再安装态势感知Agent插件。

**前提条件**

安装前，请确认您的服务器环境符合以下条件：

-   服务器在阿里云上，可以直接安装。
-   服务器不在阿里云上，与阿里云走Internet通信，应确保Intetnet连通。
-   服务器不在阿里云上，与阿里云通过专线连接走内网通信，则您需要在域名解析记录中添加以下DNS配置，指定态势感知服务端DNS：
    -   `100.100.25.3 jsrv.aegis.aliyun.com`
    -   `100.100.25.4 update.aegis.aliyun.com`

**操作步骤**

参照以下步骤，手动安装态势感知Agent插件：

1.  登录 [云盾态势感知控制台](https://yundun.console.aliyun.com/?p=sas)。
2.  在左侧导航栏，单击**设置**。
3.  单击**安装/卸载插件**，进入态势感知Agent页面。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13631/4558_zh-CN.png)

4.  根据您的服务器操作系统，选择安装步骤，获取并安装最新版本的态势感知Agent插件。
    -   Windows系统
        1.  在态势感知Agent页面，单击**点击下载**，下载最新版本态势感知Agent插件安装文件到本地计算机。
        2.  将安装文件上传至您的Windows服务器。例如，您可以通过FTP工具，将安装文件上传到服务器。
        3.  在Windows服务器上，以管理员权限运行态势感知Agent插件安装程序，完成安装。

            **Note:** 态势感知Agent插件安装过程中，您会收到提示，要求您输入安装验证Key。该安装验证Key用于关联您的阿里云账号，您可在云盾态势感知Agent页面找到您的安装验证Key。

            ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13631/4559_zh-CN.png)

    -   Linux系统
        1.  根据您的实际情况，在态势感知Agent页面选择**阿里云服务器**或**非阿里云服务器**。
        2.  以管理员身份登录您的Linux服务器。
        3.  根据您的操作系统类型，选择32位或64位的安装命令，并复制至您的Linux服务器上。
        4.  执行安装命令，完成态势感知Agent插件的下载及安装。

            **Note:** 该安装命令包含从阿里云站点下载最新版本的态势感知Agent插件，请确认您的服务器已连接公网。

5.  态势感知Agent插件安装完成约五分钟后，您即可在云盾态势感知控制台上，查看您服务器的保护情况：
    -   阿里云服务器将会从未受保护变成保护中。
    -   非阿里云服务器将会被添加至您的服务器列表中。

## 验证Agent安装 {#section_csp_z1d_zdb .section}

在您成功安装态势感知Agent后，建议您参照以下步骤进行验证：

1.  检查您的服务器上态势感知Agent的`AliYunDun`和`AliYunDunUpdate`进程是否正常运行。关于态势感知Agent进程说明，请参考[Agent说明](cn.zh-CN/用户指南/Agent插件/Agent说明.md#)。
2.  在您的服务器上，执行以下telnet命令，检查您的服务器是否能正常连通态势感知服务器。确保您的服务器能够连通至少一个jsrv和一个update服务域名。
    -   `telnet jsrv.aegis.aliyun.com 80`
    -   `telnet jsrv2.aegis.aliyun.com 80`
    -   `telnet jsrv3.aegis.aliyun.com 80`
    -   `telnet update.aegis.aliyun.com 80`
    -   `telnet update2.aegis.aliyun.com 80`
    -   `telnet update3.aegis.aliyun.com 80`

如果态势感知Agent安装验证失败，请参考[Agent离线排查](cn.zh-CN/用户指南/Agent插件/Agent离线排查.md#)。

## 注意事项 {#section_fsp_z1d_zdb .section}

非阿里云服务器必须通过安装程序（Windows）或脚本命令（Linux）方式安装态势感知Agent插件。

如果您的非阿里云服务器通过以下方式安装态势感知Agent插件，则您需要删除态势感知Agent插件目录后，按照上述手动安装步骤重新安装态势感知Agent插件。

-   通过已安装态势感知Agent插件的镜像批量安装服务器。
-   从已安装态势感知Agent插件的服务器上直接复制态势感知Agent插件文件。

**态势感知Agent插件文件目录**

-   Windows： C:\\Program Files \(x86\)\\Alibaba\\Aegis
-   Linux： /usr/local/aegis

