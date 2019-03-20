# Machine group {#reference_oqd_t5q_12b .reference}

After a machine with Logtail installed is started normally, the machine is automatically associated with the current user based on the user information in the Logtail configuration.  Currently, the machine can be identified in the following three ways:

-   IP: The IP address corresponding to the hostname.  This is the easiest method to understand, but the IP address may be duplicated in the VPC and other environments.
-   UUID \(machine-uniqueid\): The UUID in DMI devices. For more information, see [RFC4122](http://www.ietf.org/rfc/rfc4122.txt).
-   Userdefined-id: You can customize the machine identification in the Logtail directory.

Attributes of each machine are as follows:

```
{
    "ip" : "testip1",
    "machine-uniqueid" : "testuuid1",
    "userdefined-id" : "testuserdefinedid1",
    "lastHeartbeatTime":1397781420
 }
```

The machine property parameters are as follows:

|Parameter|Type|Description|
|:--------|:---|:----------|
|ip|string|The IP address corresponding to the machine hostname.|
|uuid|string|The unique primary key marked by the machine, uploaded by Logtail.|
|userdefined-id|string|The user-defined machine identification,  uploaded by Logtail.|
|lastHeartbeatTime\(output-only\)|integer|The last heartbeat time of the machine \(the number of seconds since the epoch time\).|

## machinegroup {#section_lyj_k4f_sy .section}

Machinegroup is the machine group that belongs to the current user in the project. You can identify your machine group in a project by using IP address or user-defined identity.  The IP address is more easily identified while the user-defined identity can solve the problem of identical IP address in the VPC environment. You can select either of the two machine identification methods.

Machinegroup naming rules:

-   The name can only contain lowercase letters, numbers, hyphens \(-\), and underscores \(\_\).
-   The name must begin and end with a lowercase letter or number.
-   The name must be 2–128 bytes long.

## Example of the complete resource: {#section_ktz_l4f_sy .section}

```
{
    "groupName" : "testgroup",
    "groupType" : "",
    "groupAttribute" : {
        "externalName" : "testgroup",
        "groupTopic": "testgrouptopic"
    },
    "machineIdentifyType": "ip",
    "machineList" : [
        "ip1",
        "ip2"
        …
    ],
    "createTime": 1431705075,
    "lastModifyTime" : 1431705075
}
```

|Attribute name|Type|Required|Description|
|:-------------|:---|:-------|:----------|
|groupName|string|Yes| The machine group name, which must be unique in the project.|
|groupType|string|No|The machine group type, which is empty by default.|
|machineIdentifyType|string|Yes|The machine identification type, including IP and user-defined identity.|
|groupAttribute|object|Yes|The machine group attribute, which is empty by default.|
|machineList|array|Yes|The specific machine identification, which can be an IP address or user-defined identity.|
|createTime\(output-only\)|int|No|The resource creation time.|
|lastModifyTime\(output-only\)|int|No|The resource server update time.|

groupAttribute is described as follows.

|Attribute name|Type|Required|Description|
|:-------------|:---|:-------|:----------|
|groupTopic|string|No|The topic of a machine group, which is empty by default.|
|externalName|string|No|The external identification that the machine group depends on, which is empty by default.|

