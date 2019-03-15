# Troubleshoot the problem of TDS agent going offline {#task_fkr_2lc_zdb .task}

If you have followed instructions in [Install the TDS agent](intl.en-US/User Guide/Access Threat Detection Service/Install the TDS agent.md#) and successfully installed the Threat Detection Service \(TDS\) agent on your server, but the security status of the server is still **Unprotected**, then the agent goes doffline. This article describes how to resolve this issue.

If your TDS agent is offline, follow these steps to resolve the issue:

1.  Log on to your server and check whether the TDS agent processes \(AliYunDun and AliYunDunUpdate\) are running. 

    If the TDS agent processes are not running, we recommend that you restart your server or reinstall the TDS agent. For more information, see [Install the TDS agent](intl.en-US/User Guide/Access Threat Detection Service/Install the TDS agent.md#).

    -   **Windows**

        Open the Task Manager and check whether the following processes are running.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13634/15526334694635_en-US.png)

    -   **Linux**

        Run the `top` command to check whether the following processes are running.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13634/15526334694636_en-US.png)

2.  If you have installed the TDS agent on a server for the first time and the security status of the server is **Unprotected** after installation, you can restart the TDS agent using the following methods: 
    -   Linux: Run the following command: `killall AliYunDun && killall AliYunDunUpdate && /usr/local/aegis/aegis_client/aegis_10_xx/AliYunDun`.

        **Note:** You must replace `xx` with the largest number in the directory.

    -   Windows: Restart the two services displayed in the following screenshot by right-clicking and selecting Restart.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13634/15526334704637_en-US.png)

3.   Check whether the network connection on your server is normal. 
    -   Servers with public IP addresses \(for example, servers connected to classic networks, EIPs, or external hosts\)
        -   Windows: Run the following command: `ping jsrv.aegis.aliyun.com -l 1000`
        -   Linux: Run the following command: `ping jsrv.aegis.aliyun.com -s 1000`
    -   Servers without public IP addresses \(for example, servers connected to the Financial Cloud, or VPCs\)
        -   Windows: Run the following command: `ping jsrv3.aegis.aliyun.com -l 1000`
        -   Linux: Run the following command: `ping jsrv3.aegis.aliyun.com -s 1000`
4.   If the ping command does not work, try the following methods: 
    1.  Make sure that the DNS service is running on your server. If the DNS service is not running, restart your server or check whether a DNS error has occurred.
    2.  Check whether firewall ACL rules or Alibaba Cloud security group rules have been configured on your server. If firewall rules or security group rules have been configured, make sure that the IP address of the TDS server is added to the whitelist \(both in the inbound and outbound directions\).

        **Note:** Allow the following network segments to access your server on port 80. For the last network segment, both port 80 and 443 must be enabled.

        -   140.205.140.0/24 80
        -   106.11.68.0/24 80
        -   110.173.196.0/24 80
        -   106.11.68.0/24 80
        -   100.100.25.0/24 80 443
    3.  Check whether the public network bandwidth on your server is zero. If the public network bandwidth on your server is zero, try the following methods:
        1.  Add the following name resolution rules to the hosts file on your server:
            -   Domestic classic websites: `100.100.110.61 jsrv.aegis.aliyun.com`, `100.100.45.131 jsrv.aegis.aliyun.com`, `100.100.110.62 update.aegis.aliyun.com` and `100.100.45.29 update.aegis.aliyun.com`
            -   International classic websites: `100.100.103.52 jsrv.aegis.aliyun.com`, `100.100.30.54 jsrv.aegis.aliyun.com`, `100.100.30.55 update.aegis.aliyun.com` and `100.100.103.54 update.aegis.aliyun.com`
        2.  After changing the hosts file, run the following command: `ping jsrv.aegis.aliyun.com`.

            **Note:** If `100.100.25.3` is not returned, restart your server or check whether a DNS error has occurred.

        3.  If the ping command does not return expected results, change the values of `t_srv_domain` and `h_srv_domain` in the `network_config` file under the TDS agent installation directory \(conf\) to `100.100.25.3` and `100.100.25.4` respectively. After making the changes, restart the TDS agent.

            **Note:** You must create a copy of the `network_config` file before making the changes.

            This method only applies when the public network bandwidth on the server is zero and the TDS agent is offline.

    4.  If the ping command returns the correct IP address, run the following telnet command to verify connectivity: `telnet 140.205.140.205 80`. If no connectivity is found, check firewall restrictions.
5.   Check whether high CPU or memory usage \(maintained at 95% or higher for a long period\) has occurred. High CPU or memory usage may prevent the TDS agent from running properly. 
6.   Check whether third-party security products \(such as Fortinet FortiGate\) have been installed on your server. Some third-party security software may prevent the TDS agent from accessing the network. 

    If security software is installed on your servers, we recommend that you temporarily disable or uninstall the software before reinstalling the TDS agent.


