# 如何使用Access Key接入API威胁情报？ {#concept_vmr_2bc_b2b .concept}

用阿里云账号登录后，[前往RAM控制台](https://ak-console.aliyun.com/?spm=5176.8407944.1001.d605.XXK4OU#/accesskey)，复制您的Access Key信息（在下面的代码中会使用到）。

在阿里云[sdk官网](https://develop.aliyun.com/tools/sdk?java#/java)，下载对应语言的sdk ，其中java提供Maven 方式自动下载和/手动下载两种方式，在代码中粘贴之前复制的Access Key信息。

-   调用JAVA代码示例

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
            
            //查询手机号画像
            getPhoneProfile();
    		
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
    
        private static void getPhoneProfile() throws Exception {
            GetPhoneProfileRequest request = new GetPhoneProfileRequest();
            request.setPhone("13111111111");
            // set其他参数
    
            // 调用方式一：
            GetPhoneProfileResponse response = (GetPhoneProfileResponse) client.getAcsResponse(request);
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

-   PHP方式代码示例

    ```
    <?php
    require_once '/xxx/aliyun-openapi-php-sdk/aliyun-php-sdk-core/Config.php';   # 您的aliyun-php-sdk-core的路径
    use Sas_api\Request\V20170705\GetPhoneProfileRequest;
    # 创建 DefaultAcsClient 实例并初始化
    $clientProfile = DefaultProfile::getProfile(
        "cn-hangzhou",                   # 您的 Region ID 
        "xxx",               # 您的 Access Key ID
        "xxx"            # 您的 Access Key Secret
    );
    DefaultProfile::addEndpoint("cn-hangzhou", "cn-hangzhou", "Sas-api", "sas-api.aliyuncs.com");
    $client = new DefaultAcsClient($clientProfile);
    # 创建 API 请求并设置参数
    $request = new GetPhoneProfileRequest();
    $request->setPhone(13111111111);
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

-   Python方式示例

    ```
    ```
    # -*- coding: utf8 -*-
    from aliyunsdkcore.client import AcsClient
    from aliyunsdkcore.acs_exception.exceptions import ClientException
    from aliyunsdkcore.acs_exception.exceptions import ServerException
    from aliyunsdksas_api.request.v20170705 import GetPhoneProfileRequest
    from aliyunsdkcore.profile import region_provider
    region_provider.add_endpoint('Sas-api', 'cn-hangzhou', 'sas-api.aliyuncs.com');
    # 创建 AcsClient 实例
    client = AcsClient(
        "xxx",      #  您的 Access Key ID      
        "xxx",      # 您的 Access Key Secret
        "cn-hangzhou"
    );
    # 创建 request，并设置参数
    request = GetPhoneProfileRequest.GetPhoneProfileRequest()
    request.set_Phone('13111111111')
    # 发起 API 请求并打印返回
    response = client.do_action_with_exception(request)
    print response
    ```

-   http方式
    -   请求方法：支持HTTP GET或POST方法发送请求。
    -   请求参数：每个请求都需要包含公共的鉴权、签名相关请求参数和相关操作所特有的请求参数。

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

-   公共参数

    |名称|类型|是否必须|描述|
    |--|--|----|--|
    |Format|String|否|返回值的类型，支持JSON和XML，默认为XML|
    |Version|String|是|API版本号，为日期形式：YYYY-MM-DD，本版本对应为2017-07-05|
    |AccessKeyId|String|是|阿里云颁发给用户的访问服务所用的密钥ID|
    |Signature|String|是|签名结果串，关于签名的计算方法，请参见<[签名机制](http://https//help.aliyun.com/document_detail/25492.html?spm=5176.doc25490.2.1.0Me7ot)\>|
    |SignatureMethod|String|是|签名方式，目前支持HMAC-SHA1|
    |Timestamp|String|是|请求的时间戳。日期格式按照ISO8601标准表示，并需要使用UTC时间。格式为：YYYY-MM-DDThh:mm:ssZ例如，2017-03-23T06:59:55Z（为北京时间2017年3月23日14点59分55秒）|
    |SignatureVersion|String|是|签名算法版本，目前版本是1.0|
    |SignatureNonce|String|是|唯一随机数，用于防止网络重放攻击。用户在不同请求间要使用不同的随机数值|

    -   更多API接口返回详细见[API文档](cn.zh-CN/常见问题/技术问题/情报API接口文档.md#)。

