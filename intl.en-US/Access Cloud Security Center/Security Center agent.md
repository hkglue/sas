# Security Center agent {#concept_rbw_fzc_zdb .concept}

## How Security Center agent works {#section_oqs_fdd_zdb .section}

The Security Center agent automatically sends online data to the Security Center server at an interval of five hours.

If the Security Center server has not received any information from the agent for 12 hours, the server determines that the server where the agent runs is offline. The Security Center server then changes the security status of the server to **Unprotected** in the console.

## Agent processes {#section_pqs_fdd_zdb .section}

Security Center runs the following Security Center agent processes on a server:

**Note:** Security Center uses the root account to run the Security Center agent processes on a Linux server. Security Center uses the system account to run the Security Center agent processes on a Windows server.

-   **AliYunDun** 

    Security Center runs this process on a server to establish a connection to the Security Center server.

    The directory of the process file varies by operating system, as follows:

    -   Windows 32-bits: C:\\Program Files\\Alibaba\\aegis\\aegis\_client
    -   Windows 64-bits: C:\\Program Files \(x86\)\\Alibaba\\aegis\\aegis\_client
    -   Linux: /usr/local/aegis/aegis\_client
-   **AliYunDunUpdate** 

    Security Center periodically runs this process on a server to verify if an update is available for the Security Center agent.

    The path of the process file varies depending on the operating system, as follows:

    -   Windows 32-bits: C:\\Program Files\\Alibaba\\aegis\\aegis\_update
    -   Windows 64-bits: C:\\Program Files \(x86\)\\Alibaba\\aegis\\aegis\_update
    -   Linux: /usr/local/aegis/aegis\_update

