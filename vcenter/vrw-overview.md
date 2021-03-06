---

copyright:

  years:  2020, 2021

lastupdated: "2021-01-28"

keywords: regulated workloads, workloads instance, regulated instance

subcollection: vmwaresolutions

---

{:external: target="_blank" .external}
{:tip: .tip}
{:note: .note}
{:important: .important}

# Regulated workloads overview
{: #vrw-overview}

The VMware® regulated workloads offering includes a secure-by-default architecture that follows IBM's unique policy controls framework and include continuous compliance monitoring and the highest level of data encryption (FIPS 140-2 Level 4).

Review the following specifications before you begin:
* Regulated workloads are based on VMware NSX-T and VMware vSphere® 7.0 Update 1a.
* [Hyper Protect Crypto Services](https://cloud.ibm.com/catalog/services/hyper-protect-crypto-services), [KMIP for VMware](https://cloud.ibm.com/infrastructure/vmware-solutions/console/servicestandalonenew/KMIPAdapter), and [Direct Link Dedicated](https://cloud.ibm.com/interconnectivity/direct-link) are required for the regulated workloads. Ensure that you order these services before you start your regulated workloads order.
* If you are planning to use BYOL licenses for the VMware components, ensure that you have the complete list of BYOL licenses that are required.
* The uplink speed is set to 10 Gb.
* Some of the add-on services require configuration setup. Review each service and ensure that you configure its settings properly, as indicated.

## Options not available for regulated workloads
{: #vrw-overview-before-not-avail-options}

The following options or settings are not available for regulated workloads:
* VMware Subscription Purchasing Program
* Local disks
* High performance with Intel® Optane
* vSAN™ deduplication and compression
* Selection of existing VLANs. Only the option to order new VLANs is available.
* Single public Windows® VSI for Active Directory™ DNS configuration. Only the option to order two highly available dedicated Windows server virtual machines (VMs) on the management cluster is available.

## Related links
{: #vrw-overview-related}

* [Requirements and planning for regulated workloads](/docs/vmwaresolutions?topic=vmwaresolutions-vrw-planning)
* [Ordering regulated workloads](/docs/vmwaresolutions?topic=vmwaresolutions-vrw-orderinginstance)
* [VMware regulated workloads reference architecture overview](/docs/vmwaresolutions?topic=vmwaresolutions-vrw-archi-overview)
* [Viewing and deleting regulated workloads](/docs/vmwaresolutions?topic=vmwaresolutions-vrw-view-delete-instance)
* [FAQ](/docs/vmwaresolutions?topic=vmwaresolutions-faq-vmwaresolutions)
