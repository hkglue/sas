# ModifyTagWithUuid {#doc_api_Sas_ModifyTagWithUuid .reference}

调用该接口修改标签与服务器或云产品的关系。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Sas&api=ModifyTagWithUuid&type=RPC&version=2018-12-03)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ModifyTagWithUuid|系统规定参数。取值：ModifyTagWithUuid。

 |
|MachineTypes|String|否|ecs|指定待修改的资产类型。

 |
|TagId|String|否|7E0618A9-D5EF-4220-9471-C42B5E92719F|指定待修改标签ID。

 |
|TagList|String|否|ac,ad|指定待修改标签列表。

 |
|UuidList|String|否|111-xx,aa-bb|指定待修改机器列表。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|"requestId": "7E0618A9-D5EF-4220-9471-C42B5E92719F",|返回结果的请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=ModifyTagWithUuid
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<ModifyTagWithUuid>
	  <code>200</code>
	  <requestId>7E0618A9-D5EF-4220-9471-C42B5E92719F</requestId>
	  <success>true</success>
    </ModifyTagWithUuid>
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

