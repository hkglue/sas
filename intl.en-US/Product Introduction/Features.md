# Features {#concept_fc1_xvb_zdb .concept}

Threat Detection Service \(TDS\) is available with the Basic Edition and the Enterprise Edition:

-   Basic Edition: Detects unusual logon and server vulnerabilities for free.
-   Enterprise Edition: supports annual and monthly subscriptions, and provides comprehensive security services, such as security events detection, server vulnerability detection and resolution, baseline check, asset fingerprints, log retrieval, overall log analysis and big screen monitoring.

## Feature comparison between Basic Edition and Enterprise Edition {#section_gmh_xvb_zdb .section}

The following table lists the features of TDS and compares the differences between Basic Edition and Enterprise Edition:

-   ×: indicates that the related feature is excluded in the service.
-   √: indicates that the related feature is included in the service.
-   Value-added: indicates that you must purchase the related feature additionally.

|Feature|Item|Description|Basic Edition|Enterprise Edition|
|-------|----|-----------|-------------|------------------|
|Security events|Unusual logon detection|Basic-   Logon from unusual locations: TDS automatically records locations that are commonly used to log on to Elastic Compute Service \(ECS\) instances. You can also manually specify these locations. The system generates an alarm when a logon from an unusual location is detected.
-   Brute-force password cracking: detects a logon to ECS instances after multiple failed attempts, which may be caused by brute-force password cracking.

|√|√|
|Advanced-   Invalid IP logon: This feature allows you to specify valid IP addresses to be used to log on to ECS instances, such as bastion host IP addresses and local area network \(LAN\) IP addresses. Therefore, this system generates an alarm when detecting a logon with an unspecified IP address.
-   Invalid account logon: This feature allows you to specify the valid accounts for logging on to ECS instances. Therefore, this system generates an alarm when detecting a logon with an unspecified account.
-   Logon during invalid periods: This feature allows you to specify valid periods, such as office hours, for logging on to ECS instances. Therefore, this system generates an alarm when detecting a logon that does not occur during the specified period.

|X|√|
|Security events|Webshell removal|Webshell detection: checks both instances and networks for web scripts, such as PHP, ASP, and JSP files. -   Instance check: monitors the changes of Web directories on an instance in real time.
-   Network check: simulates Webshell execution and analyzes network protocols.

|√ \(Checks instances only.\)|√|
|Webshell removal: easily quarantines the detected Webshell in the console. You can restore the Webshell within 30 days after isolation.|X|√|
|Malicious processes \(malware checking\)|Virus detection: Periodically scans processes, monitors process initiation events, and detects malicious viruses and Trojans using the anti-virus mechanism in the cloud.Virus removal: easily terminates processes and quarantines malicious files in the console.

Scope of virus targets:-   Ransomware: file-encrypting ransomware such as WannaCry and CryptoLocker.
-   Malicious attacks: Distributed Denial-of-Service \(DDoS\) Trojans, malicious scanning Trojans, and spam Trojans.
-   Mining software: resource consumption software that uses instances for illegal virtual currency mining.
-   Zombies: central control Trojans, malicious central control connections, and hacking tools.
-   Other viruses: worms, Mirai, and infectious viruses.

Virus database:-   Update mechanism: updates the virus management in the cloud, and does not provide any on-premises detection engine.
-   Virus sample coverage: detects all types of viruses, and integrates the worldwide major anti-virus engines, proprietary sandbox, and machine learning engine in the cloud.

|X|√|
|Suspicious processes|Suspicious process detection: restores intrusion links based on real attack-defense scenarios in the cloud, creates a process whitelist, and generates alarms when detecting illegal and intrusive processes.Scope of suspicious processes:-   Reverse shell: suspicious commands in Bash processes, and arbitrary commands remotely executed by instances.
-   Suspicious database commands: suspicious commands in databases, such as MySQL, PostgreSQL, SQLServer, Redis, and Oracle.
-   Illegal operations in application processes: illegal operations in application processes, such as Java, FTP, Tomcat, Docker containers, and Lsass.exe.
-   Illegal system processes: PowerShell, Secure Shell \(SSH\), Remote Desktop Protocol \(RDP\), smbd, and secure copy protocol \(SCP\).
-   Other suspicious processes: Visual Basic Script \(VBScript\) execution, accessing instances, writing crontab files, and Webshell injection.

Suspicious process coverage: builds more than 1,000 process patterns for hundreds of processes, and analyzes suspicious processes by comparing them with these patterns.

