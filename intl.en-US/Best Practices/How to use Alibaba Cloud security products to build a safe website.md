# How to use Alibaba Cloud security products to build a safe website {#concept_rfh_ldb_ygb .concept}

This article describes how to build a safe website with Alibaba Cloud security products DDoS Protection, Web Application Firewall \(WAF\) and Security Center.

## DDoS Protection {#section_nsb_ckb_ygb .section}

DDoS Protection is a service that features a set of high-defensive IPs, and acts as a protective barrier for the origin. It safeguards network servers under high volume DDoS attacks. There are two DDoS Protection editions in Alibaba Cloud, they are [Anti-DDoS Pro](https://www.alibabacloud.com/help/doc-detail/28464.htm) and [Anti-DDoS Premium](https://www.alibabacloud.com/help/doc-detail/86301.htm).

## Web Application Firewall \(WAF\) {#section_jlv_hkb_ygb .section}

[Alibaba Cloud WAF](https://www.alibabacloud.com/help/doc-detail/28517.htm) helps you to defend against common web attacks such as SQL injections, Cross-site scripting \(XSS\), web shell, Trojan, and unauthorized access, and to filter out massive HTTP flood requests. It protects your web resources from being exposed and guarantees your website security and availability.

## Security Center {#section_upx_3kb_ygb .section}

Security Center service with security event detection, vulnerability scanning, and configuration baseline check.

## Limitations of use DDoS Protection and Web Application Firewall in China {#section_tsy_mkb_ygb .section}

According to Measures for the Administration of Internet Information Services and Registration Administration Measures for Non-Commercial Internet Information Services, China mandates a filing system for non-commercial Internet information services and a licensing system for commercial Internet information services. Anyone that has not obtained an ICP registration is prohibited from operating Internet information services. Specifically, all websites that provide services to Mainland China must first obtain the ICP registration. If your website is hosted on an instance deployed within Mainland China or uses Security Products like DDoS Protection, Web Application Firewall \(WAF\) within Mainland China, you can apply for ICP registration through the [Alibaba Cloud ICP Filing system](https://beian.aliyun.com/order/selfBaIndex.htm). For more information, see [ICP Registration](https://www.alibabacloud.com/help/doc-detail/36907.htm).

## Prerequisites {#section_mr4_4kb_ygb .section}

Before you begin, make sure of the following:

-   You have Alibaba Cloud Account If not, [sign up with Alibaba Cloud](https://www.alibabacloud.com/help/doc-detail/50482.htm) and [add a payment method](https://www.alibabacloud.com/help/doc-detail/50517.htm).
-   If you want to purchase any security products in Mainland China, [register by using your real name](https://www.alibabacloud.com/help/doc-detail/52595.htm) and at least one domain completed ICP filing.

## Overview {#section_gmd_rkb_ygb .section}

The following figure illustrates the best practice to build up a safe website:

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/133907/156032216039794_en-US.jpg)

In order to improve user experience in Mainland China. Alibaba Cloud recommend you to duplicate your website resources in China Region to guarantee performance is not impacted by GFW. You can also use Alibaba Cloud DNS to ensure all DNS queries are rapidly responded to by the server in closest geographic proximity. For more information, see [Alibaba Cloud DNS](https://www.alibabacloud.com/help/doc-detail/58165.htm).

## Procedure {#section_qzj_2lb_ygb .section}

1. Enable and configure Web Application Firewall \(WAF\).

2. Apply protection configuration in Web Application Firewall \(WAF\).

|Protection Function|Recommended Setting|Description|
|-------------------|-------------------|-----------|
|Web Application Protection| -   **Status:** Enable
-   **Mode:** Protection
-   **Mode of protection policy:** Normal

 |When you find that many requests are intercepted by mistake under the normal mode, we recommend that you use the **Loose mode**. When you require stricter protection against path traversal, SQL injection, and command running attacks, we recommend that you use the **Strict mode**.|
|Malicious IP Penalty|**Status:** Enable|The IP address would be blocked for 6 minutes if there are 2 threats from that IP found in 1 minute.|
|HTTP Flood Protection| -   **Status:** Enable
-   **Mode:** Normal
-   **Custom Rules:** Enable
-   **Recommended Rules setting**:When a single source IP address accesses \[URL\] for more than \[XX\] times within \[XX\] seconds, block this IP address for \[XX\] hour. The block frequency depends on your actual business situation.

 |When you find many HTTP flood attacks are not blocked in the Normal mode, you can switch to the **Emergency mode**. In Emergency mode, WAF imposes strong blocking rules against HTTP flood attacks, but it may also cause many false positives.|
|HTTP ACL Policy| -   **Status:** Enable
-   **Matching Field:** IP
-   **Logical Operator:** Does not have
-   **Matching content:** \[IP subnet\]
-   **Action:**Block

 |If your website is not serve public. You can configure IP HTTP fields in HTTP ACL Policy to whitelist certain of IP addresses. You can also combine three conditions at most to fit different business scenarios such as anti-leech and allow specify User-Agent.|
|New intelligent protection engine|**Status:** Enable|The intelligent protection engine mainly protects against SQL injection and other web attack methods, not HTTP flood attacks. If you have high web attack protection requirements, we recommend that you enable the new intelligent protection engine function.|
|Sensitive information leak prevention| -   **Status:** Enable
-   **Matching Condition:**Response Code includes \[4XX\]
-   **Matching Action:** Block
-   **Matching Condition:**Sensitive Info includes \[ ID Cards, Credit Cards, Telephone No.\]
-   **Matching Action:** Sensitive Information filtering

 |You can set rules to block of specific HTTP request status codes to avoid leaking sensitive server information. For example, you can set the following protection rule to block HTTP 404 status codes. For specified webpage URLs that may display mobile phone numbers, ID card numbers, and other sensitive information, configure the relevant rules to filter this information or provide warnings. For example, you can set the following protection rule to filter ID card numbers on the webpage.|

3. Configure security group to protect source website servers.

4. Enable and configure DDoS Protection.

5. Enable Security Center and install the Agent.

6. Configure Security Center Baseline check and vulnerability scanning.

Below are listed of supported check items and recommended setting:

|Category|Check items|Recommended Setting|
|--------|-----------|-------------------|
|Database| -   Memcached Security Baseline
-   Redis Security Baseline
-   MongoDB Baseline

 |If you are running NoSQL services in ECS. Select the according database security baseline checking.|
|System| -   CentOS Linux 7 Security Baseline
-   CentOS Linux 6 Security Baseline
-   Windows 2008 R2 Security Baseline
-   Windows 2012 R2 Security Baseline

 |Depends on the operating system you are running. Select the according system security baseline checking.|
|Weak Password| -   PostgreSQL Weak Password
-   Linux Weak Password
-   FTP Anonymous Logon Configurations
-   SQL Server Weak Password
-   MySQL Weak Password
-   Windows Account Weak Password
-   FTP Weak Password

 |Depends on the operating system you are running. Select **Linux Weak Password** or **Windows Account Weak Password**. If you are running additional services in ECS. Select the according weak password baseline checking.|
|Middleware Baseline| -   Apache Tomcat 7 Security Baseline

 |Currently Alibaba Security Center only support Tomcat 7 security baseline checking. If you are running Tomcat 7 in ECS. Select Apache Tomcat 7 Security Baseline checking.|

