# DescribePropertyCount {#doc_api_Sas_DescribePropertyCount .reference}

调用该接口获取资产指纹，即进程、端口、软件、账户4种类型的统计数量。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Sas&api=DescribePropertyCount&type=RPC&version=2018-12-03)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribePropertyCount|系统规定参数。取值：DescribePropertyCount。

 |
|Type|String|否|port|指定待查询的指纹类型。可选：

 -   **user**：账户
-   **software**：软件
-   **process**：进程
-   **port**：端口

 **说明：** 类型不填表示获取所有类型信息。

 |
|UuidList|String|否|\[\]|指定待查询的资产UUID。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Port|Integer|163|返回的端口数量信息。

 |
|Process|Integer|367|返回的进程数量信息。

 |
|RequestId|String|7E0618A9-D5EF-4220-9471-C42B5E92719F|返回结果的请求ID。

 |
|Software|Integer|5073|返回的软件数量信息。

 |
|User|Integer|114|返回的账户数量信息。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribePropertyCount
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribePropertyCount>
	  <data>
		    <Process>367</Process>
		    <Software>5037</Software>
		    <Port>163</Port>
		    <User>114</User>
	  </data>
    </DescribePropertyCount>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"data":{
		"User":114,
		"Software":5037,
		"Port":163,
		"Process":367
	}
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/Sas)查看更多错误码。

