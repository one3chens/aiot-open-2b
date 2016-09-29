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
| Doorbell | doorbell_bell_index | uint32_t | -- | -- | -- | 播放门铃index，当index=10000时播放默认铃声 |
| Doorbell | doorbell_bell_volume | uint8_t | -- | 0 | 100 | 门铃音音量,0~100 |
| Clock | clock_status | uint8_t | 0,1 | -- | -- | 闹钟状态 0: 停止播放 1：开始播放 |
| Clock | clock_bell_index | uint32_t | -- | -- | -- | 播放闹钟index，当index=10000时播放默认铃声 |
| Clock | clock_volume | uint8_t | -- | 0 | 100 | 闹钟音量,0~100 |
| arming | arming_status | uint8_t | 1,2,3,4 | -- | -- | 布防状态：1:开/0:关/2:启动中/3:toggle /4:消警但不撤防 |
| arming | arming_last_alert_time | uint32_t | -- | -- | -- | 上次改变布防状态的时间,1970.1.1以后的秒数 |
| arming | arming_delay_time | uint32_t | -- | -- | -- | 布防等待时间，单位秒，PROP_TIME_DELAY = 113 |
