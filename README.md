# ansible-active-directory-infrastructure

Automated Microsoft Active Directory infrastructure deployment using **Ansible**, **PowerShell**, and **Infrastructure as Code principles**.

---

## Overview

This project demonstrates automated deployment of a Microsoft infrastructure environment using Ansible.  
The infrastructure includes Active Directory, DNS, IIS, domain clients, organizational units, users, groups, and policies.

The goal of the project is to provision and configure a complete Windows domain environment with minimal manual work.

---

## Architecture

The infrastructure is deployed in a virtual lab environment.

**Components:**

- Ubuntu Automation Node (Ansible)
- Windows Server 1 — Domain Controller + DNS
- Windows Server 2 — File Server + DNS
- Windows Server 3 — Web Server (IIS)
- Windows Client Workstations (Domain joined)

Network: VMware NAT (VMnet)

---

## Automation Features

The infrastructure is automatically configured using Ansible playbooks and roles.

Automation includes:

- Domain Controller installation
- Active Directory configuration
- Organizational Unit creation
- User and group provisioning
- Computer account generation
- Domain join automation
- IIS installation
- Group Policy deployment

Approximately **70% of the infrastructure is automated**.

---
## Technologies Used

- Ansible
- PowerShell
- Windows Server
- Active Directory
- WinRM
- Jinja2 Templates
- VMware Workstation
- CSV Data Generation

---

## How to Run

Run the full infrastructure automation:

```bash
ansible-playbook -i inventory.ini site.yml
