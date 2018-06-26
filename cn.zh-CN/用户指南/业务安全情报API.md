# 业务安全情报API {#concept_gvv_3qw_f2b .concept}

态势感知通过API接口提供业务安全情报查询功能，您可以调用API查询收录在态势感知安全数据库中的IP或手机号的详细安全情报，用作业务安全分析。

**说明：** 在使用服务前，您需要[购买态势感知（情报资源包）](https://common-buy.aliyun.com/?commodityCode=sas_ip#/buy)。

## GetIpProfile {#section_tgy_4wb_b2b .section}

**接口描述**

调用该接口仅获取指定IP的安全情报。

**请求参数**

|名称|类型|是否必需|描述|示例|
|--|--|----|--|--|
|Ip|string|是|要查询的IP。只支持IPv4格式。|1.1.1.1|
|others|integer|否|补充说明场景行业等信息。|无|

**返回参数**

|名称|类型|描述|示例|
|--|--|--|--|
|Ip|string|被查询的IP。|1.1.1.1|
|Info|String|被查询IP的详细安全信息。**说明：** 字符串符合标准JSON格式，使用时请自行反序列化。

具体结构说明见[表 1](#table_t3j_mwb_b2b)。

|\{‘country’：’中国’\}|

|名称|类型|描述|示例|
|--|--|--|--|
|country|string|被查询IP所在国别。|中国|
|province|string|被查询IP所在省份。|浙江|
|city|string|指定IP所在地级市。|杭州|
|is\_abroad|string|被查询IP是否是国外IP地址， 取值：-   1：是
-   0：否

|1|
|isp|string|被查询IP的互联网服务提供商。|china telecom|
|asn\_id|string|被查询IP的ASN编号。|9416|
|is\_idc|string|被查询IP是否是IDC IP， 取值：-   1：是
-   0：否

|0|
|is\_proxy|string|被查询IP的是否是代理服务器， 取值：-   1：是
-   0：否

|0|
|is\_nat|string|被查询IP的是否是NAT出口， 取值：-   1：是
-   0：否

|0|
|is\_base|string|被查询IP是否是移动基站， 取值：-   1：是
-   0：否

|0|
|is\_tor|string|被查询IP是否是暗网IP， 取值：-   1：是
-   0：否

|0|
|is\_bind\_domain\_1d|string|被查询IP在近1天是否绑定域名， 取值：-   1：是
-   0：否

|0|
|is\_bind\_domain\_7d|string|被查询IP在近7天是否绑定域名， 取值：-   1：是
-   0：否

|0|
|is\_bind\_domain\_30d|string|被查询IP在近30天是否绑定域名， 取值：-   1：是
-   0：否

|1，表示30天内绑定过域名|
|is\_net\_attack\_1d|string|被查询IP在近1天是否发起过网络攻击（DDoS攻击、Web攻击、常见协议的暴力破解攻击等）， 取值：-   1：是
-   0：否

|0|
|is\_net\_attack\_7d|string|被查询IP在近7天是否发起过网络攻击， 取值：-   1：是
-   0：否

|0|
|is\_net\_attack\_30d|string|被查询IP在近30天是否发起过网络攻击， 取值：-   1：是
-   0：否

|1， 表示30天内有网络攻击|
|is\_botnet\_1d|string|被查询IP在近1天之内是否为僵尸网络， 取值：-   1：是
-   0：否

|0|
|is\_botnet\_7d|string|被查询IP在近7天之内是否为僵尸网络， 取值：-   1：是
-   0：否

|0|
|is\_botnet\_30d|string|被查询IP在近30天之内是否为僵尸网络， 取值：-   1：是
-   0：否

|1，30天存在僵尸网络行为|
|is\_c2\_1d|string|被查询IP在近1天之内是否是恶意软件中控， 取值：-   1：是
-   0：否

|0|
|is\_c2\_7d|string|被查询IP在近7天之内是否是恶意软件中控， 取值：-   1：是
-   0：否

|0|
|is\_c2\_30d|string|被查询IP在近30天之内是否是恶意软件中控， 取值：-   1：是
-   0：否

|0|
|is\_black\_campaign\_1d|string|被查询IP在近1天内是否有过疑似黑产行为（包含短信验证码接码攻击、图片验证码打码攻击、恶意注册、恶意撞库等行为）， 取值：-   1：是
-   0：否

|0|
|is\_black\_campaign\_7d|string|被查询IP在近7天内是否有过疑似黑产行为， 取值：-   1：是
-   0：否

|0|
|is\_black\_campaign\_30d|string|被查询IP在近30天内是否有过疑似黑产行为， 取值：-   1：是
-   0：否

|0|
|is\_open\_common\_port\_1d|string|被查询IP在近1天内是否开放常用端口（21、22、80、443等）， 取值：-   1：是
-   0：否

|0|
|is\_open\_common\_port\_7d|string|被查询IP在近7天内是否开放常用端口（21、22、80、443等）， 取值：-   1：是
-   0：否

|0|
|is\_open\_common\_port\_30d|string|被查询IP在近30天内是否开放常用端口（21、22、80、443等）， 取值：-   1：是
-   0：否

|0|
|is\_cheatflow\_1d|string|被查询IP在近1天内是否有垃圾流量， 取值：-   1：是
-   0：否

|0|
|is\_cheatflow\_7d|string|被查询IP在近7天内是否有垃圾流量， 取值：-   1：是
-   0：否

|0|
|is\_cheatflow\_30d|string|被查询IP在近30天内是否有垃圾流量， 取值：-   1：是
-   0：否

|0|
|is\_hijack\_1d|string|被查询IP在最近1天是否有过流量劫持， 取值：-   1：是
-   0：否

|0|
|is\_hijack\_7d|string|被查询IP在最近7天是否有过流量劫持， 取值：-   1：是
-   0：否

|0|
|is\_hijack\_30d|string|被查询IP在最近30天是否有过流量劫持， 取值：-   1：是
-   0：否

|0|
|is\_proxy\_1d|string|被查询IP在最近1天是否是代理服务器， 取值：-   1：是
-   0：否

|0|
|is\_proxy\_7d|string|被查询IP在最近7天是否是代理服务器， 取值：-   1：是
-   0：否

|0|
|is\_proxy\_30d|string|被查询IP在最近30天是否是代理服务器， 取值：-   1：是
-   0：否

|0|

**请求示例**

见[请求示例](#section_oqr_byb_b2b)。

**返回示例**

-   XML格式

    ```
    <GetIpProfile>
        <Data>
    	    <Ip>8.8.8.8</Ip>
    		<Info>{'country':'', 'province':'', city:'', 'is_bind_domain_1d':'1', 'is_bind_domain_7d':'1', 'is_bind_domain_30d':'1'}</Info>
    	</Data>
    	<Message>successful</Message>
    	<RequestId>xxx</RequestId>
    	<Success>true</Success>
    	<Code>200</Code>
    </GetIpProfile>
    ```

-   JSON格式

    ```
    {
        "code": 200, 
        "data": {
            "info": "{'country':'', 'province':'', city:'', 'is_bind_domain_1d':'1', 'is_bind_domain_7d':'1', 'is_bind_domain_30d':'1'}", 
            "ip": "8.8.8.8"
        }, 
        "message": "successful", 
        "requestId": "xxx", 
        "success": true
    }
    ```


## getAccountProfile {#section_up5_lxb_b2b .section}

**接口描述**

调用该接口同时获取指定IP和手机号的安全情报。

**请求参数**

|名称|类型|是否必需|描述|示例|
|--|--|----|--|--|
|Ip|string|是|要查询的IP。只支持IPv4格式。|1.1.1.1|
|Phone|string|是|要查询的手机号。只支持中国手机号。|13111111111|
|AccessTimestamp|string|是|用户操作时间戳，单位秒。|1504772090|
|others|integer|否|补充说明场景或行业等信息。|无|

**返回参数**

|名称|类型|描述|示例|
|--|--|--|--|
|IP|string|被查询的IP。|1.1.1.1|
|Phone|string|被查询的手机号。|13111111111|
|IpInfo|string|被查询IP的详细安全信息。**说明：** 字符串符合标准JSON格式，使用时请自行反序列化。

具体结构见[表 1](#table_t3j_mwb_b2b)。

|\{‘country’：’中国’\}|
|PhoneInfo|String|被查询手机号的详细安全信息。**说明：** 字符串符合标准JSON格式，使用时请自行反序列化。

具体结构见[表 2](#table_lkj_mwb_b2b)。

|\{‘country’：’中国’\}|

|名称|类型|描述|示例|
|--|--|--|--|
|province|string|被查询手机号所在省份。|浙江|
|city|string|被查询手机号所在地级市。|杭州|
|operator|string|被查询手机号的运营商。|联通|
|is\_virtual\_operator|string|被查询手机号是否是虚拟运营商，取值：-   1：是
-   0：否

|0|
|is\_black\_phone|string|被查询手机号是否是黑产手机号，取值：-   1：是
-   0：否

|1|
|is\_grey\_phone|string|被查询手机号是否疑似黑产手机号，取值：-   1：是
-   0：否

|0|
|is\_black\_campaign\_1d|string|被查询手机号在近1天是否存在黑产行为，取值：-   1：是
-   0：否

|0|
|is\_black\_campaign\_7d|string|被查询手机号在近7天是否存在黑产行为，取值：-   1：是
-   0：否

|0|
|is\_black\_campaign\_30d|string|被查询手机号在近30天是否存在黑产行为，取值：-   1：是
-   0：否

|1|

**请求示例**

见[请求示例](#section_oqr_byb_b2b)。

**返回示例**

-   XML格式

    ```
    <GetAccountProfile>
        <Data>
    	    <Ip>1.1.1.1</Ip>
    		<Phone>13111111111</Phone>
    		<IpInfo>{'country':'中国'}</IpInfo>
    		<PhoneInfo>{'country':'中国'}</PhoneInfo>
    	</Data>
    	<Message>successful</Message>
    	<RequestId>xxx</RequestId>
    	<Success>true</Success>
    	<Code>200</Code>
    </GetAccountProfile>
    ```

-   JSON格式

    ```
    {
        "code": 200, 
        "data": {
            "ipInfo": "{'country':'中国'}", 
            "ip": "1.1.1.1",
    		"phone":"13111111111",
    		"phoneInfo":"{'country':'中国'}"
        }, 
        "message": "successful", 
        "requestId": "xxx", 
        "success": true
    }
    ```


## 错误码 {#section_irv_yxb_b2b .section}

|错误码|错误信息|描述|操作建议|
|---|----|--|----|
|101|Invalid parameters|参数有误。|请检查参数类型是否有误，要查询的IP是否真实有效。|
|102|The specified IP does not exist|被查询IP在情报库中不存在。|请查询其他IP。|
|103|The API requests have exceeded the limit|查询API调用次数超过已购买的可调用次数。|请[购买态势感知（情报资源包）](https://common-buy.aliyun.com/?commodityCode=sas_ip#/buy)。|
|104|The specified Phone does not exist|被查询手机号在情报库中不存在。|-|
|403|The user is not authorized|无权访问该接口。|请[购买态势感知（情报资源包）](https://common-buy.aliyun.com/?commodityCode=sas_ip#/buy)。|
|500|An internal error occurred|系统内部错误。|请重试。若重试仍未成功，请提交工单联系我们。|

## 请求示例 {#section_oqr_byb_b2b .section}

以下示例中会用到阿里云账号下创建的AccessKey密钥，您可以登录[AccessKey管理控制台](https://ak-console.aliyun.com/#/accesskey)，复制您的AccessKey信息（AccessKeyId和AccessKeySecret），并替换到以下示例代码中。

**说明：** AccessKeyID和AccessKeySecret是您访问阿里云API的密钥，具有您的阿里云账户完全的权限，请您妥善保管。

更多语言的SDK信息，请参考[阿里云开发者工具包（SDK）](https://develop.aliyun.com/tools/sdk?java#/java)。

**（推荐）Java示例**

```
public class Test {

    private static final String accessId       = "xxx"; // 请替换成阿里云账号accessId
    private static final String accessIdSecret = "xxx"; // 请替换成阿里云账号accessIdSecret

    private static IAcsClient   client;

    private static void initClient() throws Exception {
        // client只需要在启动时new一次，加快查询速度
        IClientProfile profile = DefaultProfile.getProfile("cn-hangzhou", accessId, accessIdSecret);
        DefaultProfile.addEndpoint("cn-hangzhou", "cn-hangzhou", "Sas-api", "sas-api.aliyuncs.com"); // 添加自定义endpoint。
        client = new DefaultAcsClient(profile);
    }

    public static void main(String[] args) throws Exception {
        initClient(); // 如果使用spring，请将此方法放至init方法中，只初始化一次client

        // 查询ip画像
        getIpProfile();
		
		//查询业务安全情报
		getAccountProfile();

    }

    private static void getIpProfile() throws Exception {
        GetIpProfileRequest request = new GetIpProfileRequest();
        request.setIp("8.8.8.8");
        // set其他参数

        // 调用方式一：
        GetIpProfileResponse response = (GetIpProfileResponse) client.getAcsResponse(request);
        System.out.println(response.getSuccess());
        if (response.getSuccess()) {
            if (response.getData() != null) {
                System.out.println(response.getData().getInfo());
            }
        }
        
        // 调用方式二：
        request.setAcceptFormat(FormatType.JSON);
        HttpResponse httpResponse = client.doAction(request);
        System.out.println(new String(httpResponse.getContent(), "UTF-8"));
    }
	
	private static void getAccountProfile() throws Exception {
        GetAccountProfileRequest request = new GetAccountProfileRequest();
        request.setIp("1.1.1.1");
        request.setPhone("13111111111");
        request.setAccessTimestamp(123L);
        // set其他参数

        // 调用方式一：
        GetAccountProfileResponse response = (GetAccountProfileResponse) client.getAcsResponse(request);
        System.out.println(response.getSuccess());
        if (response.getSuccess()) {
            if (response.getData() != null) {
                System.out.println(response.getData().getIpInfo());
                System.out.println(response.getData().getPhoneInfo());
            }
        }

        // 调用方式二：
        request.setAcceptFormat(FormatType.JSON);
        HttpResponse httpResponse = client.doAction(request);
        System.out.println(new String(httpResponse.getContent(), "UTF-8"));
    }
}
```

**php示例**

```
markup
<?php
require_once '/xxx/aliyun-openapi-php-sdk/aliyun-php-sdk-core/Config.php';   # 您的aliyun-php-sdk-core的路径
use Sas_api\Request\V20170705\GetAccountProfileRequest;
# 创建 DefaultAcsClient 实例并初始化
$clientProfile = DefaultProfile::getProfile(
    "cn-hangzhou",       # 您的 Region ID 
    "xxx",               # 您的 Access Key ID
    "xxx"                # 您的 Access Key Secret
);
DefaultProfile::addEndpoint("cn-hangzhou", "cn-hangzhou", "Sas-api", "sas-api.aliyuncs.com");
$client = new DefaultAcsClient($clientProfile);
# 创建 API 请求并设置参数
$request = new GetAccountProfileRequest();
$request->setPhone(13111111111);
$request->setIp(1.1.1.1);
$request->setAccessTimestamp(1504772090);
# 发起请求并处理返回
try {
    $response = $client->getAcsResponse($request);
    print_r($response);
} catch(ServerException $e) {
    print "Error: " . $e->getErrorCode() . " Message: " . $e->getMessage() . "\n";
} catch(ClientException $e) {
    print "Error: " . $e->getErrorCode() . " Message: " . $e->getMessage() . "\n";
}
?>
```

**python示例**

```
markup
# -*- coding: utf8 -*-
from aliyunsdkcore.client import AcsClient
from aliyunsdkcore.acs_exception.exceptions import ClientException
from aliyunsdkcore.acs_exception.exceptions import ServerException
from aliyunsdksas_api.request.v20170705 import GetAccountProfileRequest
from aliyunsdkcore.profile import region_provider
region_provider.add_endpoint('Sas-api', 'cn-hangzhou', 'sas-api.aliyuncs.com');
# 创建 AcsClient 实例
client = AcsClient(
    "xxx",      #  您的 Access Key ID      
    "xxx",      # 您的 Access Key Secret
    "cn-hangzhou"
);
# 创建 request，并设置参数
request = GetAccountProfileRequest.GetAccountProfileRequest()
request.set_Phone('13111111111')
request.set_Ip('1.1.1.1')
request.set_AccessTimestamp(1504772090)
# 发起 API 请求并打印返回
response = client.do_action_with_exception(request)
print response
```

**http请求示例**

**请求方法**

支持以HTTP GET或POST方法发送请求。

**请求参数**

每个请求都需要包含公共的鉴权、签名相关请求参数和相关操作所特有的请求参数。

```
https://sas-api.aliyuncs.com/?Action=GetIpProfile
&RegionId=cn-hangzhou
&ip=1.1.1.1
&sensType=1
&businessType=1
&requestUrl=xx
&userAgent=xx
&deviceIdMd5=xx
&os=Mac
&deviceType=1
&connectionType=1
&carrier=1
&公共请求参数
```

|名称|类型|是否必需|描述|
|--|--|----|--|
|Format|String|否|返回值的类型，支持JSON和XML，默认为XML。|
|Version|String|是|API版本号，日期形式：YYYY-MM-DD，本版本对应为2017-07-05。|
|AccessKeyId|String|是|阿里云颁发给用户的访问服务所用的密钥ID。|
|Signature|String|是|签名结果串，关于签名的计算方法，参见[签名机制](../../../../cn.zh-CN/API 参考/调用方式/签名机制.md#)。|
|SignatureMethod|String|是|签名方式，取值范围：HMAC-SHA1。|
|Timestamp|String|是|请求的时间戳。日期格式按照ISO8601标准表示，并需要使用UTC时间。格式为：YYYY-MM-DDThh：mm：ssZ。例如，2017-03-23T06：59：55Z（表示北京时间2017年3月23日14点59分55秒）。

|
|SignatureVersion|String|是|签名算法版本，目前版本是1.0。|
|SignatureNonce|String|是|唯一随机数，用于防止网络重放攻击。用户在不同请求间要使用不同的随机数值。|

