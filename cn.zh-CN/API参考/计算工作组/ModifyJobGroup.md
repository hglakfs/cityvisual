# ModifyJobGroup {#doc_api_cityvisual_ModifyJobGroup .reference}

调用ModifyJobGroup修改计算工作组信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cityvisual&api=ModifyJobGroup&type=RPC&version=2018-10-30)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ModifyJobGroup|系统规定参数。取值：**ModifyJobGroup**。

 |
|AlgoLibId|String|是|2|算法库ID。

 |
|JobGroupId|String|是|3|待修改的JobGroup的ID。

 |
|JobGroupName|String|是|JobGroupName|JobGroup名称。

 长度为`[2,128]`个英文或中文字符。必须以大小字母或中文开头，不能以 http:// 和https:// 开头。可以包含数字、半角冒号（:）、下划线（\_）或者连字符（-）。

 |
|ResourceProfileId|String|是|23|资源参数集ID。

 |
|JobCount|Integer|否|3|实际计算Job数量。

 |
|JobGroupParams.N.Key|String|否|ES\_ENABLE|JobGroup参数的键，取值范围：

 \* ES\_ENABLE: 结果输出到ES

 \* RDS\_ENABLE: 结果输出到RDS

 \* OUT\_MQ\_ENABLE: 结果输出到MQ

 \* DATAHUB\_ENABLE: 结果输出到DataHub

 \* SCHEDULE\_FLOW\_START\_TIME: 调度开始时间

 |
|JobGroupParams.N.Value|String|否|True|JobGroup参数的值。

 当参数键为****\_ENABLE**时,取值范围: -**True:**输出 -**False**: 不输出 当参数键为**SCHEDULE\_FLOW\_START\_TIME**时,取值范围: -**Latest**: 最新 -**Oldest**: 最旧**

 |
|PlanedJobCount|Integer|否|10|期望的计算Job数量。

 |
|RegionId|String|否|cn-shanghai|地域ID。

 |
|Status|String|否|Running|JobGroup状态。取值范围：

 \* Running: 运行中

 \* Stopped: 已停止

 |
|StreamPerJob|Integer|否|5|计算Job处理的视频流数量。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|E175B041-75A2-4335-B3AC-0FD008F93627|请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=ModifyJobGroup
&AlgoLibId=2
&JobGroupId=3
&JobGroupName=JobGroupName
&ResourceProfileId=23
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<ModifyJobGroupResponse>
      <RequestId>E175B041-75A2-4335-B3AC-0FD008F93627</RequestId>
</ModifyJobGroupResponse>
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
|404|InvalidAlgoLibId.NotFound|The specified algorithm library does not exist.|指定的算法库不存在。|
|404|InvalidResourceProfileId.NotFound|The specified resource profile does not exist.|指定的资源参数集不存在。|
|400|InvalidStatus.ValueNotSupported|The specified status is invalid.|指定的状态不合法。|
|403|InvalidParameter.KeyNotSupported|One or more parameter keys are not supported.|至少存在一个不支持的参数键。|
|403|MissingParameter|You must specify the required resource parameters.|资源参数缺少必需项。|
|404|InvalidJobGroupId.NotFound|The specified job group does not exist.|指定的JobGroup不存在。|

访问[错误中心](https://error-center.aliyun.com/status/product/cityvisual)查看更多错误码。

