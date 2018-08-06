# Agent相关FAQ {#concept_bvy_mb5_q2b .concept}

-   [在ECS Linux系统服务器中安装Agent时，收到“Permission denied”的错误提示，应该如何处理？](#section_qt5_nb5_q2b)
-   [如何查看态势感知Agent的日志？](#section_bcm_ydk_s2b)

## 在ECS Linux系统服务器中安装Agent时，收到“Permission denied”的错误提示，应该如何处理？ {#section_qt5_nb5_q2b .section}

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/17031/15335448488509_zh-CN.jpg)

您可以参考以下方法进行排查，并解决该问题。

1.  检查是否通过root账号进行安装，并且执行`ls -al /etc/init.d/aegis`命令查看对于/etc/init.d/aegis目录是否有执行权限。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/17031/15335448488510_zh-CN.png)

2.  查看您的服务器是否安装了云锁。您可以通过执行`ps -ef | grep yunsuo_agent`或`ps aux | grep yunsuo`命令进行检查。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/17031/15335448488511_zh-CN.png)

    如果服务器上已安装了云锁，可能会对态势感知 Agent 的安装进行拦截。建议您暂时关闭云锁后，再尝试安装。

    云锁的默认目录是/usr/local/yunsuo\_agent。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/17031/15335448488512_zh-CN.png)


## 如何查看态势感知Agent的日志？ {#section_bcm_ydk_s2b .section}

态势感知Agent的默认安装路径下包含一个data目录，该目录下的data.x即是日志文件。

-   Linux的默认安装路径如下：/usr/local/aegis/aegis\_client/aegis\_xx\_xx

    查看data目录时，系统返回结果如下。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/17031/15335448488966_zh-CN.png)

-   Windows的默认安装路径如下：C:\\Program Files \(x86\)\\Alibaba\\Aegis\\aegis\_client\\aegis\_xx\_xx

    查看data目录，系统返回结果如下。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/17031/15335448488967_zh-CN.png)


