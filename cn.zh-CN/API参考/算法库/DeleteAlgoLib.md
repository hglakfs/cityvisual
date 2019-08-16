# DeleteAlgoLib {#doc_api_cityvisual_DeleteAlgoLib .reference}

调用DeleteAlgoLib删除指定的算法库。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cityvisual&api=DeleteAlgoLib&type=RPC&version=2018-10-30)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteAlgoLib|系统规定参数。取值：**DeleteAlgoLib**。

 |
|AlgoLibId|String|是|842|算法库ID。

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

http(s)://[Endpoint]/?Action=DeleteAlgoLib
&AlgoLibId=842
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DeleteAlgoLibResponse>
      <RequestId>E175B041-75A2-4335-B3AC-0FD008F93627</RequestId>
</DeleteAlgoLibResponse>
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
|400|InvalidParameter|The specified AlgoLibId is invalid.|指定的算法库 ID 不合法。|
|404|InvalidAlgoLibId.NotFound|The specified AlgoLibId does not exist.|指定的算法库不存在。|
|403|DependencyViolation|The specified algorithm library is still in use.|指定的算法库仍在使用中。|

访问[错误中心](https://error-center.aliyun.com/status/product/cityvisual)查看更多错误码。

