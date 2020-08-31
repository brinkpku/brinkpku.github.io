## k8s名词概念

**Node**: kubernetes集群中的一台虚拟机或物理机。

**Controller**: Kubernetes 通常不会直接创建 Pod，而是通过 Controller 来管理 Pod 的。Kubernetes 提供了多种 Controller，包括 Deployment、ReplicaSet、DaemonSet、StatefuleSet、Job 等。

**Service**: 一种Kubernetes服务，它使用标签选择器标识一组pod。除非另有说明，否则假定服务只有在集群网络中可路由的虚拟ip。Kubernetes 运行容器（Pod）与访问容器（Pod）这两项任务分别由 Controller 和 Service 执行。
