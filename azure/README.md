## Azure
Microsoft Azure 是一个不断扩展的云服务集合，它可以帮助组织应对各种商业挑战。

![Azure](https://azurecomcdn.azureedge.net/cvt-4af460b5a4cb5588efc577973d9720ec2a0bd2b50f05bbbfd34608e573aebb38/images/page/overview/azure-vs-aws/chart.jpg)

### Azure 与 AWS
世界上的所有组织都认为相较于 Amazon Web Services (AWS)，[Microsoft Azure](https://azure.microsoft.com/zh-cn/overview/azure-vs-aws/) 是适用于企业和混合基础结构的最可信的云。

我们这里不做对比，这个是专业机构干得事，我们用好 Azure 和 AWS 就对了。

### 全球基础结构
* [54 个Azure 区域](https://azure.microsoft.com/zh-cn/global-infrastructure/regions/) 
* 140 个国家/地区可用 
* 区域中的带宽高达 1.6 Pbps

### 体系结构
[体系结构](https://docs.microsoft.com/zh-cn/azure/architecture/)包含用于在 Azure 上构建端到端解决方案的指南，包含参考体系结构、最佳实践、设计模式、方案指南和参考实现等。

### 构建微服务
[在 Azure 中设计、构建和操作微服务](https://docs.microsoft.com/zh-cn/azure/architecture/microservices/)

端到端方案：[无人机交付服务](https://github.com/mspnp/microservices-reference-implementation)，可让客户安排通过无人机收寄包裹。 

* 使用域驱动的设计 (DDD) 来设计微服务体系结构；
* 为计算、存储、消息传递和其他设计元素选择适合的 Azure 服务 ；
* 了解微服务设计模式；
* 容错、可伸缩和性能设计；
* 构建 CI/CD 流水线。

![Microservices](https://github.com/mspnp/microservices-reference-implementation/raw/master/architecture.png)

### 解决方案
可通过[Azure解决方案体系结构](https://azure.microsoft.com/en-us/solutions/architecture/)帮助用户快速构建云基础设施。

如：基于机器学习的异常检测

![ml](https://wiki.huihoo.com/images/1/10/Anomaly-detection-with-machine-learning.png)


### 开放超大规模云硬件
Microsoft 正通过 [Open Compute Project](https://github.com/opencomputeproject) 和其他开创性协作公开硬件设计和开发。
* [Project Olympus](https://www.opencompute.org/wiki/Server/ProjectOlympus) 可供 IT 和数据中心操作员利用社区开发的创新，并根据其特定使用模型缩放经过验证的硬件设计。
* Cerberus 提供服务器硬件缺失的重要安全保护组件：在平台固件上添加保护、检测以及攻击恢复功能。
* Denali 是简化的固态硬盘 (SSD) 体系结构，它也设定了新的行业标准 - 实现创新、提高可靠性、缩短上市时间。

### AI + 边缘计算
![ai](https://azurecomcdn.azureedge.net/cvt-4af460b5a4cb5588efc577973d9720ec2a0bd2b50f05bbbfd34608e573aebb38/images/page/overview/future-of-cloud/iot-diagram.svg)

* Azure Sphere
创建安全的且已连接 Internet 的微控制器设备，以实现端到端设备安全性。
* Azure Data Box Edge
在将本地数据传输到 Azure 之前，使用支持 AI 的计算对其进行分析、预处理和转换。
* Azure IoT Edge
通过完全托管的服务将云智能和分析扩展到边缘设备。
* Azure Stack
将 Azure 扩展引入本地环境，并在任何地方生成和部署混合应用程序。