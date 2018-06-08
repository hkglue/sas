# 对外 DDoS 攻击行为排查 {#concept_cvk_x1c_b2b .concept}

## ECS 出现肉鸡行为，并有对外 DDoS 行为如何排查原因？ {#section_ifw_x1c_b2b .section}

一般情况下， ECS 对外发起 DDoS 是被黑客入侵成功导致，可以查看服务器是否有可疑进程和异常网络连接，对外 DDoS 后门一般具有高 CPU 使用率，高带宽使用的特点。

## ECS 上没有可疑进程，为什么态势感知也提示对外 DDoS 攻击？ {#section_jfw_x1c_b2b .section}

这种情况下请先确认对外 DDoS 中的攻击类型:

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13698/5992_zh-CN.png)

当攻击类型为：

-   **DNS**
-   **NTP**
-   **SNMP**
-   **SSDP**
-   **CHARGEN**
-   **PORTMAP**

这几类是黑客利用了服务器上 DNS、NTP 等服务进行反射型 DDoS 攻击，服务器并未被入侵，请检查 ECS 上有无对应服务或者端口。可以使用安全组或者 ECS 防火墙来限制访问，防止被恶意利用。

