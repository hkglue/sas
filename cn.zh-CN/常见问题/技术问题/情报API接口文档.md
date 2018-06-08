# 情报API接口文档 {#concept_xgr_lwb_b2b .concept}

## 描述 {#section_j3j_mwb_b2b .section}

查询IP画像，手机号画像接口。

2018-05-31，新增灰产手机号新标签。

2017-09-21，新增最近1天是否劫持流量等6个IP画像新标签。

2017-07-13，新增6个IP画像新标签。

2017-07-12，新增手机号画像。

2017-07-08，修改IP画像请求参数。

2017-06-24，新增IP画像。

## 获取IP情报 {#section_tgy_4wb_b2b .section}

GetIpProfile

**请求参数**

|名称|类型|说明|示例|是否必须|
|--|--|--|--|----|
|Ip|string|客户提交待查询的IP，只支持IPv4|1.1.1.1|是|
|其余字段非必填|integer|场景行业等|无|否|

**返回参数**

|名称|类型|说明|举例|
|--|--|--|--|
|Ip|string|查询的IP|1.1.1.1|
|Info|String|ip信息，字符串符合标准json格式，使用时请自行反序列化|\{‘country’：’中国’\}|

**Info字段的明细说明**

|返回值字段名称|类型|说明|举例|
|-------|--|--|--|
|country|string|国别|中国|
|province|string|省份|浙江|
|city|string|地市|杭州|
|is\_abroad|string|是否国外IP地址， 1：是/0：否|1|
|isp|string|互联网服务提供商|china telecom|
|asn\_id|string|ASN编号|9416|
|is\_idc|string|是否IDC IP， 1：是/0：否|0|
|is\_proxy|string|是否代理服务器， 1：是/0：否|0|
|is\_nat|string|是否NAT出口， 1：是/0：否|0|
|is\_base|string|是否移动基站， 1：是/0：否|0|
|is\_tor|string|是否暗网IP， 1：是/0：否|0|
|is\_bind\_domain\_1d|string|近1天是否绑定域名，1：是/0：否|0|
|is\_bind\_domain\_7d|string|近7天是否绑定域名， 1：是/0：否|0|
|is\_bind\_domain\_30d|string|近30天是否绑定域名， 1：是/0：否|1，表示30天内绑定过域名|
|is\_net\_attack\_1d|string|近1天，是否发起过网络攻击，包含DDoS攻击、Web攻击、常见协议的暴力破解攻击等， 1：是/0：否|0|
|is\_net\_attack\_7d|string|近7天是否发起过网络攻击，1：是/0：否|0|
|is\_net\_attack\_30d|string|近30天是否发起过网络攻击， 1：是/0：否|1， 表示30天内有网络攻击|
|is\_botnet\_1d|string|近1天之内是否为僵尸网络， 1：是/0：否|0|
|is\_botnet\_7d|string|近7天之内是否为僵尸网络， 1：是/0：否|0|
|is\_botnet\_30d|string|近30天之内是否为僵尸网络， 1：是/0：否|1，30天存在僵尸网络行为|
|is\_c2\_1d|string|近1天之内是否是恶意软件中控， 1：是/0：否|0|
|is\_c2\_7d|string|近7天之内是否是恶意软件中控， 1：是/0：否|0|
|is\_c2\_30d|string|近30天之内是否是恶意软件中控， 1：是/0：否|0|
|is\_black\_campaign\_1d|string|近1天内是否有过疑似黑产行为，包含短信验证码接码攻击、图片验证码打码攻击、恶意注册、恶意撞库等行为。1：是/0：否|0|
|is\_black\_campaign\_7d|string|近7天内是否有过疑似黑产行为， 1：是/0：否|0|
|is\_black\_campaign\_30d|string|近30天内是否有过疑似黑产行为， 1：是/0：否|0|
|is\_open\_common\_port\_1d|string|近1天内是否开放常用端口：21、22、80、443等， 1：是/0：否|0|
|is\_open\_common\_port\_7d|string|近7天内是否开放常用端口：21、22、80、443等， 1：是/0：否|0|
|is\_open\_common\_port\_30d|string|近30天内是否开放常用端口：21、22、80、443等， 1：是/0：否|0|
|is\_cheatflow\_1d|string|近1天内是否有垃圾流量， 1：是/0：否|0|
|is\_cheatflow\_7d|string|近7天内是否有垃圾流量， 1：是/0：否|0|
|is\_cheatflow\_30d|string|近30天内是否有垃圾流量， 1：是/0：否|0|
|is\_hijack\_1d|string|最近1天是否有过流量劫持， 1：是/0：否|0|
|is\_hijack\_7d|string|最近7天是否有过流量劫持， 1：是/0：否|0|
|is\_hijack\_30d|string|最近30天是否有过流量劫持， 1：是/0：否|0|
|is\_proxy\_1d|string|最近1天是否代理服务器， 1：是/0：否|0|
|is\_proxy\_7d|string|最近7天是否代理服务器， 1：是/0：否|0|
|is\_proxy\_30d|string|最近30天是否代理服务器， 1：是/0：否|0|

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


