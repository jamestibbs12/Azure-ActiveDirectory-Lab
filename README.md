# Azure Active Directory & Security Hardening Lab

## Objective
To design, deploy, and harden a secure enterprise network infrastructure entirely within Microsoft Azure. This hands-on project demonstrates competency in cloud architecture, network segmentation, identity management via Active Directory Domain Services (AD DS), and automation using PowerShell.

## Environments & Tools Used
* Microsoft Azure (Cloud Infrastructure)
* Windows Server 2022 (Primary Domain Controller)
* Windows 10 Enterprise (Workstation Client)
* PowerShell (Automation & Bulk Account Creation)

## Network Architecture
* **Virtual Network (VNet):** `AD-VNet` (10.0.0.0/16)
* **Subnet:** `default` (10.0.0.0/24)
* **Domain Controller Internal IP:** 10.0.0.4 (Static Assignment)
* **Client Workstation Internal IP:** Dynamic (DHCP via VNet)
* **DNS Configuration:** Custom VNet DNS routing traffic through 10.0.0.4

---

## Progress Log

### Phase 1: Cloud Infrastructure Provisioning
*Status: Complete*

1. **Resource Group Isolation:** Created `ActiveDirectory-Lab-RG` to contain all network and compute resources, enabling clean lifecycle management.
2. **Virtual Network (VNet) Topology:** Designed `AD-VNet` utilizing a `10.0.0.0/16` address space with a default subnet (`10.0.0.0/24`) to establish a secure enterprise boundary.
3. **Compute Provisioning:** Deployed a Windows Server 2022 instance named `DomainController` leveraging a `Standard_DC1ds_v3` size (1 vCPU, 8 GiB RAM) to guarantee stable performance for directory operations.
4. **Network Hardening & Static IP:** Modified the Domain Controller's network interface card from a dynamic lease to a **Static Internal IP assignment** (`10.0.0.4`) to maintain consistent DNS resolution.
5. **Custom DNS Routing:** Altered the entire VNet's configuration from default Azure DNS to **Custom DNS**, pointing directly to `10.0.0.4` to ensure future domain client joins resolve correctly.

---

### Phase 2: Active Directory Domain Services (AD DS) Installation
*Status: In Progress...*
1. Initiated the installation of the **Active Directory Domain Services** binary roles via Windows Server Manager.
2. Configured a fresh enterprise forest (`labdomain.local` domain topology) and initiated active server promotion.

