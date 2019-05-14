# Features {#concept_fc1_xvb_zdb .concept}

Security Center is available in Basic edition and Enterprise Editio.:

-   **Basic** Edition: Detects unusual logon and server vulnerabilities. Basic Edition is available for free.
-   **Enterprise** Edition: Provides comprehensive security services, including security events, server vulnerability detection and resolution, baseline check, asset fingerprints, and log retrieval. Enterprise Edition is charged by annual and monthly subscription.

## Feature comparison between Basic/Advanced/Enterprise Edition {#section_gmh_xvb_zdb .section}

The following table compares the features provided by Basic Edition, Advanced Edition and Enterprise Edition of Security Center:

-   **×** indicates that the related feature is excluded in the service.
-   **√** indicates that the related feature is included in the service.
-   **Value-added** indicates that you must purchase the related feature additionally.

|Feature|Item|Description|Basic|Advanced|Enterprise|
|-------|----|-----------|-----|--------|----------|
|Security events|Unusual logon detection|Basic detection -   Logon from unusual locations: Security Center automatically records locations that are commonly used to log on to Elastic Compute Service \(ECS\) instances. You can also manually specify these locations in Security Center console. The system will generate an alarm when a logon from an unusual location is detected.
-   Brute-force cracking: Security Center detects a logon to ECS instances after multiple failed attempts, which may be caused by brute-force password cracking.

 |√|√|√|
|Advanced detection -   Invalid IP logon: This feature allows you to configure valid IP addresses for logging on to ECS instances, such as bastion host IP addresses and local area network \(LAN\) IP addresses. Therefore, this system generates an alarm when detecting a logon with an unspecified IP address.
-   Invalid account logon: This feature allows you to specify the valid accounts for logging on to ECS instances. Therefore, this system generates an alarm when detecting a logon with an unspecified account.
-   Logon during invalid periods: This feature allows you to specify valid periods, such as office hours, for logging on to ECS instances. Therefore, this system generates an alarm when detecting a logon that does not occur during the specified period.

 |X|√|√|
|Security events|Webshell removal|Webshell detection: checks both instances/servers and networks for web scripts, such as PHP, ASP, and JSP files. -   Instance check: monitors the changes of Web directories on an instance in real time.
-   Network check: simulates Webshell execution and analyzes network protocols.

 |X|√|√|
|Webshell removal: easily quarantines the detected Webshell in the console. You can restore the Webshell within 30 days after isolation.|X|√|√|
|Malicious processes \(malware checking\)|Virus detection: Periodically scans processes, monitors process initiation events, and detects malicious viruses and Trojans using the anti-virus mechanism in the cloud. Virus removal: Terminates processes and quarantines malicious files in the console.

 Scope of virus targets: -   Ransomware: File-encrypting ransomware such as WannaCry and CryptoLocker.
-   Malicious attacks: Distributed Denial-of-Service \(DDoS\) Trojans, malicious scanning Trojans, and spam Trojans.
-   Mining software: Resource consumption software that uses instances for illegal virtual currency mining.
-   Zombies: Central control Trojans, malicious central control connections, and hacking tools.
-   Other viruses: Worms, Mirai, and infectious viruses.

 Virus database: -   Update mechanism: Updates the virus management in the cloud, and does not provide any on-premises detection engine.
-   Virus sample coverage: Detects all types of viruses, and integrates the worldwide major anti-virus engines, proprietary sandbox, and machine learning engine in the cloud.

 |X|√|√|
|Suspicious processes|Suspicious process detection: Restores intrusion links based on real attack-defense scenarios in the cloud, creates a process whitelist, and generates alarms when detecting illegal and intrusive processes. Scope of suspicious types:

 -   Reverse shell: Suspicious commands in Bash processes, and arbitrary commands remotely executed by instances.
-   Suspicious database commands: Suspicious commands in databases, such as MySQL, PostgreSQL, SQLServer, Redis, and Oracle.
-   Illegal operations in application processes: Illegal operations in process such as Java, FTP, Tomcat, Docker containers, and Lsass.exe.
-   Illegal system processes: PowerShell, Secure Shell \(SSH\), Remote Desktop Protocol \(RDP\), smbd, and secure copy protocol \(SCP\).
-   Other suspicious processes: Visual Basic Script \(VBScript\) execution, accessing instances, writing crontab files, and Webshell injection.

 Suspicious process coverage: Builds more than 1,000 process patterns for hundreds of processes, and analyzes suspicious processes by comparing them with these patterns.

 |X|√|√|
