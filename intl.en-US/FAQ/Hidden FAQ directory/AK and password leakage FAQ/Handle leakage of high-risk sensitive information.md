# Handle leakage of high-risk sensitive information {#concept_ejd_xvb_b2b .concept}

GitHub is a popular open-source code management and version control system. Though GitHub brings convenience to developers, it also causes a lot of security risks. If a developer uses **public** code bases to manage source code, the code may be leaked. As a result, sensitive information is leaked, including the accounts and passwords, AccessKey information, and email accounts and passwords in database connection configuration files.

## Leakage of high-risk sensitive enterprise information {#section_cl4_xvb_b2b .section}

Users often use GitHub, Gitee, or other platforms to manage source code. The code contains or may contain the following sensitive information: Alibaba Cloud account AccessKey information, accounts and passwords of RDS databases, accounts and passwords of emails, or accounts and passwords of user-created databases based on ECS. If the preceding account information is leaked, malicious users may **use the information to access the Alibaba Cloud resources and data of the enterprise or individual users**.

After a user uses ECS to create a cloud database, developers may write sensitive information, such as the database connection password and email password, in the database connection configuration file. Attackers may obtain the leaked passwords from GitHub and steal the enterprise data. This may cause major security risks to the enterprise.

## Solutions {#section_dl4_xvb_b2b .section}

-   We recommend that you use a **private** GitHub code base or build an internal code management system to prevent source code leakage.
-   If sensitive information is leaked, log on to the console to prevent further leakage. For example, if the AccessKey information is leaked, [disable and reset the AccessKey, or delete the AccessKey](https://ak-console.aliyun.com/#/accesskey), and delete the code from GitHub.
-   Regularly go to the [log retrieval platform](https://sls.console.aliyun.com/#/) to view the server access logs. Check whether data leakage has occurred. For example, open the Web access log, and specify the URI field to locate the paths that contain files related to the AccessKey pair.
-   Set internal standards on security O&M and restricted development operations. Provide training for IT administrators to improve information security.