|X|√|
|Sensitive file tampering|Tampering detection: monitors sensitive directories and files in real time, and generates alarms when detecting suspicious reading, writing, and deletion processes.Scope of tampering detection:-   System file tampering: malicious replacement of processes that run Bash and ps commands, and operation of hidden illegal processes.
-   Core dump removal: malicious removal of website core dump files after an illegal logon to instances.
-   Drive-by downloading: malicious code injection into a Web page that causes the auto downloading of Trojans.
-   Other suspicious events: ransomware on the logon pages of Linux and MysqlDB, creating emails or Bitcoin wallet addresses.

|X|√|
|Unusual network connection|Unusual connection: monitors connections between instances and networks, and generates an alarm when detecting an illegal connection.Scope of unusual connections: -   Active connections to unknown servers: active connections to suspicious IP addresses using reverse shell and Bash commands.
-   Malicious attacks: malicious software injection used to launch malicious attacks, such as SYN floods, User Datagram Protocol \(UDP\) floods, and Internet Control Message Protocol \(ICMP\) floods.
-   Suspicious communications: suspicious Webshell communications.

|X|√|
|Vulnerability management|Vulnerabilities of Linux software|Detection of Linux software vulnerabilities: compares software versions by using the Open Vulnerability and Assessment Language \(OVAL®\) matching engine, and generates alarms when detecting vulnerabilities from the Common Vulnerabilities and Exposures \(CVE®\) vulnerability database.|√|√|
|Vulnerability fix: fixes vulnerabilities automatically with easily applied updates, and generates vulnerability fix instructions for manual fixes.|X|√|
|Windows vulnerabilities|Detection of Windows vulnerabilities: obtains updates from Microsoft Updates for the Windows operating system, detects critical and other vulnerabilities, and generates alarms of these vulnerabilities.|√|√|
|Vulnerability fix: easily downloads updates, installs the updates silently, and then prompts you to restart the system if a restart is required.|√|√|
|WCMS vulnerabilities|Detection of Web content management system \(WCMS\) vulnerabilities: monitors Web directories, recognizes common website builders, and checks the vulnerability database to identify vulnerabilities in the website builders.|√|√|
|Vulnerability fix: uses proprietary updates developed by Alibaba Cloud to replace or modify source code and allows you to easily fix vulnerabilities.|X|√|
|Baseline check|Server baseline|Server baseline check: initiates tasks to scan security configurations of servers, and generates notifications of vulnerable configurations. Scope of server baseline check:-   Account security: password policy compliance, and weak passwords of systems and applications.
-   System configurations: potential risks in group policies, logon baseline policies, and registry configurations.
-   Databases: critical threats in the configurations of databases such as Redis.
-   Compliance requirements: compliance with system baseline requirements, such as the CIS-Linux Centos7 benchmark.

Check policy: supports a customized check policy that specifies the checked items, check cycle, and target server group. The system does not support customized check scripts.

|X|√|
|Asset fingerprints|Asset fingerprints|Port: collects and displays port listening information, and records changes to track opened ports.Account: collects information about accounts and related permissions, and checks privileged accounts for privilege elevation.

Process: collects and displays process snapshots to track normal processes and detect unusual processes.

Software: checks software installation information, and in the case of critical vulnerabilities, quickly locates affected assets.

Website background: recognizes website back-end assets, and detects user enumeration attempts and unusual background logons.

|X|√|
|Log retrieval|Log retrieval|Server logs-   Logon: searches logs of SSH and RDP logon processes.
-   Brute-force cracking: searches logs of consecutive logon failures from SSH and RDP logon processes.
-   Port listening snapshot: takes and stores a snapshot of all listening ports at a specified time, and supports searching port listening snapshots.
-   Account snapshot: takes and stores a snapshot of all accounts at a specified time, and supports searching snapshots of accounts.
-   Process snapshots: takes and stores a snapshot of all processes that are running at a specified time, and can be used to search process snapshots.
-   Process initiation: records the details of process initiation, and supports searching process initiation logs.
-   Network connection logs: searches records of network connections that have been initiated by an instance.

Network logs-   Web session logs: collects 5-tuples for Web sessions between instances and networks, and supports searching Web session content.
-   Web access logs: captures HTTP access logs of a website, and supports searching web access logs. This feature currently does not support HTTPS access logs.
-   DNS logs: searches outbound Domain Name System \(DNS\) request logs. This feature currently does not support private DNS servers.

|X|Value-added|
|Log analysis|Overall log analysis|TDS provides real-time log search and analysis, which covers all types of logs for TDS, such as starting of server process, outgoing network connection, system logon, DNS request, etc.|X|√|

