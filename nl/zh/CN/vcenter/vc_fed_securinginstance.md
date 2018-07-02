---

copyright:

  years:  2016, 2018

lastupdated: "2018-05-24"

---

# 确保 VMware Federal 实例安全

完成以下过程，以确保已部署 VMware Federal 实例的安全，即，除去用于持续对实例进行访问的开放管理连接。

## 开始之前

查看以下信息，以了解确保已部署 VMware Federal 实例安全的结果：

* 在完成此过程之前，记录并保存环境可能需要的任何凭证。调用安全操作后，环境的所有凭证都将从 {{site.data.keyword.vmwaresolutions_full}} 数据库中擦除，并且无法取回。
* 在调用安全操作之后，将禁用所有管理功能，但完全实例删除操作除外。
* 在确保已部署 VMware Federal 实例安全的操作过程中，会删除用于出站 HTTPS 管理流量的 VMware NSX Edge 服务网关 (ESG) 和 IBM CloudDriver 虚拟机。

## 过程

1. 在 {{site.data.keyword.vmwaresolutions_short}} 控制台中，单击左侧导航窗格中的**部署的实例**。
2. 在 **vCenter Server 实例**表中，单击要确保安全的实例。
3. 单击 **vCenter 控制台**右侧的溢出菜单图标。
4. 单击**确保实例安全**。
5. 单击**确定**以确认要将实例与自动化断开连接。
   
   
   **注**：在完成此步骤之前，请确保已查看**开始之前**部分中的信息。

## 结果

实例的状态会更改为**正在修改**。

成功确保实例安全后，该实例的状态会更改为**已保护**，并且只有实例属性和部署历史记录可用。

## 相关链接

* [VMware Federal on IBM Cloud 概述](vc_fed_overview.html)
* [订购 VMware Federal 实例](vc_fed_orderinginstance.html)
* [查看 VMware Federal 实例](vc_fed_viewinginstance.html)
* [删除 VMware Federal 实例](vc_fed_deletinginstance.html)
* [联系 IBM 支持](../vmonic/trbl_support.html)