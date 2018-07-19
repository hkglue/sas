# Features {#concept_fc1_xvb_zdb .concept}

Situation Awareness Service \(SAS\) is available with the Basic Edition and the Enterprise Edition:

-   Basic Edition: detects unusual logon and instance vulnerabilities for free.
-   Enterprise Edition: supports annual and monthly subscriptions, and provides comprehensive security services, such as security alarms, instance and network vulnerability detection and resolution, baseline check, asset fingerprints, security analysis, and log retrieval.

For more information about the features of the Basic Edition and the Enterprise Edition, see the following descriptions:

## Comparison of features between the Basic Edition and the Enterprise Edition {#section_gmh_xvb_zdb .section}

The following table lists the features of SAS and compares the differences between the Basic Edition and the Enterprise Edition:

-   ×: indicates that the related feature is excluded in the service.
-   √: indicates that the related feature is included in the service.
-   Value-added: indicates that you must select the related feature to include it in your purchase.

|Feature|Item|Description|Basic Edition|Enterprise Edition|
|Security alarms|Unusual logon detection|Logon from unusual locations: SAS automatically records locations that are commonly used to log on to Elastic Compute Service \(ECS\) instances. You can also manually specify these locations. The system generates an alarm when a logon from an unusual location has been detected.|√|√|
|Brute-force password cracking: detects a logon to ECS instances after multiple failed attempts, which may be caused by brute-force password cracking.|√|√|
|Invalid IP logon: This feature allows you to specify valid IP addresses to be used to log on to ECS instances, such as bastion host IP addresses and local area network \(LAN\) IP addresses. Therefore, this system generates an alarm when detecting a logon with an unspecified IP address.|×|√|
|Invalid account logon: This feature allows you to specify the valid accounts for logging on to ECS instances. Therefore, this system generates an alarm when detecting a logon with an unspecified account.|×|√|
|Logon during invalid periods: This feature allows you to specify valid periods, such as office hours, for logging on to ECS instances. Therefore, this system generates an alarm when detecting a logon that does not occur during the specified period.|×|√|
|Webshell removal|Webshell detection: checks both instances and networks.-   Instance check: monitors the changes of Web directories on an instance in real time.
-   Network check: simulates Webshell execution and analyzes network protocols.

|Detects instances only.|√|
|Webshell removal: easily quarantines the detected Webshell in the console. Note: You can restore the Webshell within 30 days after isolation.|×|√|
|Scope of Webshell targets: Web scripts, such as PHP, ASP, and JSP files.|√|√|
|Malicious processes \(malware checking\)|Virus detection: Periodically scans processes, monitors process initiation events, and detects malicious viruses and Trojans using the anti-virus mechanism in the cloud.|×|√|
|Virus removal: easily terminates processes and quarantines malicious files in the console.|×|√|
|Scope of virus targets:-   Ransomware: file-encrypting ransomware such as WannaCry and CryptoLocker.
-   Malicious attacks: distributed denial-of-service \(DDoS\) Trojans, malicious scanning Trojans, and spam Trojans.
-   Mining software: resource consumption software that uses instances for illegal virtual currency mining.
-   Zombies: central control Trojans, malicious central control connections, and hacking tools.
-   Other viruses: worms, Mirai, and infectious viruses.

|×|√|
|Virus database:-   Update mechanism: updates the virus management in the cloud, and does not provide any on-premises detection engine.
-   Virus sample coverage: detects all types of viruses, and integrates the worldwide major anti-virus engines, proprietary sandbox, and machine learning engine in the cloud.

|×|√|
|Suspicious processes|Suspicious process detection: restores intrusion links based on real attack-defence scenarios in the cloud, creates a process whitelist, and generates alarms when detecting illegal and intrusive processes.|×|√|
|Scope of suspicious processes:-   Reverse shell: suspicious commands in Bash processes, and arbitrary commands remotely executed by instances.
-   Suspicious database commands: suspicious commands in databases, such as MySQL, PostgreSQL, SQLServer, Redis, and Oracle.
-   Illegal operations in application processes: illegal operations in application processes, such as Java, FTP, Tomcat, Docker containers, and Lsass.exe.
-   Illegal system processes: PowerShell, Secure Shell \(SSH\), Remote Desktop Protocol \(RDP\), smbd, and secure copy protocol \(SCP\).
-   Other suspicious processes: Visual Basic Script \(VBScript\) execution, accessing instances, writing crontab files, and Webshell injection.

|×|√|
|Suspicious process coverage: builds more than 1,000 process patterns for hundreds of processes, and analyzes suspicious processes by comparing them with these patterns.|×|√|
|Sensitive file tampering|Tampering detection: monitors sensitive directories and files in real time, and generates alarms when detecting suspicious reading, writing, and deletion processes.|×|√|
|Scope of tampering detection:-   System file tampering: malicious replacement of processes that execute Bash and ps commands, and operation of hidden illegal processes.
-   Core dump removal: malicious removal of website core dump files after an illegal logon to instances.
-   Drive-by downloading: malicious code injection into a Web page that causes the auto downloading of Trojans.
-   Other suspicious events: ransomware on the logon pages of Linux and MysqlDB, creating emails or Bitcoin wallet addresses.

|×|√|
|Unusual network connection|Unusual connection: monitors connections between instances and networks, and generates an alarm when detecting an illegal connection.|×|√|
|Scope of unusual connections: -   Active connections to unknown servers: active connections to suspicious IP addresses using reverse shell and Bash commands.
-   Malicious attacks: malicious software injection used to launch malicious attacks, such as SYN floods, User Datagram Protocol \(UDP\) floods, and Internet Control Message Protocol \(ICMP\) floods.
-   Suspicious communications: suspicious Webshell communications.

