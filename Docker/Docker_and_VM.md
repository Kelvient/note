#虚拟化概论


##当下主流的IT三大技术

1. 虚拟化
2. 云计算
3. 大数据


## 目前主流的虚拟化技术

1. KVM -> 完全虚拟化，Redhat开发，集成在Linux内核，与QEMU技术结合使用
2. ESXI -> 完全虚拟化，VMware开发，也叫vSphere，适合小型企业
3. XEN -> 半虚拟化，由剑桥大学开发，是一个开源的虚拟机监视器，需要修改Linux内核
4. Docker -> 轻量级（操作系统级）虚拟化，有Docker Inc开发，目前使用最多，采用沙箱机制，主要用于Paas


## Docker技术与传统虚拟机的对比

用Docker Engine取代了Guest OS和Hypervisor
直接复用本地主机的操作系统实现生成Docker容器


Docker的资源隔离方面比虚拟机差 -> **安全性比较差**

### Docker与传统虚拟机相比的优点

1. 操作启动快
2. 资源消耗少
3. 开源免费
