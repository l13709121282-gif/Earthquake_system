# Earthquake_system
基于 ESP32 的分布式地震预警系统，包含 LoRa 无线传感节点、4G/WiFi 双模网关、云端 SeisBench AI 分析引擎和 React Native 手机 APP。  节点通过 MPU6050 传感器 100Hz 采集三轴加速度，Edge Impulse TFLite 模型进行波形预测和 PCA 压缩，经 DX-LR22 LoRa 模块发送至网关。网关支持 WiFi+4G 双网冗余，集成 PhaseNet/EQTransformer 深度学习模型进行多节点联合判定，通过钉钉机器人、MQTT 和邮件多渠道推送预警。手机 APP 可自动获取震中位置并计算地震波到达倒计时。  适用于地震多发地区的低成本、快速部署预警网络。
