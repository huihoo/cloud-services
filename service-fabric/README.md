## Service Fabric
Service Fabric 是一款开源(MIT)分布式系统平台，可方便用户轻松打包、部署和管理可缩放的可靠微服务和容器。

Service Fabric 为当今很多 Microsoft 服务提供技术支持，包括 Azure SQL 数据库、Azure Cosmos DB、Cortana、Microsoft Power BI、Microsoft Intune、Azure 事件中心、Azure IoT 中心、Dynamics 365、Skype for Business 以及其他许多核心 Azure 服务。

![service-fabric](https://docs.microsoft.com/zh-cn/azure/service-fabric/media/service-fabric-overview/service-fabric-overview.png)

### 体系结构
![architecture](https://docs.microsoft.com/zh-cn/azure/service-fabric/media/service-fabric-architecture/service-fabric-architecture.png)

* 传输子系统
* 联邦子系统
* 可靠性子系统
* 管理子系统
* 宿主子系统
* 通信子系统
* 可测试性子系统


### 微服务平台
Service Fabric 作为微服务平台旨在解决构建和运行服务方面的难题，并有效地利用基础结构资源，使团队可以使用微服务方法来解决业务问题。

### 无状态和有状态
使用 Service Fabric，可以生成包含微服务或容器的应用程序。 无状态微服务（例如网关、Web 代理）不维护除请求及其来自服务的响应之外任何可变状态。 Azure 云服务辅助角色是无状态服务的一个示例。 有状态微服务（例如，用户帐户、数据库、设备、购物车、队列）维护除请求及其响应之外的可变、授权状态。 当今的 Internet 规模应用程序包含无状态和有状态微服务的组合。

### 编程模型
* guest可执行文件
* 容器：
默认情况下，Service Fabric 以进程形式部署和激活这些服务。 Service Fabric 还可以在容器中部署服务。 
* Reliable Services 是一个用于编写与 Service Fabric 平台集成的服务的轻型框架，并且受益于完整的平台功能集， Reliable Services 提供最小 API 集合。
* ASP.NET Core 是新的开源跨平台框架，用于构建现代基于云的连接 Internet 的应用程序，如 Web 应用、IoT 应用和移动后端。
* Reliable Actor 框架在 Reliable Services 的基础上构建，是根据执行组件设计模式实现虚拟执行组件模式的应用程序框架。

### 最佳实践https://github.com/Microsoft/service-fabric

### 用户

### 链接
* [Service Fabric中文](https://docs.microsoft.com/zh-cn/azure/service-fabric/)
* [Service Fabric @ GitHub](https://github.com/Microsoft/service-fabric)