# Authentication rules {#reference_hkk_n5q_12b .reference}

## Authentication rules used when a RAM user accesses the resources of a primary account by using Log Service APIs {#section_rj5_qj5_12b .section}

When a Resource Access  Management \(RAM\) user accesses the resources of a primary account by using Log Service APIs, Log Service backend performs RAM permission inspection to make sure the resource owner has granted relevant permissions to the caller.

Different  Log Service APIs determine the resources whose permissions must be checked according to the involved resources and the meanings of the API.  The authentication rules for each API are as follows.

**logstore**

|Action|Resource|
|:-----|:-------|
|Log: getlogstore|acs:log:**$\{regionName\}**:**$\{projectOwnerAliUid\}**:project/**$\{projectName\}**/logstore/**$\{logstoreName\}**|
|log:ListLogStores|acs:log:**$\{regionName\}**:**$\{projectOwnerAliUid\}**:project/**$\{projectName\}**/logstore/\*|
|log:CreateLogStore|acs:log:**$\{regionName\}**:**$\{projectOwnerAliUid\}**:project/**$\{projectName\}**/logstore/\*|
|log:DeleteLogStore|`acs:log:**$\{regionName\}**:**$\{projectOwnerAliUid\}**:project/**$\{projectName\}**/logstore/**$\{logstoreName\}**`|
|log:UpdateLogStore|`acs:log:**$\{regionName\}**:**$\{projectOwnerAliUid\}**:project/**$\{projectName\}**/logstore/**$\{logstoreName\}**`|

**Loghub**

The rule is applicable to APIs for data writing and consumption. The API GetCursor for getting data cursor and API GetLogs for getting data share the same action  \(log:GetCursorOrData\).

|Action|Resource|
|:-----|:-------|
|log:GetCursorOrData|acs:log:**$\{regionName\}**:**$\{projectOwnerAliUid\}**:project/**$\{projectName\}**/logstore/**$\{logstoreName\}**|
|log:ListShards|`acs:log:**$\{regionName\}**:**$\{projectOwnerAliUid\}**:project/**$\{projectName\}**/logstore/**$\{logstoreName\}**`|
|Log: postlogstorelogs|`acs:log:**$\{regionName\}**:**$\{projectOwnerAliUid\}**:project/**$\{projectName\}**/logstore/**$\{logstoreName\}**`|

**Config**

|Action|Resource|
|:-----|:-------|
|Log: createconfig|`acs:log:**$\{regionName\}**:**$\{projectOwnerAliUid\}**:project/**$\{projectName\}**/logtailconfig/*`|
|log:UpdateConfig|`acs:log:**$\{regionName\}**:**$\{projectOwnerAliUid\}**:project/**$\{projectName\}**/logtailconfig/**$\{logtailConfigName\}**`|
|log:DeleteConfig|`acs:log:**$\{regionName\}**:**$\{projectOwnerAliUid\}**:project/**$\{projectName\}**/logtailconfig/**$\{logtailConfigName\}**`|
|log:GetConfig|`acs:log:**$\{regionName\}**:**$\{projectOwnerAliUid\}**:project/**$\{projectName\}**/logtailconfig/**$\{logtailConfigName\}**`|
|log:ListConfig|`acs:log:**$\{regionName\}**:**$\{projectOwnerAliUid\}**:project/**$\{projectName\}**/logtailconfig/*`|

**machinegroup**

|Actions|Resources|
|:------|:--------|
|log:CreateMachineGroup|`acs:log:**$\{regionName\}**:**$\{projectOwnerAliUid\}**:project/**$\{projectName\}**/machinegroup/*`|
|log:UpdateMachineGroup|`acs:log:**$\{regionName\}**:**$\{projectOwnerAliUid\}**:project/**$\{projectName\}**/machinegroup/**$\{machineGroupName\}**`|
|log:DeleteMachineGroup|acs:log:**$\{regionName\}**:**$\{projectOwnerAliUid\}**:project/**$\{projectName\}**/machinegroup/**$\{machineGroupName\}**|
|log:GetMachineGroup|`acs:log:**$\{regionName\}**:**$\{projectOwnerAliUid\}**:project/**$\{projectName\}**/machinegroup/**$\{machineGroupName\}**`|
|log:ListMachineGroup|`acs:log:**$\{regionName\}**:**$\{projectOwnerAliUid\}**:project/**$\{projectName\}**/machinegroup/*`|
|log:ListMachines|acs:log:**$\{regionName\}**:**$\{projectOwnerAliUid\}**:project/**$\{projectName\}**/machinegroup/**$\{machineGroupName\}**|

**Interactive APIs for configuration and machine group**

|Actions|Resources|
|:------|:--------|
|log:ApplyConfigToGroup|`acs:log:**$\{regionName\}**:**$\{projectOwnerAliUid\}**:project/**$\{projectName\}**/logtailconfig/**$\{logtailConfigName\}** acs:log:**$\{regionName\}**:**$\{projectOwnerAliUid\}**:project/**$\{projectName\}**/machinegroup/**$\{machineGroupName\}**`|
|log:RemoveConfigFromGroup|`acs:log:**$\{regionName\}**:**$\{projectOwnerAliUid\}**:project/**$\{projectName\}**/logtailconfig/**$\{logtailConfigName\}** acs:log:**$\{regionName\}**:**$\{projectOwnerAliUid\}**:project/**$\{projectName\}**/machinegroup/**$\{machineGroupName\}**`|
|log:GetAppliedMachineGroups|`acs:log:**$\{regionName\}**:**$\{projectOwnerAliUid\}**:project/**$\{projectName\}**/logtailconfig/**$\{logtailConfigName\}**`|
|log:GetAppliedConfigs|`acs:log:**$\{regionName\}**:**$\{projectOwnerAliUid\}**:project/**$\{projectName\}**/machinegroup/**$\{machineGroupName\}**`|

