## 分布式、微服务、容器云
我们将围绕分布式、微服务、容器云和开源项目展开深入交流和实践，帮助更多中小企业部署这样的基础设施，提供相关的咨询、培训、教育等服务。

这里我们不讨论类似OpenStack这样支持100万物理机和1000万核的大型公有云开源基础设施解决方案，因为众多的中小企业都不需要这样的超大规模和伸缩性。

如果你对OpenStack很感兴趣，可参考[灰狐百科](https://wiki.huihoo.com/wiki/OpenStack)。

### Mesos
Apache Mesos 是一个分布式、集群管理系统和框架，被称为是分布式系统的内核。

* 2010年12月，Mesos 进入了Apache孵化项目。
* 2013年6月，Mesos成功从Apache孵化项目毕业，成为顶级项目。
* 2013.04，一些在Twitter和Airbnb中使用Mesos的工程师们一起创建了Mesosphere。
* 2015.08，Verizon 成功演示了在90秒内使用Mesos和Mesosphere的Marathon框架启动 50,000 个容器。
* 2018.05，Mesosphere获得1.25亿美金的D轮投资。

Mesos是分布式操作系统内核，Mesos是以与Linux内核同样的原则而创建的，不同点仅仅是在于抽象的层面。Mesos内核运行在每一个机器上，同时通过 API 为各种应用提供跨数据中心和云的资源管理调度能力。这些应用包括Hadoop、Spark、Kafka、Elasticsearch。还可配合框架 Marathon 来管理大规模的Docker等容器化应用。

Mesos特性：

* 可扩展到10000个节点；
* 使用 ZooKeeper 实现 Master 和 Slave 的容错；
* 支持 Kubernetes 集群和 Docker 容器；
* 使用 Linux 容器实现本地任务隔离；
* 多资源调度能力（内存，CPU、磁盘、端口）；
* 提供 Java，Python，C++等多种语言 APIs；
* 通过 Web 界面查看集群状态；
* 新版本将支持更多功能。

Apple、Cisco、eBay、PayPal、Netflix、Twitter、Uber、Airbnb、豆瓣、微博、小米、今日头条都是Mesos用户。

更多信息可访问：[Mesos ecosystem](https://wiki.huihoo.com/wiki/Mesos_ecosystem)

### 微服务
除了主流的Spring Cloud和Apache Dubbo这样的常见Microservices和RPC项目，还有类似 [Envoy](https://www.envoyproxy.io/)、[Istio](https://istio.io/)、[Apache ServiceComb](https://servicecomb.apache.org/)的项目大家也可更多关注下。

一个微服务架构参考技术栈

![microservices](https://blog.huihoo.com/wp-content/uploads/Microservices-01.png)

主要包含 11 大核心组件，分别是：

核心支撑组件
* 服务网关 [Zuul](https://github.com/Netflix/zuul)
* 服务注册发现 [Eureka](https://github.com/Netflix/eureka) + [Ribbon](https://github.com/Netflix/ribbon)
* 服务配置中心 [Apollo](https://github.com/ctripcorp/apollo)
* 认证授权中心 [Spring Security OAuth2](https://github.com/spring-projects/spring-security-oauth)
* 服务框架 [Spring MVC](https://github.com/spring-projects/spring-mvc-showcase)/[Spring Boot](https://github.com/spring-projects/spring-boot)

监控反馈组件
* 数据总线 [Kafka](https://github.com/apache/kafka)
* 日志监控 [ELK](https://github.com/deviantony/docker-elk)
* 调用链监控 [CAT](https://github.com/dianping/cat)
* Metrics 监控 [KairosDB](https://github.com/kairosdb/kairosdb)
* 健康检查和告警 [ZMon](https://github.com/zalando/zmon)
* 限流熔断和流聚合 [Hystrix](https://github.com/Netflix/Hystrix)/[Turbine](https://github.com/Netflix/Hystrix)

### Spring Cloud
微服务架构集大成者，云计算最佳业务实践。

这是一个全家桶，集成了很多东西，大家做微服务基本第一反应就是它，这也是它非常成功的地方。

### Apache Dubbo
Apache Dubbo 是一款高性能Java RPC框架，目前正在Apache基金会孵化。

Dubbo 未来的定位并不是要成为一个微服务的全面解决方案，而是专注在 RPC 领域，成为微服务生态体系中的一个重要组件。

三大核心能力：
* 面向接口的远程方法调用；
* 智能容错和负载均衡；
* 服务自动注册和发现。

![Dubbo](https://wiki.huihoo.com/images/2/21/Dubbo-architecture.png)Dubbo架构

![Dubbo architecture roadmap](https://wiki.huihoo.com/images/c/c7/Dubbo-architecture-roadmap.jpg)Dubbo架构路线图

### Rancher
Rancher是一个开源的可用于生产环境的企业级Kubernetes平台。通过Rancher，企业不必利用一系列的开源软件去从头搭建自己的容器服务平台。Rancher提供了在生产环境中使用的全栈化容器部署与管理平台。

* 应用负载管理：用户界面，应用商店，CI/CD，监控，日志收集
* 统一集群管理：配置，认证，RBAC，策略，安全，容量，成本

Rancher是全球唯一提供Kubernetes、Mesos和Swarm三种调度工具的企业级分发版和商业技术支持的容器管理平台。

通过Rancher，企业不必利用一系列的开源软件去从头搭建自己的容器服务平台。Rancher提供了在生产环境中使用的全栈化容器部署与管理平台。

Rancher由以下四个部分组成：
* 基础设施编排
* 容器编排与调度
* 应用商店
* 企业级权限管理

Rancher是我们重点推荐的企业级Kubernetes平台。

### OpenShift
OpenShift 是 Red Hat 推出的 Platform as a Service (PaaS) 开源云平台。

OpenShift 3 使用 Docker 和 Kubernetes 帮助用户构建、部署和管理他们的应用。

产品形态
* OpenShift Origin(OKD)：开源云PaaS
* OpenShift Online：公有云PaaS
* OpenShift Enterprise：私有云PaaS

OpenShift功能和优势：

* 开源技术：结合 docker 格式 Linux 容器、Kubernetes 及 其 他 开 源 技 术 ，帮 助 用 户 摆 脱 特定供应商技术锁定或业务规划束缚。
* 自助服务配置：开发人员可直接通过最常用的工具，轻松、快速、按需创建各种应用，同时还能让运营团队全面控制整个环境。
* 持久存储：红帽 OpenShift 容器平台支持持久存储，允许用户同时运行有状态的应用和无状态的云原生应用。
* 多语种支持：开发人员可轻松地在同一平台使用多种语言、框架和数据库工作。
* 自动化：红帽 OpenShift 容器平台自带多种功能，包括经过简化且可自动实施的应用构建、部署、扩展、运行状况管理等。
* 用户界面：开发人员可直接访问多种命令行工具、多设备 Web 控制台和基于 Eclipse 的整合开发环境（如红帽 JBoss®开发 人员工作室）。
* 运营管理：该产品所含的红帽 CloudForms 让用户能够实时了解单个容器和整个基础架构的运行情况。
* 深化协作：OpenShift 允许运营和开发人员在同一平台上使用各种容器，实现深入合作。
* 可扩展性：在 OpenShift 上运行的应用,可在数秒内轻松地扩展到数百个节点上的数千个实例中。
* 强大的生态系统：红帽的合作伙伴生态系统持续扩展，旨在为用户提供广泛多样集成。该系统中的第三方合作伙伴可提供额外的存储和网络提供商、集成开发环境 (IDE) 和 CI 整合、独立软件 供 应 商 (ISV) 解决方案等，均可以和 OpenShift 搭配使用。
* 容器可移植性：基于红帽应用编程接口 (API) 支持的、标准化 Linux 容 器 模 型构建。让 所有基于 OpenShift 上创建的应用都能在支持 docker 格式容器的任意环境中轻松运行。
* 自由选择云架构：按照您的特定需求，选择在物理或虚拟、公共、私有甚至混合云基础架构上运行应用。

用户可基于OpenShift快速构建自己的DevOps & PaaS基础设施。

更多OpenShift细节可访问：[灰狐百科](https://wiki.huihoo.com/wiki/OpenShift)


### 文档
* [Mesos，数据中心操作系统的核心](http://docs.huihoo.com/apache/mesos/mesos-the-heart-of-the-data-center-operating-system.pdf)
* [RESTful Microservices](http://docs.huihoo.com/javaone/2015/CON2885-RESTful-Microservices.pdf)
* [Microservices for the IoT](http://docs.huihoo.com/javaone/2015/CON7034-Microservices-for-the-IoT.pdf)
* [基于连接与组合的微服务架构剖析](http://docs.huihoo.com/infoq/qconshanghai/2015/%e5%85%ac%e6%9c%89%e4%ba%91%e6%9c%8d%e5%8a%a1%e4%b8%8e%e5%9f%ba%e7%a1%80%e8%ae%be%e6%96%bd%e5%bb%ba%e8%ae%be%e4%b8%93%e5%9c%ba/QCon%e4%b8%8a%e6%b5%b72015-%e5%9f%ba%e4%ba%8e%e8%bf%9e%e6%8e%a5%e4%b8%8e%e7%bb%84%e5%90%88%e7%9a%84%e5%be%ae%e6%9c%8d%e5%8a%a1%e6%9e%b6%e6%9e%84%e5%89%96%e6%9e%90-%e5%be%90%e7%ab%8b.pdf)
* [使⽤微服务架构改造企业核⼼业务系统的实践](http://docs.huihoo.com/infoq/qconbeijing/2015/day3/%E4%BD%BF%E2%BD%A4%E7%94%A8%E5%BE%AE%E6%9C%8D%E5%8A%A1%E6%9E%B6%E6%9E%84%E6%94%B9%E9%80%A0%E4%BC%81%E4%B8%9A%E6%A0%B8%E2%BC%BC%E5%BF%83%E4%B8%9A%E5%8A%A1%E7%B3%BB%E7%BB%9F%E7%9A%84%E5%AE%9E%E8%B7%B5.pdf)
* [平台即服务、DevOps和应用集成：加速交付应用新途径](http://docs.huihoo.com/openshift/openshift-deliver-apps-faster-paas-devops-and-application-integration-zh-cn.pdf)
* [OpenShift 3 Technical Architecture](http://docs.huihoo.com/openshift/OpenShift-3-Technical-Architecture.pdf)
* [OpenShift 3 and The Next Generation of PaaS](http://docs.huihoo.com/redhat/summit/2015/13544_openshift-3-the-next-generation-of-paas.pdf)
* [Using OpenShift & PaaS to accelerate DevOps & Continuous Delivery](http://docs.huihoo.com/redhat/summit/2015/12218_use-openshift-paas-to-accelerate-devops-continuous-delivery.pdf)

### 图集
![mesos](https://wiki.huihoo.com/images/e/e0/Mesos-the-heart-of-the-data-center-operating-system.png)Mesos

![DC/OS](https://wiki.huihoo.com/images/2/2c/DCOS-Dasboard.png)DC/OS仪表盘

![microservices](https://wiki.huihoo.com/images/9/95/Architecture-evolution.png)架构变化

![microservice-platform](https://wiki.huihoo.com/images/7/7a/Microservice-platform.png)微服务平台

![FaaS](https://wiki.huihoo.com/images/9/9c/Functions-as-a-Service.png)Functions as a Service（FaaS）

![Rancher](https://wiki.huihoo.com/images/6/68/Rancher-key-value.jpg)Rancher核心价值

![compare](https://wiki.huihoo.com/images/d/d7/Rancher-compare.png)编排工具比较

![OpenShift v3](https://wiki.huihoo.com/images/9/93/OpenShift-v3.png)OpenShift v3架构

### 链接
* [Apache Mesos](http://mesos.apache.org)
* [Mesosphere DC/OS](http://dcos.io)
* [Rancher中文](https://cnrancher.com)
* [OpenShfit OKD](https://www.okd.io/)
* [Spring Cloud中文](https://springcloud.cc/)
* [Apache Dubbo](http://dubbo.apache.org/zh-cn/)

## 许可协议 License

课程和课件采用CC

[![CC](http://wiki.huihoo.com/images/4/4e/CC-BY-SA_3.0-88x31.png)](http://wiki.huihoo.com/wiki/CC-BY-SA_3.0)

代码采用Apache v2

## 赞助与支持
本服务教程为免费教程，若需要得到更多技术支持，可通过赞助我们的方式获得，谢谢。

![灰狐会员](http://wiki.huihoo.com/images/2/25/Zsxq.jpg)

[灰狐会员](https://wiki.huihoo.com/wiki/%E7%81%B0%E7%8B%90%E4%BC%9A%E5%91%98)
