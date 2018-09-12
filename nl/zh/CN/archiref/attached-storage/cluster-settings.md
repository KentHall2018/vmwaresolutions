---

copyright:

  years:  2016, 2018

lastupdated: "2018-08-13"

---

# 集群设置

在添加连接的存储器之前，vCenter Server 解决方案不会启用高级功能，例如，vSphere 分布式资源调度程序 (DRS) 和 vSphere 高可用性 (HA)。通过添加 NFS 连接的存储器，在具有以下部分中列出的设置的集群上启用这些功能。

## vSphere 分布式资源调度程序

在集群上开启 vSphere DRS 时，启用了两个主要功能：负载均衡和电源管理。

### 负载均衡

利用负载均衡，将持续监视集群中所有主机和虚拟机 (VM) 的 CPU 和内存资源的分配和使用。DRS 将这些度量与理想资源利用率（给定集群的资源池和 VM、当前需求以及不平衡度目标的属性）进行比较。然后，相应地执行（或建议）VM 迁移。

在集群中首次开启 VM 时，DRS 尝试通过将 VM 放在相应的主机上或者给出建议，来维持适当地负载均衡。在集群设置的“DRS 自动化”部分中设置放置或建议设置。

在此设计中，“DRS 自动化”级别设置为完全自动化，因此，在开启 VM 时，会自动将它们放置在具有足够容量的主机上。VM 也会自动从一个主机迁移到另一个，从而使集群实现负载均衡。此外，权衡保守和积极，设置 DRS 集群的迁移阈值，从而应用优先级 1、优先级 2 和优先级 3 建议。这意味着 vCenter Server 至少针对集群的负载均衡提供改进。

下表显示 VMware vSphere Web Client 中 vSphere DRS 集群的设置。

表 1. vSphere DRS 集群的“DRS 自动化”设置

|设置|值|
|:------------------- |:------ |
|开启 vSphere DRS |已选
|
|自动级别|完全自动|
|迁移阈值|应用优先级 1、优先级 2 和优先级 3 建议|
|启用单个机器自动化级别|已选，设置为 15 毫秒|

有关在 vSphere Web Client 中配置这些设置的更多信息，请参阅[在 vSphere Web Client 中设置虚拟机的定制自动化级别](https://docs.vmware.com/en/VMware-vSphere/5.5/com.vmware.vsphere.resmgmt.doc/GUID-C21C0609-923B-46FB-920C-887F00DBCAB9.html)。

除了集群的自动化级别和迁移阈值，此设计启用 VM 自动化，因此可针对单个 VM 设置覆盖。这支持更精确地控制 VM，并且使您能够进一步划分 VM 负载均衡的优先级。

### 电源管理

在启用 VMware Distributed Power Management 功能时，DRS 将集群级别和主机级别容量与集群的 VM 需求进行比较，包括最新的历史需求。如果找到足够的过剩容量，那么其使（或建议使）主机进入备用电源方式，或者如果需要容量，那么开启主机电源。根据生成的主机电源状态建议，VM 可能需要在主机之间进行迁移。
在此设计中，禁用电源管理，因为开启和关闭集群中主机的电源无运营或财务收益。

## vSphere 高可用性

vSphere 通过将 VM 及其所在的主机聚集到一个集群，为 VM 提供高可用性。将监视集群中的主机，如果发生故障，那么将在备用主机上重新启动发生故障的主机上的 VM。
在此设计中，使用集群上的主机监视和 VM 监视启用 vSphere 高可用性。

### 主机监视

主机监视允许集群中的主机交换网络脉动信号并允许 vSphere HA 在检测到故障时执行操作。在此设计中启用此功能。

### 虚拟机监视

VM 监视功能使用 VMware Tools 捕获的脉动信号作为代理以获取访客操作系统可用性。这允许 vSphere HA 自动重置或重新启动丢失其脉动信号能力的单个 VM。此设计支持 VM 和应用程序监视。

#### 故障条件和 VM 响应

故障条件定义 VM 的故障情况以及针对每个故障给定的响应。在此设计中，VM 重新启动优先级设置为中；强烈建议复查此值并相应调整设置，从而使重新启动优先级匹配工作负载的重要性。此外，主机隔离的响应设置为“关闭并重新启动 VM”，因此集群中隔离的主机不影响 VM。此设置的其余值设置为缺省值。

下表显示 VMware vSphere Web Client 中 vSphere HA 集群的设置。

表 2. vSphere HA 集群的故障条件和 VM 响应设置

|设置|值|
|:------------------- |:------ |
|VM 重新启动优先级|中|
|主机隔离的响应|关闭并重新启动 VM|
|发生永久设备损失 (PDL) 的数据存储的响应|已禁用|
|所有路径断开 (APD) 的数据存储的响应|已禁用|
|APD 超时后 APD 恢复的响应|已禁用|
|VM 监视敏感度|定制|
|故障时间间隔|50 秒|
|最短正常运行时间|90 秒|
|每个 VM 的最大重置数|10|
|最长重置时间窗口|1 小时内|

有关在 vSphere Web Client 中配置这些设置的更多信息，请参阅[配置虚拟机响应](https://docs.vmware.com/en/VMware-vSphere/6.0/com.vmware.vsphere.avail.doc/GUID-3DAED2B1-55B8-4877-BD0F-BC57C10A516C.html)。

#### 许可控制

vCenter Server 使用许可控制以确保集群中有足够的资源来提供故障转移保护和确保考虑 VM 资源预留。在此设计中，通过指定集群资源的百分比保留故障转移容量。定义的故障转移容量设置为 25% CPU 和 25% 内存。

#### 用于脉动信号的数据存储

vSphere HA 使用数据存储脉动信号以区分发生故障的主机和位于网络分区中的主机。数据存储脉动信号允许 vSphere HA 在发生管理网络分区时监视主机，并继续响应发生的故障。在此设计中，脉动信号数据存储选择策略设置为“自动选择可从主机访问的数据存储”。

### 相关链接

* [解决方案概述](../solution/solution_overview.html)