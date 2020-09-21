---

copyright:
  years: 2019, 2020
lastupdated: "2020-08-07"

subcollection: vmwaresolutions

keywords: vmware solutions responsibilities, customer responsibilities, management responsibilities

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:download: .download}
{:preview: .preview}
{:term: .term}

# Understanding your responsibilities when using VMware Solutions
{: #understand-responsib}

Learn about the management responsibilities and terms and conditions that you have when you use {{site.data.keyword.vmwaresolutions_full}}. For a high-level view of the service types in {{site.data.keyword.cloud}} and the breakdown of responsibilities between the customer and {{site.data.keyword.IBM_notm}} for each type, see [Shared responsibilities for {{site.data.keyword.cloud_notm}} offerings](/docs/overview?topic=overview-shared-responsibilities).
{:shortdesc}

Review the following sections for the specific responsibilities for you and for {{site.data.keyword.IBM_notm}} when you use {{site.data.keyword.vmwaresolutions_short}}. For the overall terms of use, see [{{site.data.keyword.cloud_notm}} terms and notices](/docs/overview/terms-of-use?topic=overview-terms).

## Incident and operations management
{: #understand-responsib-incident-and-ops}

Incident and operations management includes tasks such as monitoring, event management, high availability, problem determination, recovery, and full state backup and recovery.

The following table describes the responsibilities that are related to incident and operations management for VMware Solutions Shared.

| Task | {{site.data.keyword.IBM_notm}} responsibilities | Your responsibilities |
|:---- |:----------------------------------------------- |:--------------------- |
| Availability | Offer high availability options through multizone region[^mzr1] virtual data centers. | Provision virtual data centers in each multizone region[^mzr2] and deploy workloads. |
| Infrastructure monitoring and notification | Remediate all environment issues. Notify customers of applicable impacts. | Ascertain the impact of each notification that is reported. Engage IBM Support as required. |
| Workload monitoring | Forward to customer any network intrusion notifications detected. Triage virtualization and backup-related errors to determine whether the customer issue needs assistance. Remediate all hardware failures, notification of potential workload impact. | Monitor and respond to OS or software failures, backup, and replication jobs. Engage IBM Support as required. |
| Infrastructure management | New features, updates, and bug fixes are continuously delivered as needed in a manner transparent to you. Maintenance activities that have customer impact are scheduled in advance, and notifications are posted to the IBM Cloud status page. | Set preferences to receive emails notifications. Monitor the IBM Cloud status page for general announcements. |
| Incident management | Unplanned incidents with customer impact are communicated through the CIE process. | Impacted customers can obtain a report about the incident upon request. |
{: row-headers}
{: caption="Table 1. Responsibilities for incident and operations for VMware Solutions Shared" caption-side="top"}
{: summary="The rows are read from left to right. The first column describes the task that a customer or IBM might be responsible for. The second column describes {{site.data.keyword.IBM_notm}} responsibilities for that task. The third column describes your responsibilities as the customer for that task."}

[^mzr1]: Multizone region virtual data centers are limited to allowlisted customers. For more information, contact your {{site.data.keyword.vmwaresolutions_short}} representative.

[^mzr2]: Multizone region virtual data centers are limited to allowlisted customers. For more information, contact your {{site.data.keyword.vmwaresolutions_short}} representative.

The following table describes the responsibilities related to incident and operations management for VMware Solutions Dedicated.

| Task | {{site.data.keyword.IBM_notm}} responsibilities | Your responsibilities |
|:---- |:----------------------------------------------- |:--------------------- |
| Availability | Offer VMware infrastructure in multiple locations, including [multizone regions](#x9774820){: term}. | Plan and provision VMware infrastructure according to your availability requirements. |
| Infrastructure monitoring and notification | Forward to the client all network intrusion notifications detected. Send notification upon hardware failures. | Implement monitoring system and integrate with virtualization management. Ascertain the impact of each notification reported. Engage IBM support as required. |
| Workload monitoring |  | Monitor and respond to OS or software failures. |
| Infrastructure management | | Implement monitoring and management system integrated with virtualization management. |
| Incident management | Unplanned incidents with customer impact are communicated through the CIE process. | Impacted customers can obtain a report about the incident upon request. |
{: row-headers}
{: caption="Table 2. Responsibilities for incident and operations for VMware Solutions Dedicated" caption-side="top"}
{: summary="The rows are read from left to right. The first column describes the task that a customer or IBM might be responsible for. The second column describes {{site.data.keyword.IBM_notm}} responsibilities for that task. The third column describes your responsibilities as the customer for that task."}

## Change management
{: #understand-responsib-change-management}

Change management includes tasks such as deployment, configuration, upgrades, patching, configuration changes, and deletion.

The following table describes the responsibilities that are related to change management for VMware Solutions Shared.

| Task | {{site.data.keyword.IBM_notm}} responsibilities | Your responsibilities |
|:---- |:----------------------------------------------- |:--------------------- |
| Updates, fixes, and new features | Regular updates, bug fixes, and new features are provided, following a continuous delivery model in a way that is transparent to you. Notifications are posted for changes that impact you. | Set preferences to receive email notifications. Monitor the IBM Cloud status page for general announcements. |
| Scaling | Scale the customer VMware infrastructure as requested and to meet the capacity that you selected. | Choose the capacity for your VMware Solutions instances. |
{: row-headers}
{: caption="Table 3. Responsibilities for change management for VMware Solutions Shared" caption-side="top"}
{: summary="The rows are read from left to right. The first column describes the task that a customer or IBM might be responsible for. The second column describes {{site.data.keyword.IBM_notm}} responsibilities for that task. The third column describes your responsibilities as the customer for that task."}

The following table describes the responsibilities that are related to change management for VMware Solutions Dedicated.

| Task | {{site.data.keyword.IBM_notm}} responsibilities | Your responsibilities |
|:---- |:----------------------------------------------- |:--------------------- |
| Scaling | Scale your VMware infrastructure as requested. | Choose the capacity for your VMware Solutions instances. |
| Upgrading |  | Keep your VMware environment updated. |
{: row-headers}
{: caption="Table 4. Responsibilities for change management for VMware Solutions Dedicated" caption-side="top"}
{: summary="The rows are read from left to right. The first column describes the task that a customer or IBM might be responsible for. The second column describes {{site.data.keyword.IBM_notm}} responsibilities for that task. The third column describes your responsibilities as the customer for that task."}

## Identity and access management
{: #understand-responsib-iam-responsibilities}

Identity and access management includes tasks such as authentication, authorization, access control policies, and approving, granting, and revoking access.

The following table describes the responsibilities that are related to identity and access management for both VMware Solutions Shared and Dedicated.

| Task | {{site.data.keyword.IBM_notm}} responsibilities | Your responsibilities |
|:---- |:----------------------------------------------- |:--------------------- |
| Identity and access | Provide the function to restrict access to resources through the IBM Cloud console and REST APIs. Provide default access to the provisioned VMware environment. | Manage access to resources through IAM. Manage access to the VMware environment. |
{: row-headers}
{: caption="Table 5. Responsibilities for identity and access management" caption-side="top"}
{: summary="The rows are read from left to right. The first column describes the task that a customer or IBM might be responsible for. The second column describes {{site.data.keyword.IBM_notm}} responsibilities for that task. The third column describes your responsibilities as the customer for that task."}

## Security and regulation compliance
{: #understand-responsib-security-compliance}

Security and regulation compliance includes tasks such as security controls implementation and compliance certification.

The following table describes the responsibilities that are related to security and regulation compliance for VMware Solutions Shared.

| Task | {{site.data.keyword.IBM_notm}} responsibilities | Your responsibilities |
|:---- |:----------------------------------------------- |:--------------------- |
| Encryption | Secure connections are provided to administration portals and replication endpoints. Backups are encrypted uniquely per customer. | If required, secure with HTTPS. |
{: row-headers}
{: caption="Table 6. Responsibilities for security and regulation compliance for VMware Solutions Shared" caption-side="top"}
{: summary="The rows are read from left to right. The first column describes the task that a customer or IBM might be responsible for. The second column describes {{site.data.keyword.IBM_notm}} responsibilities for that task. The third column describes your responsibilities as the customer for that task."}

The following table describes the responsibilities that are related to security and regulation compliance for VMware Solutions Dedicated.

| Task | {{site.data.keyword.IBM_notm}} responsibilities | Your responsibilities |
|:---- |:----------------------------------------------- |:--------------------- |
| Encryption | Provide integration with Key Protect and Hyper Protect Crypto Services through KMIP add-on service as an option for implementing data at-rest encryption. | Configure and manage encryption for both data at rest and in transit, as needed. |
{: row-headers}
{: caption="Table 7. Responsibilities for security and regulation compliance for VMware Solutions Dedicated" caption-side="top"}
{: summary="The rows are read from left to right. The first column describes the task that a customer or IBM might be responsible for. The second column describes {{site.data.keyword.IBM_notm}} responsibilities for that task. The third column describes your responsibilities as the customer for that task."}

## Disaster recovery
{: #understand-responsib-disaster-recovery}

Disaster recovery includes tasks such as providing dependencies on disaster recovery sites, provision disaster recovery environments, data and configuration backup, replicating data and configuration to the disaster recovery environment, and failover on disaster events.

The following table describes the responsibilities that are related to disaster recovery for VMware Solutions Shared.

| Task | {{site.data.keyword.IBM_notm}} responsibilities | Your responsibilities |
|:---- |:----------------------------------------------- |:--------------------- |
| Backup of configuration data | Backups are conducted of the shared management components to include customer environment configurations. Offsite backup copies are enabled and they run daily. |  |
| Backup of workload | Backup services are enabled for customer workload. | Configure individual backup jobs to include critical systems. Offsite copies can be enabled per request. |
| Recovery of configuration | Recovery will be conducted in the original data center after the infrastructure is available. If long-term outage occurs, offsite recovery is conducted. | |
| Recovery of workloads | Restore capabilities are available in normal operations. For configuration restores, customer restore services will be provided after the infrastructure is available. If an offsite recovery is required, IBM works with the customer to help recover. | Restore systems from the configured backup jobs. |
{: row-headers}
{: caption="Table 8. Responsibilities for disaster recovery for VMware Solutions Shared" caption-side="top"}
{: summary="The rows are read from left to right. The first column describes the task that a customer or IBM might be responsible for. The second column describes {{site.data.keyword.IBM_notm}} responsibilities for that task. The third column describes your responsibilities as the customer for that task."}

The following table describes the responsibilities that are related to disaster recovery for VMware Solutions Dedicated.

| Task | {{site.data.keyword.IBM_notm}} responsibilities | Your responsibilities |
|:---- |:----------------------------------------------- |:--------------------- |
| Business continuity and Disaster Recovery (DR) | Provide automated provision and integration for third-party add-on services such as Veeam and Zerto. | Provision third-party solutions such as Veeam and Zerto, or other solutions of your choice, along with the VMware Solutions instance. Configure these solutions to meet your business continuity and DR requirements for your workload. |
{: row-headers}
{: caption="Table 9. Responsibilities for disaster recovery for VMware Solutions Dedicated" caption-side="top"}
{: summary="The rows are read from left to right. The first column describes the task that a customer or IBM might be responsible for. The second column describes {{site.data.keyword.IBM_notm}} responsibilities for that task. The third column describes your responsibilities as the customer for that task."}

## Related links
{: #understand-responsib-related}

* [Compliance information for vCenter Server instances](/docs/vmwaresolutions?topic=vmwaresolutions-vc_compl_info)
* [Managing your data in VMware Solutions Shared](/docs/vmwaresolutions?topic=vmwaresolutions-shared_data)
* [Post-deployment considerations for your VMware instance](/docs/vmwaresolutions?topic=vmwaresolutions-solution_considerations)
* [Day 2 operational procedures guide](/docs/vmwaresolutions?topic=vmwaresolutions-opsprocs-intro-overview)
* [Operations management guide](/docs/vmwaresolutions?topic=vmwaresolutions-opsmgmt-intro)
* [VMware Update Manager guide](/docs/vmwaresolutions?topic=vmwaresolutions-vum-intro)