## 获取业务安全情报 {#section_up5_lxb_b2b .section}

getAccountProfile

**请求参数**

|名称|类型|说明|示例|是否必须|
|--|--|--|--|----|
|Ip|string|待查询的IP，只支持IPv4|1.1.1.1|是|
|Phone|string|待查询的手机号，只支持国内手机号|13111111111|是|
|AccessTimestamp|string|用户操作时间戳，单位秒|1504772090|是|
|其余字段非必填|integer|场景/行业等|无|否|

**返回参数**

|名称|类型|说明|示例|
|--|--|--|--|
|IP|string|查询的IP|1.1.1.1|
|Phone|string|查询的手机号|13111111111|
|IpInfo|string|ip信息，字符串符合标准json格式，使用时请自行反序列化|\{‘country’：’中国’\}|
|PhoneInfo|String|手机号信息，字符串符合标准json格式，使用时请自行反序列化|\{‘country’：’中国’\}|

**IpInfo字段说明参见 IP情报接口返回字段说明。**

**PhoneInfo字段说明**

|名称|类型|说明|举例|
|--|--|--|--|
|province|string|省份|浙江|
|city|string|地市|杭州|
|operator|string|运营商|联通|
|is\_virtual\_operator|string|是否虚拟运营商 1：是/0：否|0|
|is\_black\_phone|string|是否黑产手机号 1：是/0：否|1|
|is\_grey\_phone|string|疑似黑产手机号 1：是/0：否|0|
|is\_black\_campaign\_1d|string|近1天是否存在黑产行为 1：是/0：否|0|
|is\_black\_campaign\_7d|string|近7天是否存在黑产行为 1：是/0：否|0|
|is\_black\_campaign\_30d|string|近30天是否存在黑产行为 1：是/0：否|1|

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


## 错误码说明 {#section_irv_yxb_b2b .section}

|code|message|说明|排错方法|
|----|-------|--|----|
|101|Invalid parameters|参数有误|请检查参数类型是否有误，ip是否真实有效|
|102|The specified IP does not exist|IP在情报库中不存在|-|
|103|The API requests have exceeded the limit|查询API调用次数超过已购买的可调用次数|请购买态势感知情报资源包|
|104|The specified Phone does not exist|手机号在情报库中不存在|-|
|403|The user is not authorized|无权访问该接口|请购买态势感知情报资源包|
|500|An internal error occurred|系统内部错误|请重试，若重试仍未成功请提工单联系我们|

## 请求示例 {#section_oqr_byb_b2b .section}

**（推荐）. JAVA API**

用阿里云账号登录，[前往RAM控制台](https://ak-console.aliyun.com/?spm=5176.8407944.1001.d605.XXK4OU#/accesskey)，复制您的Access Key信息（在下面的代码中会使用到）。

各语言sdk参考 [阿里云sdk官网](https://develop.aliyun.com/tools/sdk?java#/java)。

调用JAVA代码实例

```
public class Test {

    private static final String accessId       = "xxx";              // 请替换成阿里云账号accessId
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

php方式

```
markup
<?php
require_once '/xxx/aliyun-openapi-php-sdk/aliyun-php-sdk-core/Config.php';   # 您的aliyun-php-sdk-core的路径
use Sas_api\Request\V20170705\GetAccountProfileRequest;
# 创建 DefaultAcsClient 实例并初始化
$clientProfile = DefaultProfile::getProfile(
    "cn-hangzhou",                   # 您的 Region ID 
    "xxx",               # 您的 Access Key ID
    "xxx"            # 您的 Access Key Secret
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

python方式

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

**http方式**

**请求方法**

支持HTTP GET或POST方法发送请求。

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
&<公共请求参数>
```

**公共参数**

|名称|类型|是否必须|描述|
|--|--|----|--|
|Format|String|否|返回值的类型，支持JSON和XML，默认为XML|
|Version|String|是|API版本号，为日期形式：YYYY-MM-DD，本版本对应为2017-07-05|
|AccessKeyId|String|是|阿里云颁发给用户的访问服务所用的密钥ID|
|Signature|String|是|签名结果串，关于签名的计算方法，请参见<签名机制\>|
|SignatureMethod|String|是|签名方式，目前支持HMAC-SHA1|
|Timestamp|String|是|请求的时间戳。日期格式按照ISO8601标准表示，并需要使用UTC时间。格式为：YYYY-MM-DDThh：mm：ssZ例如，2017-03-23T06：59：55Z（为北京时间2017年3月23日14点59分55秒）|
|SignatureVersion|String|是|签名算法版本，目前版本是1.0|
|SignatureNonce|String|是|唯一随机数，用于防止网络重放攻击。用户在不同请求间要使用不同的随机数值|

签名机制

[参考文档](https://help.aliyun.com/document_detail/25492.html?spm=5176.doc25490.2.1.0Me7ot)

