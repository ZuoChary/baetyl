# Roadmap

## 2019年度目标

Baetyl将云原生带入边缘创新，包括：

- 提供基于Linux内核的轻量级、不可修改、全内存运行的边缘计算操作系统。
- 打通跨越云、边缘和物联网设备的服务网格，实现应用和数据的自由流动。
- 改进生产条件下Baetyl的故障排查和可调式性。
- 支持由大量节点组成的边缘集群，提供智能化的任务调度能力。
- 提供对AMQP、OPC-UA、ZigBee等各种形式的设备和数据连接能力。

## Release 1.0，2019年秋季

Baetyl将为IoT和边缘计算提供基础设施平台和应用开发工具，包括：
- 核心框架方向
   - 系统安全
      - 支持边缘设备激活，动态下发唯一证书
      - 提供批量设备激活的机制
   - 应用支持
      - 日志可远程查看，支持分应用采集，能够根据容量和时间等因素设置截断
      - 提供服务间依赖能力，支持使用端口等方式进行健康检查
      - 提供预下载应用镜像的能力
   - 远程管理
      - 提供开源的远程管理控制台
- 系统相关能力
   - Linux平台
      - 向containerd迁移，消除对docker的依赖，进一步轻量化
      - 消除容器模式的虚拟网络引入的传输开销
      - 支持Linux各主要发行版上的原生包管理
      - 支持x86/x86-64/armv7/aarch64/mips/mipsle/mips64/mips64le
   - Windows平台
      - 支持WSL+Docker形式运行
      - 试验性的支持Windows Container
      - 试验性的支持Windows 10 IoT Core
   - Kubernetes平台
      - 试验性的支持K3S作为分布式化的基础
      - 试验性的支持函数计算在多机上的分布式运行
- 应用开发支持
   - SDK
      - 提供C接口的SDK
      - 提供本机函数计算的调用API
      - 提供调用ML推断的API
      - 提供图像视频采集和处理的API
      - 提供本地KV存储的API
   - 南向消息服务
      - 进一步降低在资源有限设备上的性能消耗
   - 函数计算
      - 支持C++等二进制函数
      - 支持Shell函数
   - 流式计算
      - 支持Flink SQL兼容的流式计算
   - 北向数据同步
      - 支持与Mosquito、EMQ和AWS的IOTHUB的连接
      - 支持与Kafka的连接