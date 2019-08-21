# CreateOrUpdateAssetGroup {#doc_api_Sas_CreateOrUpdateAssetGroup .reference}

调用该接口修改资产与分组的关系。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Sas&api=CreateOrUpdateAssetGroup&type=RPC&version=2018-12-03)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateOrUpdateAssetGroup|系统规定参数。取值：CreateOrUpdateAssetGroup。

 |
|GroupId|Long|否|111111|指定待修改分组ID。

 |
|GroupName|String|否|test|指定待修改分组名称。

 |
|Uuids|String|否|\[\]|UUIDS列表信息。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|7E0618A9-D5EF-4220-9471-C42B5E92719F|返回结果的请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=CreateOrUpdateAssetGroup
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<CreateOrUpdateAssetGroup>
	  <code>200</code>
	  <requestId>7E0618A9-D5EF-4220-9471-C42B5E92719F</requestId>
	  <success>true</success>
    </CreateOrUpdateAssetGroup>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"requestId":"7E0618A9-D5EF-4220-9471-C42B5E92719F",
	"code":200,
	"success":true
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/Sas)查看更多错误码。

