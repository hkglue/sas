# Agent离线排查 {#task_fkr_2lc_zdb .task}

如果您已按照[安装Agent](intl.zh-CN/用户指南/接入云安全中心/安装Agent.md#)为服务器成功安装云安全中心Agent，但在云安全中心控制台上仍看到该服务器的保护状态为**未受保护**，则说明Agent处于离线状态，请参照本文进行排查。

如果您的云安全中心Agent处于离线状态，请按照以下步骤进行排查：

1.  登录您的服务器，查看云安全中心Agent相关进程（`AliYunDun`和`AliYunDunUpdate`）是否正常运行。 

    如果云安全中心Agent相关进程无法运行，建议您重启服务器，或者参考[安装Agent](intl.zh-CN/用户指南/接入云安全中心/安装Agent.md#)重新安装云安全中心Agent。

    -   **Windows系统**

        在任务管理器中，查看相关进程是否正常运行。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13634/15531522524635_zh-CN.png)

    -   **Linux系统**

        执行`top`命令，查看相关进程是否正常运行。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13634/15531522524636_zh-CN.png)

2.  对于首次安装云安全中心Agent的服务器，如果在安装Agent后，保护状态仍然为**未受保护**，请参考以下方法，重新启动云安全中心Agent： 
    -   Linux 系统：执行`killall AliYunDun && killall AliYunDunUpdate && /usr/local/aegis/aegis_client/aegis_10_xx/AliYunDun`命令。

        **说明：** 您必须将命令中的`xx`替换为该目录下的最大的数字。

    -   Windows 系统：在服务项中重新启动以下两个服务项，选中对应服务，右键选择重新启动即可。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13634/15531522524637_zh-CN.png)

3.   检查您的服务器网络连接是否正常。 
    -   服务器有公网IP（如经典网络、EIP、云外机器）
        -   Windows 系统：在命令行中执行`ping jsrv.aegis.aliyun.com -l 1000`命令。
        -   Linux 系统：执行`ping jsrv.aegis.aliyun.com -s 1000`命令。
    -   服务器无公网IP（如金融云、VPC专有网络）
        -   Windows 系统：在命令行中执行`ping jsrv3.aegis.aliyun.com -l 1000`命令。
        -   Linux 系统：执行`ping jsrv3.aegis.aliyun.com -s 1000`命令。
4.   如果解析不通，请使用以下方法，检查您的服务器网络连接状况： 
    1.  确认您的服务器的DNS服务正常运行。如果DNS服务无法运行，重启您的服务器，或者检查服务器DNS服务是否有故障。
    2.  检查服务器是否设置了防火墙ACL规则或阿里云安全组规则。如果有，请确认已将云安全中心的服务端IP加入防火墙白名单（出、入方向均需添加）以允许网络访问。

        **说明：** 请将下列IP段的80端口添加至白名单，最后一个IP段需要同时添加80和443端口至白名单。

        -   140.205.140.0/24 80
        -   106.11.68.0/24 80
        -   110.173.196.0/24 80
        -   106.11.68.0/24 80
        -   100.100.25.0/24 80 443
    3.  检查您的服务器公网带宽是否为零。如果您的服务器公网带宽为零，请参考以下步骤进行处理：
        1.  在您服务器的hosts文件添加以下域名解析记录：
            -   国内经典网络： `100.100.110.61 jsrv.aegis.aliyun.com`、`100.100.45.131 jsrv.aegis.aliyun.com`、`100.100.110.62 update.aegis.aliyun.com`和 `100.100.45.29 update.aegis.aliyun.com`
            -   国外经典网络： `100.100.103.52 jsrv.aegis.aliyun.com`、`100.100.30.54 jsrv.aegis.aliyun.com` 、`100.100.30.55 update.aegis.aliyun.com`和`100.100.103.54 update.aegis.aliyun.com`
        2.  修改hosts文件后，执行`ping jsrv.aegis.aliyun.com`命令。

            **说明：** 如果返回的结果不是`100.100.25.3`，请您重启服务器或检查服务器DNS服务是否有故障。

        3.  如果仍然无法解析到正确的IP，您可以尝试修改云安全中心Agent安装目录下conf目录中的`network_config`配置文件，将`t_srv_domain`、`h_srv_domain`对应的值分别修改为`100.100.25.3`及`100.100.25.4`。修改完成后，重启云安全中心Agent进程。

            **说明：** 修改前请务必备份`network_config`配置文件。

            此方法只适用于公网带宽为零，且保护状态为**未受保护**的服务器。

    4.  如果Ping命令执行解析成功，再次尝试通过Telnet命令连接解析出的域名IP的80端口（例如，执行`telnet 140.205.140.205 80`命令），查看是否连通。如果无法连通，请确认防火墙是否存在相关限制。
5.  检查您的服务器CPU、内存是否长期维持较高占用率（如 95%、100%），此情况可能导致云安全中心Agent进程无法正常工作。 
6.  检查服务器是否已安装第三方的防病毒产品（如安全狗、云锁等）。部分第三方防病毒软件可能会禁止云安全中心Agent插件访问网络。 

    如果有，请暂时关闭该产品，并重新安装云安全中心Agent。


