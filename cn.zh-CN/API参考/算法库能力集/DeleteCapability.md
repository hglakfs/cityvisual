# DeleteCapability {#doc_api_cityvisual_DeleteCapability .reference}

调用DeleteCapability删除指定的算法库能力集。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cityvisual&api=DeleteCapability&type=RPC&version=2018-10-30)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteCapability|系统规定参数。取值：**DeleteCapability**。

 |
|CapabilityId|String|是|262|算法库能力集ID。

 |
|RegionId|String|否|cn-shanghai|地域ID。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|E175B041-75A2-4335-B3AC-0FD008F93627|请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DeleteCapability
&CapabilityId=262
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DeleteCapabilityResponse>
      <RequestId>E175B041-75A2-4335-B3AC-0FD008F93627</RequestId>
</DeleteCapabilityResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"E175B041-75A2-4335-B3AC-0FD008F93627"
}
```

## 错误码 { .section}

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|404|InvalidCapabilityId.NotFound|The specified CapabilityId does not exist.|指定的标签不存在。|
|400|InvalidParameter|The specified CapabilityId is invalid.|指定的算法库能力集标签ID不合法。|

访问[错误中心](https://error-center.aliyun.com/status/product/cityvisual)查看更多错误码。

