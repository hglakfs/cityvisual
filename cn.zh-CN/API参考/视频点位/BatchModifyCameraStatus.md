# BatchModifyCameraStatus {#doc_api_cityvisual_BatchModifyCameraStatus .reference}

调用BatchModifyCameraStatus批量修改点位状态。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cityvisual&api=BatchModifyCameraStatus&type=RPC&version=2018-10-30)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|BatchModifyCameraStatus|系统规定参数。取值：**BatchModifyCameraStatus**。

 |
|CameraIds|String|是|\["xxxxxxxxx", "yyyyyyyyy", … "zzzzzzzzz"\]|视频点位ID。

 取值可以由多个视频点位ID组成一个JSON数组，ID之间用半角逗号（,）隔开。

 |
|StreamStatus|String|是|ON\_LINE|待修改的视频点位状态。 取值范围：

 \* ON\_LINE: 接流

 \* OFF\_LINE: 断流

 |
|WorkGroupId|String|是|123|接流工作组ID。

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

http(s)://[Endpoint]/?Action=BatchModifyCameraStatus
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<BatchModifyCameraStatusResponse>
      <RequestId>E175B041-75A2-4335-B3AC-0FD008F93627</RequestId>
</BatchModifyCameraStatusResponse>
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
|400|InvalidStatus.ValueNotSupported|The specified status is invalid.|指定的状态不合法。|
|404|InvalidCameraId.NotFound|The specified camera does not exist.|指定的视频点位不存在。|

访问[错误中心](https://error-center.aliyun.com/status/product/cityvisual)查看更多错误码。

