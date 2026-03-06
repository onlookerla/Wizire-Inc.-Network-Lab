# Getting Started
## Overview
This section covers the prerequisites, environment requirements and initial setup context for the project. It is intended to be read before proceeding to any deployment or configuration documentation.
## Environment Summary
The Wizire Inc. lab simulates a multi-site enterprise network for a 75-100 employee SaaS company. The environment spans four locations with New York City serving as its headquarters and Chicago, San Francisco and Dallas being branch sites.
## Site Architecture

| Site | Role | Domain Controller |
|---|---|---|
| New York City | Headquarters / PDC Emulator | NYCDC01 |
| Chicago | Branch | CHIDC02 |
| San Francisco | Branch | SFODC03 |
| Dallas | Branch | DALDC04 |

Inter-site connectivity is simulated through isolated virtual network segments in VirtualBox. pfSense handles all routing between sites and enforces firewall policy at the perimeter. AD Sites and Services defines replication topology, site link costs, and replication schedules across all four sites.

## System Inventory

| Host | Site | Role | OS |
|---|---|---|---|
| NYCDC01  | New York City | Primary Domain Controller | Windows Server 2019 |
|CHIDC02| Chicago | Domain Controller | Windows Server 2019 |
| SFODC03 | San Francisco | Domain Controller | Windows Server 2019 |
| DALDC04 | Dallas | Domain Controller | Windows Server 2019 |
| SIEM01 | New York City | Security Monitoring (Wazuh) | Ubuntu Server 22.04 |
| FW01 | New York City | Perimeter Firewall | pfSense |
| WRK01-04 | All Sites | Domain-joined Workstations | Windows 11 |

---

## Technology Stack

| Component | Technology |
|---|---|
| Hypervisor | VirtualBox |
| Firewall | pfSense |
| Directory Services | Active Directory, Entra ID |
| Server OS | Windows Server 2019 |
| Client OS | Windows 11 |
| SIEM | Wazuh on Ubuntu Server 22.04 |
| Hybrid Identity | Azure AD Connect |
| Automation | Python |


## Host Machine

| Component | Specs |
|---|---|
| CPU | Intel Core i7-13700k 16-Core|
| RAM| 64GB DDR4-3200 |
| Storage | 2TB NVMe PCIe 4.0 |
| GPU | NVIDIA RTX 3060 12GB |
| OS | Linux Mint (Host) |

