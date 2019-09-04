# Security Center agent FAQ {#concept_bvy_mb5_q2b .concept}

-   [How do I view the log file of the Security Center agent?](#)
-   [How do I handle the "Permission denied" error when I install the Security Center agent on a Linux server?](#)

## How do I view the log file of the Security Center agent? {#2 .section}

The default installation path of the agent contains the data directory. The data.x file in this directory is the log file.

-   On a Linux server, the default installation path of the agent is /usr/local/aegis/aegis\_client/aegis\_xx\_xx.

    You can open this path and view the log file in the data directory.

    ![](images/8966_en-US.png)

-   On a Windows server, the default installation path of the agent is C:\\Program Files \(x86\)\\Alibaba\\Aegis\\aegis\_client\\aegis\_xx\_xx.

    You can open this path and view the log file in the data directory.

    ![](images/8967_en-US.png)


## How do I handle the "Permission denied" error when I install the Security Center agent on a Linux server? {#1 .section}

![](images/8509_en-US.jpg)

You can use the following methods to handle the error:

1.  Check whether the root account is used for installation, and run the `ls -al /etc/init.d/aegis` command to check whether you have permissions on the /etc/init.d/aegis directory.

    ![](images/8510_en-US.png)

2.  Check whether Yunsuo is installed on your server. You can run the `ps -ef | grep yunsuo_agent` or `ps aux | grep yunsuo` command to perform the check.

    ![](images/8511_en-US.png)

    If Yunsuo is installed, it may stop the installation of the agent. We recommend that you disable Yunsuo before installing the agent.

    The default path of Yunsuo is /usr/local/yunsuo\_agent.

    ![](images/8512_en-US.png)


