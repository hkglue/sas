# Agent相关FAQ {#concept_bvy_mb5_q2b .concept}

-   [如何查看云安全中心Agent的日志？](#)
-   [在ECS Linux系统服务器中安装Agent时，收到“Permission denied”的错误提示，应该如何处理？](#)

## 如何查看云安全中心Agent的日志？ {#2 .section}

云安全中心Agent的默认安装路径下包含data目录，该目录下的data.x文件就是日志文件。

-   在Linux系统中，云安全中心Agent的默认安装路径如下：/usr/local/aegis/aegis\_client/aegis\_xx\_xx 

    您可以前往以上路径，在data目录下查看日志文件。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/17031/15595299908966_zh-CN.png)

-   在Windows系统中，云安全中心Agent的默认安装路径如下：C:\\Program Files \(x86\)\\Alibaba\\Aegis\\aegis\_client\\aegis\_xx\_xx 

    您可以前往以上路径，在data目录下查看日志文件。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/17031/15595299908967_zh-CN.png)


## 在ECS Linux系统服务器中安装Agent时，收到“Permission denied”的错误提示，应该如何处理？ {#1 .section}

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/17031/15595299908509_zh-CN.jpg)

您可以参考以下方法来解决该问题。

1.  检查是否通过root账号进行安装，并且执行`ls -al /etc/init.d/aegis`命令查看对/etc/init.d/aegis目录是否有操作权限。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/17031/15595299908510_zh-CN.png)

2.  查看您的服务器是否安装了云锁。您可以通过执行`ps -ef | grep yunsuo_agent`或`ps aux | grep yunsuo`命令进行检查。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/17031/15595299908511_zh-CN.png)

    如果服务器上已安装云锁，则云安全中心Agent的安装过程可能会被云锁拦截。建议您暂时关闭云锁后，再尝试安装。

    云锁的默认目录是/usr/local/yunsuo\_agent。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/17031/15595299908512_zh-CN.png)


## Agent一键安装失败怎么办？ {#section_vut_h20_6e0 .section}

云安全中心支持对阿里云服务器进行一键安装Agent。Agent一键安装失败时，请排查是否存在以下不支持一键安装的情况：

-   您的服务器为非阿里云服务器
-   网络类型为经典网络
-   ECS不在[支持的区域](../intl.zh-CN/接入云安全中心/安装Agent.md#table_ec1_2lh_ghb)内
-   服务器操作系统为Windows 2008、Redhat、FreeBSD、Coreos
-   未安装[云助手](../intl.zh-CN/部署与运维/云助手/云助手概述.md#)
-   服务器未开启

对于以上不支持一键安装的情况，您需执行手动安装。有关手动安装Agent的详细操作，参见[手动安装Agent](../intl.zh-CN/接入云安全中心/安装Agent.md#section_qxq_hkv_ghb)。

