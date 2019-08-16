# API概览 {#doc_974624 .concept}

城市视觉智能引擎提供以下相关API接口。

## 实例 {#section_y6r_0ug_4va .section}

|API|描述|
|---|--|
|[ModifyInstance](cn.zh-CN/API参考/实例/ModifyInstance.md)|调用ModifyInstance修改实例。|
|[DescribeInstances](cn.zh-CN/API参考/实例/DescribeInstances.md)|调用DescribeInstances查询一个或多个实例的详细信息。|
|[DeleteInstance](cn.zh-CN/API参考/实例/DeleteInstance.md)|调用DeleteInstance释放一台到期的预付费（包年包月）实例。|
|[CreateInstance](cn.zh-CN/API参考/实例/CreateInstance.md)|调用CreateInstance创建一个实例。|

## 接流工作组 {#section_0gr_hmi_e6a .section}

|API|描述|
|---|--|
|[DeleteWorkGroup](cn.zh-CN/API参考/接流工作组/DeleteWorkGroup.md)|调用DeleteWorkGroup删除指定的接流工作组。|
|[DescribeWorkGroups](cn.zh-CN/API参考/接流工作组/DescribeWorkGroups.md)|调用DescribeWorkGroups获取已创建的接流工作组。|
|[CreateWorkGroup](cn.zh-CN/API参考/接流工作组/CreateWorkGroup.md)|调用CreateWorkGroup创建接流工作组。|
|[ModifyWorkGroup](cn.zh-CN/API参考/接流工作组/ModifyWorkGroup.md)|调用ModifyWorkGroup修改接流工作组信息。|
|[DescribeProtocols](cn.zh-CN/API参考/接流工作组/DescribeProtocols.md)|调用DescribeProtocols获取已支持的工作组协议。|

## 视频点位 {#section_hgv_ll7_vue .section}

|API|描述|
|---|--|
|[DescribeCameras](cn.zh-CN/API参考/视频点位/DescribeCameras.md)|调用DescribeCameras获取已创建的视频点位信息。|
|[CreateCamera](cn.zh-CN/API参考/视频点位/CreateCamera.md)|调用CreateCamera创建视频点位信息。|
|[BatchModifyCameraStatus](cn.zh-CN/API参考/视频点位/BatchModifyCameraStatus.md)|调用BatchModifyCameraStatus批量修改点位状态。|
|[ModifyCamera](cn.zh-CN/API参考/视频点位/ModifyCamera.md)|调用ModifyCamera修改视频点位信息。|
|[GetStreamsForCameras](cn.zh-CN/API参考/视频点位/GetStreamsForCameras.md)|调用GetStreamsForCameras根据视频点位获取相应的视频流信息。|
|[DeleteCamera](cn.zh-CN/API参考/视频点位/DeleteCamera.md)|调用DeleteCamera删除指定的视频点位信息。|

## 算法库 {#section_p8x_zc3_zz2 .section}

|API|描述|
|---|--|
|[ModifyAlgoLib](cn.zh-CN/API参考/算法库/ModifyAlgoLib.md)|调用ModifyAlgoLib修改算法库信息。|
|[DescribeAlgoLibs](cn.zh-CN/API参考/算法库/DescribeAlgoLibs.md)|调用DescribeAlgoLibs获取已创建的算法库信息。|
|[DeleteAlgoLib](cn.zh-CN/API参考/算法库/DeleteAlgoLib.md)|调用DeleteAlgoLib删除指定的算法库。|
|[CreateAlgoLib](cn.zh-CN/API参考/算法库/CreateAlgoLib.md)|调用CreateAlgoLib创建算法库。|

## 算法库能力集 {#section_s2l_0b8_l8s .section}

|API|描述|
|---|--|
|[CreateCapability](cn.zh-CN/API参考/算法库能力集/CreateCapability.md)|调用CreateCapability创建算法库能力集。|
|[DescribeCapabilities](cn.zh-CN/API参考/算法库能力集/DescribeCapabilities.md)|调用DescribeCapabilities获取已创建的算法库能力集信息。|
|[DeleteCapability](cn.zh-CN/API参考/算法库能力集/DeleteCapability.md)|调用DeleteCapability删除指定的算法库能力集。|
|[ModifyCapability](cn.zh-CN/API参考/算法库能力集/ModifyCapability.md)|调用ModifyCapability修改算法库能力集。|

## 计算资源配置 {#section_b6c_r8m_z81 .section}

|API|描述|
|---|--|
|[DescribeResourceProfiles](cn.zh-CN/API参考/计算资源配置/DescribeResourceProfiles.md)|调用DescribeResourceProfiles获取已创建的计算资源配置信息。|
|[CreateResourceProfile](cn.zh-CN/API参考/计算资源配置/CreateResourceProfile.md)|调用CreateResourceProfile创建计算资源配置信息。|
|[DeleteResourceProfile](cn.zh-CN/API参考/计算资源配置/DeleteResourceProfile.md)|调用DeleteResourceProfile删除指定的计算资源配置。|
|[ModifyResourceProfile](cn.zh-CN/API参考/计算资源配置/ModifyResourceProfile.md)|调用ModifyResourceProfile修改资源参数集。|

## 计算工作组 {#section_rg4_zh5_qer .section}

|API|描述|
|---|--|
|[StopJobGroup](cn.zh-CN/API参考/计算工作组/StopJobGroup.md)|调用StopJobGroup停止指定的计算工作组。|
|[ListComputeJobLogs](cn.zh-CN/API参考/计算工作组/ListComputeJobLogs.md)|调用ListComputeJobLogs获取计算日志名称列表。|
|[CreateJobGroup](cn.zh-CN/API参考/计算工作组/CreateJobGroup.md)|调用CreateJobGroup创建计算工作组信息。|
|[ModifyJobGroup](cn.zh-CN/API参考/计算工作组/ModifyJobGroup.md)|调用ModifyJobGroup修改计算工作组信息。|
|[DescribeJobGroups](cn.zh-CN/API参考/计算工作组/DescribeJobGroups.md)|调用DescribeJobGroups获取已创建的计算工作组信息。|
|[StartJobGroup](cn.zh-CN/API参考/计算工作组/StartJobGroup.md)|调用StartJobGroup启动指定的计算工作组。|
|[DeleteJobGroup](cn.zh-CN/API参考/计算工作组/DeleteJobGroup.md)|调用DeleteJobGroup删除指定的计算工作组。|
|[GetComputeJobLog](cn.zh-CN/API参考/计算工作组/GetComputeJobLog.md)|调用GetComputeJobLog获取计算Job日志。|

## 视频流 {#section_45s_fit_3sm .section}

|API|描述|
|---|--|
|[AttachStream](cn.zh-CN/API参考/视频流/AttachStream.md)|调用AttachStream给指定的计算工作组绑定Stream。|
|[DetachStream](cn.zh-CN/API参考/视频流/DetachStream.md)|调用DetachStream给指定的计算工作组解绑视频流。|
|[DescribeStreams](cn.zh-CN/API参考/视频流/DescribeStreams.md)|调用DescribeStreams获取指定的计算工作组已绑定的视频流。|

## 图搜 {#section_4p5_rqt_7ky .section}

|API|描述|
|---|--|
|[SearchImages](cn.zh-CN/API参考/图搜/SearchImages.md)|调用SearchImages搜索图片。|

## 地域 {#section_iwb_qmv_sgb .section}

|API|描述|
|---|--|
|[DescribeRegions](cn.zh-CN/API参考/地域/DescribeRegions.md)|调用DescribeRegions查询您可以使用的阿里云地域。|

