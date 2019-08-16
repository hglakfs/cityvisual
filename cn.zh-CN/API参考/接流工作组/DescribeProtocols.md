# DescribeProtocols {#doc_api_cityvisual_DescribeProtocols .reference}

调用DescribeProtocols获取已支持的工作组协议。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cityvisual&api=DescribeProtocols&type=RPC&version=2018-10-30)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeProtocols|系统规定参数。取值：**DescribeProtocols**。

 |
|RegionId|String|否|cn-shanghai|地域ID。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Protocols|Map|\{"rtmp":"RTMP"\}|获取到的协议Map。

 |
|RequestId|String|E175B041-75A2-4335-B3AC-0FD008F93627|请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeProtocols
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeProtocolsResponse>
      <RequestId>E175B041-75A2-4335-B3AC-0FD008F93627</RequestId>
      <Protocols>
            <onvif>ONVIF</onvif>
      </Protocols>
</DescribeProtocolsResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"Protocols":{
		"onvif":"ONVIF",
		"transfer_topic_data":"TRANSFER_TOPIC_DATA",
		"video_records":"VIDEO_RECORDS",
		"gb28181":"GB28181",
		"file":"FILE",
		"hk_ivms_8700":"HK_IVMS_8700",
		"dahua_vcloud_1":"DAHUA_VCLOUD_1",
		"video_clips_oss":"VIDEO_CLIPS_OSS",
		"rtmp":"RTMP",
		"rtsp":"RTSP",
		"video_clips_ceph":"VIDEO_CLIPS_CEPH"
	},
	"RequestId":"E175B041-75A2-4335-B3AC-0FD008F93627"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/cityvisual)查看更多错误码。

