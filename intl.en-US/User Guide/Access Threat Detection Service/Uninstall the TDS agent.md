# Uninstall the TDS agent {#concept_cwf_hzc_zdb .concept}

You can use the following methods to uninstall the Threat Detection Service \(TDS\) agent and disable the protection. After you have uninstalled the TDS agent, there is a waiting period of six hours before the Security Status of the server in the TDS console changes to unprotected.

**Note:** After you have uninstalled the agent, TDS initializes self protection. The protection duration is 24 hours. During this period, you can only manually reinstall the agent. When you reinstall the agent, you must ignore all the error messages that the system displays and run the install command more than three times.

## Automatically uninstall the TDS agent {#section_tdh_2kd_zdb .section}

**Prerequisites**

To uninstall the TDS agent, you must make sure that the status of the agent on the current server is online. An offline server cannot receive the uninstall instruction.

**Procedure**

Follow these steps to automatically uninstall the TDS agent:

1.  Log on to the [Threat Detection Service console](https://yundun.console.aliyun.com/?p=sas).
2.  In the left-side navigation pane, click **Settings**.
3.  Click **Install/Uninstall TDS Agent**.
4.  Click **Uninstall Agent** in the upper-right corner.
5.  Specify the server where the TDS agent runs in the Uninstall Agent dialog box, and click **Uninstall Now**.
6.  Wait for the system to uninstall the TDS agent on the specified server.

## Manually uninstall the TDS agent {#section_xdh_2kd_zdb .section}

Select a method that is applicable to the operating system of your server to manually uninstall the TDS agent:

**Linux servers**

1.  Log on to your server.
2.  Run the following command to download the script for uninstalling the TDS agent.

    ```
    wget http://update.aegis.aliyun.com/download/uninstall.sh
    ```

3.  Sequentially run the following commands to uninstall the TDS agent. 
    -   `chmod +x uninstall.sh`
    -   `./uninstall.sh`

**Windows servers**

1.  Log on to your server.
2.  [Download the script for uninstalling the TDS agent](http://update.aegis.aliyun.com/download/uninstall.bat) to your server.

    **Note:** You can also download the script to your computer and use an FTP client to upload the script to your server.

3.  Double-click the uninstall.bat file to run the script and uninstall the agent.

