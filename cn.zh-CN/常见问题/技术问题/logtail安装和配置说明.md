# logtail安装和配置说明 {#concept_vpl_m2c_b2b .concept}

## Linux安装logtail {#section_af5_m2c_b2b .section}

具体内容请参考[Linux](https://help.aliyun.com/document_detail/28982.html)。

以华北 2（北京）为例，代码示例如下：

```
wget http://logtail-release-bj.oss-cn-beijing-internal.aliyuncs.com/linux64/logtail.sh 
chmod 755 logtail.sh 
sh logtail.sh install cn_beijing
```

## 配置logtail {#section_bf5_m2c_b2b .section}

具体内容请参考[非本人ECS配置logtail](https://help.aliyun.com/document_detail/49007.html)。

1.  查看阿里云账号ID。
2.  登录机器配置账号ID标识文件。

创建账号ID同名文件到/etc/ilogtail/users目录，如目录不存在请手动创建，一台机器上可以配置多个账号 ID，例如：

Linux

touch /etc/ilogtail/users/1559122535028493

touch /etc/ilogtail/users/1329232535020452

## logtail 动态机器组-自定义标识 {#section_cf5_m2c_b2b .section}

具体内容请参考[机器组标识](https://help.aliyun.com/document_detail/28983.html)。

开启 userdefined-id：

通过文件 /etc/ilogtail/user\_defined\_id 来设置 userdefined-id\(注意：若目录 /etc/ilogtail/ 或文件 /etc/ilogtail/user\_defined\_id 不存在，请手动创建。\)

例如，设置自定义机器标识如下：

cat /etc/ilogtail/user\_defined\_id1769112740192985@b3c6dbc1-0f95-4117-aaa7-b6f3692c12e7@101.201.196.217\(aliuid@机器实例@机器的公网ip\)

机器实例在配置页面可以获得：

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13700/5997_zh-CN.png)

user\_defined\_id也可以从机器组信息里获得：

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13700/5998_zh-CN.png)

点击修改机器组即可看到用户自定义标识：

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13700/5999_zh-CN.png)

