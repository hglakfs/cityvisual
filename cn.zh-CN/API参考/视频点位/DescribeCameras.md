# DescribeCameras {#doc_api_cityvisual_DescribeCameras .reference}

调用DescribeCameras获取已创建的视频点位信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cityvisual&api=DescribeCameras&type=RPC&version=2018-10-30)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeCameras|系统规定参数。取值：**DescribeCameras**。

 |
|InstanceId|String|是|cityvisual-InstanceId|实例ID。

 |
|PageNumber|Integer|是|1|视频点位列表的页码。起始值：1。

 默认值：**1** 。

 |
|PageSize|Integer|是|10|分页查询时设置的每页行数。最大值：100。

 默认值：**10**。

 |
|CameraId|String|否|003\_2|视频点位ID。

 |
|CameraName|String|否|name|视频点位名称。

 |
|RegionId|String|否|cn-shanghai|地域ID。

 |
|StreamStatus|String|否|ON\_LINE|视频点位状态：

 -   **ON\_LINE**: 在线
-   **OFF\_LINE**: 离线

 |
|WorkGroupId|String|否|283|接流工作组ID。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Cameras| | |视频点位信息。

 |
|CameraId|String|003\_2|摄像头ID。

 |
|CameraName|String|name|视频点位名称。

 |
|Conf|String|\{"shardId":"0","storageType":"mq","readType":"file2ts","mediaType":"mp4","outputFormat":"raw"\}|视频点位配置信息。

 |
|InviteUri|String|002\_1|视频点位GUID。

 |
|Location|String|\{"latitude":"1.1","longitude":"2.2"\}|视频点位经纬度坐标。

 |
|RtmpPath|String|rtmp://IP/mylive/002\_1|视频流地址。

 |
|StreamStatus|String|ON\_LINE|视频点位状态：

 -   **ON\_LINE**：在线
-   **OFF\_LINE**：离线

 |
|UpdateTime|String|2018-10-10T10:30:30Z|视频点位更新时间。

 按照ISO8601标准表示，并需要使用UTC时间，格式为**yyyy-MM-ddTHH:mm:ssZ**。

 |
|WorkGroupId|String|637|工作组的ID。

 |
|PageNumber|Integer|1|视频点位列表的页码。起始值：1。

 默认值：1 。

 |
|PageSize|Integer|10|分页查询时设置的每页行数。最大值：100。

 默认值：10。

 |
|RequestId|String|E175B041-75A2-4335-B3AC-0FD008F93627|请求ID。

 |
|TotalCount|Integer|300|该实例下的视频点位总数。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeCameras
&InstanceId=cityvisual-InstanceId
&PageNumber=1
&PageSize=10
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeCamerasResponse>
    <PageNumber>1</PageNumber>
    <TotalCount>20</TotalCount>
    <PageSize>10</PageSize>
    <RequestId>14A07460-EBE7-47CA-9757-12CC4761D47A</RequestId>
    <Cameras>
        <Camera>
            <CameraId>003_2</CameraId>
            <Conf>{"shardId":"0","storageType":"mq","readType":"file2ts","mediaType":"mp4","outputFormat":"raw"}</Conf>
            <Id>51</Id>
            <InviteUri>003_2</InviteUri>
            <Location>{"latitude":"1.1","longitude":"2.2"}</Location>
            <Name>002_1</Name>
            <RtmpPath>rtmp://IP/mylive/002_1</RtmpPath>
            <UpdationTime>2015-07-27T07:08Z</UpdationTime>
            <StreamStatus>ON_LINE</StreamStatus>
        </Camera>
    </Cameras>
</DescribeCamerasResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"PageNumber":"1",
	"TotalCount":"1",
	"PageSize":"10",
	"Cameras":{
		"Camera":[
			{
				"Name":"002_1",
				"Conf":"{\"shardId\":\"0\",\"storageType\":\"mq\",\"readType\":\"file2ts\",\"mediaType\":\"mp4\",\"outputFormat\":\"raw\"}",
				"CameraId":"003_2",
				"UpdationTime":"2017-12-10T04:04Z",
				"Location":"{\"latitude\":\"1.1\",\"longitude\":\"2.2\"}",
				"Id":"51",
				"RtmpPath":"rtmp://IP/mylive/002_1",
				"InviteUri":"003_2",
				"StreamStatus":"ON_LINE"
			}
		]
	},
	"RequestId":"14A07460-EBE7-47CA-9757-12CC4761D47A"
}
```

## 错误码 { .section}

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|404|InvalidStreamStatus.NotFound|The specified StreamStatus does not exist.|指定的StreamStatus不存在。|

访问[错误中心](https://error-center.aliyun.com/status/product/cityvisual)查看更多错误码。

