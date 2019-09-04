# Suggestions on handling baseline risks {#concept_vrh_x3p_r2b .concept}

Security Center can check the baseline configuration on your servers and alert you about the detected risks. This topic describes suggestions on handling these risks.

## SSH logon configuration {#section_ysm_bjp_r2b .section}

**Change the default logon port to a non-22 port**

1.  For a Linux system server, run the `vim /etc/ssh/sshd_config` command to modify the configuration file.
2.  Locate the line that contains `#Port 22`. Delete the number sign \(`#`\), and change 22 to a new port number.

    For example, modify this line to `Port 50000`.

3.  Press the ESC key to enter the command-line mode, and enter `:wq` to save the changes.
4.  Run the `service sshd restart` or `/etc/init.d/sshd restart` command to restart the sshd service.

**Modify PermitRootLogin to disable remote SSH logon for the root user**

1.  For a Linux system server, run the `vim /etc/ssh/sshd_config` command to modify the configuration file.
2.  Locate the line `PermitRootLogin yes`, and modify this line to `PermitRootLogin no`.
3.  Press the ESC key to enter the command-line mode, and enter `:wq` to save the changes.
4.  Run the `service sshd restart` or `/etc/init.d/sshd restart` command to restart the sshd service.

## Process permission configuration {#section_gzj_y3p_r2b .section}

Security Center checks whether the Web server processes and the database processes are run by the root user or system user in Linux or by the administrator or system user in Windows. If any risk is detected, you can perform the following steps to enable a lower-privilege account to run the Web server or database processes.

**Windows OS**

1.  For a Windows system, open Windows Task Manager to view the process details. If the username of the Web server or the database service is administrator or system, go to the next step.
2.  Create an account with normal privileges.
3.  Grant this account the read and write permissions on the execution directory of the Web server or the database.
4.  Use this account to log on to the system, and start the Web server or database.

**Linux OS**

For a Linux system, you can compile source code to handle risks in applications such as NGINX, Apache, and MySQL.

You can perform the operations recommended for Windows users to handle risks in applications such as Memcache, MongoDB, and Redis.

**Note:** For a Linux system, you can run the `ps –aux` command to check whether the first line of a process is root. This line indicates the user that is allowed to run the process.

## Registry configuration {#section_jzj_y3p_r2b .section}

Security Center can detect risks in the registry of your server. We recommend that you handle these risks by modifying the related registry keys.

For example, if a registry key is Scripting.FileSystemObject,

![](images/8918_en-US.png)

modify it to Scripting.FileSystemObject.bak.

![](images/8919_en-US.png)

If you are not authorized to modify a registry key, you can take the following steps to change the permission settings of this registry key and its subkeys:

1.  Right-click this registry key, and choose **Permissions**.
2.  Click **Advanced**. Click the **Owner** tab.

    ![](images/8920_en-US.png)

    As shown in the preceding figure, the current owner of the registry key is TrustedInstaller. Therefore, the current administrator is not authorized to modify this key.

3.  Change the owner to Administrators. If the Administrators group is not displayed, click **Other users or groups**, and add **Administrator**.

    ![](images/8921_en-US.png)

4.  After the owner of the registry key is changed to Administrators, you can modify this key.

