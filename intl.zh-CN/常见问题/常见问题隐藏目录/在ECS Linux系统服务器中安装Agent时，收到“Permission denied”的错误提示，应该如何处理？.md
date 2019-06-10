# 在ECS Linux系统服务器中安装Agent时，收到“Permission denied”的错误提示，应该如何处理？ {#concept_593050 .concept}

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/475623/156015945748946_zh-CN.jpg)

您可以参考以下方法来解决该问题。

1.  检查是否通过root账号进行安装，并且执行`ls -al /etc/init.d/aegis`命令查看对/etc/init.d/aegis目录是否有操作权限。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/475623/156015945748948_zh-CN.png)

2.  查看您的服务器是否安装了云锁。您可以通过执行`ps -ef | grep yunsuo_agent`或`ps aux | grep yunsuo`命令进行检查。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/475623/156015945848949_zh-CN.png)

    如果服务器上已安装云锁，则云安全中心Agent的安装过程可能会被云锁拦截。建议您暂时关闭云锁后，再尝试安装。

    云锁的默认目录是/usr/local/yunsuo\_agent。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/475623/156015945848950_zh-CN.png)


