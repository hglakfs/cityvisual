# CreateInstance {#doc_api_cityvisual_CreateInstance .reference}

调用CreateInstance创建一个实例。

**说明：** 请确保在使用该接口前，已充分了解该产品的收费方式和价格。更多详情，请参见[计费概述](https://www.aliyun.com/price/product#/cityvisual/detail])。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cityvisual&api=CreateInstance&type=RPC&version=2018-10-30)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateInstance|系统规定参数。取值：CreateInstance。

 |
|InstanceCapacity|Integer|是|20|实例规格,指视频点位接入路数。

 |
|RegionId|String|是|cn-shanghai|所属的地域ID。您可以调用DescribeRegions查看最新的阿里云地域列表。

 |
|Description|String|否|SHInstance|实例描述。长度为2~256个英文或中文字符，不能以 http:// 和 https:// 开头。默认值：空。

 |
|InstanceName|String|否|ShangHai|实例名称。长度为2~128个英文或中文字符。必须以大小字母或中文开头，不能以 http:// 和 https:// 开头。可以包含数字、半角冒号（:）、下划线（\_）或者连字符（-）。默认值：空。

 |
|Status|String|否|Running|实例状态，取值范围：

 -   Running 运行中
-   Stopped 已停止

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|InstanceId|String|cityvisual-instance1|实例ID

 |
|RequestId|String|7D800EB6-8565-47EC-87B2-213960F77508|请求 ID

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=CreateInstance
&InstanceCapacity=20
&RegionId=cn-shanghai
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<CreateInstanceResponse>
    <RequestId>7D800EB6-8565-47EC-87B2-213960F77508</RequestId>
    <InstanceId>cityvisual-instance1</InstanceId>
</CreateInstanceResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"7D800EB6-8565-47EC-87B2-213960F77508",
	"InstanceId":"cityvisual-instance1"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/cityvisual)查看更多错误码。

