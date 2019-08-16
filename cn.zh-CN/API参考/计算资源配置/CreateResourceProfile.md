# CreateResourceProfile {#doc_api_cityvisual_CreateResourceProfile .reference}

调用CreateResourceProfile创建计算资源配置信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cityvisual&api=CreateResourceProfile&type=RPC&version=2018-10-30)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateResourceProfile|系统规定参数。取值：**CreateResourceProfile**。

 |
|InstanceId|String|是|cityvisual-Instance|实例ID。

 |
|ResourceProfileName|String|是|name|计算资源配置名称。

 长度为`[2,128]`个英文或中文字符。必须以大小字母或中文开头，不能以http:// 和https:// 开头。可以包含数字、半角冒号（:）、下划线（\_）或者连字符（-）。

 |
|RegionId|String|否|cn-shanghai|地域ID。

 |
|ResourceProfileParams.N.Key|String|否|key|计算资源配置的参数键。

 一旦传入该值，则不允许为空字符串。最多支持64个字符，不能以aliyun、acs:、http:// 或者https:// 开头。

 |
|ResourceProfileParams.N.Value|String|否|value|计算资源配置的参数值。

 一旦传入该值，则不允许为空字符串。最多支持128个字符，不能以aliyun、acs:、http:// 或者https:// 开头。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|E175B041-75A2-4335-B3AC-0FD008F93627|请求ID。

 |
|ResourceProfileId|String|56yf5dt5i88b78ft5fhyt6|计算资源配置ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=CreateResourceProfile
&InstanceId=cityvisual-Instance
&ResourceProfileName=name
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<CreateResourceProfileResponse>
      <ResourceProfileId>56yf5dt5i88b78ft5fhyt6</ResourceProfileId>
      <RequestId>E175B041-75A2-4335-B3AC-0FD008F93627</RequestId>
</CreateResourceProfileResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"E175B041-75A2-4335-B3AC-0FD008F93627",
	"ResourceProfileId":"56yf5dt5i88b78ft5fhyt6"
}
```

## 错误码 { .section}

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|400|InvalidName.Malformed|The specified Name is incorrectly formatted.|指定的Name格式不合法。|
|400|InvalidName.Duplicate|The specified name already exists.|指定的名称已存在。|
|403|InvalidParameter.KeyNotSupported|One or more parameter keys are not supported.|至少存在一个不支持的参数键。|
|403|MissingParameter|You must specify the required resource parameters.|资源参数缺少必需项。|

访问[错误中心](https://error-center.aliyun.com/status/product/cityvisual)查看更多错误码。

