# 卸载Agent {#concept_cwf_hzc_zdb .concept}

如果您决定不再使用云盾态势感知服务的安全防护功能，您可以选择自动或手动卸载态势感知Agent。卸载态势感知Agent后，请耐心等待六个小时，然后该服务器在态势感知控制台上的保护状态就会由**保护中**变更为**未受保护**。

## 自动卸载态势感知Agent {#section_tdh_2kd_zdb .section}

使用以下方式，在云盾态势感知控制台上自动卸载态势感知Agent。

**说明：** 如果在卸载Agent插件后需要重新安装它，请进行手工安装，并忽略期间的报错，重复操作3次以上。因为态势感知在卸载后会有一段24小时的保护期，期间重新安装时需要重复执行3次以上安装命令。

**前提条件**

请务必确保态势感知Agent在当前主机上处于在线状态（即服务器保护状态为**保护中**），否则该主机无法接收到卸载指令。

**操作步骤**

参照以下步骤，自动卸载态势感知Agent插件：

1.  登录[云盾态势感知控制台](https://yundun.console.aliyun.com/?p=sas)。
2.  在左侧导航栏，单击**设置**。
3.  单击**安装/卸载插件**，进入态势感知Agent页面。
4.  单击页面右上方的**卸载插件**。
5.  在弹出的卸载提示对话框中，选择您要卸载态势感知Agent的服务器，单击**确认卸载**。
6.  系统将自动卸载目标服务器上的态势感知Agent。

## 手动卸载态势感知Agent {#section_xdh_2kd_zdb .section}

参考以下步骤手动卸载服务器上的态势感知Agent。

**Linux系统服务器**

1.  登录Linux系统服务器。
2.  执行以下命令，下载态势感知Agent卸载脚本。

    ```
    wget http://update.aegis.aliyun.com/download/uninstall.sh
    ```

3.  依次执行以下命令，卸载态势感知Agent。
    -   `chmod +x uninstall.sh`
    -   `./uninstall.sh`

**Windows系统服务器**

1.  登录Windows系统服务器。
2.  在服务器上下载[态势感知Agent卸载脚本](http://update.aegis.aliyun.com/download/uninstall.bat)。

    **说明：** 您也可以将态势感知Agent卸载脚本下载至本地计算机后，通过FTP文件传输工具将脚本文件上传至您的服务器。

3.  双击uninstall.bat文件执行脚本，卸载态势感知Agent。

