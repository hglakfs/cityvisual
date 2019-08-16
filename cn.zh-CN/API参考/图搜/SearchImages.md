# SearchImages {#doc_api_cityvisual_SearchImages .reference}

调用SearchImages搜索图片。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cityvisual&api=SearchImages&type=RPC&version=2018-10-30)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|SearchImages|系统规定参数。取值：SearchImages。

 |
|Contents|String|是|/9j/4AAQSkZJRgABAQAAAQABAAD/2wB...|图像内容，base64 编码，多个用","隔开。

 **说明：** 当**NoFeature**值为**False**时，为必选项。

 |
|From|Integer|是|0|返回结果在查询结果集中的偏移量，默认为**0**。

 |
|InstanceId|String|是|cityvisual-xxxxxx|实例ID。

 |
|Size|Integer|是|100|返回结果数量，默认为**10**。

 |
|StartTime|String|是|1553734800000|查询范围起始时间戳 \(毫秒\)，

 13 位， 如1553734800000。

 |
|Attribute.N.Key|String|否|Age|待查询对象详细属性的键.

 当Type取值为“Person”时,取值范围:

 \* Sex: 性别

 \* Age: 年龄

 \* Hair: 头发类型

 \* Pose: 身体姿态

 \* ClothType: 上衣类型

 \* ClothColor: 上衣颜色

 \* TrouserType: 下衣类型

 \* TrouserColor: 下衣颜色

 当Type取值为“Vehicle”时,取值范围:

 \* PlateNumber: 车牌号

 \* VehicleColor: 车身颜色

 \* VehicleType: 车辆

 \* Brand: 车辆品牌

 当Type取值为“Bicycle”时,取值范围:

 \* Sex: 骑车人性别

 \* Age: 骑车人年龄

 \* HeadWear: 骑车人头饰

 \* NonVehicleType: 非机动车类型

 |
|Attribute.N.Value|String|否|12|待查询对象详细属性的值。

 |
|CameraIds|String|否|003\_2|摄像头点位id，支持多点位查询。

 各个点位之间用逗号"," 隔开，如"0001,0002", 查询摄像头0001和0002下的目标。

 |
|EndTime|String|否|1553735800000|查询范围结束时间戳 \(毫秒\)，

 13 位， 如1553756400000。

 |
|ImageIds|String|否|001,002|支持使用多个目标id查询，实现渐进性查询。

 id与id之间用逗号“,”隔开，如:”001,002”,

 查询的结果是与001和002两个目标共同相似度最高的图像。

 |
|NoFeature|String|否|True|"True"表示不用特征匹配查询，纯属性或id 查询， "False"表示使用特征查询。

 |
|RegionId|String|否|cn-shanghai|地域ID。

 |
|Type|String|否|person|查询类型。根据算法不同查询不同的类型，天擎算法查询类型示例:

 -   person\(行人\)
-   bicycle \(非机动⻋\)
-   vehicle\(机动⻋\)

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Images| | |图片

 |
|AgeType|String|Youth|当ObjType为“Person” 或“NonVehicle”时,年龄类型,取值范围:

 \* Youth: 青年

 \* Midlife: 中年

 \* OldAge: 老年

 \* Uncertain: 无法判断

 |
|AgeTypeScore|Float|0.99|当ObjType为“Person”时,年龄类型置信度, 取值范围`[0,1]`。

 |
|Brand|String|DZ|当ObjType为“Vehicle”时,车辆品牌。

 |
|BrandScore|Float|0.89|当ObjType为“Vehicle”时,车辆品牌置信度, 取值范围`[0,1]`。

 |
|CameraId|String|003\_2|摄像头id。

 |
|ClothColor|String|White|当ObjType为“Person”时,上衣颜色,取值范围:

 \* Black: 黑色

 \* White: 白色

 \* Gray: 灰色

 \* Red: 红色

 \* Blue: 蓝色

 \* Yellow: 黄色

 \* Orange: 橙色

 \* Brown: 棕色

 \* Green: 绿色

 \* Purple: 紫色

 \* Cyan 青色

 \* Pink: 粉色

 \* Transparent: 透明

 \* Other: 其他

 |
