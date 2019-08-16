# CreateCamera {#doc_api_cityvisual_CreateCamera .reference}

调用CreateCamera创建视频点位信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cityvisual&api=CreateCamera&type=RPC&version=2018-10-30)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateCamera|系统规定参数。取值：**CreateCamera**。

 |
|CameraId|String|是|003\_2|视频点位ID。

 |
|CameraName|String|是|name|视频点位名称。

 |
|InstanceId|String|是|cityvisual-xxxx|实例ID。

 |
|InviteUri|String|是|002\_1|实时视频点位网络url。

 |
|LocationInfo|String|是|\{"latitude":"30.245853","longitude":"120.209947"\}|视频点位经纬度坐标。

 |
|WorkGroupId|String|是|511|工作组ID。

 |
|OssPath|String|否|https://cityvisual.oss-cn-shanghai.aliyuncs.com/xxx.mp4|离线视频文件的OSS地址。

 |
|RegionId|String|否|cn-shanghai|地域ID。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|CameraId|String|003\_2|视频点位ID。

 |
|RequestId|String|E175B041-75A2-4335-B3AC-0FD008F93627|请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=CreateCamera
&CameraId=003_2
&CameraName=name
&InstanceId=cityvisual-xxxx
&InviteUri=002_1
&LocationInfo={"latitude":"30.245853","longitude":"120.209947"}
&WorkGroupId=511
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<CreateCameraResponse>
      <CameraId>1</CameraId>
      <RequestId>20</RequestId>
</CreateCameraResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"CameraId":"003_21",
	"RequestId":"E175B041-75A2-4335-B3AC-0FD008F936271"
}
```

## 错误码 { .section}

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|400|InvalidName.Malformed|The specified Name is incorrectly formatted.|指定的Name格式不合法。|
|400|InvalidName.Duplicate|The specified name already exists.|指定的名称已存在。|

访问[错误中心](https://error-center.aliyun.com/status/product/cityvisual)查看更多错误码。

