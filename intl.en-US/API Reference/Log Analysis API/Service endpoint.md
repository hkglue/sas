# Service endpoint {#reference_wgx_pwq_zdb .reference}

## Service endpoints for the public network {#section_rxx_n4w_12b .section}

The Log Service endpoint is a URL used to access a project and logs in the project. It is associated with the Alibaba Cloud region where the project resides and the project name. Currently, Log Service has been activated in multiple Alibaba Cloud regions. The following table lists the public network service endpoints for each region.

|Region|Root service endpoint|
|:-----|:--------------------|
|China \(Hangzhou\)|cn-hangzhou.log.aliyuncs.com|
|China \(Shanghai\)|cn-shanghai.log.aliyuncs.com|
|China \(Qingdao\)|cn-qingdao.log.aliyuncs.com|
|China \(Beijing\)|cn-beijing.log.aliyuncs.com|
|China \(Zhangjiakou\)|cn-zhangjiakou.log.aliyuncs.com|
|China \(Hohhot\)|cn-huhehaote.log.aliyuncs.com|
|China \(Shenzhen\)|cn-shenzhen.log.aliyuncs.com|
|China \(Chengdu\)|cn-chengdu.log.aliyuncs.com|
|Hong Kong|cn-hongkong.log.aliyuncs.com|
|Japan \(Tokyo\)|ap-northeast-1.log.aliyuncs.com|
|Singapore|ap-southeast-1.log.aliyuncs.com|
|Australia \(Sydney\)|ap-southeast-2.log.aliyuncs.com|
|Malaysia \(Kuala Lumpur\)|ap-southeast-3.log.aliyuncs.com|
|Indonesia \(Jakarta\)|ap-southeast-5.log.aliyuncs.com|
|UAE \(Dubai\)|me-east-1.log.aliyuncs.com|
|US \(Silicon Valley\)|us-west-1.log.aliyuncs.com|
|Germany \(Frankfurt\)|eu-central-1.log.aliyuncs.com|
|US \(Virginia\)|us-east-1.log.aliyuncs.com|
|India \(Mumbai\)|ap-south-1.log.aliyuncs.com|
|UK \(London\)|eu-west-1.log.aliyuncs.com|

When accessing a specific project, you need to construct the final service endpoint based on the project name and region. The format is as follows:

```
<project_name>.<region_endpoint>
```

For example, if the project name is big-game and the region is China \(Hangzhou\), the service endpoint is as follows:

```
big-game.cn-hangzhou.log.aliyuncs.com
```

**Note:** 

You must specify a region when creating a Log Service project. After the project is created, you cannot change the region or migrate the project across regions. You must select a root service endpoint that matches the region to compose the service endpoint for this project. The service endpoint is used for API operation requests.

## Service endpoints for the classic network or VPC {#section_p5r_r4w_12b .section}

You can also use private network service endpoints to call Log Service API operations on an Alibaba Cloud Elastic Compute Service \(ECS\) instance, including the Virtual Private Cloud \(VPC\) environment. Access to Log Service through private network service endpoints does not consume the Internet traffic of ECS instances, and therefore saves the Internet bandwidth of ECS instances. The following table lists the private network service endpoints for each region.

|Region|Root service endpoint|
|:-----|:--------------------|
|China \(Hangzhou\)|cn-hangzhou-intranet.log.aliyuncs.com|
|China \(Shanghai\)|cn-shanghai-intranet.log.aliyuncs.com|
|China \(Qingdao\)|cn-qingdao-intranet.log.aliyuncs.com|
|China \(Beijing\)|cn-beijing-intranet.log.aliyuncs.com|
|China \(Shenzhen\)|cn-shenzhen-intranet.log.aliyuncs.com|
|China \(Zhangjiakou\)|cn-zhangjiakou-intranet.log.aliyuncs.com|
|China \(Hohhot\)|cn-huhehaote-intranet.log.aliyuncs.com|
|China \(Chengdu\)|cn-chengdu-intranet.log.aliyuncs.com|
|Hong Kong|cn-hongkong-intranet.log.aliyuncs.com|
|US \(Silicon Valley\)|us-west-1-intranet.log.aliyuncs.com|
|Japan \(Tokyo\)|ap-northeast-1-intranet.log.aliyuncs.com|
|Singapore|ap-southeast-1-intranet.log.aliyuncs.com|
|Australia \(Sydney\)|ap-southeast-2-intranet.log.aliyuncs.com|
|Malaysia \(Kuala Lumpur\)|ap-southeast-3-intranet.log.aliyuncs.com|
|Indonesia \(Jakarta\)|ap-southeast-5-intranet.log.aliyuncs.com|
|UAE \(Dubai\)|me-east-1-intranet.log.aliyuncs.com|
|Germany \(Frankfurt\)|eu-central-1-intranet.log.aliyuncs.com|
|US \(Virginia\)|us-east-1-intranet.log.aliyuncs.com|
|India \(Mumbai\)|ap-south-1-intranet.log.aliyuncs.com|
|UK \(London\)|eu-west-1-intranet.log.aliyuncs.com|

For example, if the project name is big-game and the region is China \(Hangzhou\), the private network service endpoint is as follows:

```
big-game.cn-hangzhou-intranet.log.aliyuncs.com
```

**Note:** Currently, Log Service supports only HTTP and HTTPS for API operations through the preceding service endpoints.

## Service endpoint for Internet-based Global Acceleration {#section_kp3_42h_cgb .section}

In addition to VPC and the public network, Log Service adds a network type of **[Internet-based Global Acceleration](../../../../intl.en-US/Data Collection/Collection acceleration/Overview.md)**. Compared with the ordinary Internet access, Internet-based Global Acceleration has significant advantages in terms of latency and stability. It is suitable for scenarios with high requirements for data collection, low consumption latency, and reliability.

The service endpoint for Internet-based Global Acceleration is the same in all regions as follows: `log-global.aliyuncs.com`.

**Note:** The Global Acceleration feature is disabled by default. You must manually enable it. For more information about how to enable Global Acceleration, see [Enable Global Acceleration](../../../../intl.en-US/Data Collection/Collection acceleration/Enable Global Acceleration.md).