|ClothColorScore|Float|0.5|当ObjType为“Person”时,上衣颜色置信度, 取值范围`[0,1]`。

 |
|ClothType|String|Other|当ObjType为“Person”时,上衣类型,取值范围:

 \* ShortSleeve: 短袖

 \* MiddleSleeve: 中袖

 \* Sleeveless: 无袖

 \* Other: 其他

 |
|ClothTypeScore|Float|0.4|当ObjType为“Person”时,上衣类型置信度, 取值范围**\[0,1\]**。

 |
|CropImage|String|https://oss-cn-shanghai.aliyuncs.com/cropImage/20180610/15571409324/1560148924921.jpg|对象抠图存储路径。

 |
|EntryTime|String|2018-10-10T10:20:30Z|进入视频时间。

 |
|Feature|String|/9j/4AAQSkZJRgABAQAAAQABAAD/2wB...|图像的高维特征向量， base64编码。

 |
|HairType|String|Crop|当ObjType为“Person”时,发型,取值范围:

 \* Crop: 平头

 \* CentreParting: 中分

 \* ForeheadBaldness: 额秃

 \* NeckBaldness: 颈秃

 \* Bald: 全秃

 \* CurlyHair: 卷发

 \* WavyHair: 波浪发

 \* Braid: 麻花辫

 \* Updo: 盘发

 \* LongHair: 披肩发

 \* Other: 其他

 |
|HairTypeScore|Float|0.7|当ObjType为“Person”时,头发类型置信度, 取值范围`[0,1]`。

 |
|HeadWear|String|Hat|当ObjType为“NonVehicle”时,骑车人头饰,取值范围:

 \* None: 无

 \* Hat: 帽子

 \* Helmet: 头盔

 \* Scarf: 头巾

 \* Other: 其他

 |
|HeadWearScore|Float|0.6|当ObjType为“NonVehicle”时, 骑车人头饰置信度, 取值范围`[0,1]`。

 |
|ImageId|String|xxx|图片ID。

 |
|LeaveTime|String|2018-10-10T10:20:40Z|离开视频画面时间。按照ISO8601标准表示，并需要使用UTC时间，格式为yyyy-MM-ddTHH:mm:ssZ。

 |
|NonVehicleType|String|Bicycle|当ObjType为“NonVehicle”时,非机动车类型,取值范围:

 \* Bicycle: 自行车

 \* ElectricVehicle: 电瓶车

 \* ClosedTricycle: 封闭三轮车

 \* OpenedTricycle: 开放式三轮车

 \* Other: 其他

 |
|NonVehicleTypeScore|Float|0.1|当ObjType为“NonVehicle”时,非机动车类型置信度, 取值范围`[0,1]`。

 |
|ObjBottom|Integer|1068|对象轮廓外接矩形在画面中的位置，右下角Y坐标。

 |
|ObjLeft|Integer|1630|对象轮廓外接矩形在画面中的位置，左上角X坐标。

 |
|ObjRight|Integer|1774|对象轮廓外接矩形在画面中的位置，右下角X坐标。

 |
|ObjTop|Integer|863|对象轮廓外接矩形在画面中的位置，左上角Y坐标。

 |
|ObjType|String|Person|对象类型,取值范围：

 \* Person: 行人

 \* Vehicle: 机动车

 \* NonVehicle: 非机动车

 |
|OrigImage|String|http://oss-cn-shanghai.aliyuncs.com/……|原图存储路径地址。

 |
|PlateNumber|String|浙A8888|当ObjType为“Vehicle”时,车牌号。

 |
|PoseType|String|Lie|当ObjType为“Person”时,身体姿态,取值范围:

 \* Stand: 站

 \* Squat: 蹲

 \* LieDown: 卧

 \* Lie: 躺

 \* Sit: 坐

 \* Walk: 行走

 \* Run: 奔跑

 \* Jump: 跳跃

 \* Climb: 攀登

 \* Crawl: 匍匐

 \* Other: 其他

 |
|PoseTypeScore|Float|0.6|当ObjType为“Person”时, 身体姿态置信度, 取值范围`[0,1]`。

 |
|Score|Float|0.3|图片相似度得分。

 |
