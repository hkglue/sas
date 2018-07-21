# 金融云、VPC用户安装Agent {#concept_vth_3zc_zdb .concept}

针对无法直接连通公网的云服务器（如阿里金融云上的服务器或使用专有网络VPC的云服务器），您可以参照本文介绍的方法为其安装态势感知Agent。

## 操作步骤 {#section_qqt_mcd_zdb .section}

参照以下步骤，为金融云或VPC环境下的服务器安装态势感知Agent：

**说明：** 如果您的服务器上安装了安全软件（如安全狗、云锁等），则态势感知Agent可能无法正常安装。在安装态势感知Agent前，请确认您的服务器上是否存在这类安全软件。如果存在，建议您关闭或卸载该安全软件后，再安装态势感知Agent。

1.  登录[云盾态势感知控制台](https://yundun.console.aliyun.com/?p=sas)。
2.  前往**设置**页面。
3.  选择**安装/卸载插件**。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13632/4566_zh-CN.png)

4.  根据服务器操作系统类型，选择安装步骤，获取并安装最新版本的态势感知Agent。
    -   **Windows 系统**
        1.  在安装/卸载插件页面，单击**点击下载**，下载最新版本态势感知Agent安装文件到本地计算机。
        2.  将安装文件上传到Windows服务器。例如，通过FTP工具将安装文件上传到服务器。
        3.  在Windows服务器上，以管理员权限运行态势感知Agent安装程序，按照向导完成安装。

            **说明：** 态势感知Agent安装过程中可能会提示您输入安装验证Key。该安装验证Key用于关联您的阿里云账号，您可在安装/卸载插件页面找到您的安装验证 Key。

            ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13632/4567_zh-CN.png)

    -   **Linux系统**
        1.  根据服务器的Linux系统版本，单击以下链接将态势感知Agent安装程序下载至本地计算机。
            -   Linux 32位系统：[态势感知Agent安装程序](https://aegis.alicdn.com/download/AliAqsInstall_32.sh)
            -   Linux 64位系统：[态势感知Agent安装程序](https://aegis.alicdn.com/download/AliAqsInstall_64.sh)
        2.  将态势感知Agent安装程序上传至Linux服务器。例如，通过FTP工具将安装文件上传到服务器。
        3.  以管理员身份登录Linux服务器。
        4.  定位到已上传的态势感知Agent安装程序所在目录，根据服务器的Linux系统版本，执行以下命令安装态势感知Agent。

            -   Linux 32位系统：`chmod +x AliAqsInstall_32.sh && ./AliAqsInstall_32.sh xxxxxx`
            -   Linux 64位系统：`chmod +x AliAqsInstall_64.sh && ./AliAqsInstall_64.sh xxxxxx`
            **说明：** 此安装命令末尾处的`xxxxxx`为安装验证Key，执行安装命令时请使用安装/卸载插件页面中显示的六位安装验证Key替换`xxxxxx`部分。该安装验证Key与Windows系统安装步骤中的安装验证Key一致，用于关联您的阿里云账号。

            ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13632/4567_zh-CN.png)

5.  态势感知Agent安装完成约五分钟后，您可在云盾态势感知控制台资产列表页面查看服务器的保护状态。服务器保护状态将从**未受保护**变为**保护中**。

## 验证Agent安装 {#section_art_mcd_zdb .section}

成功安装态势感知Agent后，建议您参考以下步骤进行验证：

1.  检查服务器上态势感知Agent的AliYunDun和AliYunDunUpdate进程是否正常运行。关于态势感知Agent进程说明，请参考[Agent说明](intl.zh-CN/用户指南/接入态势感知/Agent说明.md#)。
2.  在服务器上执行以下telnet命令，检查服务器是否能正常连通态势感知服务器。

    **说明：** 确保以下两个服务器都能连通。

    -   `telnet jsrv3.aegis.aliyun.com 80`
    -   `telnet update3.aegis.aliyun.com 80`

如果态势感知Agent安装验证失败，请参考[Agent离线排查](intl.zh-CN/用户指南/接入态势感知/Agent离线排查.md#)。

