# ModifyInstance {#doc_api_cityvisual_ModifyInstance .reference}

调用ModifyInstance修改实例。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cityvisual&api=ModifyInstance&type=RPC&version=2018-10-30)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ModifyInstance|系统规定参数。取值：**ModifyInstance**。

 |
|InstanceId|String|是|cityvisual-Instance|实例ID

 |
|Description|String|否|实例描述|实例描述

 |
|InstanceName|String|否|实例名称|实例名称

 |
|RegionId|String|否|cn-shanghai|地域ID

 |
|Status|String|否|Running|实例状态，取值范围：

 -   Running 运行中
-   Stopped 已停止

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|7D800EB6-8565-47EC-87B2-213960F77508|请求ID

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=ModifyInstance
&InstanceId=cityvisual-Instance
&Description=xxxxx
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<ModifyInstanceResponse>
    <RequestId>7D800EB6-8565-47EC-87B2-213960F77508</RequestId>
</ModifyInstanceResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"7D800EB6-8565-47EC-87B2-213960F77508"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/cityvisual)查看更多错误码。