|Sensitive file tampering|Tampering detection: Monitors sensitive directories and files in real time, and generates alarms when detecting suspicious reading, writing, and deletion processes.Scope of tampering detection: -   System file tampering: Malicious replacement of processes that run Bash and ps commands, and operation of hidden illegal processes.
-   Core dump removal: Malicious removal of website core dump files after an illegal logon to instances.
-   Drive-by downloading: Malicious code injection into a Web page that causes the auto downloading of Trojans.
-   Other suspicious events: Ransomware on the logon pages of Linux and MysqlDB, creating emails or Bitcoin wallet addresses.

 |X|√|√|
|Unusual network connection|Unusual connection: Monitors connections between instances and networks, and generates an alarm when detecting an illegal connection.Scope of unusual connections: -   Active connections to unknown servers: Active connections to suspicious IP addresses using reverse shell and Bash commands.
-   Malicious attacks: Malicious software injection used to launch malicious attacks, such as SYN floods, User Datagram Protocol \(UDP\) floods, and Internet Control Message Protocol \(ICMP\) floods.
-   Suspicious communications: Suspicious Webshell communications.

 |X|√|√|
|Vulnerability management|Vulnerabilities of Linux software|Detection of Linux software vulnerabilities: Compares software versions by using the Open Vulnerability and Assessment Language \(OVAL®\) matching engine, and generates alarms when detecting vulnerabilities from the Common Vulnerabilities and Exposures \(CVE®\) vulnerability database.|√|√|√|
|Vulnerability fix: Fixes vulnerabilities automatically with easily applied updates, and generates vulnerability fix instructions for manual fixes.|X|√|√|
|Windows vulnerabilities|Detection of Windows vulnerabilities: Obtains updates from Microsoft Updates for the Windows operating system, detects critical and other vulnerabilities, and generates alarms of these vulnerabilities.|√|√|√|
|Vulnerability fix: Downloads updates, installs the updates silently, and then prompts you to restart the system if required.|X|√|√|
|WCMS vulnerabilities|Detection of Web content management system \(WCMS\) vulnerabilities: Monitors Web directories, recognizes common website builders, and checks the vulnerability database to identify vulnerabilities in the website builders.|√|√|√|
|Vulnerability fix: Uses proprietary updates developed by Alibaba Cloud to replace or modify source code and allows you to easily fix vulnerabilities.|X|√|√|
|Baseline check|Server baseline|Server baseline check: Initiates tasks to scan security configurations of servers, and generates notifications for vulnerable configurations. Scope of server baseline check: -   Account security: Password policy compliance, and weak passwords of systems and applications.
-   System configurations: Potential risks in group policies, logon baseline policies, and registry configurations.
-   Databases: Critical threats in the configurations of databases such as Redis.
-   Compliance requirements: Compliance with system baseline requirements, such as the CIS-Linux Centos7 benchmark.

 Check policy: Supports a customized check policy that specifies the checked items, check cycle, and target server group. The system does not support customized check scripts.

 |X|X|√|
|Asset fingerprints|Asset fingerprints|Port: Collects and displays port listening information, and records changes to track opened ports. Account: Collects information about accounts and related permissions, and checks privileged accounts for privilege elevation.

 Process: Collects and displays process snapshots to track normal processes and detect unusual processes.

 Software: Checks software installation information, and in the case of critical vulnerabilities, quickly locates affected assets.

 Website background: Recognizes website back-end assets, and detects user enumeration attempts and unusual background logons.

 |X|X|√|
|Log analysis|Overall log analysis|Security Center provides real-time log search and analysis, which covers all types of logs for Cloud Security Center, such as starting of server process, outgoing network connection, system logon, DNS request, etc.|X|Value-added|Value-added|
|Alert correlation analysis|Alert correlation analysis|Alert correlation rules automatically group the related events together and then generate a related alert. It can help you see all the related alerts on one page, and provide you with centralized management on the alerts and related events.|X|X|√|

