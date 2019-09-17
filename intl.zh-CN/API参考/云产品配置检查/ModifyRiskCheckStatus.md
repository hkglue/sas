# ModifyRiskCheckStatus {#doc_api_Sas_ModifyRiskCheckStatus .reference}

修改检查项的检测结果状态。

调用ModifyRiskCheckStatus可修改检查项检测结果状态，进行忽略或标记误报。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Sas&api=ModifyRiskCheckStatus&type=RPC&version=2018-12-03)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ModifyRiskCheckStatus|系统规定参数。取值：ModifyRiskCheckStatus。

 |
|ItemId|Long|否|1|检查项id

 |
|Lang|String|否|cn|语种

 |
|SourceIp|String|否|1.1.1.1|请求源ip

 |
|Status|String|否|ignored|新状态

 |
|TaskId|Long|否|57|任务id

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|48D2E9A9-A1B0-4295-B727-0995757C47E9|请求id

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=ModifyRiskCheckStatus
&ItemId=1
&TaskId=57
&Status=ignored
&<公共请求参数>

```

正常返回示例

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"48D2E9A9-A1B0-4295-B727-0995757C47E9"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/Sas)查看更多错误码。

