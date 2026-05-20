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
*Status: Staging...*

