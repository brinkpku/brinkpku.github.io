初学k8s,对集群里面的IP真的不是很理解，一会是PodIP,一会是ClusterIP,总结一下这些IP。

Kubernetes集群里有三种IP地址，分别如下：

    Node IP：Node节点的IP地址，即物理网卡的IP地址。
    Pod IP：Pod的IP地址，即docker容器的IP地址，此为虚拟IP地址。
    Cluster IP：Service的IP地址，此为虚拟IP地址。

https://blog.csdn.net/qq_21187515/article/details/101363521