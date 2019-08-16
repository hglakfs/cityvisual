# GetStreamsForCameras {#doc_api_cityvisual_GetStreamsForCameras .reference}

调用GetStreamsForCameras根据视频点位获取相应的视频流信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cityvisual&api=GetStreamsForCameras&type=RPC&version=2018-10-30)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|GetStreamsForCameras|系统规定参数。取值：**GetStreamsForCameras**。

 |
|CameraIds|String|是|\["xxxxxxxxx", "yyyyyyyyy", … "zzzzzzzzz"\]|视频点位ID。

 取值可以由多个视频点位ID组成一个JSON数组，ID之间用半角逗号（,）隔开。

 |
|InstanceId|String|是|cityvisual-xxxxx|实例ID。

 |
|RegionId|String|否|cn-shanghai|地域ID。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|E175B041-75A2-4335-B3AC-0FD008F93627|请求ID。

 |
|Streams| |\{"StreamName":"ipc\_101","StreamUrl":"mq://ipc\_10"\}|视频流信息。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=GetStreamsForCameras
&CameraIds=["xxxxxxxxx", "yyyyyyyyy", … "zzzzzzzzz"]
&InstanceId=cityvisual-xxxxx
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<GetStreamsForCamerasResponse>
      <Streams>
            <Stream>
                  <StreamName>ipc_001</StreamName>
                  <StreamUrl>mq://ipc_001</StreamUrl>
            </Stream>
      </Streams>
      <RequestId>E175B041-75A2-4335-B3AC-0FD008F93627</RequestId>
</GetStreamsForCamerasResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"E175B041-75A2-4335-B3AC-0FD008F93627",
	"Streams":{
		"Stream":[
			{
				"StreamName":"ipc_001",
				"StreamUrl":"mq://ipc_001"
			}
		]
	}
}
```

## 错误码 { .section}

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|404|InvalidCameraIds.NotFound|The specified CameraIds does not exist.|指定的视频点位不存在。|

访问[错误中心](https://error-center.aliyun.com/status/product/cityvisual)查看更多错误码。

