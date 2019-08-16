# AttachStream {#doc_api_cityvisual_AttachStream .reference}

调用AttachStream给指定的计算工作组绑定Stream。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cityvisual&api=AttachStream&type=RPC&version=2018-10-30)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|AttachStream|系统规定参数。取值：**AttachStream**。

 |
|JobGroupId|String|是|4|计算工作组的ID。

 |
|InstanceId|String|否|cityvisual-xxxxx|实例ID。

 |
|RegionId|String|否|cn-shanghai|地域ID。

 |
|Streams.N.StreamName|String|否|ipc\_001|视频流名称。

 |
|Streams.N.StreamURL|String|否|mq://ipc\_001|视频流地址。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|E175B041-75A2-4335-B3AC-0FD008F93627|请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=AttachStream
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<AttachStreamResponse>
      <RequestId>E175B041-75A2-4335-B3AC-0FD008F93627</RequestId>
</AttachStreamResponse>
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
|404|InvalidJobGroupId.NotFound|The specified job group does not exist.|指定的JobGroup不存在。|
|400|InvalidName.Malformed|The specified Name is incorrectly formatted.|指定的Name格式不合法。|
|400|InvalidStreamURL.Malformed|The specified StreamURL is incorrectly formatted.|指定的StreamURL格式不合法。|
|400|InvalidName.Duplicate|The specified name already exists.|指定的名称已存在。|

访问[错误中心](https://error-center.aliyun.com/status/product/cityvisual)查看更多错误码。