|SexType|String|Male|当ObjType为“Person”或“NonVehicle”时,性别,取值范围:

 \* Male: 男

 \* Female: 女

 \* Uncertain: 不确定

 |
|SexTypeScore|Float|0.5|当ObjType为“Person”时,性别置信度, 取值范围`[0,1]`。

 |
|TimeStamp|String|2018-10-10T10:20:40Z|请求的时间戳。按照ISO8601标准表示，并需要使用UTC时间，格式为yyyy-MM-ddTHH:mm:ssZ。示例：2018-01-01T12:00:00Z 表示北京时间 2018 年 01 月 01 日 20 点 00 分 00 秒。

 |
|TrouserColor|String|Black|当ObjType为“Person”时，下衣颜色类型，取值范围同ClothColor。

 |
|TrouserColorScore|Float|0.8|当ObjType为“Person”时, 下衣颜色置信度, 取值范围`[0,1]`。

 |
|TrouserType|String|Trousers|当ObjType为“Person”时,下衣类型,取值范围:

 \* Trousers: 长裤

 \* Shorts: 短裤

 \* Longuette: 长裙

 \* ShortSkirt: 短裙

 \* Other: 其他

 |
|TrouserTypeScore|Float|0.3|当ObjType为“Person”时，下衣颜色置信度，取值范围`[0,1]`。

 |
|VehicleColor|String|Black|当ObjType为“Vehicle”时,车身颜色类型,取值范围同ClothColor.

 |
|VehicleColorScore|Float|0.9|当ObjType为“Vehicle”时，车身颜色置信度，取值范围`[0,1]`。

 |
|VehicleType|String|Van|当ObjType为“Vehicle”时,车辆类型,取值范围:

 \* SUV: SUV

 \* Car: 小轿车

 \* Truck: 大货车

 \* Van: 小货车

 \* Taxi: 出租车

 \* Bus: 公交车

 \* Minibus: 面包车

 \* Machineshop: 工程车

 |
|VehicleTypeScore|Float|0.7|当ObjType为“Vehicle”时，车辆类型置信度，取值范围`[0,1]`。

 |
|RequestId|String|E175B041-75A2-4335-B3AC-0FD008F93627|请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=SearchImages
&Contents=/9j/4AAQSkZJRgABAQAAAQABAAD/2wB...
&InstanceId=cityvisual-xxxxxx
&From=0
&Size=100
&StartTime=1553734800000
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<SearchImagesResponse>
    <PageNumber>1</PageNumber>
    <TotalCount>4000</TotalCount>
    <PageSize>1</PageSize>
    <RequestId>E175B041-75A2-4335-B3AC-0FD008F93627</RequestId>
    <Images>
        <Image>
            <CameraId>301</CameraId>
            <CropImage>http://tq-output-image.oss-cn-shanghai.aliyuncs.com/cropImage/20190724/301/10/1563933744137-34250.jpg</CropImage>
            <CropImageSigned>http://tq-output-image.oss-cn-shanghai.aliyuncs.com/cropImage/20190724/301/10/1563933744137-34250.jpg</CropImageSigned>
            <EntryTime>2019-09-01T18:00:00Z</EntryTime>
            <ExtImage>null</ExtImage>
            <Feature></Feature>
            <Hair>1</Hair>
            <HairScore>0.7153491</HairScore>
            <ImageId>9771a825f344a0a21ac9a443e2350c6d</ImageId>
            <LeaveTime>2019-09-01T18:10:00Z</LeaveTime>
            <TrouserColor>9</TrouserColor>
            <TrouserColorScore>0.582683</TrouserColorScore>
            <TrouserType>2</TrouserType>
            <TrouserTypeScore>0.82184184</TrouserTypeScore>
            <ObjBottom>1068</ObjBottom>
            <ObjLeft>1630</ObjLeft>
            <ObjRight>1774</ObjRight>
            <ObjTop>8631</ObjTop>
            <ObjType>person</ObjType>
            <OriImageSigned>http://tq-output-image.oss-cn-shanghai.aliyuncs.com/origImage/20190724/301/10/1563933744107-22551.jpg</OriImageSigned>
            <OrigImage>http://tq-output-image.oss-cn-shanghai.aliyuncs.com/origImage/20190724/301/10/1563933744107-22551.jpg</OrigImage>
            <Score>0.89514667</Score>
            <Sex>1</Sex>
            <SexScore>0.56595963</SexScore>
            <TimeStamp>2019-09-01T18:00:00Z</TimeStamp>
            <ClothColor>10</ClothColor>
            <ClothColorScore>0.7773359</ClothColorScore>
            <ClothType>1</ClothType>
            <ClothTypeScore>0.32749894</ClothTypeScore>
        </Image>
    </Images>
</SearchImagesResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"PageNumber":"1",
	"TotalCount":"4000",
	"PageSize":"1",
	"RequestId":"E175B041-75A2-4335-B3AC-0FD008F93627",
	"Images":{
		"Image":[
			{
				"ImageId":"9771a825f344a0a21ac9a443e2350c6d",
				"OrigImage":"http://tq-output-image.oss-cn-shanghai.aliyuncs.com/origImage/20190724/301/10/1563933744107-22551.jpg?Expires=1563937360&OSSAccessKeyId=LTAIWshnEfiYqcgw&Signature=5IaQKKUz1W4W4grsMvFBhBMa7m4%3D",
				"CameraId":"301",
				"LeaveTime":"2019-09-01T18:00:00Z",
				"Feature":"",
				"TrouserTypeScore":0.82184184,
				"SexScore":0.56595963,
				"TrouserType":2,
				"ObjType":"person",
				"ClothTypeScore":0.32749894,
				"Score":"0.89514667",
				"TrouserColor":9,
				"EntryTime":"2019-09-01T18:00:00Z",
				"Sex":1,
				"ClothColorScore":0.7773359,
				"CropImageSigned":"http://tq-output-image.oss-cn-shanghai.aliyuncs.com/cropImage/20190724/301/10/1563933744137-34250.jpg?Expires=1563937360&OSSAccessKeyId=LTAIWshnEfiYqcgw&Signature=wI8R3RRTn7ywqOi0khqR389uJao%3D",
				"Hair":1,
				"ObjBottom":1068,
				"ClothType":1,
				"ObjRight":1774,
				"TimeStamp":"2019-09-01T18:00:00Z",
				"ClothColor":10,
				"TrouserColorScore":0.582683,
				"HairScore":0.7153491,
				"ObjTop":863,
				"OriImageSigned":"http://tq-output-image.oss-cn-shanghai.aliyuncs.com/origImage/20190724/301/10/1563933744107-22551.jpg?Expires=1563937360&OSSAccessKeyId=LTAIWshnEfiYqcgw&Signature=5IaQKKUz1W4W4grsMvFBhBMa7m4%3D",
				"CropImage":"http://tq-output-image.oss-cn-shanghai.aliyuncs.com/cropImage/20190724/301/10/1563933744137-34250.jpg?Expires=1563937360&OSSAccessKeyId=LTAIWshnEfiYqcgw&Signature=wI8R3RRTn7ywqOi0khqR389uJao%3D",
				"ObjLeft":1630
			}
		]
	}
}
```

## 错误码 { .section}

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|404|InvalidCameraIds.NotFound|The specified CameraIds does not exist.|指定的视频点位不存在。|
|404|InvalidImageIds.NotFound|The specified image does not exist.|指定的图片不存在。|
|400|InvalidType.ValueNotSupported|The specified Type is invalid.|指定的Type不合法。|
|400|InvalidAttribute.KeyNotSupported|The specified Attribute.n.Key is invalid.|指定的Attribute.n.Key不合法。|
|400|InvalidFrom.ValueNotSupported|The specified From is invalid.|指定的From不合法。|
|400|InvalidSize.ValueNotSupported|The specified Size is invalid.|指定的Size不合法。|
|400|InvalidAttribute.KeyIsEmpty|You must specify Attribute.n.Key.|指定的Attribute.n.Key不允许为空。|
|400|InvalidAttribute.ValueNotSupported|The specified Attribute.n.Value is invalid.|指定的Attribute.n.Value不合法。|
|400|InvalidContents.Malformed|The specified Contents is incorrectly formatted.|指定的Contents格式不合法。|

访问[错误中心](https://error-center.aliyun.com/status/product/cityvisual)查看更多错误码。