|×|√|
|Vulnerability management|Vulnerabilities of Linux software|Detection of Linux software vulnerabilities: compares software versions by using the Open Vulnerability and Assessment Language \(OVAL®\) matching engine, and generates alarms when detecting vulnerabilities from the Common Vulnerabilities and Exposures \(CVE®\) vulnerability database.|√|√|
|Vulnerability fix: fixes vulnerabilities automatically with easily applied updates, and generates vulnerability fix instructions for manual fixes.|×|√|
|Windows vulnerabilities|Detection of Windows vulnerabilities: obtains updates from Microsoft Updates for the Windows operating system, detects critical and other vulnerabilities, and generates alarms of these vulnerabilities.|√|√|
|Vulnerability fix: easily downloads updates, installs the updates silently, and then prompts you to restart the system if a restart is required.|√|√|
|WCMS vulnerabilities|Detection of Web content management system \(WCMS\) vulnerabilities: monitors Web directories, recognizes common website builders, and checks the vulnerability database to identify vulnerabilities in the website builders.|√|√|
|Vulnerability fix: uses proprietary updates developed by Alibaba Cloud to replace or modify source code and allows you to easily fix vulnerabilities.|×|√|
|Other vulnerabilities|Detection of other vulnerabilities: detects vulnerabilities related to software configurations and system components. The system can detect but cannot fix vulnerabilities.|√|√|
|Web vulnerability scanning|Simulates attacks on the Internet by using services in [Website Threat Inspector](https://www.aliyun.com/product/avds) to actively detect security vulnerabilities exposed to the Internet on your instance.|×|×|
|Baseline check|Instance baseline|Instance baseline check: initiates tasks to scan security configurations of instances, and generates notifications of vulnerable configurations.|×|√|
|Scope of instance baseline check:-   Account security: password policy compliance, and weak passwords of systems and applications.
-   System configurations: potential risks in group policies, logon baseline policies, and registry configurations.
-   Databases: critical threats in the configurations of databases such as Redis.
-   Compliance requirements: compliance with system baseline requirements, such as the CIS-Linux Centos7 benchmark.

|×|√|
|Check policy: supports a customized check policy that specifies the checked items, check cycle, and target instance group. Note: The system does not support customized check scripts.|×|√|
|Cloud service baseline|Cloud service baseline check: checks security configurations of ECS instances, Relational Database Service \(RDS\) instances, and other cloud services for hidden risks.|×|√|
|Scope of baseline check:-   ECS: checks for unnecessary ports opened by security groups.
-   Server Load Balancer \(SLB\): checks for unnecessary ports opened to the Internet for traffic forwarding, increasing the risk of system attacks.
-   RDS: checks whether database service is exposed to the Internet and whether a whitelist is configured.
-   Actiontrail: checks whether operation auditing is enabled, which facilitates event tracing.
-   Multi-factor authentication \(MFA\): checks whether two-factor authentication is enabled to prevent cracking of Alibaba Cloud accounts.
-   Others: checks whether an SLB whitelist and RDS encrypted communications are enabled.

|×|√|
|Asset fingerprints|Port listening|Collects and displays port listening information, and records changes to track opened ports.|×|√|
|Account management|Collects information about accounts and related permissions, and checks privileged accounts for privilege elevation. |×|√|
|Process management|Collects and displays process snapshots to track normal processes and detect unusual processes.|×|√|
|Software management|Checks software installation information, and in the case of critical vulnerabilities, quickly locates affected assets.|×|√|
|Website back-end management|Recognizes website back-end assets, and detects database-hitting attacks and unusual background logons. |×|√|
|Security analysis|Access analysis|Collects all traffic of SLB and ECS instances for centralized management, and recognizes crawling traffic and normal access traffic.|×|√|
|Attack analysis|Checks details of Web attacks and brute-force cracking against ECS instances.|×|√|
|Threat analysis|Recognizes targeted brute-force cracking and database-hitting, and discovers critical threats.|×|√|
|AK and password leakage|Monitors third-party code repository websites such as Github, retrieves public source code, such as the code uploaded and exposed without permissions, and checks the code for accounts and passwords of ECS, RDS, Redis, MySQL, and other assets.|×|√|
|10 screens|Provides the monitoring of business operations, such as the service operation monitor, the security emergency response center, the security awareness system, the security defense system, and the visits overview.|×|Value-added|
|Log retrieval|Process logs|Process initiation: records the details of process initiation, and supports searching process initiation logs.|×|Value-added|
|Process snapshots: takes and stores a snapshot of all processes that are running at a specified time, and can be used to search process snapshots.|×|Value-added|
|Network logs|Network connection logs: searches records of network connections that have been initiated by an instance. Web session logs: collects 5-tuples for Web sessions between instances and networks, and supports searching Web access logs. Web access logs: captures HTTP access logs of a website, and supports searching web access logs. This feature currently does not support HTTPS access logs.  DNS logs: searches outbound Domain Name System \(DNS\) request logs. This feature currently does not support private DNS servers. |×|Value-added|
|Other logs|Logon: searches logs of SSH and RDP logon processes.|×|Value-added|
|Brute-force cracking: searches logs of consecutive logon failures from SSH and RDP logon processes. |×|Value-added|
|Port listening snapshot: takes and stores a snapshot of all listening ports at a specified time, and supports searching port listening snapshots.|×|Value-added|
|Account snapshot: takes and stores a snapshot of all accounts at a specified time, and supports searching snapshots of accounts.|×|Value-added|
|Log shipping|Transfers security logs to [Log Service](https://www.aliyun.com/product/sls) for further analysis. You can also use Log Service to ship the security logs to MaxCompute or Object Storage Service \(OSS\) for custom analysis . |×|Value-added|

