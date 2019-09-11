# Information collection scope of Security Center {#concept_ic3_lvz_dhb .concept}

Security Center connects the agent on your server and the security module in the cloud. It provides features including security alerts, vulnerability management, baseline check, attack analysis, and security situation visualization.

Read the following note carefully:

**Note:** If the information collection scope of Security Center changes, Alibaba Cloud informs you of the changes on the Alibaba Cloud official website. If you do not accept the changes, you have the right to stop using Alibaba Security Center. In this case, you can uninstall the agent on your server. For more information, see [Uninstall the agent](../../../../reseller.en-US/Access Cloud Security Center/Uninstall the Security Center agent.md#). If you continue using Alibaba Security Center, you are deemed to have accepted these changes.

## Suspicious file information {#section_xmt_vhc_3gb .section}

To provide malicious file detection, Security Center uploads the information about suspicious files to the security module in the cloud for verification. The file information includes the path, MD5 value, and time of creation. If a file is confirmed to be malicious, Security Center sends you an alert.

## Suspicious process information {#section_egh_rvz_dhb .section}

To provide malicious process detection, Security Center uploads the information about suspicious processes to the security module in the cloud for verification. The process information includes the process name, parameters required to start the process, process file path, and process start time. If a process is confirmed to be malicious, Security Center sends you an alert.

## Account information {#section_fgh_rvz_dhb .section}

To provide features such as logon audit, suspicious account alerts, and brute-force attack prevention, Security Center regularly analyzes and uploads account information and logon information of the server. The account information includes usernames and user permissions. The logon information includes logon names and logon IP addresses. If an unusual logon is detected, Security Center sends you an alert.

## Suspicious connection information {#section_ggh_rvz_dhb .section}

To provide unusual connection detection, Security Center uploads the information about suspicious connections to the security module in the cloud for verification. The suspicious connection information includes the source IP address, source port, destination IP address, and destination port. If a connection is confirmed to be unusual, Security Center sends you an alert.

## Server asset information {#section_hgh_rvz_dhb .section}

To provide asset management, Security Center regularly collects the server asset information, including the software information, port listening information, and running website information.

