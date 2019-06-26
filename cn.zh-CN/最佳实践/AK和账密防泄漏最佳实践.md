# AK和账密防泄漏最佳实践 {#concept_188635 .concept}

API凭证（即阿里云AccessKey）是用户访问内部资源最重要的身份凭证。用户调用API时的通信加密和身份认证会使用API凭证（即基于非对称密钥算法的鉴权密钥对）。API凭证是云上用户调用云服务API、访问云上资源的唯一身份凭证。

API凭证相当于登录密码，只是使用场景不同。前者用于程序方式调用云服务API，而后者用于登录控制台。

在阿里云，用户可以使用AccessKey（简称AK）构造一个API请求（或者使用云服务SDK）来操作资源。AccessKey包括AccessKeyId和AccessKeySecret。其中AccessKeyId用于标识用户，AccessKeySecret是用来验证用户身份合法性的密钥。AccessKeySecret必须保密。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/162630/156157335245369_zh-CN.png)

**说明：** API凭证泄露会导致数据泄露，从而给用户带来严重的损失。

## 云安全中心实现AK安全自动化检测闭环 {#section_6ji_cfk_6ps .section}

云安全中心为了应对用户不慎泄漏AccessKey造成恶劣影响，设计了全方位检测理念，从泄漏前配置检查——泄漏行为检测——黑客异常调用三点完成检测闭环，为用户的云上业务安全保驾护航。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/162630/156157335345378_zh-CN.png)

阿里云已率先和最大的开源代码托管服务商Github合作，引入Token scan机制。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/162630/156157335345374_zh-CN.png)

云安全中心AK检测流程完全自动化，可以对在Github上泄漏的AccessKey进行高效和精准地检测。在实际场景中，阿里云已实现含有AccessKey的代码提交到Github后数秒之内，就可以通知用户并且做出响应，尽可能减少对用户产生的负面影响。

-    **泄露前配置检测-云平台配置检查** 

    在云产品的过程中为了防患于未然，您也可以在您可在云安全中心控制台**云平台配置检查**模块检查您当前云产品的配置项是否存在安全风险。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/162630/156157335349836_zh-CN.png)

    -   确保云产品的操作审计日志处于**开启**状态，可以帮助您分析是否有异常的调用行为。
    -   确保使用RAM用户的AK、而不是主账号AK，并且遵守最小权限原则。这样AK发生泄漏问题不至于失去整个云账号的控制权限。
    -   确保开启主账号双因素认证（MFA）。开启多因素认证可明显降低因为密码泄漏导致的未授权访问。
-    **用户泄露行为检测-AK&账密泄露检测** 

    您可在云安全中心控制台**AK&账密泄露检测**模块查看AK泄漏的详情。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/162630/156157335346799_zh-CN.png)

-    **黑客异常调用检测**-**安全告警处理** \> **云产品威胁检测** 

    除了泄漏前的提前预防，在云安全中心控制台**安全告警处理**模块，您可以筛选并查看**云产品威胁检测**告警类型。云安全中心会在出现疑似黑客异常AK调用行为时进行告警，及时提醒用户做出响应，做到泄漏后及时检测。


## 补充安全建议 {#section_f5o_2io_uoi .section}

除了上述云安全中心提供的AK泄露检测和响应措施外，建议您在使用阿里云产品过程中遵循以下几点安全规范，降低凭证泄漏造成的影响：

-    **不要将AccessKey嵌入代码中** 

    嵌入代码中的AK凭证容易被人忽视，经验丰富的开发者会将其写入数据库或者独立的文件中，使得其管理起来更方便。

-    **定期轮换AccessKey ** 

    定期更新代码中存在的AccessKey，可保证一些旧的代码泄漏后不会影响当前线上业务。

-    **定期吊销不需要的AccessKey ** 

    在阿里云AccessKey控制台可查看最后一次AccessKey的访问时间，建议**禁用**所有不用的AccessKey。

-    **遵循最小权限原则，使用RAM账户** 

    根据不同业务需要授予不同子账户的读写权限，为不同业务分配不同子账户的AccessKey。

-    **开启操作日志审计，并将其投递至OSS和SLS长期保存和审计** 

    将操作日志存储至OSS，异常情况时可以起到固证的作用；操作日志投递至SLS，帮助您在日志数量大的时候也能实现高效检索。


