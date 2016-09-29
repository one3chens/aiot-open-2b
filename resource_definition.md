# 资源定义

绿米智能设备均具备完善的资源定义，便于设备的管理。下面会根据设备类型，分别列出这些设备所具有的资源。

##网关300

model: lumi.gateway.v3

| 功能模块 | 资源 | 值类型 | 取值范围 | 最大值 | 最小值 | 描述 |
| -- | -- | -- | -- | -- | -- | -- |
| Alarm | alarm_status | uint8_t | 0,1 | -- | -- | 报警状态, 0-没报警，1-报警 |
| Alarm | alarm_bell_index | uint32_t | -- | -- | -- | 播放警报index，当index=10000时播放默认铃声 |
| Alarm | alarm_bell_volume | uint8_t | -- | 0 | 100 | 报警状态，0:没报警 ，1：报警 |
| Alarm | alarm_time_length | uint32_t | -- | -- | -- | 报警时长 |
| Doorbell | doorbell_status | uint8_t | 0,1 | -- | -- | 门铃状态 |
| Doorbell | doorbell_bell_index | uint32_t | 0,1 | -- | -- | 门铃状态 |
