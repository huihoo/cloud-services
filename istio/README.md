## istio
istio：第二代Servie Mesh产品

### 介绍
Service Mesh：下一代微服务架构

* [linkerd](https://linkerd.io/)：目前最多生产部署的 Service Mesh 方案，Scala开发。
* [Envoy](https://www.envoyproxy.io/)：第一代Service Mesh产品
* Istio：第二代Servie Mesh产品，使用Envoy网络代理。

Linkerd 更加成熟稳定些，Istio 功能更加丰富、设计上更为强大，社区相对也更加强大一些。Istio由Google和IBM牵头，大厂背书。

Envoy被大量主流互联网公司采用：Airbnd, Apple, Google, eBay, Microsoft, Uber ... 包括推出微服务堆栈的 Netflix 也采用了它。

### Service Mesh
Service Mesh产生背景：

在云原生模型里，一个应用可以由数百个服务组成，每个服务可能有数千个实例，而每个实例可能会持续地发生变化。这种情况下，服务间通信不仅异常复杂，而且也是运行时行为的基础。管理好服务间通信对于保证端到端的性能和可靠性来说是无疑是非常重要的。

以上种种复杂局面便催生了服务间通信层的出现，这个层既不会与应用程序的代码耦合，又能捕捉到底层环境高度动态的特点，让业务开发者只关注自己的业务代码，并将应用云化后带来的诸多问题以不侵入业务代码的方式提供给开发者。

这个服务间通信层就是 Service Mesh，它可以提供安全、快速、可靠的服务间通讯（service-to-service）。

可以简单地说，Service Mesh 就是微服务的动态链接器（Dynamic Linker）。

大胆预测，在三到五年之后，Kubernetes 会成为服务器端的标准环境，就像现在的 Linux，而 Service Mesh 就是运行在 Kubernetes 上的分布式应用的动态链接器，届时开发一个分布式应用将会像开发单机程序一样简单，业界在分布式操作系统上长达三十多年的努力将以这种方式告一段落。

### 架构
Istio 的架构并不复杂，其核心组件只有四个。首先是名为 Envoy 的网络代理，用来协调服务网格中所有服务的出入站流量，并提供服务发现、负载均衡、限流熔断等能力，还可以收集大量与流量相关的性能指标；其次是名为 Mixer 收集器，用来从 Envoy 代理收集流量特征和性能指标；然后是名为 Pilot 的控制器，用来将流量协调的策略和规则发送到 Envoy 代理；最后是名为 Istio-Auth 的身份认证组件，用来做服务间访问的安全控制。

* Envoy：一个高性能的C++的Proxy，包含：服务发现、负载均衡、熔断器等功能；
* Mixer：访问控制、策略、适配器
* Pilot：为Envoy提供服务发现、流量控制
* Citadel：为service-to-service 和 end-user身份认证、证书管理
* Galley：提供配置和API管理，将用户配置的细节隔离开来。

### 项目
* [kiali](https://www.kiali.io/): Service mesh observability

### 文档

### 图集
![istio](https://istio.io/docs/concepts/what-is-istio/arch.svg)Istio Architecture

![pilot](https://istio.io/docs/concepts/traffic-management/PilotAdapters.svg)Pilot Architecture

![istio security](https://istio.io/docs/concepts/security/architecture.svg)Istio Security Architecture

![mixer](https://istio.io/docs/concepts/policies-and-telemetry/topology-without-cache.svg)Mixer Topology

![](https://ibmcloud-perf.istio.io/regpatrol/istio_regpatrol_readme_files/image004.png)Microservices and Istio

### 链接
* [istio官网](https://istio.io/)
* [istio @ github](https://github.com/istio)