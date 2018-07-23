# Supported logs and fields {#concept_vm2_pzc_zdb .concept}

This document introduces the types of logs and fields that are supported by the log retrieval feature of Threat Detection Service.

## Supported logs and fields {#section_tls_cwk_zdb .section}

The log retrieval feature allows you to query the following types of logs. You can click a log to view the fields that can be retrieved.

|Type| Log|Description|
|Server log|[Logon history](#section_ams_cwk_zdb)|Logs of successful logons|
|[Brute-force attack](#section_gms_cwk_zdb)|Logs of brute force cracking attacks|
|[Process snapshot](#section_qns_cwk_zdb)|Logs of process execution on the server|
|[Port snapshot](#section_tms_cwk_zdb)|Logs of listener ports on the server|
|[Account snapshot](#section_gns_cwk_zdb)|Logs of accounts on the server|
|[Process startup](#section_mms_cwk_zdb)|Logs of process initiation on the server|
|[Network connection ](#section_zms_cwk_zdb)|Logs of outgoing connections from the server|
|Web log|[Web access log](#section_xns_cwk_zdb)|HTTP logs of the cloud services|
|[Network session log](#section_j4s_cwk_zdb)|Logs of the 5-tuples of the cloud services|
|[DNS log](#section_p4s_cwk_zdb)|Domain name resolution logs|

## Logon history {#section_ams_cwk_zdb .section}

The following fields are supported in queries:

|Field|Data types|Description|
|uuid|string|Agent ID|
|ip|string|Server IP address|
|warn\_ip|string|Source IP|
|warn\_port|string|Logon port|
|warn\_user|string|Logon username|
|warn\_type|string|Logon type|
|warn\_count|string|Logon attempts|

## Brute-force attack {#section_gms_cwk_zdb .section}

The following fields are supported in queries:

|Field|Data types|Description|
|uuid|string|Agent ID|
|ip|string|Server IP address|
|warn\_ip|string|Attacker IP|
|warn\_port|string|Logon port|
|warn\_user|string|Logon username|
|warn\_type|string|Logon type|
|warn\_count|string|Logon attempts|

## Process initiation log {#section_mms_cwk_zdb .section}

The following fields are supported in queries.

|Field|Data types|Description|
|uuid|string|Agent ID|
|ip|string|Server IP address|
|pid|string|Process ID|
|groupname|string|User group|
|ppid|string|Parent process ID|
|uid|string|User ID|
|username|string|User name|
|filename|string|Filename|
|pfilename|string|Parent process filename|
|cmdline|string|Command line|
|filepath|string|Process path|
|pfilepath|string|Parent process path|

## Port snapshot {#section_tms_cwk_zdb .section}

The following fields are supported in queries:

|Field|Data types|Description|
|uuid|string|Agent ID|
|ip|string|Server IP address|
|src\_port|string|Listener port|
|src\_ip|string|Listener IP address|
|proc\_path|string|Process path|
|pid|string|Process ID|
|proc\_name|string|Process name|
|proto|string|Protocol|

## Network connection log {#section_zms_cwk_zdb .section}

The following fields are supported in queries.

|Field|Data types|Description|
|uuid|string|Agent ID|
|ip|string|Server IP address|
|src\_ip|string|Source IP|
|src\_port|string|Source port|
|proc\_path|string|Process path|
|dst\_port|string|Destination port|
|proc\_name|string|Process name|
|dst\_ip|string|Destination IP|
|status|string|Status|

## Account snapshot {#section_gns_cwk_zdb .section}

The following fields are supported in queries:

|Field|Data types|Description|
|uuid|string|Agent ID|
|IP|string|Server IP address|
|perm|string|Root permissions|
|home\_dir|string|Home directory|
|warn\_time|string|Password expiration notification time|
|groups|string|User's group|
|login\_ip|string|IP address of the last logon|
|last\_chg|string|Last time the password was modified|
|shell|string|Linux shell commands|
|domain|string|Windows domain|
|tty|string|Logon terminal|
|account\_expire|string|Account expiration time|
|passwd\_expire|string|Password expiration time|
|last\_logon|string|Last logon time|
|user|string|User|
|status|string|User status: 0 - Disabled; 1 - Normal|

## Process snapshot {#section_qns_cwk_zdb .section}

The following fields are supported in queries.

|Field|Data types|Description|
|uuid|string|Agent ID|
|ip|string|Server IP address|
|path|string|Process path|
|start\_time|string|Process start time|
|uid|string|User ID|
|cmdline|string|Command line|
|pname|string|Parent process name|
|name |string|Process name|
|pid|string|Process ID|
|User|string|User name|
|md5|string|Process file MD5; Not calculated if the file size exceeds 1 MB|

## Web access log {#section_xns_cwk_zdb .section}

The following fields are supported in queries.

|Field|Data types|Description|
|src\_ip|string|Source IP|
|src\_port|string|Source port number|
|dst\_ip|string|Destination IP|
|dst\_port|string|Destination port number|
|Request\_datatime|string|Request Time|
|host|string|hostname|
|uri|string|Request URI|
|method|string|Request method: GET or POST|
|referer|string|Source referer|
|user\_agent|string|Client user agent|
|ret\_code|string|Response code|
|jump\_location|string|URL that is redirected to|
|x\_forward\_for|string|Source x\_forward\_for|
|rsp\_content\_type|string|Request content type|
|rqs\_content\_type|string|Response content type|
|content\_length|string|Response data size|

## Network session log {#section_j4s_cwk_zdb .section}

The following fields are supported in queries.

|Field|Data types|Description|
|asset\_type|string|Asset type: RDS, SLB, or ECS|
|session\_time|datetime|Access time|
|src\_ip|string|Source IP|
|src\_port|string|Source port|
|dst\_ip|string|Destination IP|
|dst\_port|string|Destination port|
|proto|string|Protocol type: TCP/UDP|

## DNS log {#section_p4s_cwk_zdb .section}

The following fields are supported in queries.

|Field|Data types|Description|
|query\_datetime|datetime|Request time|
|src\_ip|string|Source IP|
|src\_port|string|Source port|
|dst\_ip|string|Destination IP|
|dst\_port|string|Destination port|
|response\_datetime|datetime|Response time|
|qname|string|Domain name resolved|
|Qtype|string|Request record type|
|client\_subnet|string|Client subnet|
|qid|string|Request ID|
|rcode|string|Response code|
|answer\_num|string|The number of answer fields|
|answer|string|The answer field|
|authority\_num|string|The number of authority fields|
|authority|string|The authority field|
|additional\_num|string|The number of additional fields|
|additional|string|The additional field|
|in\_out|string|In or out|
|region|string|Region|

