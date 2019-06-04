# 安装Agent提示“Permission denied”错误 {#concept_40494_zh .concept}

您在 ECS Linux 系统服务器中安装云安全中心Agent插件时，收到“Permission denied”的错误提示。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/163231/155962736845517_zh-CN.jpg)

## 解决方法 {#section_3q7_pvt_11p .section}

您可以参考以下方法进行排查，并解决该问题。

1.  检查是否通过 root 账号进行安装，并且执行`ls -al /etc/init.d/aegis`命令查看对于 /etc/init.d/aegis 目录是否有执行权限。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/163231/155962736845521_zh-CN.png)

2.  查看您的服务器是否安装了云锁。您可以通过执行`ps -ef | grep yunsuo_agent`或 `ps aux | grep yunsuo`命令进行检查。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/163231/155962736845522_zh-CN.png)

    如果服务器上已安装了云锁，可能会对安骑士插件的安装进行拦截。建议您暂时关闭云锁后，再尝试安装。

    云锁的默认目录是 /usr/local/yunsuo\_agent。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/163231/155962736845523_zh-CN.png)


