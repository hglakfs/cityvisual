# DeleteResourceProfile {#doc_api_cityvisual_DeleteResourceProfile .reference}

调用DeleteResourceProfile删除指定的计算资源配置。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cityvisual&api=DeleteResourceProfile&type=RPC&version=2018-10-30)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteResourceProfile|系统规定参数。取值：**DeleteResourceProfile**。

 |
|ResourceProfileId|String|是|4|资源参数集ID。

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

http(s)://[Endpoint]/?Action=DeleteResourceProfile
&ResourceProfileId=4
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DeleteResourceProfileResponse>
      <RequestId>E175B041-75A2-4335-B3AC-0FD008F93627</RequestId>
</DeleteResourceProfileResponse>
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
|400|InvalidName.Malformed|The specified Name is incorrectly formatted.|指定的Name格式不合法。|
|400|InvalidParameter|The specified resource profile ID is invalid.|指定的资源参数集 ID 不合法。|

访问[错误中心](https://error-center.aliyun.com/status/product/cityvisual)查看更多错误码。

