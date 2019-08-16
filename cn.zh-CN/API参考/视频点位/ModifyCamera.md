# ModifyCamera {#doc_api_cityvisual_ModifyCamera .reference}

调用ModifyCamera修改视频点位信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cityvisual&api=ModifyCamera&type=RPC&version=2018-10-30)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ModifyCamera|系统规定参数。取值：**ModifyCamera**。

 |
|CameraId|String|是|003\_2|视频点位ID，指定待修改的视频点位。

 |
|CameraName|String|是|CameraName|视频点位名称。

 长度为`[2,128]`个英文或中文字符。必须以大小字母或中文开头，不能以http:// 和https:// 开头。可以包含数字、半角冒号（:）、下划线（\_）或者连字符（-）。

 |
|InviteUri|String|是|320599500@xxx|实时视频点位网络url。

 |
|LocationInfo|String|是|\{"latitude":"30.245853","longitude":"120.209947"\}|视频点位经纬度坐标

 |
|RegionId|String|否|cn-shanghai|地域ID。

 |
|StreamStatus|String|否|ON\_LINE|视频点位状态：

 -   **ON\_LINE**: 在线
-   **OFF\_LINE**: 离线

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|E175B041-75A2-4335-B3AC-0FD008F93627|请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=ModifyCamera
&CameraId=003_2
&CameraName=CameraName
&InviteUri=320599500@xxx
&LocationInfo={"latitude":"30.245853","longitude":"120.209947"}
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeCamerasResponse>
      <RequestId>E175B041-75A2-4335-B3AC-0FD008F93627</RequestId>
</DescribeCamerasResponse>
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
|400|InvalidName.Duplicate|The specified name already exists.|指定的名称已存在。|

访问[错误中心](https://error-center.aliyun.com/status/product/cityvisual)查看更多错误码。

